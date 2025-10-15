# Setup for Dynamic E-mail/SMS Center

### Overview

The **New Email Template** feature within the Dynamic E-mail/SMS Center allows users to create customizable email or SMS templates that can be sent automatically based on specific booking conditions, events, or customer interactions. Templates can include personalized information and support various triggers to enhance communication with guests.

### Purpose

This feature is designed to:

* Automate guest communication for different scenarios (e.g., booking confirmation, trip reminders, promotions).
* Ensure consistent messaging across email and SMS channels.
* Reduce manual workload by allowing predefined templates to be sent dynamically based on filters and triggers.

### General <a href="#general" id="general"></a>

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Dynamic communication types:

* &#x20;Dynamic E-mail/SMS
* Confirmation Transfer
* Confirmation Hotel

To set up a dynamic e-mail/sms, the user needs to first select a brand from the brand selection dropdown in the upper left corner of the window.

* Template Name: Insert the name of the template
* Template type: Select the template type
* Active: When checked, the template will be used to send e-mails or SMS to bookings.
* Hidden: When checked, the template will not be visible in the Dynamic E-mail/SMS Dashboard.
* Hour to Send: Insert the time the e-mails/SMS will be sent. May have a 20-minute delay. (If left blank, will be sent as soon as requirements are met.)
* Attach ticket: A booking ticket will be attached to the e-mail. (available for e-mail template)
* From name: Insert the name of the sender. (available for e-mail template)
* From e-mail: Insert the sending e-mail address - MUST BE A VALID ONE. (available for e-mail template)
* Reply to: Insert the address that will receive the replies, if any - MUST BE A VALID ONE. (available for e-mail template)
* BCC: Insert the BCC address/addresses - MUST BE A VALID ONE. (available for e-mail template)
* Customers who have bought: selected category(es) from booking
* Customers who have not bought: selected category(es) from booking

For confirmation templates, please check the [Hotel and transfer the confirmation e-mail to the suppliers](../../hotel-and-transfer-confirmation-e-mail-to-suppliers.md).

### Sending Options <a href="#sending-options" id="sending-options"></a>

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

From these fields, the sending configuration can be set:

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

In the third field, you need to insert the number of days to be taken from the first 2 options when the e-mail will be sent. The e-mail/SMS will be sent as soon as all requirements are met.

> <mark style="color:blue;">📝</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**IMPORTANT**</mark>**:** Additional rules can be configured in the sending option, but you should be cautious when combining them. The system applies the AND condition between different rule types and the OR condition within the same rule type. A valid set of sending rules is illustrated in the following examples:

**Example:** An e-mail or SMS can be sent 60 days before the departure date AND 2 days after the booking date.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Example:** An e-mail or SMS can be sent within 102, 103, or 104 days before the departure date.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Product and disc/suppl filters <a href="#product-and-discsuppl-filters" id="product-and-discsuppl-filters"></a>

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Using these fields, the number of bookings that will receive the e-mail can be filtered by bought or not-bought products and disc/suppl.

#### **Product Resourser**

**Default set-up**

If multiple products are selected in the filters for bought, a booking that has bought at least one of the products or disc/suppl will receive the e-mail/sms.

If multiple products are selected in the filters for not bought, a booking that has bought at least one of the products or disc/suppl will not receive the e-mail/sms.

**Product Resourser With And** - This setup will change the described behavior from "OR" to "AND".

If multiple products are selected in the filters for bought, a booking that has bought all of the products or disc/suppl will receive the e-mail/sms.

If multiple products are selected in the filters for not bought, a booking that has bought at least one of the products or disc/suppl will receive the e-mail/sms.

For example, the email will be sent out as follows:

![!](https://docs.tourpaq.com/assets/images/email_center_bought_or_not-2d059498dd98bfbfdb95f18ad94222f1.png)

Note: 1 - the email is sent; 0 - the email is NOT sent

### Message content <a href="#message-content" id="message-content"></a>

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

These are the text cases. They work just like the regular **E-mail Center** and have the same features.

For inserting links to the customer center, the process is the following:

Write the text that will have the link in the back, for example //here//, select it, and click on the circled button from the screenshot.

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Next, in the URL, insert the \[Hash-key-link] and select the other protocol

<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Date filters**

<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

These fields allow the user to filter the receiving bookings by booking, departure, arrival, and return dates.

### **Destination filters**

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

These fields allow the user to filter the received bookings by hotel, room, transport, real transport, resort, arriving airport, and count received **filters**

**The Resource filters** tab is a new addition to the **Dynamic E-mail/SMS** feature, allowing the users to send product links to the guests through which said products can be booked with minimal effort from the guest.

Product categories and products are selected from the Resource filters tab.

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

A new variable has been created for this in the e-mail body.

<figure><img src="../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

This variable can be linked to a photo or phrase/word that upon being clicked, will send the guest to the CC. In CC a message will appear informing the guest that product have been added to the booking and he needs to save the booking. Upon save the product will be added to the booking.

If multiple links are sent through the e-mail, only the product from the clicked link will be booked.

**There can be only one link per category.**

**If multiple products are selected for one category, for multiple selection category, all products will be booked; if a normal category is involved, then the cheapest product will be booked.**

> ⚠️ <mark style="color:red;">**Caution:**</mark>

* An e-mail or SMS template that has been sent to a booking cannot be resent.
* Please be carefull when creating a template. If mistakes are made during the creation of a template, editing is not advised since a booking cannot receive more than on e-mail or SMS from 1 template.
