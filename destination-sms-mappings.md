# Destination SMS Mappings

### Overview

Use **Destination SMS Mappings** to set up the messages sent from the Destination app.

These templates are used for both **SMS** and **email**.

Good templates help customers get clear and timely updates. For example, order confirmations and arrival messages.

### Access

Open **E-mail Setup → Destination SMS Mappings**.

{% hint style="warning" %}
Messages set here are usually sent automatically.

For emails linked to **Excursions**, **Arrivals**, **Hotels**, and **Resorts**, the Destination app may replace the default text. This depends on your setup and whether you use custom text.
{% endhint %}

### Purpose

Use this page to:

* Define templates for automatic SMS and email notifications.
* Make sure messages for orders, cancellations, and payments are sent correctly.
* Keep customer communication accurate and consistent.

<figure><img src=".gitbook/assets/image (107).png" alt="Destination SMS Mappings page."><figcaption><p>Overview of template mappings.</p></figcaption></figure>

### Types of SMS/Email Templates

<figure><img src=".gitbook/assets/image (108).png" alt="Template types in Destination SMS Mappings."><figcaption><p>Template types you can configure.</p></figcaption></figure>

### Field Explanation

#### Template Name (required)

* An internal name for the template.
* Used in the back office only.
* Keep it short and descriptive.

Example: `Arrival information – Resort SMS`

#### Template For

Defines **when** the template can be used.

Available options:

* **Order**: General booking or order messages. SMS is sent when you book an extra order.
* **Excursion**: Excursion-related messages. SMS is sent from Guide APP > SMS > Excursion.
* **Arrival**: Arrival-day info, welcome messages, and practical details. SMS is sent from Guide APP > SMS > Arrival (will filter the bookings by arrival date).
* **Hotel**: Hotel messages, like check-in info or reminders. SMS is sent from Guide APP > SMS > Hotel.
* **Resort**: Destination or resort-wide messages. SMS is sent from Guide APP > SMS > Resort.
* **Pending payment notification**: Reminders for unpaid or partly paid bookings. If the extra order payment is not confirmed, the payment provider will send the transaction back to 'in pending' status, and the customer will receive this SMS.
* **Cancel order**: SMS is sent when you cancel an extra order.
* **Flight Change**: SMS is sent when the transport has a flight schedule change.

The templates for Hotel, Excursion, Arrival and Resort (Called 'Destination' in the Guide APP) are displayed like this in the Guide APP.

<br>

<figure><img src=".gitbook/assets/image (5) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### FAQ

<details>

<summary>Do messages from this page send automatically?</summary>

In most setups, yes.

The Destination app uses these templates when the related event happens.

</details>

<details>

<summary>Why does the email text look different from what I wrote here?</summary>

For some email types (like Excursions, Arrivals, Hotels, and Resorts), the Destination app may replace the default text.

This can depend on whether you use custom text and how your app is configured.

</details>

<details>

<summary>What should I write in “Template Name”?</summary>

Use a name your team will recognize later.

Include the purpose and channel if helpful. For example: “Arrival info – SMS”.

</details>

<details>

<summary>Which “Template For” option should I choose?</summary>

Choose the option that matches when the message should be used.

If you are unsure, start with **Order** for general messages.

</details>

<details>

<summary>Why didn’t a customer receive an SMS or email?</summary>

Common reasons:

* The customer has no phone number or email address.
* The wrong template type was used for that situation.
* The app is using a different default text for that message type.

</details>
