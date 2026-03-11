---
description: Create a new reservation from scratch — step by step.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# New Booking

### **Overview**

The **New Booking** section covers everything needed to build a reservation manually in Tourpaq. From the initial search for available transport and accommodation, through adding passengers and extras, reviewing economics, and confirming the booking — every step is documented here.

This page is the section index. It gives you an orientation of the full New Booking workflow and maps out every sub-page so you can jump directly to the area you need.

{% hint style="info" %}
**Looking for an existing booking?** Go to [All Bookings](https://manual.tourpaq.com/booking/all-bookings) to search, filter, and open bookings that have already been created.&#x20;
{% endhint %}

***

### **Purpose**

The New Booking functionality is designed to support agents and internal users who create reservations manually — for example, in response to phone enquiries, email requests, agency sales, or special cases that cannot be handled through the self-service web booking engine.

It supports all booking configurations: standard packages, hotel-only, transport-only, a la carte, circuit trips, group bookings, and more.

***

### **Preconditions**

Before creating a new booking, make sure the following are in place:

* You are logged in with a user role that has permission to **create and edit bookings**. Contact your administrator if the New Booking option is not visible or accessible.
* The correct **Brand** is selected. Prices, hotels, transports, and extras are all Brand-specific — selecting the wrong Brand will produce incorrect or empty search results.
* The following data must be configured in the system before a booking can be created:
  * Active **Transports** (flights, buses, etc.) with available seats
  * **Hotels** with valid room types and allotment
  * A valid **Price List** covering the intended travel period
  * **Extras** configured if the customer requires add-ons

{% hint style="warning" %}
If you search for departures or hotels and nothing appears, the most common cause is a missing or expired **Price List** for the selected Brand and travel period. Check [Price List](https://manual.tourpaq.com/price-list/pricelist) before contacting support.
{% endhint %}

***

### New Booking Workflow

The standard workflow for creating a new booking follows these six steps:

#### Step 1 — Open New Booking

1. Go to **Booking → New Booking** in the left sidebar
2. Confirm the correct **Brand** is selected at the top of the screen
3. You are now on the main booking creation screen

***

#### Step 2 — Search for travel options

Enter the basic search criteria:

* **Departure gateway** — where the customer is travelling from
* **Destination** — resort, area, or specific hotel
* **Travel dates** — outbound and return
* **Passengers** — number of adults, children, and infants

Click **Search** to see available transport and accommodation options. If no results appear, try widening the dates or destination, and verify that a valid Price List exists for the period.

***

#### Step 3 — Select transport and accommodation

From the search results:

1. Choose the **outbound transport** (and return transport if applicable)
2. Select the **hotel**, **room type**, and **board type**
3. Verify the selected combination is available and that the **price looks correct**

***

#### Step 4 — Add passengers and details

1. Add all **passengers** with their required personal data (name, date of birth, etc.)
2. Assign passengers to **rooms** and **seats** where relevant
3. Open **Passenger Details** to add contact information or special needs

***

#### Step 5 — Add extras and review economics

1. Add any **extras** requested by the customer — insurance, transfers, activities, equipment, etc.
2. Open **Economics** to review:
   * Total **price** charged to the customer
   * Underlying **supplier costs**
   * Calculated **profit / margin**
3. Adjust components if the price or profit needs to change within your permitted rules

***

#### Step 6 — Confirm and save

1. Verify all required data is complete — passenger details, travel components, payment terms
2. Save and confirm the booking
3. Note the **Booking Number** assigned by the system
4. Proceed to send **tickets and confirmation** via the E-mails tab
5. Add any internal **Comments** or notes as needed

***

### Sub-Pages in This Section

#### Core Booking Flow

| Page                                                                                    | What it covers                                                          |
| --------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| [New Booking — Main Screen](https://manual.tourpaq.com/booking/new-booking/new-booking) | The primary search and selection screen — transport, hotel, room, board |
| [Economics](https://manual.tourpaq.com/booking/new-booking/economics)                   | Full price, cost, and profit breakdown per booking                      |
| [Passenger Details](https://manual.tourpaq.com/booking/new-booking/passenger-details)   | Personal data, contact info, and options per traveller                  |
| [History](https://manual.tourpaq.com/booking/new-booking/history)                       | Full audit log of all changes and actions on a booking                  |

***

#### Communication

| Page                                                                                               | What it covers                                                |
| -------------------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| [E-mails](https://manual.tourpaq.com/booking/new-booking/e-mails)                                  | Send and track booking confirmation emails and tickets        |
| [SMS](https://manual.tourpaq.com/booking/new-booking/sms)                                          | Send and manage SMS messages linked to a booking              |
| [Comments](https://manual.tourpaq.com/booking/new-booking/comments)                                | Internal notes visible only to agents — not sent to customers |
| [Conversation](https://manual.tourpaq.com/booking/new-booking/conversation)                        | Full communication thread attached to a booking               |
| [Don't Send Ticket Option](https://manual.tourpaq.com/booking/new-booking/dont-sent-ticket-option) | Suppress ticket sending for specific bookings                 |

***

#### Financials

| Page                                                                                                              | What it covers                                                           |
| ----------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| [Profit](https://manual.tourpaq.com/booking/new-booking/profit)                                                   | Detailed profit view and margin handling per booking                     |
| [Individual Payments](https://manual.tourpaq.com/booking/new-booking/individual-payments)                         | Register and manage payments per passenger or per booking                |
| [Keep Automatic Discounts Prices](https://manual.tourpaq.com/booking/new-booking/keep-automatic-discounts-prices) | Control whether automatic discounts recalculate when a booking is edited |
| [Coded Discount Booking](https://manual.tourpaq.com/booking/new-booking/coded-discount-booking)                   | Apply a promotional code at the time of booking                          |

***

#### Services & Allocation

| Page                                                                                                                              | What it covers                                                          |
| --------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| [Hotel Room](https://manual.tourpaq.com/booking/new-booking/hotel-room)                                                           | Hotel room assignment and management within a booking                   |
| [Transport Seating](https://manual.tourpaq.com/booking/new-booking/transport-seating)                                             | Assign and manage passenger seats on a transport                        |
| [SSR — Special Service Requests](https://manual.tourpaq.com/booking/new-booking/ssr)                                              | Airline special requests: wheelchair, meal preferences, bassinets, etc. |
| [Extra Orders](https://manual.tourpaq.com/booking/new-booking/extra-orders)                                                       | Add and manage extras ordered during or after booking creation          |
| [Tee Times](https://manual.tourpaq.com/booking/new-booking/tee-times)                                                             | Golf tee time booking and scheduling                                    |
| [Golf Courses](https://manual.tourpaq.com/booking/new-booking/golf-courses)                                                       | Golf course information linked to a booking                             |
| [QR Code for Vouchers](https://manual.tourpaq.com/booking/new-booking/qr-code-for-vouchers)                                       | Generate and configure QR codes on vouchers for destination check-in    |
| [Customer Info / Details on Customer Card](https://manual.tourpaq.com/booking/new-booking/customer-info-details-on-customer-card) | View and manage customer profile data from within a booking             |

***

#### Special Booking Types & Behaviours

| Page                                                                                                                                | What it covers                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| [Waiting List](https://manual.tourpaq.com/booking/new-booking/waitting-list)                                                        | Place a booking on hold pending availability confirmation                |
| [Moved Booking](https://manual.tourpaq.com/booking/new-booking/moved-booking)                                                       | Move a booking to a different departure, hotel, or date                  |
| [Copy Booking](https://manual.tourpaq.com/booking/new-booking/copy-booking)                                                         | Duplicate an existing booking as a starting point for a new one          |
| [Circuit Bookings](https://manual.tourpaq.com/booking/new-booking/circuit-bookings)                                                 | Multi-destination round-trip itineraries                                 |
| [Booking for 2 One Ways](https://manual.tourpaq.com/booking/new-booking/booking-for-2-one-ways)                                     | Two separate one-way transports combined in a single booking             |
| [Multiple One Way Flights Bookings](https://manual.tourpaq.com/booking/new-booking/multiple-one-way-flights-bookings)               | More complex combinations of one-way flight legs                         |
| [Multiple Transports One Room Bookings](https://manual.tourpaq.com/booking/new-booking/multiple-transports-one-room-bookings)       | Passengers using different transports but sharing the same accommodation |
| [Hotel Only Bookings](https://manual.tourpaq.com/booking/new-booking/hotel-only-bookings)                                           | Accommodation without transport                                          |
| [Transport Only Booking](https://manual.tourpaq.com/booking/new-booking/transport-only-booking)                                     | Transport without accommodation                                          |
| [Child Price](https://manual.tourpaq.com/booking/new-booking/child-price)                                                           | How child pricing rules are applied within a booking                     |
| [A la Carte](https://manual.tourpaq.com/booking/new-booking/a-la-carte)                                                             | Fully custom package with individually priced components                 |
| [Remove Pax on Outbound or Homebound Only](https://manual.tourpaq.com/booking/new-booking/remove-pax-on-outbound-or-homebound-only) | Remove a passenger from only one leg of a two-way booking                |

***

### FAQ

**Q: When should I use New Booking instead of Web Booking?** Use **New Booking** when an agent or internal user is creating or managing a reservation manually — for example, bookings received by phone, email, or through a partner agency, or any case requiring special handling. Use **Web Booking** when the customer is booking directly through the online booking engine.

***

**Q: Why do I see no available departures or hotels when I search?** The most common reasons are: the selected **Brand** has no valid Price List for the chosen period; the departure dates fall outside the configured travel lengths; or the gateway, destination, or passenger count filters are too restrictive. Start by widening the search, then check the [Price List](https://manual.tourpaq.com/price-list/pricelist) configuration if nothing appears.

***

**Q: The price is showing as 0 or looks wrong — what should I check?** Open **Economics** to see the full price breakdown and identify which components are missing or zero. Confirm the correct Brand is selected, verify a valid Price List exists for the period, and check whether any discount or supplement rules are affecting the price unexpectedly. See [Economics](https://manual.tourpaq.com/booking/new-booking/economics) for details.

***

**Q: Can I use New Booking to edit an existing booking?** No. New Booking is only for creating new reservations. To edit an existing booking, find it in [All Bookings](https://manual.tourpaq.com/booking/all-bookings) and open it from there. All editing is done within the booking's own sub-pages.

***

**Q: How do I handle a large group booking?** Define the number of passengers and room distribution carefully from the start. Use [Passenger Details](https://manual.tourpaq.com/booking/new-booking/passenger-details) to maintain clear records for each traveller. Use [Economics](https://manual.tourpaq.com/booking/new-booking/economics) to verify group profitability. Consider using [Copy Booking](https://manual.tourpaq.com/booking/new-booking/copy-booking) for similar group configurations.

***

**Q: Where do I add internal notes about a booking?** Use the [Comments](https://manual.tourpaq.com/booking/new-booking/comments) sub-page. Comments are internal only — they are never visible to the customer and do not appear on tickets, vouchers, or confirmation emails.

***

### Related Pages

* [All Bookings](https://manual.tourpaq.com/booking/all-bookings) — search and manage existing bookings
* [Booking Overview](https://manual.tourpaq.com/booking) — introduction to the full Booking section
* [Price List](https://manual.tourpaq.com/price-list/pricelist) — the pricing foundation required before bookings can be created
* [Customers](https://manual.tourpaq.com/customer/customers) — customer profiles linked to bookings
* [Notifications](https://manual.tourpaq.com/notifications/notification) — monitor booking errors and warnings after saving
* [Extras Setup](https://manual.tourpaq.com/extras-setup/extras) — configure the extras available to add to bookings
