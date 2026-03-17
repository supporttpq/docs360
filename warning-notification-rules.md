# Warning notification rules

### Overview

Use **Warning Notification Rules** to send automatic warning messages to your team.

Warnings can be sent by **email** or **SMS**.

They help you react faster when something important goes wrong. For example, when an email fails to send or a booking task fails.

### Access

Open **E-mail Setup → Warning Notification Rules**.

### Purpose

Use this feature to:

* Notify users about problems and important changes automatically.
* Reduce response time by alerting the right people immediately.
* Avoid missed issues by using clear rules for who gets what.

### Tabs Overview

You will see three tabs:

1. **Warning Notification Rules**: choose which warnings are sent, and when.
2. **Warning Contacts**: choose who receives warnings.
3. **Warning Sent from E-mail**: choose the sender address shown in warning emails.

#### Warning Contacts

Create contacts that can receive warning emails or SMS messages.

<figure><img src=".gitbook/assets/image (78).png" alt="Warning Contacts list."><figcaption><p>Warning contacts list.</p></figcaption></figure>

<figure><img src=".gitbook/assets/image (79).png" alt="Add or edit a warning contact."><figcaption><p>Add or edit a warning contact.</p></figcaption></figure>

#### Warning Sent from E-mail

Set which sender email address is shown on warning emails.

All warning emails will appear to come from this address.

<figure><img src=".gitbook/assets/image (80).png" alt="Set sender email address for warnings."><figcaption><p>Choose the sender email address.</p></figcaption></figure>

#### Warning Notification Rules

Set rules for which warning types each contact should receive.

You can also control how often a warning is sent.

<figure><img src=".gitbook/assets/image (81).png" alt="Warning notification rules list."><figcaption><p>Rules list.</p></figcaption></figure>

<figure><img src=".gitbook/assets/image (82).png" alt="Edit a warning rule."><figcaption><p>Edit a rule.</p></figcaption></figure>

### Types of Warnings

Warning names match what you see in the system.

Some warnings include terms like **SMTP**, **FTP**, or **GDS**.

These are technical names used by the system. You can still use them safely as labels.

<details>

<summary>Common terms used in warning names</summary>

* **SMTP**: email sending.
* **FTP**: file transfer between systems.
* **GDS**: flight booking connection (for example Travelport).
* **PNR**: a booking reference used for flight reservations.

</details>

#### Common warning groups

These are common examples:

* **Informational**
  * General information alerts.
* **Email sending problems**
  * Hotel reporting email failed to send (SMTP error).
  * Extra reporting email failed to send (SMTP error).
  * Missing attachment when sending ticket emails.
* **Reporting problems**
  * Hotel reporting errors (other errors).
  * Extra reporting errors (other errors).
  * Transport reporting errors (FTP, SMTP, or other errors).
  * Extra supplier reporting errors (SMTP or other errors).
* **GDS and flight-related warnings**
  * GDS status changed (for example TKQ → TKOK).
  * Unable to configure GDS flight, check PNR, or apply time changes.
  * Unable to submit Web Booking to Travelport.
  * Fewer GDS flights than yesterday (for dynamic transport).
  * Queue management warnings for GDS bookings.
  * Success messages for time changes or submissions (used as confirmations).
* **Other system warnings**
  * Mail helper errors.
  * Service watcher warnings.
  * Unable to generate a price list per day.
  * Bookings staying in error status for more than 1 hour.
  * Connected hotel errors (no response from the hotel connection).

{% hint style="info" %}
If you are unsure which warning to enable, start with email failures and booking errors.
{% endhint %}

### Instructions for Use

{% stepper %}
{% step %}
#### 1. Choose who should receive warnings

Open **Warning Contacts**. Add one or more recipients.
{% endstep %}

{% step %}
#### 2. Set the sender email address

Open **Warning Sent from E-mail**. Set the sender address for warning emails.
{% endstep %}

{% step %}
#### 3. Turn on the warnings you need

Open **Warning Notification Rules**.

Pick the warning types you want. Set how often they can be sent.
{% endstep %}

{% step %}
#### 4. Review and adjust

If people get too many messages, reduce the warning list or lower the frequency.
{% endstep %}
{% endstepper %}

### FAQ

<details>

<summary>Who should receive warning notifications?</summary>

Send warnings to the people who can act on them.

Usually this is an administrator, an operations inbox, or a small support group.

</details>

<details>

<summary>Should I use email, SMS, or both?</summary>

Use **email** for most warnings.

Use **SMS** only for urgent issues that need fast attention.

</details>

<details>

<summary>Why am I getting too many warnings?</summary>

This usually happens when:

* Too many warning types are enabled, or
* The frequency is set too high.

Start small. Enable only the warnings you truly need.

</details>

<details>

<summary>Why is a warning email not being delivered?</summary>

First check that the contact has a valid email address.

Then check that your sender address is set and the warning rule is enabled.

</details>

<details>

<summary>Can I use a shared inbox for warnings?</summary>

Yes. This is often the best choice.

Use an inbox your team monitors during business hours.

</details>
