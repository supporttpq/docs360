---
description: >-
  Create hotel-only bookings in Tourpaq Office using a car-type transport as a
  placeholder. Covers setup, allotment (Fix quota), pricing.
---

# Hotel Only Bookings

### Overview

**Hotel Only Bookings** let you book **accommodation without flights/buses**.

Tourpaq handles this by using a **car-type transport** as a placeholder.

### How it works

You create a **transport** with type **Car**.

That transport behaves like a normal transport in setup:

* **Interval definition**
* **Timetable**
* **Fix quota** (allotment)

But it does **not** represent an actual scheduled service:

* no airline
* no tickets
* guests choose their own arrival/departure time

### Preconditions

* You can create/edit transports.
* You can create/edit price lists for the hotel(s) you want to sell as hotel-only.

### Setup (recommended)

{% stepper %}
{% step %}
**1. Create a car-type transport**

Create a transport with **Transport mode/type = Car**.

Configure it like a normal transport (interval + timetable).

See [Transport creation](../../transport/transport/transport-creation/) if you need the full transport setup flow.
{% endstep %}

{% step %}
**2. Create Fix quota (allotment)**

Create a **Fix quota** on the car transport.

This controls how many “hotel-only” bookings can be made per departure/check-in pattern.
{% endstep %}

{% step %}
**3. Create a pricelist between the car transport and the hotel**

Create a pricelist for:

* the **car transport** (placeholder)
* the **hotel** you want to sell as hotel-only

See [Pricelist Setup](../../price-list/pricelist-setup.md) if you need the pricelist workflow.
{% endstep %}
{% endstepper %}

### Book a hotel-only stay

Start a booking as usual in [New Booking](new-booking/).

Then:

1. Select the **car transport** instead of a flight/bus.
2. Select the hotel/room as usual.
3. Complete passenger details, extras, and payments as normal.

#### Pricing

The total price shown in the Hotel Only pop-up (**P1**) is the per-night rate multiplied by the length of stay.

This total does not include supplements or discounts from the pricelist. Supplements and discounts are not applied on a per-night basis, so they cannot currently be summed into a single per-stay total for Hotel Only — this is expected behaviour, not a defect.

{% hint style="info" %}
A total that includes supplements and discounts for Hotel Only ("Final Price") is not currently available. It is a possible future enhancement, not yet built.
{% endhint %}

### Purpose

Use hotel-only bookings when you need a standard booking flow, but without real transport.

This keeps:

* availability and allotment logic consistent (Fix quota)
* pricing logic consistent (pricelists; supplements and discounts apply to individual room prices, but are not reflected in the Hotel Only total — see Pricing)
* exports and reporting consistent (still a booking with a “transport”)
