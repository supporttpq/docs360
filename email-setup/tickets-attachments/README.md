---
description: Configure PDF documents that Tourpaq adds to ticket emails and ticket PDFs.
---

# Tickets attachments

Ticket attachments add PDF documents to customer tickets. They support standard travel documents and booking-specific information. The configuration works with [Ticket Attachments](ticket-attachments.md), [Print Tickets](../../tickets/print-tickets.md), and ticket email delivery.

### Overview

The **Ticket Attachments** module adds PDF documents to ticket emails. Depending on the delivery method, Tourpaq sends each PDF separately or appends it to the ticket PDF.

Settings apply per brand. Each brand can therefore use its own customer documents.

### Purpose

Use ticket attachments to distribute documents that customers need with their travel documents, including terms and conditions, baggage rules, and hotel information.

Tourpaq evaluates the booking when it generates a ticket. It includes every attachment that matches the booking configuration.

### Requirements

* You need access to **Ticket Attachments** and the administrator, brand manager, or support role.
* The selected brand must be the brand that sends the ticket.
* Upload PDF files. The **Ticket Attachments** page doesn't check the file type or size.
* A facility attachment requires **Show on ticket** to be selected on its category.

{% hint style="warning" %}
Large attachments can make ticket emails too big for some mailboxes. Keep PDFs small and attach only required documents.
{% endhint %}

### Navigation

In Tourpaq Office, open **Email Setup → Ticket Attachments**.

Select the brand before opening or changing an attachment configuration.

### Interface overview

The **Ticket Attachments** page contains these controls:

* The brand list at the top of Tourpaq Office selects the brand whose attachment configuration appears. This setting scopes every upload and replacement.
* Transport-type tabs define the attachment scope. For each field, Tourpaq uses the document in **All Transports** first. It uses the document of another tab only when that field is empty in **All Transports**.
* Each tab has two upload fields, one for each delivery option. An uploaded document shows as its file name: click the name to download it, or click **Delete** to remove it.

For the tab names, upload controls, and transport-specific behavior, see [Ticket Attachments](ticket-attachments.md).

### Delivery options

The field you upload a PDF into sets how Tourpaq delivers it. Each field holds one PDF:

* The field for a separate attachment sends the PDF as an additional file with the ticket email.
* The field for the end of the ticket appends the PDF pages to the ticket PDF. The customer receives one combined PDF.

Use the end-of-ticket field for documents that must remain with the ticket. Use the separate-attachment field when the document should remain a distinct file.

### Attachment sources

Tourpaq can include attachments from several booking levels:

* Documents on the **Ticket Attachments** page apply to all bookings of the brand, or of one transport type.
* **Resort**, **Hotel**, **Facility**, **Transport**, **Real Transport**, and **Extra** attachments apply when the booking contains that item.
* A PDF you add to a booking in [Comments](../../booking/new-booking/comments.md) as a ticket attachment applies to that booking only.

Facility documents support hotel facilities. The facility category must have **Show on ticket** selected. Tourpaq merges at most five facility documents per ticket.

### Configure ticket attachments

{% stepper %}
{% step %}
#### Select the brand

In **Email Setup → Ticket Attachments**, select the brand that sends the ticket.

Review the selected brand before uploading or replacing a document.
{% endstep %}

{% step %}
#### Set the shared documents

Open **All Transports**.

Upload the standard PDFs, each one in the field for its delivery option.
{% endstep %}

{% step %}
#### Add transport-specific documents

Open the required transport-type tab.

Upload the PDF for that transport type. Tourpaq uses it only when the same field is empty in **All Transports**.
{% endstep %}

{% step %}
#### Verify the result

In **Print Tickets**, enter the booking number of a test booking that matches the transport type. Select **Send E-Ticket**, leave **Print One Ticket** selected, and click **Print/Send**. The ticket PDF opens in a new tab, and Tourpaq sends the email to the customer email address of the booking. Use a test booking with your own email address.

Check the ticket PDF and the email attachments before you use the configuration for customer tickets.
{% endstep %}
{% endstepper %}

### System behavior

Tourpaq includes ticket attachments only in emails that contain a ticket PDF. Emails without a ticket PDF do not include them.

Changes do not alter emails that Tourpaq has already sent. Generate and send a ticket again to deliver updated documents.

If more than five facility documents match a booking, Tourpaq merges five of them and ignores the rest.

### Examples

#### Standard terms and conditions

In **All Transports**, upload the terms and conditions in the field for the end of the ticket. Tourpaq appends the terms to every matching ticket PDF.

#### Charter baggage rules

Open **Charter Transports** and upload the charter baggage rules in the field for a separate attachment. Leave that field empty in **All Transports**. Tourpaq sends the document only with tickets for matching charter transport bookings.

#### Hotel facility rules

Upload a pool or spa rules PDF on the relevant facility. On the facility category, select **Show on ticket**. Tourpaq includes the document when the booked hotel has that facility.

### Related pages

* [Ticket Attachments](ticket-attachments.md) explains transport-type tabs and attachment actions.
* [Print Tickets](../../tickets/print-tickets.md) explains ticket generation and email delivery.
* [E-tickets Overview](../../e-tickets-overview.md) helps verify sent and failed ticket emails.
