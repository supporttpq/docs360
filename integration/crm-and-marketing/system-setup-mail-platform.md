# System Setup – Mail Platform

### Overview

Mail Platform connects Tourpaq to an email delivery service.

Tourpaq uses it for automated emails like confirmations, reminders, and notifications.

Go to **Setup → System Setup → Mail Platform**.

{% hint style="warning" %}
The user token is a secret.

Limit access and rotate it if you suspect exposure.
{% endhint %}

### Purpose

* Enable automated email communication.
* Ensure reliable delivery of booking confirmations, reminders, and alerts.
* Centralize email settings for company-wide use.

### Configuration fields

| **Field**             | **Description**                                                        |
| --------------------- | ---------------------------------------------------------------------- |
| **Use Mail Platform** | Enables or disables the mail platform integration.                     |
| **User Name**         | Username used to authenticate with the mail service.                   |
| **User Token**        | Token used to authenticate with the mail service.                      |
| **Mail**              | Mail endpoint/account used for sending (for example a gateway domain). |
| **Mail From**         | Sender address shown to recipients (“From”).                           |

### How to set it up

1. Get the **User Name** and **User Token** from your mail platform provider.
2. Enter the credentials in **Mail Platform**.
3. Set **Mail From** to the sender address you want customers to see.
4. Save changes.
5. Trigger a known email flow in Tourpaq and verify delivery.

{% hint style="info" %}
Use a sender address that matches your company domain.

This improves deliverability and reduces spam filtering.
{% endhint %}

### Usage notes

* Ensure all credentials are correctly entered to avoid email delivery failures.
* **Mail From** should follow your sender policy and SPF/DKIM setup.
* If Mail Platform is disabled, some automated emails may not send.

### Troubleshooting

* **Emails are not sent:** Verify **Use Mail Platform** is enabled and credentials are correct.
* **Emails go to spam:** Align **Mail From** with your domain and validate SPF/DKIM with your provider.
* **Wrong sender shown:** Re-check **Mail From** and the template sender settings (if applicable).

### Related pages

* [How to set SMTP Settings](../../brands/how-to-set-smtp-settings.md)
* [E-mail center](../../email-setup/e-mail-center.md)

### FAQ

<details>

<summary><strong>What’s the difference between “Mail” and “Mail From”?</strong></summary>

**Mail** is the mail endpoint/account Tourpaq uses to send through the provider.

**Mail From** is the sender address recipients see in their inbox.

</details>

<details>

<summary><strong>Where do I get the User Name and User Token?</strong></summary>

Your mail platform provider supplies them.

Treat the token like an API key.

</details>

<details>

<summary><strong>Does disabling Mail Platform stop all emails?</strong></summary>

It can stop automated/system emails that depend on the integration.

Validate your flows after changing this setting.

</details>

<details>

<summary><strong>How do I verify that emails send correctly?</strong></summary>

Enable Mail Platform and trigger a known notification.

Then confirm receipt and check sender, subject, and deliverability.

</details>
