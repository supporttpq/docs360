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

Autobilling for handling generates supplier invoices for handling charges (fees) linked to bookings.

You configure it on the supplier profile. You also decide whether handling is invoiced separately or included on the hotel invoice.

***

### Purpose

This setup ensures that handling costs are invoiced according to supplier agreements and accounting preferences.\
It provides flexibility to:

* Automatically bill handling services using their own schedule, or
* Combine handling charges with the hotel’s main invoice.

<figure><img src="../.gitbook/assets/image (22) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Supplier handling autobilling settings"><figcaption><p>Supplier → Handling: link a creditor, set account debit and schedule, and control handling invoice behavior.</p></figcaption></figure>

### How it works

When **Automatic Billing** is enabled in the supplier’s handling configuration, Tourpaq:

1. Uses the selected **creditor** to generate invoices.
2. Applies the configured **account debit** and **schedule** (daily, weekly, monthly, or days after).
3. Determines whether handling is **invoiced separately** or **included on the hotel invoice** based on **Add Own Schedule**.

***

### Instructions

#### **Configure Handling Autobilling**

| **Step**                          | **Action**                                                                                 |
| --------------------------------- | ------------------------------------------------------------------------------------------ |
| **1. Access Supplier Settings**   | Navigate to **Users → Suppliers** and select the desired supplier.                         |
| **2. Open Handling Section**      | Scroll to the **Handling** tab in the supplier profile.                                    |
| **3. Select a Creditor**          | Choose the creditor to whom invoices for handling will be issued.                          |
| **4. Set Account Debit**          | Enter the account debit number to be displayed on the invoice.                             |
| **5. Define Schedule**            | Choose the billing frequency: **Daily**, **Weekly**, **Monthly**, or **Days After**.       |
| **6. Determine Invoice Behavior** | Add Own Schedule checked = invoiced separately. Unchecked = included on the hotel invoice. |
| **7. Save Configuration**         | Click **Save** to apply the autobilling settings.                                          |

<figure><img src="../.gitbook/assets/image (23) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Handling price configuration"><figcaption><p>Add a handling price so Autobilling has an amount to invoice.</p></figcaption></figure>

#### **Add a Handling Price**

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
