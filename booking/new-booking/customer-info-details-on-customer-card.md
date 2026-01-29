# Customer info / Details on customer card

### Overview

When enabled, **Customer details on customer card** lets authorized users view and edit extra customer information **directly from the customer card inside a booking**.

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
### 1. Enable the feature

1. Go to **System Setup → Settings**.
2. Enable **Show details of customer**.
3. Click **Save**.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### 2. Open a booking and identify the customer

1. Go to **Booking → New Booking** (or open an existing booking).
2. Select the customer (for example by entering the phone number, depending on your workflow).
{% endstep %}

{% step %}
### 3. Edit the customer card details

1. On the customer card, click **Edit**.
2. Enter/update the **Details** content.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### 4. Save and verify

1. Click **Save** on the booking.
2. Re-open the booking (or open a new booking for the same customer) and confirm the Details are shown.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

***

### What is saved (and where)

* The **Details** content is saved on the **customer record**.
* Because it is stored on the customer, it can appear again when the same customer is used on **future bookings**.

{% hint style="info" %}
If your booking flow enforces customer acknowledgements/terms, see: [Customer Information Booking Flow](../../customer-information-errata/customer-information-booking-flow.md).
{% endhint %}

***

### FAQ

#### 1. I don’t see the “Details” field on the customer card — why?

Most common reasons:

* The setting **Show details of customer** is not enabled in **System Setup → Settings**.
* Your user does not have permission to edit customer data.
* A customer has not been identified/selected on the booking yet.

***

#### 2. Are the details saved on the booking or on the customer?

They are saved on the **customer record**. That’s why they can show up again in future bookings for the same customer.

***

#### 3. Does saving the booking also save the customer details?

Yes—when this feature is used, saving the booking persists changes made on the customer card (including **Details**) back to the customer record.

***

#### 4. Who should use this feature?

It’s intended for users who create or update bookings and need a quick place to store customer-related notes or contact details as part of the booking workflow.

***

#### 5. What should _not_ be stored in the Details field?

Avoid storing unnecessary sensitive information (for example, government IDs or health data) unless your organization explicitly allows it and you have a lawful basis.

***

#### 6. The customer’s phone number matches multiple customers — what happens?

In some setups, Tourpaq can prompt you to select the correct customer. If you frequently see duplicates, consider cleaning up customer data or aligning your customer identification rules (internal procedure).
