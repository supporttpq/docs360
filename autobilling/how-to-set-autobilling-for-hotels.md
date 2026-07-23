---
description: >-
  Enable Autobilling for hotels in Tourpaq Office. Link a creditor, choose
  invoice schedule (daily/weekly/monthly/after departure), and save to generate
  supplier hotel invoices automatically.
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
  actions:
    visible: true
---

# How to set autobilling for hotels

### Overview

This page explains how to configure Autobilling for hotels, allowing the system to automatically generate supplier invoices based on booking and cost data.

Autobilling ensures that hotel-related costs are invoiced without manual intervention, using predefined schedules and creditor settings.

### Business Context

Hotel billing is one of the most repetitive and error-prone processes in travel operations.

Without automation:

* invoices must be created manually
* costs may be missed or delayed
* inconsistencies appear across bookings

Autobilling for hotels solves this by:

* automatically generating invoices based on bookings
* aligning invoices with contract costs
* ensuring suppliers receive consistent and timely billing

This feature is mainly used by:

* finance teams
* operations teams managing suppliers

### Prerequisites

Before configuring Autobilling for hotels:

* Autobilling services must be active (IGS, EBL, etc.)
* A **Creditor** must be created and configured
* Room costs must be defined in the hotel
* Booking flow must be operational
* Email templates for invoices must exist

### Configuration

#### 1. Access

Navigate to: `Hotel → Hotel → Main Tab`

#### 2. Enable Autobilling

In the hotel configuration: Enable the **Automatic Billing** checkbox.

<figure><img src="../.gitbook/assets/image (319).png" alt="Hotel autobilling settings with creditor and schedule options"><figcaption><p>Enable hotel Autobilling, link a creditor, and choose how hotel supplier invoices are generated.</p></figcaption></figure>

#### 3. Configure Required Fields

All fields are mandatory for Autobilling to work correctly:

| Field                   | Description                         | Impact                |
| ----------------------- | ----------------------------------- | --------------------- |
| Automatic Billing       | Enables invoicing                   | Activates Autobilling |
| Schedule                | Defines when invoices are generated | Controls timing       |
| Account Debit           | Accounting reference                | Used in exports       |
| Creditor                | Supplier receiving invoice          | Defines recipient     |
| Account Deposit         | Deposit accounting                  | Used for prepayments  |
| Department Code         | Internal accounting mapping         | Used in finance       |
| Schedule Before Arrival | Allows invoicing before arrival     | Enables pre-invoicing |

* **Creditor:** A linked creditor is mandatory for autobilling to function. See [How to create a creditor](how-to-create-a-creditor.md).

### System Behavior

#### Invoice Generation

* The system generates invoices automatically based on schedule
* Only bookings that match the rule are included

Invoices are generated periodically using background services (e.g. every 30 minutes or daily depending on type)

### Scheduling options

Invoices can be generated on the following schedules:

* **Daily**
* **Weekly** – select the weekday.
* **Monthly** – select the day of the month.
* **Days After Departure** – generate invoices a set number of days after guest departure.

### Invoice information fields

The following fields appear on the generated invoice:

* **Department Code**
* **Account Deposit**
* **Account Debit**

### Pre-arrival schedules

Invoices can also be scheduled **before the guest's arrival** at the hotel.\
The same scheduling options apply:

* Daily
* Weekly
* Monthly

#### Generating past invoices

You can create invoices for **past periods** by entering the desired dates in the settings.

#### Finalizing settings

After all configurations are made, click **Save** to apply the changes.

### Example Scenario

**Configuration:**

* Hotel: Marina Hotel
* Creditor: Supplier A
* Schedule: Weekly
* Automatic Billing: Enabled

**Flow:**

1. Bookings are created for the hotel
2. Weekly schedule triggers Autobilling
3. System generates invoice for all new bookings since last run
4. Invoice is sent to the creditor

**Result:**

* Supplier receives invoice automatically
* No manual billing required

### Edge Cases

* If **Automatic Billing is disabled**:
  * no invoices will be generated
* If **Creditor is missing**:
  * Autobilling will fail
* If **Room costs are not configured**:
  * invoice values may be incorrect or missing
* If **Hotel is part of a combination**:
  * invoicing is based on individual hotels in the combination

### Troubleshooting

| Issue                     | Cause                      | Solution                 |
| ------------------------- | -------------------------- | ------------------------ |
| No invoice generated      | Automatic Billing disabled | Enable checkbox          |
| Invoice missing bookings  | Schedule not triggered yet | Check schedule timing    |
| Incorrect amounts         | Room cost misconfigured    | Verify hotel cost setup  |
| Invoice not sent          | Email setup missing        | Configure Email Center   |
| Missing extras in invoice | Separate schedule enabled  | Check “Add Own Schedule” |

### Related Pages

* [Autobilling Overview](./)
* [Creditors](../creditor.md)
* [Hotel Setup](../hotel/hotel-creation/)
* [Room Cost Configuration](../hotel/hotel-creation/room-cost/)
* [Finance → Invoices](../invoice.md)
