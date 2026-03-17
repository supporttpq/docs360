---
description: Everything you need to create, manage, and analyse reservations in Tourpaq.
---

# Booking overview

### Overview

The **Booking** section is the operational heart of Tourpaq. It is where agents create new reservations, manage existing ones, send offers, track payments, handle special requests, and communicate with customers — all within a unified workflow.

A booking in Tourpaq is more than just a reservation record. It is a living document that brings together transport, accommodation, extras, passenger details, financial data, and communication history into a single, manageable object. From the moment an agent starts a search to the moment a customer boards their flight, every step is tracked here.

***

### Purpose

The Booking section exists to support the full reservation lifecycle:

| Stage                 | What happens                                                                   |
| --------------------- | ------------------------------------------------------------------------------ |
| 🔍 **Search**         | Find available transports, hotels, and packages based on customer requirements |
| 📋 **Create**         | Build a new booking with transport, accommodation, passengers, and extras      |
| 💰 **Price & Profit** | Review economics, apply discounts, and verify margins before confirming        |
| ✅ **Confirm**         | Save and confirm the booking, generating a booking number                      |
| 📧 **Communicate**    | Send tickets, confirmations, and SMS to customers                              |
| ✏️ **Manage**         | Edit existing bookings — change flights, hotels, passengers, or extras         |
| 📊 **Analyse**        | Search and filter all bookings for reporting, operations, and management       |

***

### Booking Types

Tourpaq supports several booking configurations to match different customer needs:

| Booking Type                      | Description                                                     |
| --------------------------------- | --------------------------------------------------------------- |
| **Package Booking**               | Standard booking combining transport + hotel + optional extras  |
| **Hotel Only**                    | Accommodation without transport                                 |
| **Transport Only**                | Transport without accommodation                                 |
| **A la Carte**                    | Fully custom package with individually priced components        |
| **Circuit Booking**               | Multi-destination round-trip itinerary                          |
| **Booking for 2 One Ways**        | Two separate one-way transports combined into a single booking  |
| **Multiple One Way Flights**      | More complex combinations of one-way transport legs             |
| **Multiple Transports, One Room** | Passengers using different transports but sharing accommodation |
| **Group Booking**                 | Large-party bookings with multiple rooms and passengers         |

