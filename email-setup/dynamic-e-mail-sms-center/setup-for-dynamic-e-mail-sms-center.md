# Setup for Dynamic E-mail/SMS Center

### Overview

Use this page to set up **dynamic email or SMS templates**. You can send them automatically to bookings that match your rules and filters.

### Purpose

This feature is designed to:

* Send automatic messages for common situations (confirmations, reminders, promotions).
* Keep the wording consistent across email and SMS.
* Reduce manual work by sending messages based on rules and filters.

### General

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="New template setup screen for Dynamic E-mail/SMS Center."><figcaption></figcaption></figure>

### Access

Open **E-mail Setup → Dynamic E-mail/SMS Center**, then choose **New Email Template**.

### Template types

You can create different template types, such as:

* **Dynamic Email/SMS**
* **Confirmation Transfer**
* **Confirmation Hotel**

If you are setting up confirmation templates, also read [Hotel and transfer confirmation emails to suppliers](../../hotel-and-transfer-confirmation-e-mail-to-suppliers.md).

### Required first step: select a brand

Before you edit anything, select the correct **brand** in the top-left dropdown.

#### Basic template settings

* **Template name**: a clear name you can recognize later.
* **Template type**: the kind of message you are setting up.
* **Active**: allows the template to be used for sending.
* **Hidden**: hides the template from the Dynamic E-mail/SMS Dashboard list.
* **Hour to send**: the time the email/SMS should be sent. Sending can be delayed by up to about 20 minutes. If you leave it blank, it is sent as soon as all rules match.

#### Email-only settings

* **Attach ticket**: attaches the booking ticket to the email.
* **From name**: sender name shown to the customer.
* **From e-mail**: sender email address. Use a real address.
* **Reply to**: where replies should go. Use a real address.
* **BCC**: email addresses that should receive a copy. Use real addresses.

#### Optional product filters

* **Customers who have bought**: include bookings that bought selected categories.
* **Customers who have not bought**: exclude bookings that bought selected categories.

### Sending options

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (23).png" alt="Sending options and rule builder for a dynamic template."><figcaption></figcaption></figure>

Use these fields to decide **when** the message should be sent.

The first dropdown contains the primary sending options for the template:

* Booking date
* Departure date
* Return home date
* Moved booking
* Canceled booking
* Last minute

The second dropdown contains the timeframe options:

* Before
* After

In the third field, enter the number of days. The email/SMS is sent as soon as all requirements are met.

{% hint style="danger" %}
**Important**

You can add more than one sending rule. Be careful when you combine rules.

* If you use **different rule types**, the booking must match **all** of them.
* If you use the **same rule type** more than once, the booking matches if **any** of them apply.

The examples below show how this works.
{% endhint %}

* If you use two or more different rule types, the booking must match all of them. The message is still sent only once.

**Example:** Send an email or SMS **60 days before departure** and **2 days after booking date**.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (3).png" alt=""><figcaption></figcaption></figure>

* If you set the same rule type more than once, the booking matches any of them. The system still sends only one message.

Example:

<figure><img src="../../.gitbook/assets/image (465).png" alt=""><figcaption></figcaption></figure>

1.  **First Booking**:\
    One booking is made more than 25 days before departure, and the email template is configured as follows:

    * 20 days before departure
    * 18 days before departure
    * 16 days before departure
    * 14 days before departure

    In this case, the booking will receive **only one email** scheduled for 20 days before departure. It will not receive additional emails at 18, 16, or 14 days before departure.
2. **Second Booking**:\
   This booking is made 17 days before departure. With the same configuration, it will receive **only one email** scheduled for 16 days before departure. No additional email will be sent at 14 days before departure.

The system sends **only one message per template**, even if you add several “when to send” conditions.

### Product and discount/supplement filters

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Product and discount/supplement filters for dynamic templates."><figcaption></figcaption></figure>

Use these fields to filter bookings based on what they bought. “Disc/suppl” means **discounts and supplements**.

#### Product Resourcer

**Default set-up**

If you select multiple items in **Customers who have bought**, a booking qualifies if it bought **at least one** of them.

If you select multiple items in **Customers who have not bought**, a booking is excluded if it bought **at least one** of them.

**Product Resourcer With And** changes the “at least one” behavior to “all of them”.

If you select multiple items in **Customers who have bought**, a booking qualifies only if it bought **all** of them.

