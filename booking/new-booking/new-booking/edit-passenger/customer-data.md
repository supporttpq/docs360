---
description: >-
  The Customer Data tab controls who receives booking communications. Use this
  tab to set the main customer contact and choose which passengers get emails
  and SMS messages.
---

# Customer Data

### Overview

Customer Data manages communication settings for the booking. The main tasks are selecting the primary customer contact and enabling email/SMS delivery to other passengers. The primary customer receives all booking confirmations, invoices, and travel documents. Additional passengers can be opted in to receive copies of the same communications.

{% hint style="info" %}
Need the full flow? See [Edit Passenger](./).
{% endhint %}

### Purpose

Use Customer Data to:

* Designate the main customer contact for the booking
* Control who receives booking emails (confirmations, tickets, invoices)
* Control who receives booking SMS messages
* Update customer contact information (email, phone, address)
* Ensure communications reach the right people

### Requirements

Before using Customer Data:

* Booking must be saved and accessible
* User must have permission to edit bookings
* At least one passenger must exist in the booking

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

### Related Pages

**Core Customer Pages:**

* [Edit Passenger](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/new-booking/edit-passenger) - Passengers tab for managing traveler details
* [Customers](https://tourpaq.gitbook.io/staging-tourpaq-docs/customer/customers) - Customer database management
* [Customer Info / Details on Customer Card](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/customer-info-details-on-customer-card) - Detailed customer profile

**Communication Pages:**

* [E-mails](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/e-mails) - Booking email history and management
* [SMS](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/sms) - Booking SMS history and management
* [Email Center](https://tourpaq.gitbook.io/staging-tourpaq-docs/email-setup/e-mail-center) - Email template configuration
* [Dynamic E-mail/SMS Center](https://tourpaq.gitbook.io/staging-tourpaq-docs/email-setup/dynamic-e-mail-sms-center) - Advanced communication workflows

**Booking Management:**

* [New Booking](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/new-booking) - Initial booking creation
* [Booking Overview](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/booking-overview) - Main booking interface
* [All Bookings](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/all-bookings) - Booking search and access