{% hint style="info" %}
Not sure which booking type to use? See [New Booking](https://manual.tourpaq.com/booking/new-booking) for a step-by-step guide that covers all scenarios.&#x20;
{% endhint %}

***

### Booking Statuses

Every booking in Tourpaq has a status that reflects its current state. Understanding statuses is essential for filtering, reporting, and managing your workload.

| Status           | Meaning                                                                                                     |
| ---------------- | ----------------------------------------------------------------------------------------------------------- |
| **OK**           | The booking is confirmed and all data is valid                                                              |
| **Error**        | The booking encountered a problem during saving or processing and is in an incomplete state — must be fixed |
| **Warning**      | The booking is confirmed but has a condition requiring attention (e.g. missing insurance, unsent ticket)    |
| **Cancelled**    | The booking has been cancelled by the agent or customer                                                     |
| **Locked**       | The booking is currently being edited by another user and cannot be modified                                |
| **Waiting List** | The booking is on hold pending availability confirmation                                                    |
| **Offer**        | A price quote has been sent to the customer but not yet confirmed as a booking                              |

{% hint style="warning" %}
&#x20;Bookings with **Error** status must be resolved promptly. They may not generate correct tickets, confirmations, or financial records until fixed. Monitor these daily via [Notifications](https://manual.tourpaq.com/notifications/notification).&#x20;
{% endhint %}

***

### Key Concepts

Before working with bookings, it helps to understand a few core concepts that apply throughout this section:

**Brand** — All bookings belong to a Brand. Always confirm the correct Brand is selected before searching or creating a booking. The wrong Brand will show incorrect prices, hotels, and transports.

**Pax** — Short for passengers. A single booking can contain multiple pax. Prices, seat assignments, and passenger details are tracked individually per pax.

**Economics** — The financial breakdown of a booking: the customer price, the underlying supplier costs, and the resulting profit margin. Always review Economics before confirming a booking.

**Extras** — Optional add-ons attached to a booking: insurance, transfers, golf, activities, equipment, and more. Extras are priced and tracked independently within the booking.

**Booking Number** — A unique identifier assigned to every confirmed booking. Use this to find, reference, and track any booking in the system.

**Owner** — The agent or user account responsible for a booking. Used for filtering, reporting, and commission tracking.

***

### What's in This Section

Use the pages below in order when creating a new booking from scratch, or jump directly to the page you need when managing an existing one.

#### Core Booking Flow

| Page                                                                                    | What it covers                                               |
| --------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| [All Bookings](https://manual.tourpaq.com/booking/all-bookings)                         | Search, filter, and analyse all existing bookings            |
| [New Booking](https://manual.tourpaq.com/booking/new-booking)                           | Create a new reservation from scratch — section overview     |
| [New Booking — Main Screen](https://manual.tourpaq.com/booking/new-booking/new-booking) | The primary booking creation screen: search, select, confirm |
| [Economics](https://manual.tourpaq.com/booking/new-booking/economics)                   | Price, cost, and profit breakdown per booking                |
| [Passenger Details](https://manual.tourpaq.com/booking/new-booking/passenger-details)   | Personal data and options per traveller                      |
| [History](https://manual.tourpaq.com/booking/new-booking/history)                       | Full audit log of all changes made to a booking              |

#### Communication

| Page                                                                        | What it covers                                |
| --------------------------------------------------------------------------- | --------------------------------------------- |
| [E-mails](https://manual.tourpaq.com/booking/new-booking/e-mails)           | Send and track booking-related emails         |
| [SMS](https://manual.tourpaq.com/booking/new-booking/sms)                   | Send and manage SMS messages for a booking    |
| [Comments](https://manual.tourpaq.com/booking/new-booking/comments)         | Internal notes visible only to agents         |
| [Conversation](https://manual.tourpaq.com/booking/new-booking/conversation) | Full communication thread linked to a booking |

#### Financials

| Page                                                                                                              | What it covers                                   |
| ----------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| [Profit](https://manual.tourpaq.com/booking/new-booking/profit)                                                   | Detailed profit view and handling per booking    |
| [Individual Payments](https://manual.tourpaq.com/booking/new-booking/individual-payments)                         | Manage payments per passenger or per booking     |
| [Keep Automatic Discounts Prices](https://manual.tourpaq.com/booking/new-booking/keep-automatic-discounts-prices) | Control discount recalculation behaviour on edit |

#### Services & Allocation

| Page                                                                                        | What it covers                                     |
| ------------------------------------------------------------------------------------------- | -------------------------------------------------- |
| [Hotel Room](https://manual.tourpaq.com/booking/new-booking/hotel-room)                     | Hotel room assignment and management               |
| [Transport Seating](https://manual.tourpaq.com/booking/new-booking/transport-seating)       | Seat assignment for transports                     |
| [SSR — Special Service Requests](https://manual.tourpaq.com/booking/new-booking/ssr)        | Airline special requests (wheelchair, meals, etc.) |
| [Extra Orders](https://manual.tourpaq.com/booking/new-booking/extra-orders)                 | Manage extras added during or after booking        |
| [Tee Times](https://manual.tourpaq.com/booking/new-booking/tee-times)                       | Golf tee time booking management                   |
| [Golf Courses](https://manual.tourpaq.com/booking/new-booking/golf-courses)                 | Golf course information within a booking           |
| [QR Code for Vouchers](https://manual.tourpaq.com/booking/new-booking/qr-code-for-vouchers) | QR code generation for voucher check-in            |

#### Special Booking Behaviours

| Page                                                                                                                                | What it covers                                         |
| ----------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| [Waiting List](https://manual.tourpaq.com/booking/new-booking/waitting-list)                                                        | Place and manage bookings on a waiting list            |
| [Moved Booking](https://manual.tourpaq.com/booking/new-booking/moved-booking)                                                       | Move a booking to a different departure or hotel       |
| [Copy Booking](https://manual.tourpaq.com/booking/new-booking/copy-booking)                                                         | Duplicate an existing booking                          |
| [Circuit Bookings](https://manual.tourpaq.com/booking/new-booking/circuit-bookings)                                                 | Multi-destination round-trip bookings                  |
| [Booking for 2 One Ways](https://manual.tourpaq.com/booking/new-booking/booking-for-2-one-ways)                                     | Two one-way transports in a single booking             |
| [Multiple One Way Flights Bookings](https://manual.tourpaq.com/booking/new-booking/multiple-one-way-flights-bookings)               | Complex one-way flight combinations                    |
| [Multiple Transports One Room Bookings](https://manual.tourpaq.com/booking/new-booking/multiple-transports-one-room-bookings)       | Different transports, shared accommodation             |
| [Hotel Only Bookings](https://manual.tourpaq.com/booking/new-booking/hotel-only-bookings)                                           | Accommodation without transport                        |
| [Transport Only Booking](https://manual.tourpaq.com/booking/new-booking/transport-only-booking)                                     | Transport without accommodation                        |
| [Child Price](https://manual.tourpaq.com/booking/new-booking/child-price)                                                           | How child pricing is applied in bookings               |
| [A la Carte](https://manual.tourpaq.com/booking/new-booking/a-la-carte)                                                             | Custom package booking with individual components      |
| [Remove Pax on Outbound or Homebound Only](https://manual.tourpaq.com/booking/new-booking/remove-pax-on-outbound-or-homebound-only) | One-way passenger removal from a booking               |
| [Don't Send Ticket Option](https://manual.tourpaq.com/booking/new-booking/dont-sent-ticket-option)                                  | Suppress ticket sending for specific bookings          |
| [Coded Discount Booking](https://manual.tourpaq.com/booking/new-booking/coded-discount-booking)                                     | Apply promotional codes at booking time                |
| [Customer Info / Details on Customer Card](https://manual.tourpaq.com/booking/new-booking/customer-info-details-on-customer-card)   | View and manage customer profile data within a booking |

#### Offers & Other Booking Tools

| Page                                                                          | What it covers                                  |
| ----------------------------------------------------------------------------- | ----------------------------------------------- |
| [GDS Queue Place](https://manual.tourpaq.com/gds-queue-place)                 | Manage GDS ticketing tasks and queue items      |
| [Offers](https://manual.tourpaq.com/offers)                                   | Create and track price quotes sent to customers |
| [Campaign Statistics](https://manual.tourpaq.com/campaign-statistics)         | Performance data for marketing campaigns        |
| [Live Offer Confirmation](https://manual.tourpaq.com/live-offer-confirmation) | Real-time confirmation of dynamic live offers   |

***

### Quick Start

**Creating a new booking:**

1. Go to **Booking → New Booking**
2. Select your **Brand**
3. Enter search criteria (gateway, destination, dates, pax)
4. Select transport and hotel
5. Add passengers and extras
6. Review **Economics**
7. Confirm and save — note the **Booking Number**
8. Send tickets via the **E-mails** tab

**Finding an existing booking:**

1. Go to **Booking → All Bookings**
2. Select your **Brand**
3. Enter a booking number or customer name
4. Click **Display**
5. Click the **Booking No.** to open the booking

***

### FAQ

**Q: What is the difference between New Booking and Web Booking?** **New Booking** is used by agents and internal users to create bookings manually — for example, for phone or email requests. **Web Booking** is the customer-facing online booking engine where customers book themselves. Both types of bookings appear in All Bookings once confirmed.

***

**Q: Can I edit a booking after it has been confirmed?** Yes. Open the booking via [All Bookings](https://manual.tourpaq.com/booking/all-bookings) and make changes using the relevant sub-pages (Economics, Passenger Details, Hotel Room, Transport Seating, etc.). All changes are logged in the [History](https://manual.tourpaq.com/booking/new-booking/history) tab.

***

**Q: What happens if a booking has Error status?** An Error booking is in an incomplete or invalid state and may not generate correct tickets or financial records. Open the booking, identify the issue using the error description, fix it, and save. Monitor Error bookings daily via [Notifications](https://manual.tourpaq.com/notifications/notification).

***

**Q: How do I handle a booking where the customer wants to change their flight?** Use the [Moved Booking](https://manual.tourpaq.com/booking/new-booking/moved-booking) feature to transfer the booking to a different departure while retaining the booking number and history. For flight detail changes (time, carrier), use [Flight Change](https://manual.tourpaq.com/flight-change).

***

**Q: Where do I add internal notes about a booking?** Use the [Comments](https://manual.tourpaq.com/booking/new-booking/comments) sub-page. Comments are internal only — they are not visible to the customer and do not appear on tickets or confirmations.

***

### Related Sections

* [Customer](https://manual.tourpaq.com/customer/customers) — manage the customer profiles linked to bookings
* [Finance](https://manual.tourpaq.com/finance/payment-registration) — register payments and track booking financials
* [Tickets](https://manual.tourpaq.com/tickets/print-tickets) — print and manage tickets for confirmed bookings
* [Notifications](https://manual.tourpaq.com/notifications/notification) — monitor booking errors, warnings, and unpaid balances
* [Export](https://manual.tourpaq.com/export-1/export) — export booking data for operations and reporting
* [Price List](https://manual.tourpaq.com/price-list/pricelist) — the pricing foundation behind every booking
