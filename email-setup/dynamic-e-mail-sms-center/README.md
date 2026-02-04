---
description: Send targeted emails or SMS messages to selected bookings using filters.
---

# Dynamic E-mail/SMS Center

### Overview

Use the **Dynamic E-mail/SMS Center** to send emails or SMS messages to bookings. You choose who receives the message using filters. This helps you send the right message at the right time.

### Access

Open **E-mail Setup → Dynamic E-mail/SMS Center**.

### Purpose

Use this feature to:

* Send important reminders, like departure reminders.
* Welcome guests when they arrive.
* Follow up after the trip.
* Share optional add-ons or upgrades.

### Template list columns

<figure><img src="../../.gitbook/assets/image (377).png" alt="Dynamic E-mail/SMS Center template list."><figcaption><p>Template list with status and last update.</p></figcaption></figure>

* **Template name**: a short name you recognize later.
* **Brand**: which brand or agency the template belongs to.
* **Type**: email or SMS.
* **Last update**: when the template was last changed.
* **Updated by**: who last changed it.
* **Active**: whether the template can be used.
* **Delete**: removes the template.

{% hint style="info" %}
Filters are used to pick the bookings you want to contact. For example, you can filter by departure date.
{% endhint %}

### Email vs SMS

* **Dynamic E-mail**
  * Has a subject and a message body.
  * Works well for longer messages.
* **Dynamic SMS**
  * Uses the subject text as the full message.
  * There is no separate message body.
  * Works best for short reminders.

### What you can do on this page

You can:

* Create new email or SMS templates.
* Send a template to a selected group of bookings.
* Apply filters to define the target audience.
* See when a template was last updated.

{% hint style="danger" %}
**Important**

* Once an email or SMS template is sent to a booking, it **cannot be resent**.
* Avoid editing a template after sending it. One booking can only receive it once.
* Double-check the text and filters before sending.
{% endhint %}

### Typical steps

{% stepper %}
{% step %}
#### 1. Create a template

Choose whether you want an email or an SMS template. Give it a clear name.
{% endstep %}

{% step %}
#### 2. Write the message

Write the subject text. For emails, also write the message body.
{% endstep %}

{% step %}
#### 3. Choose who should receive it

Set the filters for the bookings you want to reach.
{% endstep %}

{% step %}
#### 4. Send and confirm

Review the message and the filters. Send when you are ready.
{% endstep %}
{% endstepper %}

### Example

* Create an SMS template for a departure reminder.
* Set the filter to **departure date = tomorrow**.
* Send it to all matching bookings.

### FAQ

<details>

<summary>Can I resend the same template to the same booking?</summary>

No. A booking can receive a template only once. Create a new template if you need to send again.

</details>

<details>

<summary>Can I edit a template after sending it?</summary>

You can edit it, but it is not recommended. Edits will not resend messages already sent.

</details>

<details>

<summary>Why does my SMS not include the message body?</summary>

Dynamic SMS uses the subject as the full message. It does not have a separate body field.

</details>

<details>

<summary>What does “Active” mean?</summary>

Active means the template can be used. Inactive means it is blocked from use.

</details>

<details>

<summary>Why did nobody receive my message?</summary>

Most of the time, the filters did not match any bookings. Also check that the template is **Active**.

For SMS, make sure the booking has a phone number. For email, make sure the booking has an email address.

</details>

<details>

<summary>How do I avoid sending to the wrong customers?</summary>

Start with a narrow filter. Send to a small test group first. Then widen the filters when you are confident.

</details>

<details>

<summary>Can I test a message before I send it to everyone?</summary>

Yes. Use filters to target one test booking first. Check the result. Then send to the full audience.

</details>

<details>

<summary>What if I sent a message by mistake?</summary>

You cannot undo a send. Send a new message that corrects the information. Use a new template for the correction.

</details>

<details>

<summary>Can I send both an email and an SMS?</summary>

Yes, but they are separate templates. Create one email template and one SMS template. Send each one to the same filtered group.

</details>

<details>

<summary>Should I delete old templates?</summary>

If you might need them later, set them to **Inactive**. Delete them only when you are sure they are no longer needed.

</details>

<details>

<summary>My SMS looks too long. What should I do?</summary>

Keep SMS messages short and direct. If you need more detail, use an email instead.

</details>
