---
description: >-
  Auto-generate supplier invoices in Tourpaq Office from cost data and billing
  schedules. Suppliers approve by email. Track invoices in Finance → Invoice.
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

# Autobilling

### Overview

Autobilling automatically generates supplier invoices based on booking data, predefined schedules, and configured costs.

The system creates invoices for multiple components such as hotels, extras, transfers, and supplements, reducing manual financial processing.

### Business Context

In travel operations, billing is repetitive and highly dependent on booking data and supplier contracts.

Without automation:

* invoices are created manually
* delays occur in supplier payments
* inconsistencies appear across bookings

Autobilling solves this by:

* generating invoices automatically based on system data
* aligning costs with bookings and contracts
* ensuring suppliers receive invoices on time

It is primarily used by:

* finance teams
* operations teams managing suppliers

### Prerequisites

Autobilling requires several system components:

#### 1 Services

The following services must be active:

* IGS (Invoice Generating Service)
* EBL (Early Booking List)
* HDI (Hotel Deposit Invoice)

Each service controls when and how invoices are generated (e.g. every 30 minutes or daily).

#### 2 Creditors

A creditor must be configured with:

* name, email, IBAN, currency
* automatic billing enabled
* approval and payment intervals

#### 3 Email Setup

Required email templates:

* Creditor Invoice
* Early Booking Rooming List

#### 4 Cost Configuration

* hotel costs
* extra costs
* transfer costs

Without costs, invoices cannot be generated correctly.

### Automated invoice generation

Tourpaq generates invoices for the following components:

* **Hotel Deposit Invoice**
* **Hotel Early Booking Invoice**
* **Hotel Invoice**
* **Extra Invoice**
* **Extra Early Booking Invoice**
* **Transfer Invoice**
* **Discount/Supplement Invoice**
* **Handling Invoice**

These invoices are generated based on configured billing schedules and use the cost values stored in the system for each relevant item (e.g., hotels, extras, supplements).

### System Behavior

#### 1 Invoice Generation

* The system generates invoices automatically based on schedules
* Only bookings matching the configuration are included
* Invoices are created periodically (e.g. every 30 minutes or daily)

***

#### 2 Data Source

Invoice values are calculated using:

* booking data
* room costs
* configured pricing

***

#### 3 Approval Workflow

1. Invoice is generated
2. Supplier receives email with approval link
3. Supplier approves or rejects invoice

This creates an auditable approval flow.

***

#### 4 Invoice Lifecycle

Invoices go through the following statuses:

* Pending
* Approved
* Paid
* Archived

Only approved invoices can be paid.

***

#### 5 Regeneration

* Invoices can be regenerated
* System re-evaluates:
  * creditor
  * costs
  * configuration

Changes in setup are applied during regeneration.

### Configuration Scope (Where Autobilling Applies)

Autobilling is configured per entity:

| Entity                | Configuration Location             |
| --------------------- | ---------------------------------- |
| Hotels                | Hotel → Overview -> Basic Setup    |
| Extras                | Extra → Overview -> Basic Setup    |
| Discounts/Supplements | Discunt -> Overview -> Basic Setup |
| Handling              | Supplier configuration             |

Each entity:

* has its own schedule
* can share or separate invoices

### Viewing generated invoices

All generated invoices are available in **Finance → Invoice**.

See [Invoice](../invoice.md).

For each invoice, the following information is displayed:

* **Invoice Number**
* **Invoice Type**
* **Invoice Name**
* **Creditor Name**
* **Internal Comment**
* **Amount**
* **Approved Due Date**
* **Download Option** (PDF format)

{% hint style="info" %}
Autobilling uses supplier/creditor configuration. If a creditor is missing, create it first (see the Autobilling subpages).
{% endhint %}

### Example Scenario

**Configuration:**

* Hotel assigned to creditor
* Schedule: Weekly
* Automatic billing enabled

**Flow:**

1. Bookings are created
2. System evaluates schedule
3. Invoice is generated automatically
4. Supplier receives email
5. Supplier approves invoice

**Result:**

* invoice is created without manual work
* supplier approval is tracked

### Edge Cases

* If services are not active: no invoices are generated
* If creditor is missing: Autobilling fails
* If multiple entities share configuration: invoices may be combined
* If “Add Own Schedule” is enabled: separate invoices are generated
* If creditor is changed:  regeneration updates invoice data

### Troubleshooting

| Issue                   | Cause                 | Solution             |
| ----------------------- | --------------------- | -------------------- |
| No invoices generated   | Services not active   | Activate IGS / EBL   |
| Missing data in invoice | Costs not configured  | Verify cost setup    |
| Invoice not sent        | Email not configured  | Setup Email Center   |
| Duplicate invoices      | Overlapping schedules | Review configuration |
| Incorrect creditor      | Configuration changed | Regenerate invoice   |

***

### Related Pages

* [Autobilling for Hotels](how-to-set-autobilling-for-hotels.md)
* [Creditors](../creditor.md)
* [Finance → Invoices](../invoice.md)
* [Booking](/broken/pages/RD5atvvSmxEBqtYp4KiC)
* [Room Cost](../hotel/hotel-creation/room-cost/)
