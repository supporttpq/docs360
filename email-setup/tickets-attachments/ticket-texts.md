---
description: Add and manage reusable text blocks that are printed on customer tickets.
---

# Ticket texts

### Overview

Ticket texts are reusable text blocks that Tourpaq prints on customer tickets when a booking matches configured rules. They complement [ticket attachments](./), which add PDF documents to ticket emails and ticket PDFs.

Use ticket texts for terms and conditions, fees, or short travel instructions. This setup keeps repeated customer messages consistent across matching bookings.

### Purpose

Ticket texts control information printed within the ticket PDF. Use separate entries when a message applies to different travel dates, products, or room types.

### Requirements

* Access to **E-mail Setup → Ticket Attachments → Ticket texts** is required.
* A booking must match the ticket text rules before Tourpaq prints the text.
* A test booking is required to verify the final ticket output.

### Navigation

In Tourpaq Office, open **E-mail Setup → Ticket Attachments → Ticket texts**.

### Interface overview

Use the ticket text list to create, edit, or delete entries. Open an entry to maintain its text, effective dates, and matching rules.

Each entry uses its **Date interval** and selected rules to determine when it prints. The ticket text does not print when the booking does not match those settings.

### Field descriptions

Complete each field when creating a ticket text:

* **Text type** identifies the purpose of the text, such as information or terms. Use it to distinguish text categories during maintenance.
* **Identification code** provides a short, searchable identifier. Use a descriptive code, such as `SUMMER_FEE_2026`, to distinguish versions and seasonal messages.
* **Date interval** sets the start and end dates when Tourpaq can use the text. The booking must fall within this interval.
* **Text content** contains the customer-facing message printed on the ticket. Keep it short and use approved customer wording.

### Typical setup (step-by-step)

{% stepper %}
{% step %}
#### Create a new ticket text

In **Ticket texts**, create a new entry.
{% endstep %}

{% step %}
#### Fill in the basic fields

Complete **Text type**, **Identification code**, **Date interval**, and **Text content**.
{% endstep %}

{% step %}
#### Choose when it should appear

Select the rules that determine when Tourpaq prints the text. Rules can apply to booking dates, products, or room types.
{% endstep %}

{% step %}
#### Save and test

Save the entry.

Create a matching test booking and generate its ticket. Confirm that the text prints in the expected location.
{% endstep %}
{% endstepper %}

### System behavior

Tourpaq evaluates the **Date interval** and matching rules when it generates a ticket. It prints every ticket text whose configuration matches the booking.

Changes affect tickets generated after the change. Previously sent tickets do not change. Generate and send a ticket again to deliver updated text.

### Example

Create a ticket text for a seasonal resort fee:

1. Set **Identification code** to `SUMMER_FEE_2026`.
2. Set **Date interval** to the summer travel period.
3. Select the relevant product or room type.
4. Add the fee explanation in **Text content**.

Tourpaq prints the note only for matching bookings during that period.

### Best practices

{% hint style="info" %}
Keep **Text content** short and use approved customer wording. Create a new entry for a revised message. Set a new **Date interval** rather than overwriting a previous version.
{% endhint %}

### Related pages

* [Tickets attachments](./) explains PDF attachments sent with tickets.
* [Ticket Attachments](ticket-attachments.md) explains agency and transport-specific attachment configuration.
* [Print Tickets](../../tickets/print-tickets.md) explains how to generate, print, and email ticket PDFs.
