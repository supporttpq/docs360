# Single Room Supplement

### Overview

A **single room supplement** is an extra charge when one guest uses a room meant for two or more guests (for example, a double room).

In Tourpaq, this uses the standard supplement code `SINGLE`.

<figure><img src="../../../.gitbook/assets/image (181).png" alt=""><figcaption></figcaption></figure>

### Purpose

* Add a supplement for single occupancy.
* Limit when it applies (dates, ages, room types).
* Support both fixed amounts and percentages.

### Where to find it

Go to **Hotel → Single Room Supplement**.

### Preconditions

*   A supplement with code **SINGLE** exists.

    <figure><img src="../../../.gitbook/assets/image (546).png" alt=""><figcaption></figcaption></figure>
*   The **SINGLE** supplement is set **For sale**.

    <figure><img src="../../../.gitbook/assets/image (547).png" alt=""><figcaption></figcaption></figure>
*   The rule in **Hotel → Single Room Supplement** matches the booking.

    <figure><img src="../../../.gitbook/assets/image (549).png" alt=""><figcaption></figcaption></figure>

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
* **From Age**: Minimum guest age for the rule.
* **To Age**: Maximum guest age for the rule.
* **Start Date**: First date the rule can apply.
* **End Date**: Last date the rule can apply.
* **Supplement Code**: The supplement to apply (typically `SINGLE`).
* **Price**: Fixed amount to add.
* **Percent**: Apply **Price** as a percentage instead of a fixed amount.
* **PD**: Per day. Apply the value per day instead of per interval.
* **Hotel Room**: The room type the rule targets.
* **Period**: Limits the rule to a specific hotel period (if used).

### Instructions for use

{% stepper %}
{% step %}
#### Open Single Room Supplement

Go to **Hotel → Single Room Supplement**.
{% endstep %}

{% step %}
#### Confirm the `SINGLE` supplement is sellable

Make sure `SINGLE` exists and is set **For sale**.
{% endstep %}

{% step %}
#### Create the rule

Click **Create** and set dates, age range, room type, and value.
{% endstep %}

{% step %}
#### Save and test

Save the hotel.

Create a booking with one guest in the target room type.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
If the supplement does not apply, check dates, age limits, and room type matching first.
{% endhint %}

### FAQ

#### Does this change the room cost or the sales price?

It adds a **supplement** to the booking.

It does not directly change the **room cost** setup.

#### What’s the difference between “Single Room Cost” and “Single Room Supplement”?

[Single Room Cost](single-room-cost.md) adds cost in the **Room Cost** setup.

Single Room Supplement applies the `SINGLE` supplement on the booking.

#### Why didn’t the supplement apply?

Most cases are:

* The `SINGLE` supplement is not **For sale**.
* The booking dates are outside **Start Date / End Date**.
* The guest age is outside **From Age / To Age**.
* The room type does not match **Hotel Room**.

#### What does “PD” mean?

**PD** means **Per day**.

If enabled, Tourpaq applies the value per day, not per stay/interval.

#### Can I set different single supplements for different rooms?

Yes.

Create separate rules per room type using **Hotel Room**.
