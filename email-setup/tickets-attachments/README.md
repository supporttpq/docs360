---
description: Configure PDF documents that Tourpaq adds to ticket emails and ticket PDFs.
---

# Tickets attachments

Ticket attachments add PDF documents to customer tickets. They support standard travel documents and booking-specific information. The configuration works with [Ticket Attachments](ticket-attachments.md), [Print Tickets](../../tickets/print-tickets.md), and ticket email delivery.

### Overview

The **Ticket Attachments** module adds PDF documents to ticket emails. Depending on the delivery method, Tourpaq sends each PDF separately or appends it to the ticket PDF.

Settings apply per agency. Each agency can therefore use its own customer documents.

### Purpose

Use ticket attachments to distribute documents that customers need with their travel documents, including terms and conditions, baggage rules, and hotel information.

Tourpaq evaluates the booking when it generates a ticket. It includes every attachment that matches the booking configuration.

### Requirements

* An **Administrator** role is required.
* The selected agency must be the agency that sends the ticket.
* Each document must be a PDF no larger than 1 MB.
* A facility attachment requires its category to appear on the ticket.

{% hint style="warning" %}
Large or numerous attachments can prevent ticket emails from reaching recipients. Keep PDFs small and attach only required documents.
{% endhint %}

### Navigation

In Tourpaq Office, open **E-mail Setup → Ticket Attachments**.

Select the agency before opening or changing an attachment configuration.

### Interface overview

The **Ticket Attachments** page contains these controls:

* **Agency** selects the agency whose attachment configuration appears. This setting scopes every upload and replacement.
* Transport-type tabs define the attachment scope. **All Transports** supplies the default configuration.
* The attachment list shows configured PDF documents for the selected scope. Use its upload and download actions to manage documents.
* The delivery choice controls whether Tourpaq adds the document to the email or the ticket PDF.

For the tab names, upload controls, and transport-specific behavior, see [Ticket Attachments](ticket-attachments.md).

### Delivery options

Choose one delivery option for each uploaded PDF:

* **Separate attachment** sends the PDF as an additional file with the ticket email.
* **Merged into ticket** appends the PDF pages to the ticket PDF. The customer receives one combined PDF.

Use **Merged into ticket** for documents that must remain with the ticket. Use **Separate attachment** when the document should remain a distinct file.

### Attachment sources

Tourpaq can include attachments from several booking levels:

* **Global attachments** apply to all bookings.
* **Scenario-specific attachments** apply to configured brands, seasons, or products.
* **Resort**, **Hotel**, **Facility**, and **Transport** attachments apply when the booking contains that item.

Facility documents support hotel facilities. A facility category must print on the ticket. Tourpaq merges at most five facility documents per ticket.

### Configure ticket attachments

{% stepper %}
{% step %}
#### Select the agency

In **E-mail Setup → Ticket Attachments**, select the agency that sends the ticket.

Review the selected agency before uploading or replacing a document.
{% endstep %}

{% step %}
#### Set the default documents

Open **All Transports**.

Upload the standard PDFs and choose their delivery option.
{% endstep %}

{% step %}
#### Add transport-specific documents

Open the required transport-type tab.

Upload the replacement or additional PDF for that transport type.
{% endstep %}

{% step %}
#### Verify the result

In **Print Tickets**, generate a test ticket for a matching booking.

Check the ticket PDF and email attachments before using the configuration for customer tickets.
{% endstep %}
{% endstepper %}

### System behavior

Ticket attachments are included only with emails that contain a ticket PDF. Emails without a ticket PDF do not include them.

Changes do not alter emails that Tourpaq has already sent. Generate and send a ticket again to deliver updated documents.

If more than five facility documents match a booking, Tourpaq merges the first five. The remaining facility documents are ignored.

### Examples

#### Standard terms and conditions

Add **Terms & Conditions** in **All Transports**. Select **Merged into ticket**. Tourpaq appends the terms to every matching ticket PDF.

#### Charter baggage rules

Open **Charter Transports** and upload the charter baggage rules. Select **Separate attachment**. Tourpaq sends the document only with tickets for matching charter transport bookings.

#### Hotel facility rules

Link a pool or spa rules PDF to the relevant facility. Ensure that the facility category appears on the ticket. Tourpaq includes the document when the booking uses that facility.

### Related pages

* [Ticket Attachments](ticket-attachments.md) explains transport-type tabs and attachment actions.
* [Print Tickets](../../tickets/print-tickets.md) explains ticket generation and email delivery.
* [E-tickets Overview](../../e-tickets-overview.md) helps verify sent and failed ticket emails.
