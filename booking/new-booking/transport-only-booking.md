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
**1. Enable “Transport Hotel” on the hotel**

On the hotel, open the **Web** tab.

Enable **Transport Hotel**.

<figure><img src="../../.gitbook/assets/image (257).png" alt="Hotel Web tab with Transport Hotel checkbox enabled"><figcaption><p>Enable <strong>Transport Hotel</strong> on the hotel used for transport-only bookings.</p></figcaption></figure>
{% endstep %}

{% step %}
**2. Create a fictive room type**

Create a room type used only for transport-only bookings.

Enable **Is Fictive**.

One-way flights typically require **Is Fictive** plus the additional one-way related option on the room type.

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

Ticket information is taken from the **Transport Hotel** and can be customized via the hotel’s content/settings.
