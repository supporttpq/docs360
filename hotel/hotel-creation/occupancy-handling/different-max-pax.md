# Different Max Pax

### Overview

**Different Max Pax** is available in **Hotel → Allotments per Day**.

It lets you sell the same room type with different maximum occupancies (Max Pax). Each occupancy option gets its own daily allotment.

### Purpose

* Split a room type into multiple sellable occupancies.
* Control availability per day for each occupancy.
* Improve allocation when demand changes day by day.

<figure><img src="../../../.gitbook/assets/image (1) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

### How it works

* One room type can have multiple Max Pax configurations.
* Each configuration has its own allotment count per day.
* You decide how many rooms to “allocate” to each configuration each day.

The number of available rooms can be adjusted daily in the **Allotments per Day** tab. Set availability per configuration, per day.

<figure><img src="../../../.gitbook/assets/image (2) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

After changing values, click **Update** (marked as `1` in the screenshot) to save.

<figure><img src="../../../.gitbook/assets/image (2) (1) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Instructions for Use

{% stepper %}
{% step %}
#### Open the allotment view

Go to **Hotel → Allotments per Day**.
{% endstep %}

{% step %}
#### Select the room type

Pick the room type you want to manage.
{% endstep %}

{% step %}
#### Set Max Pax configurations

Define the Max Pax value for each configuration you want to sell.
{% endstep %}

{% step %}
#### Allocate rooms per day

In **Allotments per Day**, set how many rooms are available per configuration per day.
{% endstep %}

{% step %}
#### Save

Click **Update** to apply the changes.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
The configurations share the same underlying physical room pool. Make sure the sum of configuration allotments does not exceed your real inventory.
{% endhint %}

{% hint style="info" %}
Different Max Pax controls _occupancy and availability_. Use [Room Restriction](room-restriction.md) to control _allowed bed combinations_.
{% endhint %}

### FAQ

#### What is “Different Max Pax” used for?

To sell the same room type with different occupancies. Example: a room can be sold as Max Pax 2 or Max Pax 3.

#### Do I need to click Update after every change?

Yes. Changes are not saved until you click **Update**.

#### Why did availability disappear for one configuration?

You likely set the daily allotment for that configuration to `0`. Check the specific day and configuration row.

#### Does this change prices?

No. Pricing is still controlled by your room costs and price rules.

#### Is this the same as Room Restriction?

No. Different Max Pax sets occupancy and availability. Room Restriction blocks specific bed combinations.
