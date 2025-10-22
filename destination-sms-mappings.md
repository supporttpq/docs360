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

| Type                                     | Description                                                                                                             |
| ---------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **Order**                                | Sent when an extra order is purchased. Includes the message and the extra order ticket.                                 |
| **Cancel Order**                         | Sent when a service cancels an extra order that was already paid. Notifies the customer of the cancellation.            |
| **Payment Confirmation**                 | Sent when an extra order is placed but the payment is not yet confirmed.                                                |
| **Excursion / Arrival / Hotel / Resort** | Sent from the destination application. If no custom text is selected, the default text defined in the template is used. |
