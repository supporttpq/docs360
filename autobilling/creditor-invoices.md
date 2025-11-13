# Creditor invoices

### **Overview**

The **Creditor Invoice** feature in Tourpaq enables automated and scheduled invoicing for multiple service types — including **Hotels**, **Extras**, **Supplements**, and **Handling fees**.\
It also provides complete visibility and control over the **invoice lifecycle**, from creation to payment, including the ability to **regenerate** or **archive** invoices when necessary.

***

### **Purpose**

This feature ensures that all creditor-related billing is performed on time and in alignment with contractual and operational requirements.\
By defining invoice schedules and managing invoice statuses, administrators can:

* Automate recurring invoicing tasks
* Maintain consistent accounting processes
* Simplify creditor reconciliation and reporting

<figure><img src="../.gitbook/assets/image (24) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Setting Invoice Schedules**

Invoice schedules define when and how invoices are automatically generated for specific entities such as hotels, extras, supplements, or handling services.

#### **Supported Schedule Types**

You can create invoice schedules for:

* **Hotels**
* **Hotels (Before Arrival)**
* **Extras**
* **Supplements**
* **Handling**

#### **Configuration Steps**

| **Step**                                   | **Action**                                                                                                                                                                                                                                                                                                                         |
| ------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Add New Schedule**                    | Click **Add New Schedule** to start creating a new schedule.                                                                                                                                                                                                                                                                       |
| **2. Select Interval Type**                | <p>Choose one of the following:<br>• <strong>Daily</strong> – generates invoices every day.<br>• <strong>Weekly</strong> – select a day of the week.<br>• <strong>Monthly</strong> – select a specific day of the month.<br>• <strong>Days After</strong> – specify the number of days after an event (e.g., after departure).</p> |
| **3. Select Entity**                       | Choose the applicable hotel, extra, supplement, or handling entry.                                                                                                                                                                                                                                                                 |
| **4. Save Configuration**                  | Click **Save** to apply the new schedule.                                                                                                                                                                                                                                                                                          |
| **5. Add Additional Schedules (Optional)** | Repeat the process to configure multiple schedules as needed.                                                                                                                                                                                                                                                                      |

***

### **Invoice Statuses**

Each invoice generated in the system follows a defined status flow that reflects its current position in the billing process.

| **Status**      | **Description**                                                       |
| --------------- | --------------------------------------------------------------------- |
| **Pending**     | Automatically assigned when an invoice is first generated.            |
| **Approved**    | Indicates that the creditor has reviewed and approved the invoice.    |
| **Paid**        | Assigned when an approved invoice has been marked as paid.            |
| **Regenerated** | Set when the invoice has been recreated after updates or corrections. |
| **Archived**    | The invoice has been archived and stored for record-keeping.          |
| **Rejected**    | Indicates that the creditor has declined the invoice.                 |
| **Deleted**     | The invoice has been permanently removed from the system.             |

***

### **Status Flow Examples**

| **Example Flow**                            | **Description**                                                                         |
| ------------------------------------------- | --------------------------------------------------------------------------------------- |
| **Pending → Approved → Paid → Regenerated** | Typical flow where an invoice is processed, paid, and later regenerated for correction. |
| **Pending → Approved → Regenerated**        | The invoice is approved and then regenerated without payment.                           |
| **Pending → Rejected → Regenerated**        | The invoice is rejected by the creditor and later corrected.                            |
| **Pending → Deleted**                       | The invoice is removed before processing.                                               |
| **Pending → Regenerated**                   | The invoice is recreated before approval.                                               |

***

### **Regenerating an Invoice**

Regeneration allows you to recreate an invoice in case of data corrections, supplier changes, or updated booking values.

#### **Steps to Regenerate an Invoice**

| **Step**                    | **Action**                                                             |
| --------------------------- | ---------------------------------------------------------------------- |
| **1. Open Invoice Listing** | Go to **Finance → Invoice Listing**.                                   |
| **2. Select Invoice**       | Locate and select the invoice that needs to be regenerated.            |
| **3. Click Regenerate**     | Press the **Regenerate** button.                                       |
| **4. Confirm Action**       | Click **OK** to confirm regeneration.                                  |
| **5. Verify New Invoice**   | The regenerated invoice will appear in the list with the updated data. |

<figure><img src="../.gitbook/assets/image (25) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Result**

With invoice scheduling and lifecycle management, the **Creditor Invoice** feature provides a complete automation flow for supplier invoicing — from generation to payment — ensuring timely processing and accurate financial reporting across all creditor-related entities in Tourpaq.
