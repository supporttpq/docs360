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

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (107).png" alt="Destination SMS Mappings page."><figcaption><p>Overview of template mappings.</p></figcaption></figure></div>

### Types of SMS and email templates

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (108).png" alt="Template types in Destination SMS Mappings."><figcaption><p>Template types you can configure.</p></figcaption></figure></div>

### Field explanations

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

The templates for **Hotel**, **Excursion**, **Arrival**, and **Resort** appear as **Destination** in the Guide APP.

<div data-with-frame="true"><figure><img src=".gitbook/assets/guide app menu.png" alt="Guide APP Destination template selection for Hotel, Excursion, Arrival, and Resort messages."><figcaption><p>Destination templates in the Guide APP.</p></figcaption></figure></div>
