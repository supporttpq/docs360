---
description: >-
  Print and email ticket PDFs in Tourpaq Office. Send an e-ticket for one
  booking, copy to another email address, or bulk reprint tickets per transport
  and departure period.
---

# Print Tickets

### Overview

The Print Tickets feature allows users to generate and print customer-facing booking documents, including travel details, passenger information, and attached documents.

<figure><img src="../.gitbook/assets/image (161).png" alt="Tourpaq Office Print Tickets page with Booking No field and actions for printing and sending ticket PDFs"><figcaption><p>Print Tickets in Tourpaq Office. Use it to print or email a ticket PDF (e-ticket) for a single booking.</p></figcaption></figure>

{% hint style="info" %}
Printed tickets represent the final customer document and may include both system-generated data and manually added content.
{% endhint %}

***

### What you can do on this page

* **Print** a ticket PDF for a specific booking.
* **Send an e-ticket email** with the ticket PDF to the customer.
* **Copy the e-ticket to another email address** (for example, a colleague or a group leader).
* **Bulk reprint ticket PDFs per transport** in **Reprint Per Transport**.

***

### Purpose

This feature is used to:

* provide customers with booking confirmation documents
* include travel details and instructions
* attach additional documents (PDFs) to tickets
* validate customer-facing information before travel

***

### Access & Preconditions

#### Requirements

* A booking must exist
* Booking must contain at least one product (hotel, transport, etc.)
* Optional: comments and attachments configured

{% hint style="warning" %}
Tickets cannot display content that has not been configured or saved in the booking.
{% endhint %}

#### Navigation

Use a **code block** in GitBook: Booking > Open Booking > Tickets / Print

{% hint style="info" %}
If you only need to check whether a ticket email was sent (and whether it failed), use [E-tickets Overview](../e-tickets-overview.md).
{% endhint %}

***

### Send or print a ticket (single booking)

{% stepper %}
{% step %}
**1) Enter the booking number**

In **Booking No**, enter the booking number (booking reference).

* If the booking is valid, **Customer** is filled in automatically.
* If the customer is not filled in, re-check the booking number and that you have access to the booking.
{% endstep %}

{% step %}
**2) Choose what you want to do**

Select the options that match your task:

* **Print One Ticket**
  * Prints **one combined ticket** for the whole booking (instead of separate tickets where applicable).
* **Send E-Ticket**
  * Sends the ticket by email to the **customer email address on the booking**.
* **Copy to e-mail**
  * Sends an extra copy to the email entered in **Alternative Email**.
* **Alternative Email**
  * Optional. Use when the copy should go to a different recipient (e.g., tour leader, agent, or internal inbox).
{% endstep %}

{% step %}
**3) Generate/send**

Complete the action using the page’s button(s). Tourpaq generates the ticket PDF from the booking’s current data.

{% hint style="warning" %}
If you are sending an e-ticket and the customer does not receive it, verify the email address on the booking and check your email log in [E-tickets Overview](../e-tickets-overview.md).
{% endhint %}
{% endstep %}
{% endstepper %}

***

### Reprint Per Transport (bulk)

Use **Reprint Per Transport** when you need to print or reprint tickets for **many bookings**. This workflow groups results by transport and departure period.

<figure><img src="../.gitbook/assets/image (162).png" alt="Tourpaq Office Reprint Per Transport tab with filters for booking period, departure period, length, and transport selection"><figcaption><p>Reprint Per Transport. Bulk reprint ticket PDFs by transport, booking period, and departure period.</p></figcaption></figure>

#### When this is useful

* Preparing printed ticket packs for **airport/station check-in**.
* Printing tickets for a **specific departure date range**.
* Reprinting after changes (for example, updated meeting points, timing, or other ticket content).

#### Requirements

* Bookings must have **transport data** assigned.
* Tickets must already exist (this is primarily a **reprint** workflow).

#### Filters (what they mean)

* **Booking period**: filters by when the booking was created.
* **Departure period**: filters by the actual departure date.
* **Length**: filters by travel duration (if used in your setup).
* **Transports**: select one or more transports/routes to include.

#### Bulk reprint steps

{% stepper %}
{% step %}
**1) Open the tab**

Open **Reprint Per Transport** from the top of the **Print Tickets** page.
{% endstep %}

{% step %}
**2) Narrow down the bookings**

Set **Booking period** and/or **Departure period**.

Optionally choose **Length** if you want to limit the results further.
{% endstep %}

{% step %}
**3) Select the transport(s)**

Click **Transports** and select the transport(s) you want to print tickets for.
{% endstep %}

{% step %}
**4) Print**

Click **Print** to generate the tickets for all matching bookings.
{% endstep %}
{% endstepper %}
