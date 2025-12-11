# E-mail center

### Overview

The **E-mail Center** is the place where administrators set up and maintain all **automated email templates** used by the system.

From here you can create, edit, and test email templates so that all communication sent to customers is **consistent, professional, and up to date**.

### Purpose

The E-mail Center is used to:

* Define and maintain templates for all automated emails sent by the platform.
* Insert **dynamic content** (for example booking details) using predefined constants.
* Test email templates before they are sent to real customers.
* Control the **sender details** and **activation status** for each template.

### Template fields

For each email template, you can configure the following fields:

* **Sender email address** – The email address that appears as the sender. This is where replies will be sent if the customer responds.
* **Sender name** – The display name that appears in the recipient’s inbox (for example: your brand or company name).
* **Activation status** – Controls whether this template is **active** (emails can be sent) or **inactive** (emails will not be sent using this template).
* **Email subject** – The subject line of the email.
* **Email body (text editor)** – A rich text editor where you write the content of the email. Here you can include dynamic placeholders (predefined constants) that the system will automatically replace with the correct values when sending (such as customer name, booking number, dates, etc.).

### Types of automatic emails

The platform can send many different types of automated emails. Typical examples include:

* Thank You for Booking
* Reservation Canceled
* Payment Preminder
* Payment Reminder
* Booking Canceled in 48 Hours
* Deposit Received
* Insurance Information Missing / Still Missing
* Second Payment Received
* Full Payment Received
* Welcome Home / Welcome Home Reminder
* Reporting Schedule Communication
* LMS Booking Confirmation
* Booking Updated
* Hotel Release
* Flight Changes Notification
* Seat Reminder Email
* Financial Export Email
* Post-Deposit Questionnaire
* Wait List Booking
* Voucher Generated Notification
* Missing Attributes Notification
* Creditor Invoice
* Special Offer Rejected
* Hotel Reporting / Extras Reporting / Supplier Extras Reporting
* Documents Uploaded
* Emails sent from **View All Bookings** or **Customer Export**
* Room Request Notification
* Early Booking Rooming List
* Quotation List
* Stop Sales Introduction
* Extras Category Reporting
* **Pending Payment Notification** – Sent when DIBS needs additional time (approx. 2–72 hours) to process a transaction.
* **Captured Money But No Allotment** – Sent when a payment is successfully processed, but the requested allotment is no longer available (often followed by a refund).

### Step-by-step: configure an email template

{% stepper %}
{% step %}
#### 1. Open the E-mail Center

Go to the **E-mail Center** module in the back office.
{% endstep %}

{% step %}
#### 2. Choose a template

Either:

* Select an existing template from the list to edit it, **or**
* Create a new template (if available in your setup).
{% endstep %}

{% step %}
#### 3. Fill in sender details

Set:

* **Sender email address** – Use a valid address that belongs to your domain.
* **Sender name** – Use a clear name that customers will recognize as your company or brand.
{% endstep %}

{% step %}
#### 4. Define subject and content

* Enter a clear, descriptive **email subject**.
* In the **email body**, write the content of the message.
* Insert any required **dynamic placeholders** (predefined constants) where you want booking- or customer-specific data to appear.
{% endstep %}

{% step %}
#### 5. Set activation and save

* Choose the **activation status** (keep it inactive while you are still testing).
* Save your changes.
{% endstep %}

{% step %}
#### 6. Test the template

* Click the **Test** button for the template.
* Enter your own email address (or a dedicated test mailbox) as the recipient.
* Send the test email and then check your inbox.
* Verify that:
  * The sender, subject, and content look correct.
  * All dynamic placeholders are replaced with the expected values.
* When you are satisfied, set the template to **active** so it is used by the system triggers.
{% endstep %}
{% endstepper %}

### Best practices

{% hint style="info" %}
To keep email communication reliable and professional, follow these recommendations:

* **Use recognizable sender details** – Choose a sender name and email that clearly represent your company or brand.
* **Keep subjects clear and specific** – Make it obvious what the email is about (for example: _"Booking confirmation – \[Booking Number]"_).
* **Review dynamic content carefully** – Always test changes to constants and placeholders so that emails do not contain missing or incorrect values.
* **Avoid unnecessary changes to live templates** – When possible, clone or copy a template, adjust it, test it, and then switch over.
* **Test after major system changes** – If booking flows or payment providers change, re-test the key email templates (confirmation, payment, cancellation, etc.).
{% endhint %}
