---
description: >-
  Manage booking contact details in Tourpaq Office. Set the main
  customer/contact person and choose which passengers receive booking emails and
  SMS notifications from the Customer Data tab.
---

# Customer Data

### Overview

The **Customer Data** tab in **Tourpaq Office** controls **booking communication recipients**. You use it to pick the **main customer/contact person** and decide who receives **booking emails** and **SMS notifications**.

This view is available in the **Edit Passenger** window from a booking.

While **Passengers** focuses on personal details (name, birthdate, age), **Customer Data** defines **customer-level contact details and message distribution**.

{% hint style="info" %}
Need the full flow? See [Edit Passenger](./).
{% endhint %}

### When to use it

Use **Customer Data** when you need to:

* Change who receives confirmations, travel documents, and updates.
* Add an extra recipient for the same emails/SMS as the customer.
* Ensure the booking has correct customer contact details (email/phone/address).

This matters because invoices, confirmations, travel documents, and operational messages are typically sent to the selected **Customer** and any passengers opted in for **EMAIL**/**SMS**.

### Quick workflow (recommended)

{% stepper %}
{% step %}
### Open Customer Data

Open the booking, click **Edit** in the passenger section, then open **Customer Data**.
{% endstep %}

{% step %}
### Set the main customer/contact person

Check **CUSTOMER** on the passenger who owns the booking communication.
{% endstep %}

{% step %}
### Select recipients for Email and SMS

Use **EMAIL** and **SMS** to send the same messages to additional passengers.
{% endstep %}

{% step %}
### Save

Click **Save Changes** in the Edit Passenger window.
{% endstep %}
{% endstepper %}

### Fields

<figure><img src="../../../../.gitbook/assets/image (564).png" alt="Customer Data tab showing email and SMS recipients"><figcaption></figcaption></figure>

| Field         | What it means                                                                                                                                             |
| ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **TITLE**     | Passenger title (Mr., Mrs., Chd, Inf, etc.). Read-only here.                                                                                              |
| **F. NAME**   | First name. Read-only here.                                                                                                                               |
| **L. NAME**   | Last name. Read-only here.                                                                                                                                |
| **AGE**       | Passenger age used for pricing logic. Read-only here.                                                                                                     |
| **BIRTHDATE** | Birthdate used for passenger classification. Read-only here.                                                                                              |
| **E-MAIL**    | Email address used for booking communication and document delivery.                                                                                       |
| **PHONE**     | Phone number used for SMS and contact.                                                                                                                    |
| **ADDRESS**   | Address for the passenger. Usually stored for the main customer.                                                                                          |
| **CUSTOMER**  | Sets the passenger as the booking’s **main customer/contact person**. If the passenger has email and phone, Tourpaq can create/update a customer profile. |
| **SMS**       | Sends the same booking SMS as the customer to this passenger.                                                                                             |
| **EMAIL**     | Sends the same booking emails as the customer to this passenger.                                                                                          |

{% hint style="warning" %}
Avoid adding unnecessary sensitive data. Follow your organization’s GDPR and data-retention rules.
{% endhint %}

### Summary

Use **Customer Data** to control **who is the booking customer** and **who receives emails and SMS**. Keep contact details correct to avoid missed confirmations, invoices, and travel documents.

### FAQ

<details>

<summary><strong>What’s the difference between </strong><em><strong>Customer</strong></em><strong> and </strong><em><strong>Passengers</strong></em><strong>?</strong></summary>

Passengers are the travellers on the booking.\
The **Customer** is the main contracting/contact person who typically receives booking documents and messages.

</details>

<details>

<summary><strong>Can I send booking emails/SMS to more than one person?</strong></summary>

Yes. Set the main person using **CUSTOMER**.\
Then enable **EMAIL** and/or **SMS** on other passengers to send them the same messages.

</details>

<details>

<summary><strong>Why are some fields read-only here?</strong></summary>

Name, title, age, and birthdate are managed in the **Passengers** tab.\
Customer Data focuses on communication and customer identification.

</details>

<details>

<summary><strong>What if the wrong person is receiving confirmations and documents?</strong></summary>

Open **Customer Data** and move the **CUSTOMER** flag to the correct passenger.\
Adjust **EMAIL**/**SMS** checkboxes for any extra recipients.\
Then click **Save Changes**.

</details>

<details>

<summary><strong>Does marking a passenger as CUSTOMER create a CRM customer record?</strong></summary>

Often, yes. If the passenger has enough contact info (typically **email** and **phone**), Tourpaq can create or update the customer profile used in CRM.

</details>

<details>

<summary><strong>I updated email/phone, but messages still go to the old address. What should I check?</strong></summary>

Make sure you clicked **Save Changes** in the Edit Passenger window.\
If documents were already generated/sent, you may need to regenerate or resend them, depending on your ticket/email flow.

</details>
