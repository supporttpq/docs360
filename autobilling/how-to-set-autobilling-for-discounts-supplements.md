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

This page explains how to configure Autobilling for **discounts and supplements** so that the system automatically includes them in supplier invoicing when they apply to bookings.

Discounts and supplements adjust the net price of bookings. They can be invoiced:

* together with related services (hotel, extras, transfers), or
* as **separate billing items**, depending on configuration.

Autobilling ensures consistent invoicing of all applied pricing adjustments.

***

### Purpose

The purpose of this configuration is to:

* Automate the invoicing process for discounts and supplements applied to bookings.
* Allow financial departments to track and reconcile these adjustments with suppliers efficiently.
* Maintain consistency with the same autobilling principles used for hotels and extras.

By enabling autobilling, the system ensures that every discount or supplement is invoiced automatically, according to its defined billing frequency.

### Prerequisites

Before configuring Autobilling for discounts and supplements:

* **Autobilling services** must be active (IGS, etc.)
* A valid **Creditor** must be configured
* Pricing rules including discounts/supplements must exist
* Booking flow must include the applicable pricing adjustments
* Email templates for invoices must be configured

### Configuration

#### 1 Access

Navigate to: `Pricing → Discounts & Supplements → Main Tab`

***

#### 2 Enable Autobilling

In the discount or supplement configuration:

* Enable **Autobilling**
* Select associated **Creditor**
* Define **Schedule**
* Set required accounting codes

<figure><img src="../.gitbook/assets/image (321).png" alt="Discounts and supplements automatic billing settings"><figcaption><p>Discounts/Supplements → Automatic Billing: link a creditor, set codes, and schedule invoice generation.</p></figcaption></figure>

#### 3 Required Fields

| Field                     | Description                 | Impact                                                                                     |
| ------------------------- | --------------------------- | ------------------------------------------------------------------------------------------ |
| Automatic Billing         | Enables invoice generation  | Activates Autobilling for this pricing item                                                |
| Creditor                  | Supplier receiving invoices | Determines invoice recipient                                                               |
| Schedule                  | Timing of invoice runs      | Controls batching frequency                                                                |
| Account Debit             | Financial account reference | Used in exports and reporting                                                              |
| Department Code           | Internal financial grouping | Helps categorization                                                                       |
| Apply With Related Entity | Determines grouping         | Controls whether discount/supplement is combined with service invoice or billed separately |

### System Behavior

#### 1 Invoice Inclusion Logic

Once enabled, discounts and supplements are included automatically in invoices according to the configuration:

**If “Apply With Related Entity” is enabled:**

* the discount or supplement is included on the invoice for the related service (hotel, extra, transfer, etc.)

**If disabled:**

* a **separate invoice item or separate invoice** may be generated for the pricing adjustment

***

#### 2 Data Source

Values used in invoice calculations are taken from:

* the booking’s applied pricing (discount/supplement value)
* the pricing rule definitions
* cost configuration (if applicable)

***

#### 3 Timing

Invoices for discounts and supplements are generated on the schedule defined in the configuration. The frequency depends on system settings (e.g., hourly, daily) and cannot be manually triggered outside those schedules.

***

#### 4 Regeneration Behavior

When an invoice is regenerated:

* updated pricing adjustments are re‑evaluated
* changes in discount or supplement value are applied retroactively
* invoice lines may be added or removed

***

### Example Scenario

#### Example 1 – Combined Billing

**Configuration:**

* Discount: Early Booking
* Apply With Related Entity: Enabled

**Flow:**

1. Booking includes an early booking discount
2. Price adjustment is applied during pricing
3. Autobilling runs on schedule
4. Discount is included in related service invoice

**Result:**

* hotel invoice includes discount amount

***

#### Example 2 – Separate Billing

**Configuration:**

* Supplement: Late Check‑in Fee
* Apply With Related Entity: Disabled

**Flow:**

1. Booking includes supplement
2. System runs Autobilling
3. System generates a separate invoice for the supplement

**Result:**

* supplement appears on its own financial document

***

### Edge Cases

* If **No Creditor is set:** discount/supplement will not be invoiced
* If **Schedule is missing or paused:** no invoices are generated
* If **Discount/Supplement values change after invoice generation:** regeneration updates invoice values
* If **Related entity configuration changes:** invoice grouping may differ after regeneration

***

### Troubleshooting

| Symptom                             | Likely Cause                                    | Resolution                  |
| ----------------------------------- | ----------------------------------------------- | --------------------------- |
| Discounts not appearing on invoices | “Apply With Related Entity” disabled or missing | Check configuration         |
| Supplements not invoiced            | Creditor not set                                | Assign appropriate creditor |
| Separate invoices not created       | Schedule not configured                         | Define schedule             |
| Wrong financial values              | Pricing rules outdated                          | Review pricing rule setup   |

***

### Related Pages

* Autobilling
* How to Create a Creditor
* How to Set Autobilling for Hotels
* How to Set Autobilling for Extras
* Pricing Rules
* Finance → Invoices

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
