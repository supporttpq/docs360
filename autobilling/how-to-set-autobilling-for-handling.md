---
description: >-
  Enable Autobilling for handling fees in Tourpaq Office. Set creditor, account
  debit, schedule, and handling price to invoice handling separately or on the
  hotel invoice.
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

# How to set autobilling for handling

### Overview

Handling refers to services associated with bookings that are not tied directly to hotel rooms, transfers, or extras — for example processing fees, documentation fees, service charges, or other non‑standard supplier‑based charges.

This page explains how to configure the system to automatically generate invoices for handling items using Autobilling.

***

### Purpose

This setup ensures that handling costs are invoiced according to supplier agreements and accounting preferences.\
It provides flexibility to:

* Automatically bill handling services using their own schedule, or
* Combine handling charges with the hotel’s main invoice.

### Prerequisites

Before enabling Autobilling for handling:

‑ Handling categories or items must be defined\
‑ The handling item must be linked to a creditor (supplier)\
‑ Accounting codes (account debit / department code) must be configured\
‑ Autobilling services must be active (IGS, EBL, etc.)\
‑ Email templates must be set up for invoice sending

Without these, handling invoices will not be generated correctly.

***

### Configuration

#### 1 Access

Navigate to: `Users → Suppliers -> Handling`

***

#### 2 Enable Autobilling

<figure><img src="../.gitbook/assets/image (22) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Supplier handling autobilling settings"><figcaption><p>Supplier → Handling: link a creditor, set account debit and schedule, and control handling invoice behavior.</p></figcaption></figure>

When **Automatic Billing** is enabled in the supplier’s handling configuration, Tourpaq:

1. Uses the selected **creditor** to generate invoices.
2. Applies the configured **account debit** and **schedule** (daily, weekly, monthly, or days after).
3. Determines whether handling is **invoiced separately** or **included on the hotel invoice** based on **Add Own Schedule**.

***

#### **Add a Handling Price**

<figure><img src="../.gitbook/assets/image (23) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Handling price configuration"><figcaption><p>Add a handling price so Autobilling has an amount to invoice.</p></figcaption></figure>

| **Step**                        | **Action**                                                        |
| ------------------------------- | ----------------------------------------------------------------- |
| **1. Go to New Price**          | Open the **New Price** section for handling.                      |
| **2. Set Arrival Date**         | Define the date of arrival for which the handling price applies.  |
| **3. Define Booking Dates**     | Enter the applicable booking date range.                          |
| **4. Enter Price**              | Specify the handling price.                                       |
| **5. Set Age Range (Optional)** | Define **Start Age** and **End Age** if handling is age-specific. |
| **6. Save Price**               | Click **Save Price**, then **Save** to confirm.                   |

***

### Result

Once configured, the system automatically generates handling invoices according to the defined creditor, schedule, and billing behavior.\
This ensures accurate, timely, and supplier-specific handling invoicing within Tourpaq.

***

### FAQ

* **Where do I configure handling Autobilling?**\
  On the supplier profile: **Users → Suppliers → Handling**.
* **Do I need a creditor?**\
  Yes. Autobilling needs a creditor to issue the invoice, set currency, and export correctly. See [How to create a creditor](how-to-create-a-creditor.md).
* **Where can I see generated handling invoices?**\
  In **Finance → Invoice**. See [Invoice](../invoice.md).
* **What does “Add Own Schedule” do?**\
  Checked: handling is invoiced separately. Unchecked: handling is included on the hotel invoice (depending on your setup).
*   **Why is Autobilling enabled but no invoice is created?**\
    Confirm you have:

    1. A linked **Creditor**
    2. A schedule
    3. A handling price configured

    Then check **Finance → Invoice** with supplier/creditor and date filters.
* **When are invoices generated?**\
  Based on the schedule you select. The exact runtime depends on your scheduled job setup (often overnight).
* **How does supplier approval work?**\
  If your Autobilling flow uses approvals, suppliers receive an email link to approve or reject invoices. See [Autobilling](./).
