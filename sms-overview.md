---
description: >-
  Track SMS messages in Tourpaq Office. Search by booking number or phone
  number, filter by sent/departure period, and check the status of each SMS
  (queued, sent, failed).
---

# SMS Overview

**Tickets** › **SMS Overview**

### Overview

Use **SMS Overview** to monitor outgoing SMS messages in **Tourpaq Office**. This is the central SMS log for booking and operational notifications. Use it to troubleshoot “SMS not received” before departure.

{% hint style="info" %}
Tourpaq sends SMS through your company's SMS provider: [Compaya](integration/crm-and-marketing/compaya/), [Twilio](integration/crm-and-marketing/system-setup-sms-configuration-twilio.md), or [Mail Platform](integration/crm-and-marketing/system-setup-mail-platform.md) (deprecated). See [How Tourpaq sends SMS](sms-overview.md#how-tourpaq-sends-sms).
{% endhint %}

***

### Purpose

The SMS feature is used to:

* send messages to customers and passengers by SMS, from Tourpaq Office and automatically, such as offer reminders and flight change reminders
* send two-factor login codes to Tourpaq users
* see which SMS Tourpaq sent, and which failed

***

### Access & Preconditions

#### Requirements

* Tourpaq Support turns on **SMS integration** for your company and schedules the **SMS Service**.
* Your company has an SMS provider, chosen and set up under **Setup** › **System Setup** › **SMS Config**.
* The customer has a phone number.
* To open **Tickets** › **SMS Overview**, you need the role Administrator, Brand Manager, or Sales, and the user right **Sms Overview**.

{% hint style="info" %}
SMS communication is available in modules like service cases and offers.
{% endhint %}

{% hint style="warning" %}
If SMS integration or configuration is missing, messages cannot be sent.
{% endhint %}

### What you can do on this page

* Search the SMS log by **phone number**, or by **booking number** for **Booking SMS**.
* Filter by **sent period**, and by **departure period** for **Booking SMS**.
* Check the **status** of each SMS: queued, sent, or failed.
* Review SMS communication history for support, operations, and audits.

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (14).png" alt="Tourpaq Office SMS Overview page showing filters and an SMS log with statuses and booking references"><figcaption><p>SMS Overview in Tourpaq Office. Use it to search SMS history and check the status of each SMS for a booking.</p></figcaption></figure>

{% hint style="info" %}
If you need the SMS log for a single booking, use the booking **SMS** tab: [SMS](booking/new-booking/sms.md).
{% endhint %}

***

### Filters

Use filters to narrow down the list of SMS messages. Combine filters to find one customer fast.

#### Available filters

| Filter               | Description                                                                                                                              |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **SMS type**         | Select the SMS type, for example **Booking SMS**, **Customer SMS**, or **Dynamic SMS**                                                   |
| **Sent period**      | Define a date range in which the SMS was sent                                                                                            |
| **Phone number**     | Search by recipient phone number                                                                                                         |
| **Status**           | Filter by status, for example **queued**, **sent**, or **failed**                                                                        |
| **Departure period** | Filter based on the passenger’s departure date. Shows when **Booking SMS** is selected                                                   |
| **Booking number**   | Search for SMS linked to a specific booking number. Shows when **Booking SMS** is selected                                               |
| **Customer Email**   | Search by the customer's email address. Shows when an SMS type other than **Booking SMS** is selected, and filters only **Customer SMS** |

#### Display / More Filters / Clear

* **Display** – Apply selected filters
* **More Filters** – Show additional filter fields
* **Clear** – Reset all filters to default

***

### Table overview

Each row represents a single SMS message.

