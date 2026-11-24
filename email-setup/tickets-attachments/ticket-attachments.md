# Ticket Attachments

### Overview

Use **Ticket Attachments** to add PDF documents to tickets sent by email. These PDFs often include terms, conditions, or other important information.

This page is mainly for administrators who manage ticket emails and documents.

For the full module overview, see [Tickets attachments](./).

### Access

* Path: **Email Setup → Ticket Attachments**
* Note: Settings are brand-specific. Select the right brand before you change anything.

{% hint style="warning" %}
Always check the selected brand before you upload or replace documents. Your changes apply only to that brand.
{% endhint %}

### Purpose

You can use this page to:

* Attach **PDF documents** to tickets.
* Make sure customers get the right information every time.
* Use different documents for different **transport types**.

### Words used on this page

Some labels match what you see in the system. Here is what they mean in plain language:

* **Transport**: how the customer travels, like a flight or transfer.
* **GDS**: an external flight booking system used by some suppliers.
* **Real transport**: a transport you manage directly in Tourpaq.
* **Transport Rule**: a rule that creates transports automatically.
* **Fix Quotas**: a fixed number of seats you control.
* **Dynamic itinerary**: an itinerary set up in Tourpaq whose legs use real transports or external suppliers.

### Tabs by transport type

The page includes up to **five tabs**, each corresponding to a transport type. **System Transports** and **Sys-real Transports** show only when the company feature **UseTransportRule** is on.

1. **All Transports**
   * Documents for **all** transport types. For each field, a document here is used instead of the same field on the other tabs.
2. **Charter Transports**
   * Charter flights that use **Fix Quotas**.
3. **Dynamic Transports**
   * Trips built from a dynamic itinerary.
   * These can use real transports or external suppliers like **GDS**.
4. **System Transports**
   * Created from a **Transport Rule**.
   * At least one trip part uses an external supplier like **GDS**.
5. **Sys-real Transports**
   * Created from a **Transport Rule**.
   * Both trip parts use **real transports**.

Each tab shows which documents are set up for that transport type:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (302).png" alt="Ticket Attachments overview screen."><figcaption><p>Ticket Attachments overview for a brand.</p></figcaption></figure></div>

#### All Transports

For each field, Tourpaq uses the document in **All Transports** first. It uses the document of another tab only when that field is empty in **All Transports**.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (303).png" alt="All Transports tab with its tooltip."><figcaption><p>All Transports tab. Its documents are used for every transport type.</p></figcaption></figure></div>

### How it works

* Upload attachments as **PDF files**. This page doesn't check the file type or size when you upload.
* You can set **different documents per transport type**.
* Tourpaq includes the documents automatically when you generate and send a ticket.

### Typical setup (step-by-step)

Use this flow when configuring ticket attachments for a brand:

{% stepper %}
{% step %}
#### Open the Ticket Attachments page

* Go to **Email Setup → Ticket Attachments**.
* Select the correct brand at the top of the page.
{% endstep %}

{% step %}
#### Configure shared documents in **All Transports**

* Open the **All Transports** tab.
* Upload the standard PDFs you want on most tickets.
* Upload each PDF in the field for how it is delivered:
  * as a separate attachment in the email, or
  * added to the end of the ticket PDF.
{% endstep %}

{% step %}
#### Adjust documents per transport type

* Switch to the specific tabs (**Charter Transports**, **Dynamic Transports**, **System Transports**, **Sys-real Transports**).
* Upload different PDFs where you need different rules. Use the field for a separate attachment or the field for the end of the ticket.
* Tourpaq uses a document from these tabs only when the same field is empty in **All Transports**.
{% endstep %}

{% step %}
#### Review existing attachments

* Check each tab for the expected documents.
* Download a document to confirm it is the right version.
{% endstep %}

{% step %}
#### Verify by generating a ticket

* Create a test booking that matches the transport type. Give it your own email address as the customer email address.
* In **Print Tickets**, enter the booking number, select **Send E-Ticket**, and click **Print/Send**.
* Confirm the ticket PDF and the email attachments are the right ones.
{% endstep %}
{% endstepper %}

### Best practices

* Set shared documents in **All Transports**. Leave a field empty there when a transport type needs its own document in that field.
* Use clear file names. Include language and valid dates when relevant.
* Agree changes with the right owner before replacing official documents.
* After any change, generate a test ticket again.

### Managing attachments

#### Upload an attachment

You can upload a PDF that is:

* Sent as a separate attachment, or
* Added to the end of the ticket PDF.

Select or drag the PDF into the field, and then click **Upload**. Each field holds one document. To replace a document, click **Delete**, and then upload the new one.

{% hint style="warning" %}
Give each document its own file name. Tourpaq stores all documents of a brand in one folder, so a file with the same name as an earlier upload replaces that file, also in other tabs and fields.
{% endhint %}

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (304).png" alt="Charter Transports tab with two uploaded PDF files and their Delete buttons."><figcaption><p>Uploaded conditions documents on a transport tab.</p></figcaption></figure></div>

#### Download an attachment

You can download existing documents for review or reuse. Click the file name to download it.
