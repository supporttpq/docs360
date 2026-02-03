# Destination SMS Mappings

### Overview

The **Destination SMS Mappings** module allows administrators to configure SMS and email templates used by the destination application. Properly defined templates ensure that automated communications, such as notifications for extra orders or bookings, are correctly sent to customers.

{% hint style="warning" %}
**Note:** The emails and SMS messages configured in this menu are sent automatically by default. For emails associated with **Excursions, Arrivals, Hotels, and Resorts**, the destination application may override the default content unless you choose to use custom text.
{% endhint %}

### Purpose

The purpose of Destination SMS Mappings is to:

* Define templates for automated SMS and email notifications sent from the destination application.
* Ensure that messages related to orders, cancellations, payments, or services are delivered correctly.
* Enable customization of messages to maintain accurate and relevant communication with customers.

<figure><img src=".gitbook/assets/image (107).png" alt=""><figcaption></figcaption></figure>

### Types of SMS/Email Templates

<figure><img src=".gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

### Field Explanation

#### Template Name (required)

* Internal name of the SMS template
* Used for identification in the back office only
* Should clearly describe the purpose of the SMS

Example:\
`Arrival information - Resort SMS`

#### Template For

Defines **when** the SMS template can be used.

Available options:

* **Order -** Used for general booking or order-related messages
* **Excursion -** Used for excursion-related communication
* **Arrival -** Used for arrival-day information, welcome messages, or practical details
* **Hotel -** Used for hotel-related messages, such as check-in info or reminders
* **Resort -** Used for destination or resort-wide messages
* **Pending payment notification -** Used to remind customers about unpaid or partially paid bookings
* **Cancel order -** Used when a booking or order is canceled
* **Flight Change -** Used to notify customers about flight schedule changes

The selected value determines where the template is available and which triggers can use it.