| Column              | Description                                                                                                     |
| ------------------- | --------------------------------------------------------------------------------------------------------------- |
| **Date Sent**       | When Tourpaq created the SMS. The SMS Service sends it on its next run, or at its send time for a scheduled SMS |
| **To Phone Number** | The recipient’s phone number                                                                                    |
| **Message**         | The SMS text (may be anonymized for GDPR)                                                                       |
| **Status**          | The status of the SMS: queued, sent, or failed. See [Status](sms-overview.md#status)                            |
| **Booking**         | Booking number connected to the SMS. Shows when the SMS type is **Booking SMS**                                 |
| **Dept. Date**      | Passenger’s departure date linked to the message. Shows when the SMS type is **Booking SMS**                    |
| **Customer**        | The customer of the SMS. Shows when the SMS type isn't **Booking SMS**                                          |

***

### How Tourpaq sends SMS

Tourpaq doesn't send an SMS the moment it's created. It puts the SMS in a queue, and the **SMS Service** sends the queue through your company's SMS provider.

#### SMS providers

Your company uses one SMS provider for all its brands. You choose it in **SMS Provider** on **Setup** › **System Setup** › **SMS Config** › **General**, and fill in the provider's own tab:

| Provider                                                                         | How Tourpaq sends                                                                                |
| -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| [Twilio](integration/crm-and-marketing/system-setup-sms-configuration-twilio.md) | Through your Twilio account, from one Twilio phone number or sender ID.                          |
| [Mail Platform](integration/crm-and-marketing/system-setup-mail-platform.md)     | Deprecated. By email to Mail Platform's email-to-SMS gateway, through your brands' SMTP servers. |
| [Compaya](integration/crm-and-marketing/compaya/)                                | Through your Compaya account, with a sender name or number per brand.                            |

Without a provider, Tourpaq keeps every SMS in the queue and sends none.

#### Which messages are SMS

Tourpaq creates an SMS for:

* SMS you send to bookings from **All Bookings** (**Booking SMS**), and to customers (**Customer SMS**).
* Templates of the [Dynamic E-mail/SMS Center](email-setup/dynamic-e-mail-sms-center/) (**Dynamic SMS**).
* [Guide App SMS](guest-app/guide-app/sms.md), and confirmations and cancellations of extra orders (**Destination APP Sms**).
* Offers and offer reminders (**Select Offer Sms**). See [Customer Offer SMS template](offers/customer-offer-sms-template.md).
* Flight change reminders (**Flight Time Change**). See [Flight change](flight-change/).
* SMS from a service case. See [Communication (Email & SMS)](service-cases/communication-email-and-sms.md).
* Two-factor login codes. See [System Setup – Two-Factor Authentication (2F Auth)](setup/system-setup/system-setup-two-factor-authentication-2f-auth.md).
* Warnings, for a [warning notification rule](warning-notification-rules.md) that sends SMS.
* The daily managers' statistics, to the **Manager Statistic phone** on **System Setup** › **General information**.

The names in bold are the values of the **SMS type** filter. The other SMS show when no SMS type is selected.

#### When Tourpaq sends them

* The SMS Service runs for your company every five minutes, and sends every SMS in the queue. Tourpaq Support can set another interval.
* A two-factor login code for Tourpaq Office goes out at once.
* A scheduled SMS, such as an offer reminder, waits until its send time.

#### Phone numbers

Tourpaq cleans and formats each number before it sends the SMS:

* It removes spaces, brackets, dashes, dots, and slashes, so `+46 70-123 45 67` goes out as `+46701234567`.
* After `+` or `00` at the start, it drops a `(0)`, so `+45 (0) 12345678` goes out as `+4512345678`.
* `00` at the start becomes `+`, so `004512345678` goes out as `+4512345678`.
* With Mail Platform and Compaya, Tourpaq removes a single leading `0`.
* A number without `+` gets the dialing code of the customer's country in front, when the number, as it's stored, is the customer's **Phone**.
* A number with any other character, such as a letter, isn't sent: the SMS gets the status **failed**. The other SMS still go out.

Store phone numbers with their country code, such as `+45`, so that every SMS reaches the right phone.

#### Message length

Tourpaq cuts each SMS after 160 characters. To send longer SMS, select **Remove Body Limitation** on **Setup** › **System Setup** › **SMS Config** › **General**.

#### Status

| Status     | Meaning                                                                                                               |
| ---------- | --------------------------------------------------------------------------------------------------------------------- |
| **queued** | Waiting for the next run of the SMS Service.                                                                          |
| **sent**   | The provider accepted the SMS. Tourpaq gets no delivery reports, so **sent** doesn't mean that the phone received it. |
| **failed** | The provider refused the SMS, or Tourpaq couldn't send it. Tourpaq doesn't try again, and creates no warning for it.  |

***

### Troubleshooting checklist

If a customer says they did not receive an SMS:

1. Search by **phone number**, or select **Booking SMS** and search by **booking number**.
2. Check the **Status**:
   * **queued** for more than a few minutes: check your provider's tab on **SMS Config**, and ask Tourpaq Support whether the SMS Service runs.
   * **failed**: the provider refused the SMS. Ask Tourpaq Support for the reason, and send the SMS again if needed.
   * **sent**: the provider accepted it. Check the number, and the delivery in your provider's own log.
3. Verify the phone number format and country code in the booking/customer data.
4. Check whether the correct **SMS type** template was used.
