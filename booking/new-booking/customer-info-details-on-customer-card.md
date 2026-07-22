---
description: >-
  Enable and use Customer details on the customer card in Tourpaq Office. Edit
  and save customer information (Details field) directly from a booking for
  reuse in future bookings.
---

# Customer info / Details on customer card

### Overview

When enabled, **Customer details on customer card** lets authorized users view and edit extra **customer information** **directly from the customer card inside a booking** in **Tourpaq Office**.

The information entered in the **Details** area is saved on the **customer record** and will be shown again the next time the same customer is used in a booking.

***

### Purpose

* Capture and maintain customer information while you are already working in a booking.
* Avoid switching context to other modules to update customer data.
* Ensure consistent customer data across future bookings that reuse the same customer.

***

### Preconditions

* The feature must be enabled in **System Setup → Settings**.
* You must have permission to **edit customer information**.
* A customer must be selected/identified on the booking (often by phone number, depending on your setup).

{% hint style="warning" %}
Be careful with what you store in the **Details** field. Follow your organization’s GDPR/privacy rules and avoid storing unnecessary sensitive information.
{% endhint %}

***

### Field explanation

| UI element                                           | Description                                                                                                          |
| ---------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Show details of customer** (System Setup checkbox) | Enables/disables the feature. When enabled, a **Details** area becomes available from the customer card in bookings. |
| **Edit** (on the customer card)                      | Opens the customer card fields for editing (including **Details**).                                                  |
| **Details**                                          | Additional customer information stored on the customer record and reused on future bookings.                         |
| **Save** (booking)                                   | Saves the booking and persists the customer card changes (including **Details**) to the customer record.             |

***

### How it works

{% stepper %}
{% step %}
**1. Enable the feature**

1. Go to **System Setup → Settings**.
2. Enable **Show details of customer**.
3. Click **Save**.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="System Setup setting: Show details of customer"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**2. Open a booking and identify the customer**

1. Go to **Booking → New Booking** (or open an existing booking).
2. Select the customer (for example by entering the phone number, depending on your workflow).
{% endstep %}

{% step %}
**3. Edit the customer card details**

1. On the customer card, click **Edit**.
2. Enter/update the **Details** content.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (18).png" alt="Customer card in booking: Edit customer details field"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**4. Save and verify**

1. Click **Save** on the booking.
2. Re-open the booking (or open a new booking for the same customer) and confirm the Details are shown.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Customer Details field saved and visible on the customer card"><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

***

### What is saved (and where)

* The **Details** content is saved on the **customer record**.
* Because it is stored on the customer, it can appear again when the same customer is used on **future bookings**.

{% hint style="info" %}
If your booking flow enforces customer acknowledgements/terms, see: [Customer Information Booking Flow](../../customer-information-errata/customer-information-booking-flow.md).
{% endhint %}
