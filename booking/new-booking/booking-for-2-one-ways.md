---
description: >-
  Create a booking with two one-way flights (one-way outbound + one-way
  homebound) in Tourpaq Office. Learn transport selection, shadow passengers,
  and export/list behavior.
---

# Booking for 2 One Ways

### Overview

**Booking for 2 One Ways** lets you create one booking with **two one-way flights**:

* **One-way outbound** (OW OUT)
* **One-way homebound** (OW HOME)

This is also used for **open-jaw** style trips, where outbound and return are different transports.

### Preconditions

Before you start:

* One-way flights must be enabled for your setup.
* The selected transport(s) must have **one-way seat allotment** for **OW OUT** and **OW HOME**.

For broader one-way scenarios, see [Multiple one way flights bookings](multiple-one-way-flights-bookings.md).

### Create a 2 one-way booking

{% stepper %}
{% step %}
### 1. Start a new booking

Start in [New Booking](new-booking/).

Enter the number of passengers. Then open transport selection.
{% endstep %}

{% step %}
### 2. Select a transport with OW OUT / OW HOME seats

Pick a transport that has seat allocation for:

* **OW OUT**
* **OW HOME**

<figure><img src="../../.gitbook/assets/4d57113d-2203-4f43-b9dd-2287ab24167e.webp" alt="Transport selection showing one-way seat availability (OW OUT / OW HOME)"><figcaption><p>Select a transport that supports one-way seats for outbound and homebound.</p></figcaption></figure>
{% endstep %}

{% step %}
### 3. Set interval to one-way out and select the one-way home flight

Change **Interval (Days)** to **one way out**.

This enables an extra tab in the transport window. Use it to select the **one-way home** flight.

{% hint style="info" %}
The homebound leg is typically constrained by your gateway rules.

Example: If the booking departs from Billund, the return is typically required back to Billund.
{% endhint %}

<figure><img src="../../.gitbook/assets/bfa9c810-5db5-4a2f-9b25-6068278caf0d.webp" alt="Interval set to one-way out; new tab appears for selecting one-way home transport"><figcaption><p>Set Interval to <strong>one way out</strong> to enable selecting the homebound one-way flight.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/5f91fcdd-47be-4041-8687-0e6b6d944026.webp" alt="Selecting the one-way home flight in the transport window"><figcaption><p>Select the one-way home flight (return leg).</p></figcaption></figure>
{% endstep %}

{% step %}
### 4. Continue like a normal booking

From here, the flow is the same as a standard booking:

* customer details
* take allotment
* passenger details
* extras, supplements, and discounts

For one-way bookings, products and rules must be eligible for one-way selection. This is controlled in **Extras → Price** and **Extras → Resources**.

<figure><img src="../../.gitbook/assets/2b921626-f796-4440-abca-45c9a7957c85.webp" alt="Booking view after selecting both one-way flights, showing two legs and booking totals"><figcaption><p>After selecting both one-way legs, complete the booking as usual.</p></figcaption></figure>
{% endstep %}
{% endstepper %}

### Passenger behavior: “shadow” rows

In a 2 one-way booking, passengers appear **twice**.

The duplicate row is the **shadow passenger**. It separates data for the two flights, since each flight can have its own products, supplements, and discounts.

### Export and lists behavior

#### Finance export: passengers are doubled

In exports, passengers can appear **twice** due to the two flight legs.

<figure><img src="../../.gitbook/assets/ct7-4934b8b850549b20a7d5f04dc15b91d2.png" alt="Finance export showing passengers listed twice (one per one-way leg)"><figcaption><p>Finance export: passengers appear twice (one row per one-way flight leg).</p></figcaption></figure>

#### Export lists: grouped per leg for guide lists

In [Lists](../../export-1/lists.md), passengers are grouped by flight departure/arrival dates for guide lists.

<figure><img src="../../.gitbook/assets/image (250).png" alt="Export list grouped by flight departure and arrival dates for a guide list"><figcaption><p>Export lists: passengers are grouped per flight leg for guide lists.</p></figcaption></figure>

### FAQ

<details>

<summary><strong>When should I use a 2 one-way booking?</strong></summary>

Use it when outbound and homebound are **different transports**.

Typical cases:

* **Open** trips (outbound and return are not the same route).
* You want to sell **one-way seat allotment** on both legs (OW OUT + OW HOME).

</details>

<details>

<summary><strong>Why do passengers show up twice?</strong></summary>

Because the booking contains **two flight legs**.

Tourpaq duplicates each passenger into a **shadow passenger** row.

This lets the system separate services and pricing per leg (outbound vs homebound).

</details>

<details>

<summary><strong>Do products, supplements, and discounts apply to both legs?</strong></summary>

Not automatically.

They can be applied **per leg**, because each passenger exists as a normal row + a shadow row.

If something looks “missing” on one flight, check which passenger row the product was added to.

</details>

<details>

<summary><strong>Why is the homebound one-way flight selection limited?</strong></summary>

The homebound leg is typically constrained by your **gateway rules**.

Example: If the booking departs from Billund, the return is usually required back to Billund.

</details>

<details>

<summary><strong>Why are passengers doubled in exports?</strong></summary>

Many exports are **leg-based**.

That means one booking with two one-way flights can produce **two rows per passenger** (one per leg).

</details>
