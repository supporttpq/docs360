# Print Tickets

### Print Tickets

Use **Print Tickets** when you need to generate a ticket PDF for a single booking—either to print it, save it, or send it as an e-ticket email to the customer.

<figure><img src="../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

***

### What you can do on this page

* **Print** a ticket for a specific booking.
* **Send an e-ticket by email** to the customer.
* **Send a copy to an alternative email address** (for example, a colleague or a group leader).
* **Reprint tickets in bulk per transport** (tab at the top).

***

### Before you start

* You need a **valid booking number**.
* The booking should be **confirmed** and contain products that generate a ticket.
* You must have access rights to use ticket actions.

{% hint style="info" %}
If you only need to check whether a ticket email was sent (and whether it failed), use [E-tickets Overview](../e-tickets-overview.md).
{% endhint %}

***

### Send or print a ticket (single booking)

{% stepper %}
{% step %}
### 1) Enter the booking number

In **Booking No**, enter the booking number.

* If the booking is valid, **Customer** is filled in automatically.
* If the customer is not filled in, re-check the booking number and that you have access to the booking.
{% endstep %}

{% step %}
### 2) Choose what you want to do

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
### 3) Generate / send

Complete the action (print or send) using the page’s available action button(s).

{% hint style="warning" %}
If you are sending an e-ticket and the customer does not receive it, verify the email address on the booking and check your email log in [E-tickets Overview](../e-tickets-overview.md).
{% endhint %}
{% endstep %}
{% endstepper %}

***

### Reprint Per Transport (bulk)

Use **Reprint Per Transport** when you need to print or reprint tickets for **many bookings** connected to specific transports (for example, upcoming departures).

<figure><img src="../.gitbook/assets/image (162).png" alt=""><figcaption></figcaption></figure>

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
### 1) Open the tab

Open **Reprint Per Transport** from the top of the **Print Tickets** page.
{% endstep %}

{% step %}
### 2) Narrow down the bookings

Set **Booking period** and/or **Departure period**.

Optionally choose **Length** if you want to limit the results further.
{% endstep %}

{% step %}
### 3) Select the transport(s)

Click **Transports** and select the transport(s) you want to print tickets for.
{% endstep %}

{% step %}
### 4) Print

Click **Print** to generate the tickets for all matching bookings.
{% endstep %}
{% endstepper %}

***

### FAQ

#### Why can’t I send the e-ticket?

Common reasons:

* The booking is not confirmed yet.
* You do not have the required access rights.

#### The customer didn’t receive the e-ticket—what should I check?

* Confirm the **email address on the booking** is correct.
* Check **spam/junk** on the customer side.
* Look up the email in [E-tickets Overview](../e-tickets-overview.md) to see whether it was **sent**, **failed**, or **not sent**.

#### What’s the difference between “Send E-Ticket” and “Copy to e-mail”?

* **Send E-Ticket** sends the ticket to the **customer email** stored on the booking.
* **Copy to e-mail** sends an extra copy to the address you type in **Alternative Email**.

#### Should I use “Print One Ticket”?

Use **Print One Ticket** when you want a **single combined PDF** for the whole booking (useful for families/groups).

If you need tickets separated (for example, per transport leg or operational handling), leave it unchecked.

#### I need tickets only for one transport leg—what should I do?

Use the **Reprint Per Transport** tab and filter by the relevant transport. This is the easiest way to reprint tickets for a specific outbound/return leg.

#### My browser doesn’t download/open the ticket PDF—what can I do?

* Allow **pop-ups** for Tourpaq (some browsers open the PDF in a new tab/window).
* Try downloading the PDF instead of opening it in-browser.
* If you use a company network, check whether a browser security policy is blocking downloads.

#### Does the ticket reflect recent booking changes?

Yes—when you print/send a ticket, Tourpaq generates it from the booking’s current data. If you updated the booking (names, dates, products, etc.), reprint/resend the ticket to share the latest version.

#### Do ticket attachments also get sent when I send an e-ticket?

Yes—if your email template includes a ticket PDF, any configured ticket attachments will be included as well.

If you are an administrator and need to configure attachments, see [Tickets attachments](../email-setup/tickets-attachments/).
