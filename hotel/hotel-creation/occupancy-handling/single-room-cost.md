# Single Room Cost

### Overview

**Single Room Cost** lets you add an extra cost when a room is booked for single occupancy. This keeps cost and profit calculations accurate for single-occupancy stays.

### Purpose

* Add an extra cost for single-occupancy bookings.
* Use either a fixed amount or a percentage of the base room cost.
* Include the cost automatically in room cost calculations.

### Where to find it

Go to **Hotel → Room Costs → Room Cost tab**.

<figure><img src="../../../.gitbook/assets/image (4) (2) (1).png" alt=""><figcaption></figcaption></figure>

### Field Explanations

* **SINGLE PRICE** – The value to add for single occupancy.
* **SP%** – Treat **SINGLE PRICE** as a percentage of the base room cost.

### How it works

* If **SP%** is **not** selected, Tourpaq adds **SINGLE PRICE** as a fixed amount.
* If **SP%** **is** selected, Tourpaq adds **SINGLE PRICE** as a percentage of the base room cost.

#### Example

Base room cost: `150`

* `SINGLE PRICE = 20` and **SP%** unchecked → added cost = `20` (new cost = `170`)
* `SINGLE PRICE = 20` and **SP%** checked → added cost = `20%` of `150` = `30` (new cost = `180`)

### Instructions for Use

{% stepper %}
{% step %}
#### Open the Room Cost tab

Go to **Hotel → Room Costs → Room Cost tab**.
{% endstep %}

{% step %}
#### Find the room

Locate the room type you want to configure.
{% endstep %}

{% step %}
#### Set the single-occupancy cost

Enter a value in **SINGLE PRICE**.

Select **SP%** if the value should be treated as a percentage.
{% endstep %}

{% step %}
#### Save

Save your changes.
{% endstep %}
{% endstepper %}

> The system will now automatically include the single-occupancy cost in cost calculations.

### FAQ

#### Does Single Room Cost change the customer price?

Not directly. It changes the **room cost** used in calculations.

If your pricing uses margins on cost, the sales price may change.

#### When should I use a fixed amount vs. percentage?

Use a fixed amount when the uplift is constant.

Use a percentage when it should scale with the room cost.

#### What happens if I leave SINGLE PRICE empty?

No single-occupancy cost is added for that room type.

#### What’s the difference between “Single Room Cost” and “Single Room Supplement”?

**Single Room Cost** adds cost in the Room Cost setup.

[Single Room Supplement](single-room-supplement.md) applies the standard `SINGLE` supplement.

Use the one that matches your setup and pricing model.
