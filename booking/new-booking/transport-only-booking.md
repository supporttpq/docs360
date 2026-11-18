---
description: >-
  Create transport-only (flight-only) bookings in Tourpaq Office using a
  Transport Hotel and a fictive room type. Covers one-way vs charter, ticket
  behavior, and Profit Margin Rules cost requirements.
---

# Transport only Booking

### Overview

**Transport only booking** (also called **flight-only booking**) lets you sell a transport without a real hotel stay.

Tourpaq handles this by using:

* a **Transport Hotel** (a hotel flagged as transport-only)
* a **fictive room type** (used only for booking/pricing)

This setup is used for:

* **one-way flights**
* **charters**
* other **transport-only** scenarios

### How transport-only (flight-only) booking works

You create a hotel that acts as a **pricing container** for transport-only bookings.

On that hotel, you create a **fictive room type**.

That room type:

* is used to make the booking “complete”
* can be priced and reported
* does **not** show as a real room on the customer ticket

### Preconditions

* You can edit **Hotels** and **Room types**.
* You can create/update pricing (pricelist / room pricing rules) used by your setup.

{% hint style="info" %}
If you are also using **one-way bookings** (OW OUT / OW HOME), see:

* [Booking for 2 One Ways](booking-for-2-one-ways.md)
* [Multiple one way flights bookings](multiple-one-way-flights-bookings.md)
{% endhint %}

### Setup (Transport Hotel + fictive room type)

{% stepper %}
{% step %}
**1. Enable “Transport hotel” on the hotel**

On the hotel, open **Overview > Web** and expand **General settings**. See [Hotel Web](../../hotel/hotel-creation/hotel-web.md).

Select **Transport hotel**.

This lets you price the transport even when the room has no cost:

* The price list cost is the transport cost plus the room cost, also when the room cost is `0`.
* Without **Transport hotel**, a period with no room cost gets a total cost of `0`, transport included.

<figure><img src="../../.gitbook/assets/image (257).png" alt="Hotel Web tab with Transport Hotel checkbox enabled"><figcaption><p>Enable <strong>Transport hotel</strong> on the hotel used for transport-only bookings.</p></figcaption></figure>
{% endstep %}

{% step %}
**2. Create a fictive room type**

Create a base room type used only for transport-only bookings, with **Is Fictive** selected. See [Base room types](../../base-room-types.md).

Then add it to the hotel as a room type.

For one-way flights, also select **For one way** on the base room type.

<figure><img src="../../.gitbook/assets/image (256).png" alt="Room type setup showing Is Fictive and other options"><figcaption><p>Room type setup for transport-only and one-way scenarios.</p></figcaption></figure>
{% endstep %}

{% step %}
**3. Set a non-zero cost if you use Profit Margin Rules**

A fictive room often does not need a cost.

But if you use **Profit Margin Rules**, the system requires a **cost price** on the room type.

Set a cost price different from `0`.

See [Profit margin rules](../../profit-margin-rules.md).
{% endstep %}
{% endstepper %}

### Transport-only booking ticket behavior

#### What it looks like in Office

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Transport-only booking example in Tourpaq Office"><figcaption><p>Transport-only booking in Tourpaq Office.</p></figcaption></figure>

#### What it looks like on the ticket

The fictive room does **not** appear as a real room on the ticket.

<figure><img src="../../.gitbook/assets/image (258).png" alt="Ticket example for a transport-only booking"><figcaption><p>Ticket output for a transport-only booking.</p></figcaption></figure>

The ticket leaves the Transport hotel out of the hotel overview and doesn't add a hotel description page for it.
