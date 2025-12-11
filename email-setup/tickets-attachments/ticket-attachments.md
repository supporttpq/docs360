# Ticket Attachments

### Overview

The **Ticket Attachments** page is used to manage PDF documents that are automatically attached to tickets sent via email. This feature ensures that agencies can provide passengers with relevant conditions and supplementary information for each booking.

This page is intended for back-office users responsible for configuring ticket email delivery and legal/conditions documents.

### Access

* Path: **E-mail Setup → Ticket Attachments**
* Note: The page is **agency-specific**, meaning the agency must be selected before making changes.

{% hint style="warning" %}
Because Ticket Attachments is **agency-specific**, always confirm that you have selected the correct agency before uploading or changing documents. Changes made here apply only to the selected agency.
{% endhint %}

### Purpose

* Allows agencies to attach specific **conditions PDF documents** to tickets.
* Ensures compliance and provides clear communication to travelers.
* Supports different attachment rules depending on the **transport type**.

### Transport Type Tabs

The page includes **five tabs**, each corresponding to a transport type:

1. **All Transports**
   * Documents applied to **all types of transports**, regardless of category.
2. **Charter Transports**
   * For transports defined using **Fix Quotas** for flights.
   * Attachments apply specifically to charter flights.
3. **Dynamic Transports**
   * For transports that use **Dynamic Itineraries**.
   * Itineraries may include **real transports** or **external providers (GDS)**.
4. **System Transports**
   * Generated from a **Transport Rule**.
   * At least one of the itinerary legs uses an **external provider (GDS)**.
5. **Sys-real Transports**
   * Generated from a **Transport Rule**.
   * Both itinerary legs use **real transports**.

The Ticket Attachments page shows all configured documents per transport type:

<figure><img src="../../.gitbook/assets/image (302).png" alt="Ticket Attachments overview screen."><figcaption><p>Ticket Attachments overview for an agency.</p></figcaption></figure>

#### All Transports

If a document is uploaded for a specific document type in **All Transports**, it will be set as the default for all other sections.

<figure><img src="../../.gitbook/assets/image (303).png" alt="All Transports tab configuration."><figcaption><p>All Transports tab, showing default documents for all transport types.</p></figcaption></figure>

### How Ticket Attachments work

* Attachments must be uploaded as **PDF files**.
* Agencies can define **different documents per transport type**, ensuring passengers receive the correct terms and conditions.
* Attachments are automatically included when tickets are generated and sent.

### Typical setup (step-by-step)

Use this flow when configuring ticket attachments for an agency:

{% stepper %}
{% step %}
#### 1. Open the Ticket Attachments page

* Go to **E-mail Setup → Ticket Attachments**.
* Make sure the correct **agency** is selected at the top of the screen.
{% endstep %}

{% step %}
#### 2. Configure defaults in "All Transports"

* In the **All Transports** tab, upload the standard **conditions PDF** documents that should apply to all transports by default.
* Decide for each document type whether it should be:
  * Sent as a **separate attachment**, or
  * **Appended to the end of the ticket** in the same PDF file.
* These documents will be used as defaults for the other transport-type tabs unless specifically overridden.
{% endstep %}

{% step %}
#### 3. Adjust documents per transport type (optional)

* Switch to the specific tabs (**Charter Transports**, **Dynamic Transports**, **System Transports**, **Sys-real Transports**).
* For each tab where you need different conditions:
  * Upload the transport-specific **conditions PDFs**.
  * Choose whether they are sent as separate attachments or appended to the ticket.
* Any document added here overrides the **All Transports** default for that transport type.
{% endstep %}

{% step %}
#### 4. Review existing attachments

* Check that each tab shows the expected documents and types (separate vs appended).
* Download documents where needed to verify that the correct version is configured.
{% endstep %}

{% step %}
#### 5. Verify by generating a ticket

* Create or use a test booking that matches the relevant transport type.
* Generate and send a ticket to confirm that:
  * The **right PDF(s)** are attached or appended.
  * The behavior matches your expectations per transport type.
{% endstep %}
{% endstepper %}

### Best practices

* Prefer configuring shared documents in **All Transports** and override them only in specific tabs when necessary.
* Use clear, descriptive file names (for example, including language and validity period) so it is easy to see which version is active.
* Coordinate changes with your legal or compliance team before replacing conditions documents.
* After updating any attachment, repeat the **Verify by generating a ticket** step to ensure emails still behave as expected.

### Managing attachments

#### Upload an attachment

You can upload:

* A **conditions PDF document** that will be sent together with the ticket as a separate attachment.
* A **conditions PDF document** that will be added to the end of the ticket in the same file.

<figure><img src="../../.gitbook/assets/image (304).png" alt="Upload dialog for ticket attachments."><figcaption><p>Uploading conditions documents to be attached to tickets.</p></figcaption></figure>

#### Download an attachment

You can download existing documents for review or reuse.

<figure><img src="../../.gitbook/assets/image (305).png" alt="Download option for ticket attachments."><figcaption><p>Downloading existing ticket attachment documents.</p></figcaption></figure>
