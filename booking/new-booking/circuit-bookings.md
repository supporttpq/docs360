---
description: >-
  Create circuit bookings (multi-destination trips) in Tourpaq Office using
  multiple hotels and one-way transports. Includes prerequisites and example
  itinerary.
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

# Circuit Bookings

### Overview

Circuit bookings in **Tourpaq Office (BackOffice)** let you create a **multi-destination booking** (also called a **multi-hotel booking**) inside one booking.

Unlike a standard booking with one hotel and a return transport, a circuit booking can combine:

* Multiple hotels, potentially located in different resorts or even countries.
* Multiple transports, often **one-way flights**, to build a **multi-leg itinerary**.

***

### Purpose

* To provide greater flexibility in travel planning.
* To accommodate multi-destination trips under one booking record.
* To allow users to tailor customer journeys with varied hotels and transport legs.

***

### Preconditions (required setup)

* One-way transports must be enabled in the system.
* Custom hotel days must be enabled for hotels.
* Related price lists supporting custom hotel days and multiple one-way flights must be configured.
* Users should refer to:
  * [Price List Custom Hotel days Service](../../price-list-custom-hotel-days-service.md) for hotel duration setup.
  * [Multiple one way flights bookings](multiple-one-way-flights-bookings.md) for transport setup.

***

### How to create a circuit booking (workflow)

Use this flow when you need a **multi-leg itinerary** with **multiple hotel stays**.

{% stepper %}
{% step %}
### 1. Create a new booking draft

Start in [New Booking](new-booking/).

Set passengers first. Then build the itinerary.
{% endstep %}

{% step %}
### 2. Add the first transport leg (one-way)

Select the outbound **one-way transport** for the first destination.

Confirm dates and gateways. This sets the first leg of the route.
{% endstep %}

{% step %}
### 3. Add the first hotel stay (custom hotel days)

Select the hotel for destination 1.

Set the stay length using **custom hotel days**.
{% endstep %}

{% step %}
### 4. Add the next transport leg + hotel stay (repeat)

Add the “middle” one-way leg to the next destination.

Then add the next hotel stay with the correct nights.
{% endstep %}

{% step %}
### 5. Add the final return leg and save

Add the last one-way leg back to the home gateway.

Review the full itinerary. Then save the booking.
{% endstep %}
{% endstepper %}

### Best practices (avoid common mistakes)

* Build legs in **chronological order**.
* Check each leg’s **date and time** before you add the next.
* Confirm each hotel stay matches the intended **nights**.
* If you are rescheduling, copy passengers first. See [Copy Booking](copy-booking.md).

***

### Key benefits

* Combine multiple hotels within a single booking.
* Manage hotels across different resorts or countries seamlessly.
* Use multiple one-way flights to match complex travel itineraries.

### Example itinerary (circuit booking)

<figure><img src="https://docs.tourpaq.com/assets/images/circuit-8d9b468c853f2ffb0e4a767d96942035.png" alt="Example circuit booking with two hotel stays and three one-way transport legs"><figcaption><p>Example: two hotels in different countries connected by one-way transports.</p></figcaption></figure>

* **Leg 1 (one-way transport):** Billund → Palma (Mallorca), 21.05.2020 09:15–11:15
* **Hotel stay 1 (custom hotel days):** 7 nights, 21–28 May
* **Leg 2 (one-way transport):** Palma (Mallorca) → Porto Santo, 28.05.2020 07:15–10:45
* **Hotel stay 2 (custom hotel days):** 7 nights, 28 May–4 June
* **Leg 3 (one-way transport):** Porto Santo → Billund, 04.06.2020 09:30–11:00

In this example, the booking includes two hotel stays in two countries.

The stays are connected by three one-way transports. Each transport leg must exist in Tourpaq.

### Ticket output (example)

<figure><img src="../../.gitbook/assets/image (249).png" alt="Example ticket layout for a circuit booking with multiple hotel stays and one-way transport legs"><figcaption><p>Example ticket for a circuit booking.</p></figcaption></figure>

### FAQ

#### When should I use a circuit booking?

Use a circuit booking when the itinerary has **multiple hotel stays** and/or **multiple transport legs** (often **one-way flights**) that can’t be handled as a single “out + home” package.

#### What’s required for circuit bookings to work?

You typically need:

* **One-way transports** enabled.
* **Custom hotel days** enabled for relevant hotels/price lists.
* Price lists that support **custom hotel days** and **multiple one-way flights**.

See:

* [Price List Custom Hotel days Service](../../price-list-custom-hotel-days-service.md)
* [Multiple one way flights bookings](multiple-one-way-flights-bookings.md)

#### Can a circuit booking span multiple resorts or countries?

Yes. That’s a common use case.

Each hotel stay and each transport leg must be available and defined for the brand/agency setup you book under.

#### Why can’t I find the “middle” transport leg (between two destinations)?

Circuit bookings depend on every leg being defined (for example: **A → B**, **B → C**, **C → A**).

If a leg is missing, check:

* the transport is created and enabled
* the date range is valid for the leg
* allotment and/or stop-sale rules aren’t blocking it
* your filters aren’t hiding it

#### Does Tourpaq automatically build the route for me?

No. You select the transports and hotel stays in the booking flow.

Treat it like building a multi-leg itinerary. Verify dates and sequence before saving.

#### What should I double-check before sending tickets/documents?

Always verify:

* leg order and dates (outbound, middle legs, return)
* each hotel stay dates match the intended nights (**custom hotel days**)
* passenger names and birthdates (pricing can depend on age)
* the ticket output shows all legs and stays as expected

### Related

* [New Booking](new-booking/)
* [Copy Booking](copy-booking.md)
* [Moved Booking](moved-booking.md)
* [Multiple one way flights bookings](multiple-one-way-flights-bookings.md)
* [Booking for 2 One Ways](booking-for-2-one-ways.md)
