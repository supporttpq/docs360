---
description: >-
  Track and troubleshoot e-ticket emails in Tourpaq Office. Search by booking
  number or email address, verify delivery status (sent/opened/failed), preview
  messages, and export e-ticket logs.
---

# E-tickets Overview

### Overview

Use **E-tickets Overview** to track ticket email delivery in **Tourpaq Office**. This page is your email log for e-tickets. Use it to troubleshoot “ticket not received” cases before departure.

Common tasks:

* Search by **booking number** or **email address**.
* Check status like **Sent**, **Opened**, **Failed**, or **Not Sent**.
* Preview what was sent to the customer.
* Export the filtered list for operations and audits.

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Tourpaq Office E-tickets Overview page showing e-ticket email list, filters, and delivery status columns"><figcaption><p>E-tickets Overview in Tourpaq Office. Use it to monitor e-ticket email delivery status and troubleshoot failed or missing ticket emails.</p></figcaption></figure>

### Filters

Use filters to narrow down the e-ticket email log. Combine filters to find a specific customer fast.

#### Available filters

| Filter                                  | Description                                                                          |
| --------------------------------------- | ------------------------------------------------------------------------------------ |
| **Booking number**                      | Search for a specific booking number                                                 |
| **Email**                               | Search by customer email address                                                     |
| **Sent from / Sent to**                 | Filter based on the date the e-ticket was sent                                       |
| **Transport**                           | Filter by specific transport code(s)                                                 |
| **Departure from / Departure to**       | Filter by passenger departure date                                                   |
| **Email Type**                          | Choose the type of e-ticket email (e.g., Thank you for booking, Ticket confirmation) |
| **Status**                              | Filter by status: Sent, Opened, Failed, Confirmed, Not Sent                          |
| **Hide Confirmed**                      | Hide entries where the customer has already confirmed reading                        |
| **Show only communication email types** | Shows only e-ticket communication templates                                          |

All filters can be used simultaneously.

#### **Display / More Filters**

The **Display** button shows or hides additional filter fields. **Clear** resets all filters.

***

### Table overview

Each row represents one e-ticket email sent to a customer.

| Column             | Description                                                 |
| ------------------ | ----------------------------------------------------------- |
| **Departure**      | The passenger’s departure date                              |
| **Transport**      | Transport code (airline + routing)                          |
| **Booking Number** | Booking reference number                                    |
| **Email Type**     | Template used for this ticket (e.g., Thank you for booking) |
| **Customer Name**  | Passenger name on the booking                               |
| **Telephone**      | Customer phone number                                       |
| **Email Address**  | Destination email                                           |
| **Sent Date**      | When the email was sent                                     |
| **Opened**         | Timestamp when customer opened the email                    |
| **Confirmed**      | Confirmation received (if confirmation is required)         |
| **Failed Status**  | If sending failed, the reason is displayed                  |
| **Status**         | Overall status (sent, failed, not sent, opened…)            |

***

### Preview an e-ticket email

Click any row to open a preview of the e-ticket email. This helps when you need to confirm the content and recipient.

This is useful for:

* customer support calls
* checking if information was correct
* verifying branding or attachments
* confirming content before sending again (if your workflow allows it)

***

### Export

Use **Export** to download the filtered list in Excel format.

Useful for:

* documenting delivery issues
* auditing communication logs
* mass-checks before departure days
* sharing with airline or support teams

***

### Troubleshooting checklist

If a customer says they did not receive the ticket email:

1. Search the booking number or the customer email address.
2. Check **Status** and any **Failed Status** reason.
3. Verify the email address on the booking.
4. Ask the customer to check spam/junk folders.
5. Export the list if you need to escalate to IT/support.

{% hint style="info" %}
For printing or sending a ticket PDF from a booking, use [Print Tickets](tickets/print-tickets.md).
{% endhint %}

***

### FAQ

#### What does each status mean?

* **Sent**: Tourpaq sent the email to the recipient’s mail server.
* **Opened**: The recipient opened the email (tracking must be enabled).
* **Confirmed**: The customer completed a confirmation step (if used in your setup).
* **Failed**: The email was rejected or could not be delivered.
* **Not Sent**: No email was sent for that booking/email type in the period.

#### The status is **Failed**. What should I do?

Open the row and read **Failed Status**. Then verify the customer email address on the booking.

If the address is correct, export the list and escalate to IT/support.

#### The status is **Sent**, but the customer did not receive it. What now?

Ask the customer to check spam/junk and any quarantine folder. Then confirm the recipient address matches the booking.

If you need to send the ticket again, use [Print Tickets](tickets/print-tickets.md).

#### I can’t find the booking in the list. Why?

Most often, your filters exclude it. Clear filters, then search by **booking number**.

Also verify the booking has a ticket email generated for the selected **Email Type**.

#### Why do I see **Opened** on some emails, but not on others?

Open tracking can be blocked by the customer’s email client. Some corporate mail systems also strip tracking pixels.

#### What does **Hide Confirmed** do?

It removes rows where the customer already confirmed reading. Use it for pre-departure checks to focus on missing confirmations.
