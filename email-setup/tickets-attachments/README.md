# Tickets attachments

### **Overview**

The **Ticket Attachments** module (available only to **Administrator** users) allows a Tourpaq company to attach additional documents to booking confirmation emails and printed tickets.

Administrators can configure attachments per agency, ensuring that each agency may have its own set of documents included with the customer’s ticket.

***

### **Attachment Options**

Documents can be sent in **two different ways**:

1. **As a separate attachment**
   * Example: A Terms & Conditions PDF is sent alongside the booking ticket as an individual file.
2. **Merged into the ticket file**
   * Example: A Terms & Conditions PDF is appended at the end of the ticket PDF as part of the same document.

***

### **Types of Documents That Can Be Attached**

* **Global Attachments (all bookings)**
  * Terms & Conditions documents apply to every booking.
* **Scenario-Specific Attachments**
  * Documents that apply only under specific booking scenarios.
* **Resort-Specific Attachments**
  * A file linked to a specific resort, attached automatically when that resort is part of the booking.
* **Hotel-Specific Attachments**
  * A file linked directly to a specific hotel.
* **Facility-Specific Attachments**
  * A document linked to a facility within a hotel (e.g., _Pool Bar Rules_).
  * If a booking includes a hotel using that facility, the facility document is attached or merged.
  * **Note:** A maximum of **5 facility documents** can be merged per ticket.
* **Transport Attachments**
  * A file linked to a specific transport (e.g., _charter flight rules_).

***

### **Limitations**

To maintain email deliverability and prevent oversized attachments, the following restrictions apply:

* **Maximum number of facility documents merged**: 5 per ticket.
  * If more than 5 facilities have documents, only the first 5 will be merged.
* **Maximum file size per document**: 1 MB.
* **Facility visibility requirement**: The facility’s category must be configured to appear on the ticket; otherwise, its document will not be included.
* **Risk of undelivered emails**: Oversized attachments may prevent important booking-related emails (_Thank You_, _Booking Updated_, etc.) from being delivered.

***

### **Effect in Practice**

* Suppose a holiday booking includes a hotel with facilities (e.g., a Pool Bar, Spa, Kids' Club) that have rules or guidelines attached as documents. In that case, those files are automatically merged into the ticket or sent separately, depending on the administrator’s setup.
* Customers receive all relevant documents **without requiring manual sending**, ensuring compliance with policies and improving transparency.
