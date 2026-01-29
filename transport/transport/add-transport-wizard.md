# Add Transport Wizard

### Overview

Use **Add Transport Wizard** to create a new transport route.

You define the route, operating period, and repeat pattern.

You also assign the transport to one or more brands.

### Purpose

Use this wizard to:

* Create new transport entries used in tour packages or product configurations.
* Define the transport’s operating period and repetition.
* Link the transport to one or more brands.
* Control core settings like travel length and availability.

This ensures consistent and accurate transport data across booking systems and external integrations.

***

### Fields

<figure><img src="../../.gitbook/assets/image (431).png" alt=""><figcaption></figcaption></figure>

| **Field**                    | **Description**                                                                                                                                                                      |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Code**\*                   | Unique identifier for the transport route (e.g., _FL1234_ or _BUS001_). Used to distinguish between different connections.                                                           |
| **Return**\*                 | Specifies the return route code.                                                                                                                                                     |
| **Departure**\*              | Defines the departure location for the transport route.                                                                                                                              |
| **Arrival**\*                | Defines the destination location for the transport route.                                                                                                                            |
| **Cancellation Condition**\* | Select the cancellation rule for this transport.                                                                                                                                     |
| **Transport Mode**\*         | Defines the type of transport (e.g., _Flight_, _Bus_, _Train_).                                                                                                                      |
| **Travel Length Correction** | Adjust the travel length (days), if needed.                                                                                                                                          |
| **Free Sell**                | Checkbox that, when enabled, allows selling without seat or space limitations.                                                                                                       |
| **Interval**                 | Defines how often the transport repeats (for example, every `7` days).                                                                                                               |
| **Date From**                | The start date from which the transport becomes available for sale.                                                                                                                  |
| **Date To**                  | The last date when this transport is available.                                                                                                                                      |
| **Days**\*                   | Indicates the number of days the transport takes. It is used for automatic fix quota generation.                                                                                     |
| **API Text**                 | Custom text used for external API connections or partner systems.                                                                                                                    |
| **Override Period**          | Overrides the default period used when generating departures. Use this only if you know you need it.                                                                                 |
| **Brands**                   | Section for assigning the transport to one or more brands (e.g., _Tourpaq DK_, _Tourpaq Live_). Each brand can be set as _Assigned_ or _Not assigned_ depending on access and usage. |

{% hint style="info" %}
Fields marked with `*` are required.
{% endhint %}

***

### Typical workflow

{% stepper %}
{% step %}
### Create the transport

Fill in the required fields:

* **Code**
* **Return**
* **Departure**
* **Arrival**
* **Cancellation Condition**
* **Transport Mode**
* **Days**

If needed, set **Travel Length Correction**.
{% endstep %}

{% step %}
### Set the operating period and repetition

Set:

* **Date From** and **Date To**
* **Interval**
{% endstep %}

{% step %}
### Assign brands and save

Assign the relevant **Brands**.

Click **Save**.

If you skip brand assignment, the transport may not show up for sales flows.
{% endstep %}
{% endstepper %}

### Example

Add a weekly bus route between _Copenhagen_ and _Aarhus_:

1. Enter **Code:** _BUS1001_ and **Return:** _BUS1002_.
2. Select **Departure:** _Copenhagen_ and **Arrival:** _Aarhus_.
3. Choose **Transport Mode:** _Bus_ and **Cancellation Condition:** _Standard Policy_.
4. Set **Interval:** 7 (runs every 7 days).
5. Set **Date From:** _27-10-2025_ and **Date To:** _27-10-2026_.
6. Enter **Days:** 7.
7. Assign to brand **Tourpaq DK**.
8. Save the new transport.

***

### Tips

* Use meaningful codes (for example, `BUS101` or `FLT202`).
* Make sure **Return** points to the correct return route.
* For seasonal routes, update **Date From** and **Date To** each season.
* Assign the transport to the right brand(s).

### FAQ

<details>

<summary>What’s the difference between <strong>Interval</strong> and <strong>Days</strong>?</summary>

* **Interval** controls how often departures repeat.
* **Days** is the travel length used for automatic quota generation.

</details>

<details>

<summary>Do I have to set a <strong>Return</strong> code?</summary>

Yes. Set **Return** to the code of the opposite direction route.

This is required for round-trip flows.

</details>

<details>

<summary>When should I use <strong>Free Sell</strong>?</summary>

Use it when you don’t manage capacity with seat allotments.

Example: transfers with unlimited capacity.

</details>

<details>

<summary>Why can’t I find the transport after saving?</summary>

Most common causes:

* You did not assign any **Brands**.
* Your filters in the transport list exclude the new code.
* The transport is not in the date range you are working with.

</details>

<details>

<summary>What is <strong>Override Period</strong> used for?</summary>

It changes how departures are generated for this transport.

Use it only when you have a specific generation requirement.

</details>

### Related pages

* [Transport](./)
* [Transport creation](transport-creation/)
* [All Transports](../all-transports.md)