If you select multiple items in **Customers who have not bought**, a booking is excluded if it bought **at least one** of them.

For example, the email will be sent out as follows:

![Example of bought/not bought filter logic](https://docs.tourpaq.com/assets/images/email_center_bought_or_not-2d059498dd98bfbfdb95f18ad94222f1.png)

Note: `1` means the email is sent. `0` means it is not sent.

### Message content

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Message editor for a dynamic template."><figcaption></figcaption></figure>

The message editor works like the regular **E-mail Center**.

#### Add a link to the Customer Center

Write the link text (for example, “Open your booking”). Select it. Then click the link button shown in the screenshot.

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Add link button in the message editor."><figcaption></figcaption></figure>

In the URL field, insert the `[Hash-key-link]`. Select the other protocol, as shown in the screenshot.

<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Link settings with Hash-key-link placeholder."><figcaption></figcaption></figure>

### Date filters

<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Date filter section for bookings."><figcaption></figcaption></figure>

Use these fields to filter bookings by booking, departure, arrival, and return dates.

### Destination filters

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Destination and transport filters for bookings."><figcaption></figcaption></figure>

Use these fields to filter bookings by hotel, room, transport, real transport, resort, arrival airport, and more.

### Resource filters (product links)

Use **Resource filters** to send clickable product links to guests. Guests can add the product to their booking with very little effort.

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Resource filters selection for product links."><figcaption></figcaption></figure>

When you use Resource filters, a special variable becomes available in the email body.

<figure><img src="../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Variable for inserting product links into the email body."><figcaption></figcaption></figure>

You can attach this variable to a button, text, or image. When the guest clicks it, they are taken to the Customer Center. They will see a message that the product is added. They must save the booking to confirm it.

If you send several links, only the clicked link is applied.

**There can be only one link per category.**

**If you select multiple products in a category:**

* For a **multi-select** category, all selected products are added.
* For a **single-select** category, the cheapest selected product is added.

{% hint style="danger" %}
**Caution**

* An email or SMS template that has been sent to a booking cannot be resent.
* Be careful when creating a template. If you make a mistake, avoid editing the same template. A booking can receive a template only once.
{% endhint %}

### FAQ

<details>

<summary>Can I resend the same template to the same booking?</summary>

No. A booking can receive a template only once. Create a new template if you need to send a corrected message.

</details>

<details>

<summary>What happens if I leave “Hour to Send” blank?</summary>

The message is sent as soon as all rules and filters match.

</details>

<details>

<summary>Why can there be a delay after the selected time?</summary>

Sending can be delayed by up to about 20 minutes. This is normal.

</details>

<details>

<summary>I added several “when to send” rules. Will the booking get several messages?</summary>

No. The system sends only one message per template. The extra rules only decide when that one message should be sent.

</details>

<details>

<summary>What is the difference between email and SMS templates?</summary>

Email templates can include a subject and a message body. SMS templates are meant for short messages.

</details>

<details>

<summary>Why does my product filter include more bookings than I expected?</summary>

In the default setup, “Customers who have bought” matches if the booking bought at least one selected item. Switch to “Product Resourcer With And” if you want “all selected items”.

</details>

<details>

<summary>Where do I select the brand?</summary>

Use the brand dropdown in the top-left corner of the setup screen. Always check it before you save or activate a template.

</details>

<details>

<summary>What does “Hidden” do?</summary>

Hidden removes the template from the dashboard list. Use it to keep the list clean.

</details>

<details>

<summary>Why is my email missing sender details?</summary>

Email templates need sender details. Fill in **From name** and **From e-mail**.

</details>

<details>

<summary>Why is my link not working?</summary>

Make sure the URL contains the exact `[Hash-key-link]` text. Also make sure you selected the correct protocol in the link dialog.

</details>

<details>

<summary>How many product links can I add per category?</summary>

Only one link per category can be used.

</details>

<details>

<summary>Can I attach the ticket to an SMS?</summary>

No. Ticket attachments are available for email templates only.

</details>

<details>

<summary>What does “Attach ticket” do?</summary>

It adds the booking ticket PDF to the email.

</details>

<details>

<summary>What does “Customers who have not bought” mean?</summary>

It is an exclude filter. If a booking bought something from the selected categories, it will not receive the message.

</details>
