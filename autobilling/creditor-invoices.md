---
description: >-
  Configure supplier invoice schedules and manage creditor invoice statuses in
  Tourpaq Office Finance. Regenerate invoices and archive invoices when needed.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# Creditor invoices

### Overview

Creditor invoices automate and track **supplier invoicing** across service types like **hotels**, **extras**, **supplements**, and **handling fees**.

Use this to manage invoice schedules, track invoice statuses, and regenerate or archive invoices when needed.

***

### **Purpose**

This feature ensures that all creditor-related billing is performed on time and in alignment with contractual and operational requirements.\
By defining invoice schedules and managing invoice statuses, administrators can:

* Automate recurring invoicing tasks
* Maintain consistent accounting processes
* Simplify creditor reconciliation and reporting

<figure><img src="../.gitbook/assets/image (24) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Creditor invoice schedules overview"><figcaption><p>Configure invoice schedules for hotels, extras, supplements, and handling.</p></figcaption></figure>

### Setting invoice schedules

Invoice schedules define when and how invoices are automatically generated for specific entities such as hotels, extras, supplements, or handling services.

#### **Supported Schedule Types**

You can create invoice schedules for:

* **Hotels**
* **Hotels (Before Arrival)**
* **Extras**
* **Supplements**
* **Handling**

#### **Configuration Steps**

| **Step**                                   | **Action**                                                                                                                                                                            |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Add New Schedule**                    | Click **Add New Schedule** to start creating a new schedule.                                                                                                                          |
| **2. Select interval type**                | Choose one of: **Daily** (every day), **Weekly** (select weekday), **Monthly** (select day of month), or **Days After** (number of days after an event, for example after departure). |
| **3. Select Entity**                       | Choose the applicable hotel, extra, supplement, or handling entry.                                                                                                                    |
| **4. Save Configuration**                  | Click **Save** to apply the new schedule.                                                                                                                                             |
| **5. Add Additional Schedules (Optional)** | Repeat the process to configure multiple schedules as needed.                                                                                                                         |

***

### Invoice statuses

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

### Status flow examples

| **Example Flow**                            | **Description**                                                                         |
| ------------------------------------------- | --------------------------------------------------------------------------------------- |
| **Pending → Approved → Paid → Regenerated** | Typical flow where an invoice is processed, paid, and later regenerated for correction. |
| **Pending → Approved → Regenerated**        | The invoice is approved and then regenerated without payment.                           |
| **Pending → Rejected → Regenerated**        | The invoice is rejected by the creditor and later corrected.                            |
| **Pending → Deleted**                       | The invoice is removed before processing.                                               |
| **Pending → Regenerated**                   | The invoice is recreated before approval.                                               |

***

### Regenerating an invoice

Regeneration allows you to recreate an invoice in case of data corrections, supplier changes, or updated booking values.

#### **Steps to Regenerate an Invoice**

| **Step**                  | **Action**                                                             |
| ------------------------- | ---------------------------------------------------------------------- |
| **1. Open invoice list**  | Go to **Finance → Invoice**.                                           |
| **2. Select Invoice**     | Locate and select the invoice that needs to be regenerated.            |
| **3. Click Regenerate**   | Press the **Regenerate** button.                                       |
| **4. Confirm Action**     | Click **OK** to confirm regeneration.                                  |
| **5. Verify New Invoice** | The regenerated invoice will appear in the list with the updated data. |

<figure><img src="../.gitbook/assets/image (25) (1) (1) (1) (1) (1) (1) (1).png" alt="Regenerate invoice action in invoice list"><figcaption><p>Regenerate an invoice from Finance → Invoice when costs or booking values changed.</p></figcaption></figure>

### Result

With invoice scheduling and lifecycle management, the **Creditor Invoice** feature provides a complete automation flow for supplier invoicing — from generation to payment — ensuring timely processing and accurate financial reporting across all creditor-related entities in Tourpaq.

***

### FAQ

* **Where do I see all generated invoices?**\
  In **Finance → Invoice**. See [Invoice](../invoice.md).
* **What’s the difference between schedules and invoices?**\
  A schedule defines when invoices are generated. An invoice is the generated record with a status (Pending/Approved/Paid/etc.).
* **When are scheduled invoices generated?**\
  Based on the schedule (daily/weekly/monthly/days after). The exact runtime depends on your scheduled job setup (often overnight).
* **When should I regenerate an invoice?**\
  Regenerate after changes to costs, booking values, supplier/creditor setup, or invoice details.
* **Can I archive invoices?**\
  Yes. Archiving keeps invoices for record-keeping while hiding them from the default working list (depending on your filters).
