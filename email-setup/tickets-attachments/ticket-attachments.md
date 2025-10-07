# Ticket Attachments

### **Overview**

The **Ticket Attachments** page is used to manage PDF documents that are automatically attached to tickets sent via email. This feature ensures that agencies can provide passengers with relevant conditions and supplementary information for each booking.

### **Access**

* Path: **E-mail Setup → Ticket Attachments**
* Note: The page is **agency-specific**, meaning the agency must be selected before making changes.

### **Purpose**

* Allows agencies to attach specific **conditions PDF documents** to tickets.
* Ensures compliance and provides clear communication to travelers.
* Supports different attachment rules depending on the transport type.

### **Transport Type Tabs**

The feature includes **five tabs**, each corresponding to a transport type:

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

### **Usage Notes**

* Attachments must be uploaded as **PDF files**.
* Agencies can define **different documents per transport type**, ensuring passengers receive the correct terms and conditions.
* Attachments are automatically included when tickets are generated and sent.

<figure><img src="../../.gitbook/assets/image (302).png" alt=""><figcaption></figcaption></figure>

#### All Transports <a href="#all-transports" id="all-transports"></a>

Note: If a document is uploaded for a specific document type in 'All Transports', it will be set as the default for all other sections.

<figure><img src="../../.gitbook/assets/image (303).png" alt=""><figcaption></figcaption></figure>

#### Actions <a href="#actions" id="actions"></a>

* Upload

Upload types:

* Conditions PDF document that will be sent together with the ticket, as a separate attachment.
* Conditions PDF document that will be added to end of the ticket in the same file.

<figure><img src="../../.gitbook/assets/image (304).png" alt=""><figcaption></figcaption></figure>

* Download

Documents can also be downloaded:

<figure><img src="../../.gitbook/assets/image (305).png" alt=""><figcaption></figcaption></figure>
