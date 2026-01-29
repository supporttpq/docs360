# Transport Allotment adjustment for Dynamic Transport

### Overview

This feature adjusts hotel nights for **dynamic GDS transports**.

It covers **early arrivals** and **late departures**.

It adds hotel nights automatically.

{% hint style="warning" %}
This feature applies **only** to **GDS transports**.

It is applied when you **create a new booking**.
{% endhint %}

### Behavior

The system compares flight times against two limits:

* **Early arrival limit** (outbound arrival time)
* **Late departure limit** (homebound departure time)

If a limit is hit, the booking gets extra hotel nights.

### How It Works

{% stepper %}
{% step %}
### Configure the limits

Go to **Setup → System Setup → Transport Providers**.

Set **Early arrival limit** and **Late departure limit**.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Early arrival limit**

If the **outbound arrival time** is **before** the limit, one hotel night is added.

The extra night is added **before** the arrival date.

**Late departure limit**

If the **homebound departure time** is **after** the limit, one hotel night is added.

The extra night is added **after** the original last hotel night.
{% endstep %}

{% step %}
### Create a booking with a GDS transport

Create a booking using a transport that books flights via GDS.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

### Example

In this example, **both** conditions are met.

#### 1) Early arrival limit

* Outbound arrival time: **19:20**
* Early arrival limit: **20:00**

Result: one extra hotel night **before** the arrival date.

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### 2) Late departure limit

* Homebound departure time: **10:40**
* Late departure limit: **10:00**

Result: one extra hotel night **after** the original last night.

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Result and pricing impact

This booking gets **2 extra hotel nights**.

One night is for early arrival.

One night is for late departure.

Transport interval: **01.09–08.09**.

Hotel stay: **31.08–09.09**.

Pricing changes with the extra nights.

One hotel night cost is added per triggered limit.

### FAQ

<details>

<summary>Does this apply to charter or real transports?</summary>

No. It applies only to **GDS transports**.

</details>

<details>

<summary>Does this update existing bookings?</summary>

No. It is applied when you **create a new booking**.

Existing bookings are not recalculated automatically.

</details>

<details>

<summary>What if only one condition is met?</summary>

Then only **one** extra hotel night is added.

</details>

<details>

<summary>What happens if the flight time is exactly on the limit?</summary>

The rules use **before** and **after**.

So, an exact match does not trigger an extra night.

</details>

<details>

<summary>Where do I change the limits?</summary>

Go to **Setup → System Setup → Transport Providers**.

Update **Early arrival limit** and **Late departure limit**.

</details>

<details>

<summary>Does this affect pricing?</summary>

Yes. Each triggered limit adds the cost of **one hotel night**.

</details>

### Related pages

* [Transport Definition](transport-definition.md)
* [Setup for Transport Dynamic Packaging (GDS)](../../real-transports/setup-for-transport-dynamic-packaging-gds.md)
