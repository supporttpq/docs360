# Name change rule

Some airlines (for example, charter flights) allow passenger name changes until departure. Others do not allow name changes at all, or only until a defined cutoff before departure.

### Overview

The **Name Change Rule** controls whether passenger name changes are allowed for a transport.

It lets you set separate rules for:

* **Office** users (back office staff).
* **WebBooking** users (customers).

It also lets you enforce a shared deadline (in days before departure).

### Purpose

The purpose of this functionality is to:

* Ensure consistent handling of name change requests.
* Reduce last-minute changes that can cause supplier or cost issues.
* Separate internal changes (Office) from customer self-service (WebBooking).

### Preconditions

* A transport option must already be created in the system.
* Your supplier policy for name changes must be known.

### Instructions

1. Open the relevant transport in **Transport creation**.
2. Go to the **Name Change Rule** section.
3. Configure the fields based on your supplier policy.
4. Save.

### Field Descriptions

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (5).png" alt=""><figcaption></figcaption></figure>

| Field                                            | Description                                                                                                                                                         |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Do Not Allow Name Change Office**              | When enabled, Office users cannot change passenger names for this transport. This restriction applies after payment is registered.                                  |
| **Do Not Allow Name Change Web**                 | When enabled, customers cannot change passenger names in WebBooking.                                                                                                |
| **Name change deadline (days before departure)** | Defines the latest point a name change is allowed. Example: set to **7** to allow name changes until 7 days before departure. After that, name changes are blocked. |

{% hint style="info" %}
The deadline is evaluated against the transport’s **departure date**.
{% endhint %}

### Related pages

* [Transport creation](./)
* [Transport Definition](../../../real-transports/transport-definition.md)
