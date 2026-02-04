# Ticket Attachments

### Overview

Use **Ticket Attachments** to add PDF documents to tickets sent by email. These PDFs often include terms, conditions, or other important information.

This page is mainly for administrators who manage ticket emails and documents.

For the full module overview, see [Tickets attachments](./).

### Access

* Path: **E-mail Setup → Ticket Attachments**
* Note: Settings are **agency-specific**. Select the right agency before you change anything.

{% hint style="warning" %}
Always check the selected agency before you upload or replace documents. Your changes apply only to that agency.
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
* **Dynamic itinerary**: a trip built from live supplier data.

### Tabs by transport type

The page includes **five tabs**, each corresponding to a transport type:

1. **All Transports**
   * Default documents for **all** transport types.
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

<figure><img src="../../.gitbook/assets/image (302).png" alt="Ticket Attachments overview screen."><figcaption><p>Ticket Attachments overview for an agency.</p></figcaption></figure>

#### All Transports

If you upload a document in **All Transports**, it becomes the default. Other tabs use that default unless you override it.

<figure><img src="../../.gitbook/assets/image (303).png" alt="All Transports tab configuration."><figcaption><p>All Transports tab, showing default documents for all transport types.</p></figcaption></figure>

### How it works

* Attachments must be uploaded as **PDF files**.
* You can set **different documents per transport type**.
* Documents are included automatically when you generate and send a ticket.

### Typical setup (step-by-step)

Use this flow when configuring ticket attachments for an agency:

{% stepper %}
{% step %}
#### 1. Open the Ticket Attachments page

* Go to **E-mail Setup → Ticket Attachments**.
* Select the correct **agency** at the top of the page.
{% endstep %}

{% step %}
#### 2. Configure defaults in "All Transports"

* Open the **All Transports** tab.
* Upload the standard PDFs you want on most tickets.
* For each document type, choose how it is delivered:
  * **Separate attachment** in the email, or
  * **Added to the end of the ticket PDF**.
* These documents become the default for the other tabs.
{% endstep %}

{% step %}
#### 3. Adjust documents per transport type (optional)

* Switch to the specific tabs (**Charter Transports**, **Dynamic Transports**, **System Transports**, **Sys-real Transports**).
* Upload different PDFs where you need different rules.
* Choose separate vs added to the ticket.
* Anything you upload here overrides the **All Transports** default.
{% endstep %}

{% step %}
#### 4. Review existing attachments

* Check each tab for the expected documents.
* Download a document to confirm it is the right version.
{% endstep %}

{% step %}
#### 5. Verify by generating a ticket

* Create a test booking that matches the transport type.
* Generate and send a ticket.
* Confirm the right PDFs are included.
{% endstep %}
{% endstepper %}

### Best practices

* Set shared documents in **All Transports** first. Override only when needed.
* Use clear file names. Include language and valid dates when relevant.
* Agree changes with the right owner before replacing official documents.
* After any change, generate a test ticket again.

### Managing attachments

#### Upload an attachment

You can upload a PDF that is:

* Sent as a **separate attachment**, or
* **Added to the end** of the ticket PDF.

<figure><img src="../../.gitbook/assets/image (304).png" alt="Upload dialog for ticket attachments."><figcaption><p>Uploading conditions documents to be attached to tickets.</p></figcaption></figure>

#### Download an attachment

You can download existing documents for review or reuse.

<figure><img src="../../.gitbook/assets/image (305).png" alt="Download option for ticket attachments."><figcaption><p>Downloading existing ticket attachment documents.</p></figcaption></figure>

### FAQ

<details>

<summary>Do my changes affect all agencies?</summary>

No. Ticket Attachments are set per agency. Your changes apply only to the selected agency.

</details>

<details>

<summary>What file type can I upload?</summary>

PDF only.&#x20;

</details>

<details>

<summary>What is the difference between “separate attachment” and “added to the ticket”?</summary>

Separate attachment means the customer receives another PDF file in the email. Added to the ticket means the pages are appended to the ticket PDF.

</details>

<details>

<summary>Why does a document show in “All Transports” but not in another tab?</summary>

All Transports sets the default. Other tabs can override the default with their own documents.

</details>

<details>

<summary>How do I make sure customers get the new document?</summary>

Generate a test ticket and send it to yourself. Previously sent tickets will not change automatically.

</details>
