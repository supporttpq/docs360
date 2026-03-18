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

This page explains how to configure Autobilling for extras, enabling the system to automatically generate supplier invoices for additional services such as excursions, transfers, or add-ons.

Extras can be invoiced either:

* together with hotel invoices
* or as separate invoices, depending on configuration

***

### Purpose

The purpose of the Extras Autobilling configuration is to:

* Ensure that all extra services are billed **automatically** and **independently** from hotel or transport invoices.
* Maintain **consistency and traceability** in supplier invoicing.
* Simplify the **export process** to the accounting system by aligning each extra with its creditor and accounting codes.

This setup allows financial teams to manage and control invoicing without manual intervention.

### Prerequisites

Before enabling Autobilling for extras:

* Autobilling services must be active (IGS, etc.)
* A creditor must be configured
* Extra costs must be defined
* Booking flow must include extras
* Email templates must be configured

### Configuration

<figure><img src="../.gitbook/assets/image (20) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Extra General automatic billing settings"><figcaption><p>Extra General → Automatic Billing: link a creditor and define when the extra should be invoiced.</p></figcaption></figure>

#### 1 Access

Navigate to: `Extras → Extra → Main Tab`

***

#### 2 Enable Autobilling

In the extra configuration: enable **Automatic Billing**

***

#### 3 Configure Required Fields

All fields are mandatory for correct behavior

| Field             | Description                         | Impact                    |
| ----------------- | ----------------------------------- | ------------------------- |
| Automatic Billing | Enables invoicing for extras        | Activates Autobilling     |
| Creditor          | Supplier receiving invoice          | Defines recipient         |
| Schedule          | Defines when invoices are generated | Controls timing           |
| Account Debit     | Accounting reference                | Used in exports           |
| Department Code   | Financial grouping                  | Used in reporting         |
| Add Own Schedule  | Controls invoice separation         | Defines invoice structure |

***

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

If **Autobilling** is enabled:

* The extra will be invoiced **separately** according to the selected schedule.

If **Autobilling** is disabled:

* The extra may be invoiced as part of a combined flow (for example a hotel invoice), depending on your setup.

This ensures flexibility in how additional services are billed and supports both standalone and combined invoicing scenarios.

***

### Example Scenario

**Scenario 1 – Combined invoice**

Configuration:

* Extra: Excursion
* Add Own Schedule: Disabled

Flow:

1. Booking includes hotel + excursion
2. Autobilling runs
3. System generates ONE invoice

**Result:**

* hotel + extra included in same invoice

**Scenario 2 – Separate invoice**

Configuration:

* Add Own Schedule: Enabled

Flow:

1. Booking includes hotel + excursion
2. Autobilling runs
3. System generates:
   * hotel invoice
   * extra invoice

**Result:**

* separate financial documents

***

### Edge Cases

* If **cost is missing**: extra is not invoiced or has incorrect value
* If **creditor is not set**: invoice is not generated
* If **Add Own Schedule changes after generation**: regeneration may restructure invoices
* If **extra is removed from booking**: regenerated invoice will exclude it

***

### Troubleshooting

| Issue                               | Cause                      | Solution                 |
| ----------------------------------- | -------------------------- | ------------------------ |
| Extra not invoiced                  | Missing cost               | Configure extra cost     |
| Invoice missing extras              | Add Own Schedule enabled   | Check invoice separation |
| No invoice generated                | Automatic Billing disabled | Enable checkbox          |
| Wrong invoice structure             | Misconfigured schedule     | Review setup             |
| Extra not included in hotel invoice | Separate schedule active   | Disable Add Own Schedule |

***

### Related Pages

* Autobilling
* How to Set Autobilling for Hotels
* How to Create a Creditor
* Booking → Extras

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
