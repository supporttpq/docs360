---
description: >-
  Add a fixed or percentage extra charge for single occupancy, limited by age,
  dates, and room type, and priced in Creditor Currency.
---

# Single Room Supplement

### Overview

A **single room supplement** is an extra charge when one guest uses a room meant for two or more guests (for example, a double room).

In Tourpaq, this uses the standard supplement code `SINGLE`.

<figure><img src="../../../.gitbook/assets/single-room-supplement.png" alt="Single Room Supplement grid on a hotel&#x27;s Occupancy tab, listing rules by From Age, To Age, Start Date, End Date, Supplement Code, Price, Percent, and Room Type"><figcaption></figcaption></figure>

### Purpose

* Add a supplement for single occupancy.
* Limit when it applies (dates, ages, room types).
* Support both fixed amounts and percentages.

### Where to find it

Go to **Hotel → Single Room Supplement**.

### Preconditions

*   A supplement with code **SINGLE** exists.

    <figure><img src="../../../.gitbook/assets/image (546).png" alt=""><figcaption></figcaption></figure>
*   The **SINGLE** supplement is set **For sale + Internet sale**

    <figure><img src="../../../.gitbook/assets/image (547).png" alt=""><figcaption></figcaption></figure>
*   The rule in **Hotel → Single Room Supplement** matches the booking.

    <figure><img src="../../../.gitbook/assets/image (548).png" alt=""><figcaption></figcaption></figure>

### How it works

* Tourpaq checks the booking for **single occupancy**.
* If the booking matches a rule in this tab, Tourpaq applies the `SINGLE` supplement.

When a room type is booked for **one guest**, Tourpaq applies the rule below (if matched):

<figure><img src="../../../.gitbook/assets/image (181) (1).png" alt=""><figcaption></figcaption></figure>

When you add the first rule for a hotel, Tourpaq can auto-create missing data:

* A supplement category named `single-room` with code `SINGLE`.
* A supplement with code `SINGLE` named **Single room supplement (automatically added)**.

### Field reference

* **Actions**: Edit an existing rule.
* **From Age**: The minimum age at which the Room Supplement is added.
* **To Age**: The maximum age at which the room supplement is added.
* **Start Date**: First date the rule can apply, matched against the guest's arrival date.
* **End Date**: Last date the rule can apply, matched against the guest's arrival date.
* Supplement Code: **The code of the supplement added, typically `SINGLE`. The code must be set** For sale **on the active brand.**
* **Price: The price of the supplement, in hotel currency or as a percentage of the Single Cost. An amount is added on top of the Single Cost. When Percent is off, Tourpaq shows the amount in Creditor Currency (or Company Currency if the hotel has no creditor set), and the Booking Engine converts it to the booking's sale currency.**
* **Percent**: If checked, Price is a percentage on top of the Single Cost instead of a fixed amount.
* **Room Type:** The room type where this rule is applicable.

{% hint style="info" %}
Tourpaq calculates the Single Room Supplement once, using the Single Cost and the matching rule for the guest's arrival date (the first night of the stay). That price applies to every night of the booking, even if the Single Cost changes later in the stay. When Percent is off, Tourpaq shows Price in Creditor Currency, or Company Currency if the hotel has no creditor set, and the Booking Engine converts it to the booking's sale currency. When Percent is on, no currency conversion applies.
{% endhint %}

{% hint style="warning" %}
Changing a Single Room Supplement rule does not change the price on bookings that already exist. The new rule applies only to bookings created after the change.
{% endhint %}

### Instructions for use

{% stepper %}
{% step %}
**Open Single Room Supplement**

Go to **Hotel → Single Room Supplement**.
{% endstep %}

{% step %}
**Confirm the `SINGLE` supplement is sellable**

Make sure `SINGLE` exists and is set **For sale + Internet Sale**
{% endstep %}

{% step %}
**Create the rule**

Click **Create** and set dates, age range, room type, and price.
{% endstep %}

{% step %}
**Save and test**

Save the hotel.

Create a booking with one guest in the target room type.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
If the supplement does not apply, check dates, age limits, and room type matching first.
{% endhint %}

### Related pages

* [Single Room Cost](single-room-cost.md)
* [Hotel night calculation](../hotel-night-calculation.md)
* [Hotel creation](../)
