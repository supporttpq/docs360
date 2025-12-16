# Tickets attachments

### **Overview**

The **Ticket Attachments** module (available only to **Administrator** users) allows a Tourpaq company to attach additional PDF documents to booking confirmation emails and printed tickets.

Attachments are configured per **agency**, so each agency can have its own set of documents that are automatically included with the customer’s ticket.

### **Access & Permissions**

* Path: **E-mail Setup → Ticket Attachments**
* Only users with **Administrator** rights can configure ticket attachments.
* Settings are **agency-specific** – make sure the correct agency is selected before making changes.

***

### **How Attachments Are Delivered**

Documents can be sent in **two different ways**. When you upload a PDF, you choose one of the following delivery options:

1. **As a separate attachment**
   * Example: A _Terms & Conditions_ PDF is sent alongside the ticket as an additional file in the email.
2. **Merged into the ticket PDF**
   * Example: A _Terms & Conditions_ PDF is appended at the end of the ticket so the customer receives a **single combined PDF**.

***

### **Where Attachments Can Come From**

Ticket attachments can be linked at several levels. For a given booking, the system checks the booking data (transport, resort, hotel, etc.) and includes all relevant documents that are configured.

* **Global attachments (all bookings)**
  * Generic documents such as **Terms & Conditions** that should apply to every booking.
* **Scenario-specific attachments**
  * Documents that apply only under particular booking scenarios (for example, specific brands, seasons, or products), as defined in your setup.
* **Resort-specific attachments**
  * Files linked to a particular **resort**.
  * Whenever a booking includes that resort, the document is attached or merged according to its configuration.
* **Hotel-specific attachments**
  * Files linked directly to a **hotel**.
  * Used for hotel-level conditions, welcome information, or local rules.
* **Facility-specific attachments**
  * Documents linked to a **facility** within a hotel (e.g. _Pool Bar Rules_, _Spa Regulations_).
  * If a booking includes a hotel using that facility, the facility document is automatically included.
  * **Maximum of 5 facility documents** can be merged per ticket.
  * The **facility category must be configured to appear on the ticket**; otherwise, its document will not be included.
* **Transport attachments**
  * Files linked to a specific **transport** (e.g. _charter flight rules_, _baggage regulations_).
  * These are sent when the booking uses that transport.

***

### **Limitations & Recommendations**

To keep tickets readable and ensure email deliverability, the following technical limits apply:

* **Maximum number of facility documents merged**: **5 per ticket**
  * If more than 5 facilities have documents linked, **only the first 5** will be merged into the ticket.
* **Maximum file size per document**: **1 MB**
* **Facility visibility requirement**: The facility’s **category must be visible on the ticket** or its attachment will be ignored.

{% hint style="warning" %}
Large or numerous attachments increase the risk that important emails (such as **Thank You**, **Booking Updated**, or other ticket emails) are not delivered. Keep PDFs as small as possible and avoid adding unnecessary documents.
{% endhint %}

***

### **Example: Effect in Practice**

Consider a holiday booking that includes:

* A hotel with several facilities (Pool Bar, Spa, Kids' Club) that each have an attached rules PDF.
* A charter flight with its own flight rules PDF.
* A global Terms & Conditions PDF defined for all bookings.

If all of these are configured:

1. The global **Terms & Conditions** document is attached or merged for every booking.
2. Any **resort** and **hotel** documents linked to the selected products are included.
3. Up to **5 facility documents** (e.g. Pool Bar rules, Spa rules) are also included, provided their facilities are visible on the ticket.
4. The **transport** document (e.g. charter flight rules) is included based on the chosen transport.

The customer receives a ticket containing **all relevant information automatically**, without any manual sending from the agency, improving compliance and transparency.

***

### **FAQ**

#### 1. Which emails include ticket attachments?

Ticket attachments are included with emails that contain the **ticket PDF** (for example, booking confirmation / "Thank You" emails and booking update emails that resend the ticket). If an email does **not** include a ticket, no ticket attachments are sent.

#### 2. Why is my document not attached to the ticket?

Check the following:

* The document is uploaded as a **PDF** and is **below 1 MB**.
* You are editing the correct **agency** in **E-mail Setup → Ticket Attachments**.
* The document is linked at the right level (Global / Resort / Hotel / Facility / Transport).
* For **facility documents**, the **facility category is configured to appear on the ticket**.
* For **transport documents**, the booking actually uses that specific transport.

#### 3. What is the difference between "separate attachment" and "merged into ticket"?

* **Separate attachment** – the PDF is sent as an **additional file** in the email, alongside the ticket PDF.
* **Merged into ticket** – the PDF pages are **appended to the end of the ticket PDF**, so the customer receives one combined document.

#### 4. What happens if more than 5 facility documents are linked to a booking?

Only **5 facility documents** can be merged per ticket. If more than 5 facilities have documents configured, **only the first 5** (according to the system’s internal order) will be included. The remaining facility documents are ignored for that ticket.

#### 5. What happens if a PDF file is larger than 1 MB?

Files larger than **1 MB** should be avoided. Oversized files increase the risk that emails containing tickets and attachments are **not delivered** by the recipient’s mail server. Reduce the file size (for example, by compressing the PDF) and upload it again.

#### 6. Can I use different attachments for different transport types?

Yes. You can configure attachments per **transport** and, on the detailed **Ticket Attachments** configuration page, per **transport type** (such as charter, dynamic, or system transports). This allows you to send different rules or conditions depending on how the customer is travelling.

#### 7. Do I need to re-send the ticket after changing attachments?

Yes. Changes to ticket attachments **do not affect previously sent emails**. After updating attachments, you must **re-send the ticket email** (or create a new booking/ticket) for customers to receive the updated documents.
