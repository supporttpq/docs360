---
description: >-
  Enable Autobilling for extras in Tourpaq Office. Link a creditor, set invoice
  schedule, and generate separate supplier invoices for services like transfers,
  golf, and insurance.
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

# How to set autobilling for extras

### Overview

Autobilling for extras automates **supplier invoicing** for booking extras like transfers, golf, and insurance.

Configure it on **Extras → Extra General**, under **Automatic Billing**. When enabled, Tourpaq Office generates invoices on a schedule and assigns them to the linked creditor.

***

### Purpose

The purpose of the Extras Autobilling configuration is to:

* Ensure that all extra services are billed **automatically** and **independently** from hotel or transport invoices.
* Maintain **consistency and traceability** in supplier invoicing.
* Simplify the **export process** to the accounting system by aligning each extra with its creditor and accounting codes.

This setup allows financial teams to manage and control invoicing without manual intervention.

<figure><img src="../.gitbook/assets/image (20) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Extra General automatic billing settings"><figcaption><p>Extra General → Automatic Billing: link a creditor and define when the extra should be invoiced.</p></figcaption></figure>

### How it works

When Autobilling is activated for an Extra:

1. The system uses the **selected creditor** and its **currency** to generate the invoice.
2. The **department and account codes** are included in the invoice lines if configured.
3. The billing frequency (daily, weekly, monthly, or **days after service**) determines when invoices are created.
4. If autobilling is disabled, the extra may be handled by a combined supplier invoice flow (for example, included on a hotel invoice), depending on your setup.

Invoices follow the same scheduling logic used for hotel autobilling.

See:

* [Autobilling](./)
* [How to set autobilling for hotels](how-to-set-autobilling-for-hotels.md)

***

### Instructions

#### **Access the Extra Configuration**

Navigate to:\
**Extras → Extra General → Automatic Billing section**

#### **Configure Autobilling Settings**

| **Field**                           | **Description**                                                                                                                                                                                                   |
| ----------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Department Code**                 | Enter the department code to be displayed on the invoice.                                                                                                                                                         |
| **Account Debit / Account Deposit** | _(Optional)_ If filled, these fields will appear on the generated invoice and help with accounting allocation.                                                                                                    |
| **Creditor**                        | Select the creditor responsible for the extra. This is mandatory for autobilling to function. Once selected, the extra uses the creditor’s currency. See [How to create a creditor](how-to-create-a-creditor.md). |
| **Automatic Billing**               | _(Checkbox)_ Activate this option to enable autobilling for the extra.                                                                                                                                            |
| **Schedule**                        | Choose when invoices are generated: **Daily**, **Weekly**, **Monthly**, or **Days After** (similar to hotel autobilling). You can also generate invoices for past dates.                                          |

#### **Save the Configuration**

Click **Save** to apply the autobilling settings.

***

### **Result**

If **Autobilling** is enabled:

* The extra will be invoiced **separately** according to the selected schedule.

If **Autobilling** is disabled:

* The extra may be invoiced as part of a combined flow (for example a hotel invoice), depending on your setup.

This ensures flexibility in how additional services are billed and supports both standalone and combined invoicing scenarios.

***

### FAQ

* **Do I need to enable Autobilling for each extra?**\
  Yes. Autobilling is configured per extra. Enable **Automatic Billing** on each extra that should generate supplier invoices.
* **Why is the creditor mandatory?**\
  The creditor determines who the invoice is issued to, which currency to use, and which accounting settings apply. Create and link a creditor first: [How to create a creditor](how-to-create-a-creditor.md).
* **Where can I see the generated extra invoices?**\
  In **Finance → Invoice**. See [Invoice](../invoice.md).
* **When are invoices generated?**\
  Based on your selected schedule (daily/weekly/monthly/days after). The exact runtime is controlled by your scheduled job setup (often overnight).
* **Can I generate invoices for a past period?**\
  Yes. Use the past-date options in the schedule settings, then save.
* **Autobilling is enabled, but no invoices are created. What should I check?**\
  Confirm the extra has 1) a linked **Creditor**, 2) **Automatic Billing** enabled, and 3) cost data available for the booked extras. Then check **Finance → Invoice** and filter by creditor/date/type.
* **How does supplier approval work?**\
  If your Autobilling flow uses approvals, suppliers receive an email link to approve or reject invoices. See [Autobilling](./).
