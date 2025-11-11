# Dynamic E-mail/SMS Center

### **Overview**

The **Dynamic E-mail / SMS Center** allows administrators to send customized e-mails and SMS messages to bookings based on a wide range of filters. These communications can be tailored to specific groups of customers, ensuring that messages are both relevant and timely.

### **Purpose**

This feature is designed to:

* **Notify customers** of important events (e.g., departure reminders).
* **Welcome guests** upon arrival at their travel destination.
* **Follow up** after a trip with a return home message.
* **Promote products** by informing guests about additional services or upgrades available for booking.

### Column Explanation

<figure><img src="../../.gitbook/assets/image (377).png" alt=""><figcaption></figcaption></figure>

* **Template Name**
  * The name given to the email/SMS template.
  * Helps identify the purpose of the template (e.g., _Confirmation Hotel_, _Departure reminder_).
* **Brand**
  * The brand or agency associated with the template (e.g., _Tourpaq DK_).
  * Useful if multiple brands operate under the same system.
* **Type**
  * The communication type:
    * **Email** → Templates used for sending automated or manual emails.
    * **SMS** → Templates for sending SMS messages.
* **Last Update**
  * Shows the last date and time when the template was modified.
  * Useful for tracking the freshness of template content.
* **Updated By**
  * Indicates which user last edited the template (e.g., _Roweb Tourpaq_).
* **Active**
  * Checkbox that defines whether the template is active or inactive.
  * Only active templates are used in automated workflows.
* **Delete (Trash Icon)**
  * Allows deletion of a template if it is no longer needed.

### **Dynamic E-mail vs Dynamic SMS**

* **Dynamic E-mail**
  * Provides more configuration options.
  * Allows long-form content in both subject and body.
  * Suitable for detailed messages and promotional content.
* **Dynamic SMS**
  * Limited configuration.
  * The only message content visible to the guest is the **Subject text** (no separate body).
  * Suitable for short, critical notifications (e.g., departure reminders).

### **Administrator Capabilities**

Administrators can:

* Create and send new e-mail or SMS templates.
* Apply filters to define the target audience.
* Track which templates have been sent.

{% hint style="danger" %}
⚠️ **Caution**&#x20;

* Once an e-mail or SMS template is sent to a booking, it **cannot be resent**.
* Editing an already sent template is **not recommended**, since a booking cannot receive more than one e-mail or SMS from the same template.
* Always double-check message content and filters before sending.
{% endhint %}

### **Usage Example**

* An administrator creates a **Dynamic SMS template** to remind customers of their departure date.
* A filter is set on **departure date = tomorrow**.
* The system sends the SMS to all guests with departures scheduled for the next day.

