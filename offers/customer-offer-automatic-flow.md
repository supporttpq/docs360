---
description: >-
  Automate offer follow-ups with scheduled reminder emails and SMS. Configure
  schedules per brand, enable Send Schedule Email/SMS on offers, and
  verify/cancel reminders in Email History.
---

# Customer offers automatic flow

### Overview

**Customer offers automatic flow** lets Tourpaq automatically send **offer reminder messages** by **email and/or SMS**.

It’s designed for follow-up: once an offer is sent, the system can send reminders at the intervals you define—so consultants don’t have to remember to chase every customer manually.

***

### Before you start

* You need access to **Brands** and the **Offers** module.
* Automatic reminders are typically configured **per Brand**.

{% hint style="info" %}
This feature sends **reminders**. Your team still sends the **initial offer** manually from the offer screen.
{% endhint %}

***

### Where to configure it

Go to:

* **Brands → (select a Brand) → Select Offer**

This is the same area where you manage offer texts, images, and templates. See [Select text for Offers](select-text-for-offers.md).

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (91).png" alt="Automatic offer reminder settings in Brand → Select Offer"><figcaption><p>Brand settings for reminder schedule days and email/SMS reminder templates.</p></figcaption></figure>

***

### Key settings explained

#### Email reminder schedule days

Enter the reminder timing as **comma-separated days**, for example:

* `3,7,14,21`

Each number represents a reminder point in days based on your offer reminder rules (commonly counted from when the offer is sent).

{% hint style="warning" %}
If you enable scheduled reminders but leave the schedule days empty, nothing will be sent.
{% endhint %}

#### Reminder message templates

Configure the content used for reminders:

* **Mail reminder subject**
* **Mail reminder body**
* **SMS reminder body**

Use placeholders (variables) where supported.

If you also use SMS templates, see [Customer Offer SMS template](customer-offer-sms-template.md).

#### Send Schedule Email / Send Schedule SMS

These options control whether reminders are sent by:

* Email
* SMS

You may see these as checkboxes in the Brand setup and/or when working with the offer (depending on your configuration).

***

### Use automatic reminders on an offer

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (36).png" alt="Enable scheduled email/SMS reminders on an offer"><figcaption><p>Enable Send Schedule Email and/or Send Schedule SMS on the offer.</p></figcaption></figure>

{% stepper %}
{% step %}
#### 1) Configure the Brand reminder settings

In **Brand → Select Offer**:

1. Set **Email reminder schedule days** (for example `3,7,14`).
2. Write your reminder **email subject/body** (and SMS body if needed).
3. Save.
{% endstep %}

{% step %}
#### 2) Create and send the initial offer

Create an offer and send it to the customer.

If you need help creating an offer, see [Create new offer](create-new-offer.md).
{% endstep %}

{% step %}
#### 3) Enable scheduled reminders (email and/or SMS)

On the offer, enable:

* **Send Schedule Email** and/or
* **Send Schedule SMS**

This schedules the reminders according to the days you configured for the Brand.
{% endstep %}

{% step %}
#### 4) Verify reminders in Email History

Open **Email History** to confirm which reminders are queued/sent.
{% endstep %}
{% endstepper %}

***

### Email History (how to read it)

<figure><img src="../.gitbook/assets/image (276).png" alt="Email history showing sent and canceled scheduled emails"><figcaption><p>Email History shows sent reminders and canceled scheduled messages.</p></figcaption></figure>

Email History helps you verify what happened:

* You can see a log of **sent** messages.
* Scheduled messages that were **canceled or not sent** may appear **in red** (depending on your setup).

{% hint style="info" %}
If the customer accepts the offer and a booking is created, remaining scheduled reminders for that offer are typically **canceled automatically**.
{% endhint %}

***

### Troubleshooting (common questions)

#### No reminders are being sent

Check:

* You entered **Email reminder schedule days** (for example `3,7,14`).
* The reminder **email/SMS body** is filled in.
* **Send Schedule Email/SMS** is enabled for the offer.

#### The SMS is missing the custom text

Make sure your SMS template includes the `[Message]` placeholder. See [Customer Offer SMS template](customer-offer-sms-template.md).

***

### What this improves for your team

* **Consistent follow-up** across consultants and teams.
* **Less manual work** (reminders happen automatically).
* **Better overview** of communication through Email History.
* **Fewer duplicate messages**, because reminders are canceled when the offer turns into a booking.

### FAQ

<details>

<summary><strong>Are reminders sent automatically when I create an offer?</strong></summary>

No.

You send the initial offer manually. Reminders are scheduled only after:

* the brand schedule is configured, and
* **Send Schedule Email/SMS** is enabled on the offer.

</details>

<details>

<summary><strong>What do “Email reminder schedule days” mean?</strong></summary>

They are comma-separated day offsets like `3,7,14`.

Each value is a reminder point (commonly counted from when the offer is sent).

</details>

<details>

<summary><strong>Why are no reminders being sent?</strong></summary>

Check these first:

* schedule days are filled (`3,7,14` etc.)
* reminder subject/body (and SMS body) is filled
* **Send Schedule Email/SMS** is enabled on the offer
* you edited the correct **Brand**

</details>

<details>

<summary><strong>What happens to scheduled reminders if the customer books?</strong></summary>

Remaining scheduled reminders are typically **canceled automatically** when the offer is converted to a booking.

Verify in **Email History**.

</details>

<details>

<summary><strong>Why is the SMS missing the text I typed?</strong></summary>

Your SMS template must include the `[Message]` placeholder.

See [Customer Offer SMS template](customer-offer-sms-template.md).

</details>
