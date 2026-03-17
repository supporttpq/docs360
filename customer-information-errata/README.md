---
description: >-
  Configure customer information notices (special conditions) shown to guests
  during the booking flow. Covers examples, guest acknowledgment, and rules for
  stay period and booking period applicability.
---

# Customer information (errata)

### Customer information notices (special conditions)

Use **Customer information** to show **guest notifications** and **special conditions** during the booking flow. These notices can be informational, or require guest acknowledgment at checkout.

Typical use cases include destination rules, operational transport notes, hotel/room restrictions, or extra service details.

### Examples

Common examples:

* **Destinations**: visa requirements, local taxes, entry rules.
* **Transport**: technical stop, refueling, check-in requirements, baggage notes.
* **Hotels**: renovations, temporary facility closures, service limitations.
* **Rooms**: restricted AC periods, view obstructions, construction noise.
* **Extras**: meeting point, required items, age/fitness requirements.

### Guest acknowledgment (checkout confirmation)

If the notice can affect the guest experience, require acknowledgment. The guest must confirm it during checkout (Tourpaq Web Booking / Customer Center, depending on setup).

For phone bookings, the notice is shown to the agent. The agent can confirm the acknowledgment on the guest’s behalf.

### Conditional relevance (when the notice is shown)

Notices do not always apply to every booking. Example: hotel noise during a specific date range, added after some guests booked. Only affected bookings should see the notification.

### Rules (stay period + booking period)

Notices must respect the configured **start** and **end** dates. Show the notice only if the guest’s stay **overlaps** the validity period. Any overlap counts as eligible.

Optionally, you can also limit the notice to a **booking period**. In that case, show the notice only for bookings **created** within that booking start/end date range.

To summarize:

* **Stay period condition**: show it when the stay intersects the validity period.
* **Booking period condition**: show it only when the booking creation date is in range.

Both conditions can apply. Show the notice only when all configured criteria are met.

### Where to configure customer information

Add customer information notices on the relevant object:

* [Customer Information on Destination setup](customer-information-on-destination-setup.md)
* [Customer Information on Resort setup](customer-information-on-resort-setup.md)
* [Customer Information on Transport setup](customer-information-on-transport-setup.md)
* [Customer Information on Hotel setup](customer-information-on-hotel-setup.md)
* [Customer Information on Extra setup](customer-information-on-extra-setup.md)

To understand exactly how it appears to users:

* [Customer Information Booking Flow](customer-information-booking-flow.md)
* [Customer Information on WebBooking](customer-information-on-webbooking.md)
* [Customer Information display on Ticket](customer-information-displayed-on-the-ticket.md)
