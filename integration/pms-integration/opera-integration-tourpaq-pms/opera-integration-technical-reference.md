---
description: >-
  Technical details of the Tourpaq–Opera integration: connection settings,
  authentication, the OHIP operations Tourpaq calls, the reservation and profile
  mapping, and the Opera log.
---

# Opera integration – technical reference

This page is for Tourpaq Support, developers and hotel IT staff who set up or troubleshoot the [Opera integration](./). It describes what Tourpaq sends to Oracle OPERA Cloud and how. For setup in Tourpaq and day-to-day use, see the main page.

## Data flows

```
Opera                                        Tourpaq
Room inventory  ──┐
House inventory ──┼── every 10 hours, ─────▶ Hotel allotment (NO.)
Block inventory ──┘   or Reset Free Room Count

Tourpaq                                      Opera
Take Allotment ───── availability check ───▶ Block first, then House
               ───── one per room ─────────▶ Reservations (linked)
Save passengers ──── guests, Extras, ──────▶ Reservations updated
                     transport               Guest profiles
Cancel booking ────────────────────────────▶ Reservations cancelled

Opera                                        Tourpaq
Confirmation number ───────────────────────▶ Booking → Bed Bank tab → Reference
```

The scheduled allotment update is the **Hotel bed bank service** in **Application → Running Services** (SuperAdmin only), with **Minutes Interval** `600`: every 10 hours.

## Connection

Tourpaq connects to Opera through the Oracle Hospitality Integration Platform (OHIP) REST APIs. Tourpaq Support sets up one connection per company, for one Opera property. There is no screen for it.

| Setting                                 | Used for                                                                                                                 |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| **Endpoint**                            | The OHIP gateway URL that all API calls go to.                                                                           |
| **Authentication endpoint**             | The URL that issues the access token.                                                                                    |
| **Client ID** and **secret**            | Identify the Tourpaq integration when it requests a token.                                                               |
| **Application key**                     | Sent as `x-app-key` on every call.                                                                                       |
| **User name** and **password**          | The integration user, for the password grant.                                                                            |
| **Enterprise ID, grant type and scope** | For OAuth tokens issued per enterprise, instead of the password grant.                                                   |
| **Property**                            | The Opera property code. Sent as `x-hotelid` and used in the API paths. The hotel's **Bed Bank ID** holds the same code. |
| **Origin entity**                       | The source of sale type on reservations.                                                                                 |
| **Rate code mapping**                   | Maps Opera origin entities to rate plans.                                                                                |

## Authentication

Tourpaq requests an access token from the authentication endpoint and sends it as `Authorization: Bearer <token>` on every call, together with `x-app-key` and `x-hotelid`. Two token requests are supported:

* **Password grant:** `grant_type=password` with the integration user.
* **OAuth with enterprise ID:** the `enterpriseId` header, with the grant type and scope set up for the company.

## OHIP operations

Tourpaq calls these operations. `{hotelId}` is the Opera property.

| Purpose                                   | Method and path                                                                                                          |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Access token                              | `POST {authentication endpoint}`                                                                                         |
| Find a block by its code                  | `POST /blk/v1/blocks/searches`                                                                                           |
| Block availability per night              | `GET /blk/v1/hotels/{hotelId}/blocks/{blockId}/availability`                                                             |
| House availability and rates              | `POST /par/v1/hotels/{hotelId}/availability/searches`                                                                    |
| Room and House inventory (allotment sync) | `GET /inv/v1/hotels/{hotelId}/hotelInventory`                                                                            |
| Package rate                              | `GET /rtp/v1/hotels/{hotelId}/packages/{packageCode}`                                                                    |
| Find guest and travel agent profiles      | `POST /crm/v1/profiles/searches`                                                                                         |
| Get, create and update a profile          | `GET /crm/v1/profiles/{profileId}`, `POST /crm/v1/profiles`, `PUT /crm/v1/profiles/{profileId}`                          |
| Find a reservation by confirmation number | `POST /rsv/v1/hotels/{hotelId}/reservations/searches`                                                                    |
| Create a reservation in a block           | `POST /rsv/v1/hotels/{hotelId}/blocks/{blockId}/reservations`                                                            |
| Create a reservation on House             | `POST /rsv/v1/hotels/{hotelId}/reservations`                                                                             |
| Get and update a reservation              | `GET /rsv/v1/hotels/{hotelId}/reservations/{reservationId}`, `PUT /rsv/v1/hotels/{hotelId}/reservations/{reservationId}` |
| Link the rooms of a booking               | `POST /rsv/v1/hotels/{hotelId}/reservations/linkedReservations/{reservationId}`                                          |
| Cancel a reservation                      | `POST /rsv/v1/hotels/{hotelId}/reservations/{reservationId}/cancellations`                                               |

{% hint style="info" %}
Searches use the `POST …/searches` operations. They replace the `GET` search operations that Oracle retires on 1 November 2026, with the same parameters in the request body and the same responses.
{% endhint %}

## Block search

