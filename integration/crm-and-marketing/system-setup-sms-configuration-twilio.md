# System Setup – SMS Configuration (Twilio)

### Overview

SMS Configuration connects Tourpaq to Twilio so Tourpaq can send SMS.

It is used for automated notifications to customers and staff.

Go to **Setup → System Setup → SMS Configuration (Twilio)**.

{% hint style="warning" %}
The account token is a secret.

Limit access and rotate it if you suspect exposure.
{% endhint %}

### Purpose

* Provide real-time communication via SMS.
* Automate notifications such as booking confirmations, reminders, and alerts.
* Ensure reliable delivery using Twilio’s messaging platform.

### Configuration fields

| **Field**                 | **Description**                                                               |
| ------------------------- | ----------------------------------------------------------------------------- |
| **Twilio Account Number** | The account SID provided by Twilio for authentication.                        |
| **Twilio Account Token**  | The authentication token for the Twilio account.                              |
| **Twilio Phone Number**   | The phone number registered with Twilio (in E.164 format) used as the sender. |

### How to set it up

1. Create or access your Twilio account.
2. Copy the **Account SID** and **Auth Token** from Twilio.
3. Buy/configure a Twilio phone number for sending SMS.
4. Enter the values in **SMS Configuration (Twilio)** in Tourpaq.
5. Send a test SMS and confirm delivery.

{% hint style="info" %}
Use the E.164 phone number format.

Example: `+14155552671`
{% endhint %}

Related pages

* [SMS Overview](../../sms-overview.md)

### Troubleshooting

* **Nothing is sent:** Re-check the Account SID, token, and sender number.
* **SMS is sent but not delivered:** Verify Twilio delivery status and destination phone number format.
* **Wrong sender number:** Confirm the Twilio phone number is configured as the SMS sender.
* **Only some countries work:** Check Twilio account settings and country restrictions.

### FAQ

<details>

<summary><strong>Where do I find the Twilio Account SID and Auth Token?</strong></summary>

You can find them in the Twilio Console for your account.

Copy the values exactly and save after updating.

</details>

<details>

<summary><strong>What format should the phone number use?</strong></summary>

Use **E.164** format.

Example: `+14155552671`

</details>

<details>

<summary><strong>What happens if the token is wrong or expired?</strong></summary>

Tourpaq cannot authenticate with Twilio.

SMS sending will fail until the token is corrected.

</details>

<details>

<summary><strong>Should we use a shared Twilio account across brands?</strong></summary>

It depends on your operating model and compliance needs.

If you separate brands operationally, consider separate Twilio projects/accounts.

</details>

<details>

<summary><strong>How can I test that the integration works?</strong></summary>

Update the settings, then trigger a known SMS flow in Tourpaq.

Confirm delivery in Twilio and on the recipient phone.

</details>
