---
description: >-
  Enable Autobilling for discounts and supplements in Tourpaq Office. Link a
  creditor, set department/account codes, choose an invoice schedule, and
  generate separate supplier invoices automatically.
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

# How to set autobilling for discounts/supplements

### Overview

Autobilling for discounts and supplements automates **supplier invoices** for booking adjustments.

Each discount or supplement can be invoiced on its own schedule. This helps with supplier settlement and finance reconciliation.

***

### Purpose

The purpose of this configuration is to:

* Automate the invoicing process for discounts and supplements applied to bookings.
* Allow financial departments to track and reconcile these adjustments with suppliers efficiently.
* Maintain consistency with the same autobilling principles used for hotels and extras.

By enabling autobilling, the system ensures that every discount or supplement is invoiced automatically, according to its defined billing frequency.

<figure><img src="../.gitbook/assets/image (321).png" alt="Discounts and supplements automatic billing settings"><figcaption><p>Discounts/Supplements → Automatic Billing: link a creditor, set codes, and schedule invoice generation.</p></figcaption></figure>

### How it works

When autobilling is activated for a **discount** or **supplement**, the system:

1. Uses the configured **creditor** to generate the invoice.
2. Applies the specified **Department code** and **Account debit** to the invoice.
3. Follows the defined **invoice schedule** (daily, weekly, monthly, or days after service).
4. Creates a **separate invoice** for each discount or supplement using its dedicated schedule.

If autobilling is **disabled**, no automatic invoices are generated, and the discount/supplement remains unbilled until manual processing.

***

### Instructions

#### **Access Configuration**

Navigate to:\
**Discounts / Supplements → Automatic Billing section**

#### **Configure Autobilling Settings**

| **Field**             | **Description**                                                                                                                                                                                                    |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Department Code**   | Enter the department code to be shown on the invoice.                                                                                                                                                              |
| **Account Debit**     | Specify the account debit number that should appear on the invoice.                                                                                                                                                |
| **Creditor**          | Select the creditor to whom the invoice will be issued. This field is mandatory for autobilling.                                                                                                                   |
| **Automatic Billing** | _(Checkbox)_ Activate this option to enable automatic invoicing for the discount or supplement.                                                                                                                    |
| **Schedule**          | Choose how often invoices are generated: **Daily**, **Weekly**, **Monthly**, or **Days After** (same as hotels and extras). Using a dedicated schedule ensures a separate invoice for this discount or supplement. |

#### **Save Configuration**

Click **Save** to apply and activate autobilling for the selected discount or supplement.

***

### **Result**

Once configured:

* The system automatically generates and sends invoices to the selected creditor according to the chosen schedule.
* Each discount or supplement is invoiced independently, ensuring accurate supplier settlements and financial transparency.

***

### FAQ

* **Do I need to enable Autobilling per discount/supplement?**\
  Yes. Autobilling is configured per discount or supplement. Enable **Automatic Billing** on each item that should generate supplier invoices.
* **Why is the creditor mandatory?**\
  Autobilling needs a creditor to know who the invoice is issued to, which currency to use, and how to export to accounting. Create and link a creditor first: [How to create a creditor](how-to-create-a-creditor.md).
* **Where can I see the generated invoices?**\
  In **Finance → Invoice**. See [Invoice](../invoice.md).
* **When are invoices generated?**\
  Based on the schedule you select (daily/weekly/monthly/days after). The exact runtime depends on your scheduled job setup (often overnight).
* **Does this create separate invoices?**\
  Yes. Each discount or supplement can create its own invoice based on its schedule and creditor setup.
* **Autobilling is enabled, but no invoice is created. What should I check?**\
  Confirm 1) a **Creditor** is selected, 2) **Automatic Billing** is enabled, and 3) the discount/supplement is actually used on bookings in the period. Then check **Finance → Invoice** with creditor/date filters.
* **How does supplier approval work?**\
  If your Autobilling flow uses approvals, suppliers receive an email link to approve or reject invoices. See [Autobilling](./).
