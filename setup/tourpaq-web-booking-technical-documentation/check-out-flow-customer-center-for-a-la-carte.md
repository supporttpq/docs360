---
description: >-
  Explains how Tourpaq Customer Center and Web Booking identify and handle A la
  carte bookings that combine multiple hotels and/or one-way transports.
---

# Check-out flow/customer center for A la carte

**Applies to: Tourpaq Customer Center, Web Booking. Last reviewed: 2026-09-21.**

#### Overview

An **A la carte** booking combines more than one hotel stay and/or one-way transport in a single booking, instead of a single fixed package. This page explains how the check-out flow in Customer Center, and the equivalent Web Booking flow, identify an A la carte booking, and how passengers, products, and supplements are matched back to the correct hotel or transport inside it.

#### Purpose

* Recognise why an A la carte booking returns more than one item where a normal booking returns one.
* Match a passenger, product, or supplement to the correct hotel or transport inside an A la carte booking.
* Build or debug an integration against Customer Center or Web Booking for A la carte bookings.

#### Preconditions

* The booking is confirmed and reachable through the office API, see the [.](./ "mention") page.
* The booking's `agencyID` and `hash` are known for Customer Center, or its offer details are known for Web Booking, needed to call the API.
* A PLTA ID identifies one trip component, one hotel stay or one transport, within a booking—see [.](./ "mention") in the Tourpaq Web Booking - Technical documentation page.

#### How-to

{% stepper %}
{% step %}
#### Identify the booking type

Call the office API `api/office/bookings/0?agencyID={agencyID}&hash={hash}`. Then read the `help:priceavailability` array in the response's `_embedded` object. One item means a normal booking, a single charter or one-way hotel. More than one item means an A la carte booking, and each item holds the basic configuration for one hotel or transport.
{% endstep %}

{% step %}
#### Fetch room and transport availability

Read the same `help:priceavailability` array, this time under `_links`, which lists one GET path per item. Call each path to retrieve the full availability details for that hotel or transport. This is an array of calls to make and objects to store, one per item, instead of the single call and object a normal booking needs.
{% endstep %}

{% step %}
#### Match passengers to their room or transport

Call the passengers endpoint. Each passenger appears once per room or transport they are booked into, each occurrence with its own `roomDetails` node. A passenger sharing two rooms or hotels appears twice, once per room, but is the same physical passenger, matched back together using `uniquepaxhash`. Find which room or transport a given occurrence belongs to using the `pltaID` inside its `roomDetails`. Supplements are not affected by this multiplication since they are bound to the passenger, not the room. Preselected products are assigned to the pax/room pair and so have no PLTA ID of their own.
{% endstep %}

{% step %}
#### Match products and manual supplements to their room or transport

Call the products endpoint, where each product has an `availableForPltaIDs` array listing which hotels or transports, PLTAs, it can be sold for, and offer it only to passengers booked into one of those PLTAs. Call the manual supplements endpoint, where supplements carry the same `availableForPltaIDs` array and are matched the same way.
{% endstep %}
{% endstepper %}

Once every passenger, product, and supplement has been matched to its PLTA, checkout can be assembled and priced the same way for an A la carte booking as for a normal one.

{% hint style="info" %}
The Web Booking flow, DoBooking, follows the same logic. The only difference is the starting call: DoBooking calls `/api/offer` instead of the office call used by Customer Center.
{% endhint %}

#### Field Reference

| Field                                | Description                                                                                      | Required                                          | Notes                                                                                        |
| ------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `help:priceavailability` \[embedded] | The list of hotels/transports in the booking                                                     | Always present                                    | Contains one item for a normal booking, several for an A la carte booking.                   |
| `help:priceavailability` \[links]    | GET paths, one per item above, used to fetch each hotel's or transport's full availability       | Always present                                    | Call every path, there is no longer a single object to read.                                 |
| `roomDetails`                        | The room/transport-specific details attached to one occurrence of a passenger                    | Always present on each passenger occurrence       | A passenger booked into two rooms has two occurrences, each with its own `roomDetails`.      |
| `pltaID` \[in roomDetails]           | Identifies which hotel or transport this passenger occurrence, product, or supplement belongs to | Always present                                    | Used to route products and supplements to the right passengers.                              |
| `uniquepaxhash`                      | Identifies one physical passenger across all of their occurrences                                | Always present                                    | Use it to collapse multiplied passenger occurrences back into one person.                    |
| `availableForPltaIDs`                | The PLTA ID(s) a product or manual supplement can be sold against                                | Always present on products and manual supplements | Insurance and cancellation insurance ignore this field, they can be sold regardless of PLTA. |

{% hint style="info" %}
Supplements are matched to a passenger directly and never carry a PLTA ID of their own - only products and manual supplements do.
{% endhint %}

{% hint style="danger" %}
TO VERIFY - what are the exact endpoint paths for the passengers, products, and manual supplements calls referenced above? Only the office call and `/api/offer` are documented elsewhere in this manual.
{% endhint %}

#### Related pages

* [.](./ "mention")
* [web-service.md](../web-service.md "mention")
* [glossary.md](../../integration/glossary.md "mention")
