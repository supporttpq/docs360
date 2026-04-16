---
description: >-
  Track SMS messages in Tourpaq Office. Search by booking number or phone
  number, filter by sent/departure period, and check delivery status
  (sent/failed/pending).
---

# SMS Overview

### Overview

Use **SMS Overview** to monitor outgoing SMS messages in **Tourpaq Office**. This is the central SMS log for booking and operational notifications. Use it to troubleshoot “SMS not received” before departure.

{% hint style="info" %}
SMS functionality is integrated via an external provider (e.g. Twilio) and must be configured before use.
{% endhint %}

***

### Purpose

The SMS feature is used to:

* send real-time communication to customers
* automate notifications (confirmations, reminders, alerts)
* support quick, direct interaction without email
* improve response time and engagement

***

### Access & Preconditions

#### Requirements

* SMS integration must be enabled by a super admin
* SMS service must be activated for the company
* Valid customer phone number must exist

{% hint style="info" %}
SMS communication is available in modules like service cases and offers.
{% endhint %}

{% hint style="warning" %}
If SMS integration or configuration is missing, messages cannot be sent.
{% endhint %}

### What you can do on this page

* Search the SMS log by **booking number** or **phone number**.
* Filter by **sent period** and **departure period**.
* Verify **SMS delivery status** (Sent / Failed / Pending).
* Review SMS communication history for support, operations, and audits.

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (10).png" alt="Tourpaq Office SMS Overview page showing filters and an SMS delivery log with statuses and booking references"><figcaption><p>SMS Overview in Tourpaq Office. Use it to search SMS history and check SMS delivery status for a booking.</p></figcaption></figure>

{% hint style="info" %}
If you need the SMS log for a single booking, use the booking **SMS** tab: [SMS](booking/new-booking/sms.md).
{% endhint %}

***

### Filters

Use filters to narrow down the list of SMS messages. Combine filters to find one customer fast.

#### Available filters

| Filter               | Description                                                                  |
| -------------------- | ---------------------------------------------------------------------------- |
| **SMS type**         | Select the category of SMS (e.g., Booking SMS, Payment SMS, Operational SMS) |
| **Sent period**      | Define a date range in which the SMS was sent                                |
| **Phone number**     | Search by recipient phone number                                             |
| **Status**           | Filter by status: Sent, Failed, Pending                                      |
| **Departure period** | Filter based on the passenger’s departure date                               |
| **Booking number**   | Search for SMS linked to a specific booking number                           |

#### Display / More Filters / Clear

* **Display** – Apply selected filters
* **More Filters** – Show additional filter fields
* **Clear** – Reset all filters to default

***

### Table overview

Each row represents a single SMS message.

| Column              | Description                                      |
| ------------------- | ------------------------------------------------ |
| **Date Sent**       | Timestamp when the system sent the SMS           |
| **To Phone Number** | The recipient’s phone number                     |
| **Message**         | The SMS text (may be anonymized for GDPR)        |
| **Status**          | Delivery status of the SMS                       |
| **Booking**         | Booking number connected to the SMS              |
| **Dept. Date**      | Passenger’s departure date linked to the message |

***

### Troubleshooting checklist

If a customer says they did not receive an SMS:

1. Search by **booking number** or **phone number**.
2. Check the **Status** (Sent / Failed / Pending).
3. Verify the phone number format and country code in the booking/customer data.
4. Check whether the correct **SMS type** template was used.
5. Export the filtered list if you need to escalate to IT/support.

### FAQ

#### Why is the SMS text anonymized?

Some setups mask message text to protect personal data. This supports GDPR and internal privacy policies.

#### What does **Pending** mean?

The SMS is queued and not confirmed as delivered yet. Refresh later or narrow the sent period to confirm the final status.

#### Can I resend an SMS from this page?

That depends on your setup and permissions. If resending is not available here, resend via the booking flow or your SMS tool.
