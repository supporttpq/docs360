---
description: >-
  Deprecated SMS provider: Tourpaq emails each SMS to the phone number at Mail
  Platform's email-to-SMS gateway.
---

# Mail Platform

{% hint style="warning" %}
Mail Platform is deprecated. For a new setup, use [Compaya](compaya/) or [Twilio](system-setup-sms-configuration-twilio.md).
{% endhint %}

### Overview

Mail Platform is an SMS provider that works as an email-to-SMS gateway: for each SMS, Tourpaq sends an email to the phone number at Mail Platform's gateway domain, through the SMTP server of the booking's brand, or of the template's brand for an SMS without a booking. It doesn't send Tourpaq's emails.

For the SMS Tourpaq sends and their statuses, see [How Tourpaq sends SMS](../../sms-overview.md#how-tourpaq-sends-sms).

Go to **Setup** › **System Setup** › **SMS Config** › **Mail Platform**.

### Configuration fields

| **Field**                                                                                   | **Description**                                                                                                                                      |
| ------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mail**                                                                                    | Mail Platform's gateway domain, starting with `@`, for example `@mail2sms.mailmailmail.net`. Tourpaq puts the phone number in front of it. Required. |
| **Mail From**                                                                               | The sender address of the emails. When it's empty, Tourpaq uses the **Contact Email Address** of that brand.                                         |
| **Footer Message**                                                                          | Text that Tourpaq adds below each SMS, after a blank line. Up to 50 characters.                                                                      |
| **User Name**, **User Token**, **Uses newsletter service**, **API username**, **API Token** | Not used to send SMS.                                                                                                                                |

### Related pages

* [How to set SMTP Settings](../../brands/how-to-set-smtp-settings.md)
* [SMS Overview](../../sms-overview.md)
