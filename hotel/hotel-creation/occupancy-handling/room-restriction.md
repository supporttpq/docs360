# Room Restriction

### Overview

**Room Restriction** lets you block specific bed combinations for a room type. It prevents unsupported occupancy setups in bookings and offers.

### Purpose

* Control which bed combinations can be sold for each room type.
* Prevent unsupported combinations from being bookable.
* Keep the booking flow aligned with the real room setup.

### Where to find it

Go to **Hotel → Room Types → Edit**. Scroll to the **Restrictions** section.

<figure><img src="../../../.gitbook/assets/image (3) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

### How it works

* The **Restrictions** list shows all bed combinations for the room type.
* Each row represents one combination.
* Select the **Restriction** checkbox to disable that row.
* Disabled combinations are not available in bookings or offers.

### What a combination can include

* Ordinary beds
* Extra beds
* Extra child beds

#### Example

Room setup:

* 2 ordinary beds
* 1 extra bed
* 1 extra child bed

You can allow only specific combinations. Example: allow `2 ordinary + 1 extra child` only. Then restrict every other combination.

### Instructions for Use

{% stepper %}
{% step %}
**Open the room type**

Go to **Hotel → Room Types**. Select the room type, then click **Edit**.
{% endstep %}

{% step %}
**Review combinations**

Scroll to **Restrictions**. Review the list of combinations.
{% endstep %}

{% step %}
**Block combinations**

Select the **Restriction** checkbox for combinations you want to block.
{% endstep %}

{% step %}
**Save**

Save the room type.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Room Restriction blocks combinations. It does not change prices or room costs.
{% endhint %}

{% hint style="info" %}
Use [Different Max Pax](different-max-pax.md) to sell the same room type with different occupancies.
{% endhint %}