Tourpaq builds the block code `<departure airport><DDMMYY><interval>` from the outbound transport, for package trips with interval 1 to 4 from BLL or CPH — see [Block codes](./#block-codes). The search is filtered on the brand's rate plan. Tourpaq uses the first block that has the status `DEF` and is not classified as `MasterBlock` or `MasterAllocation`.

## Reservation mapping

Tourpaq creates one reservation per room.

| Opera field        | Value from Tourpaq                                                                                                                                                                         |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Property           | The connection's property                                                                                                                                                                  |
| External reference | The booking number, context `TA_RECORD_LOCATOR`                                                                                                                                            |
| Source of sale     | Source code = the property, source type = the origin entity                                                                                                                                |
| Room type          | The room's **Room code**                                                                                                                                                                   |
| Rate plan          | The brand's **Rate Code**                                                                                                                                                                  |
| Market code        | From the brand's country, and whether the guest is a timeshare owner                                                                                                                       |
| Source code        | `TSO` for timeshare owners, `WEB` for Web Booking, `AGE` for Office bookings                                                                                                               |
| Rooms, guests      | 1 room. Number of adults and children. Infants in the user-defined field `UDFN01`.                                                                                                         |
| Stay               | Arrival = check-in, departure = check-out                                                                                                                                                  |
| Rates              | The per-night amounts from the block or House availability answer                                                                                                                          |
| Block              | Created in the block, with the block code and block ID on the room rate, or on House                                                                                                       |
| Guests             | The booking customer at Take Allotment; afterwards the room's passengers, the first as primary guest                                                                                       |
| Transport          | Per guest: arrival and departure station, date and time, carrier and transport number                                                                                                      |
| Expected times     | The outbound arrival time and the homebound departure time                                                                                                                                 |
| Travel agent       | The travel agent profile agreed during setup                                                                                                                                               |
| Guarantee, payment | The guarantee code and payment method agreed during setup                                                                                                                                  |
| Comments           | Internal general note `OUTSIDE ALLOTMENT` on hotel-only bookings. The **Hotel** comment from the booking's **Comments** tab: an internal `GEN` comment titled `Tourpaq`, updated in place. |
| Status             | `Reserved`                                                                                                                                                                                 |

The rooms of a booking share the first room's confirmation number and are linked to each other in Opera. A cancellation is sent with the reason `TourpaqCancel`.

## Packages and inventory items

| Opera field   | Opera Package                                                                                                                               | Opera Item Inventory      |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------- |
| Code          | Package code: the Extra code, or each code after the underscore in `GROUP_CODE1-CODE2`                                                      | Item code: the Extra code |
| Package group | The part before the underscore, in the group format                                                                                         | —                         |
| Description   | The package code, or `GROUP-CODE` in the group format                                                                                       | —                         |
| Quantities    | Default quantity 1. Total quantity = passengers in the room with the Extra. Excluded quantity = the room's adults (or children) without it. | Quantity                  |
| Dates         | Start = check-in. End = check-in + the Extra's days, at the latest check-out.                                                               | Check-in to check-out     |
| Schedule      | One line per day, with the unit price from Opera                                                                                            | —                         |
| Price         | The price on the reservation for the same package and dates, otherwise the package rate                                                     | —                         |

Packages and items on the reservation that Tourpaq does not send are removed: packages are sent with quantity 0, items as an empty item.

## Profile mapping

| Opera field                             | Value from Tourpaq                           |
| --------------------------------------- | -------------------------------------------- |
| Profile type, status                    | Guest, active, registered at the property    |
| Names, title                            | First name, last name, title                 |
| Gender, language, nationality, birthday | From the passenger                           |
| Phone, email                            | From the passenger                           |
| Address                                 | Address and postcode                         |
| Passport                                | ID type `P`, from **Oracle info**            |
| `UDFC01`                                | Passenger type: `ADULT`, `CHILD` or `INFANT` |
| `UDFC10`                                | First name                                   |

Empty Tourpaq values are not sent, so they do not clear the Opera values. The matching order is on the main page — see [Guest profiles](./#guest-profiles).

## Log

Every booking-related call to Opera is stored as one row in the **OperaRequest** table of the Tourpaq database.

| Column                 | Holds                                                                                               |
| ---------------------- | --------------------------------------------------------------------------------------------------- |
| **OperaRequestID**     | The row ID. Shown as **Opera Request ID** on the **Opera Mismatch** tab.                            |
| **ClientReference**    | The Tourpaq booking number. Empty for availability checks.                                          |
| **OperaReservationID** | The Opera reservation, on reservation calls.                                                        |
| **Created**            | Date and time of the call.                                                                          |
| **CompanyID**          | The Tourpaq company.                                                                                |
| **RequestMessage**     | The call as JSON: Method, Url, Headers, RequestBody, ResponseStatus, ResponseContent, ErrorMessage. |

Logged calls: profile searches, creation and updates, the travel agent lookup, block search and availability, House availability, package rates, and reservation creation, retrieval, update, linking and cancellation.

**Error format.** Opera errors are stored in **ErrorMessage**, and shown to the user, as:

```
HTTP StatusCode: <status> (opera code: <Opera code>) <title> <detail>
```

Opera warnings come back to the booking as `<status> <text>`.

{% hint style="danger" %}
OperaRequest rows hold guest data and Opera access headers. Keep access to the table limited to Tourpaq Support and developers. Query it in date or ID ranges: the table is large.
{% endhint %}

## Related pages

* [Opera integration](./)
* [PMS Integration](../)

**Applies to:** Tourpaq Office, Web Booking · **Last reviewed:** 2026-10-30
