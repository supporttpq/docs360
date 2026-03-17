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
---

# How to set autobilling for hotels

Autobilling for hotels is configured per hotel in Tourpaq Office.

You set it in the **Autobilling** section on the hotel’s **General** tab.

### Enabling Autobilling

* **Automatic Billing (Checkbox):** Activates autobilling for the selected hotel.
* **Creditor:** A linked creditor is mandatory for autobilling to function. See [How to create a creditor](how-to-create-a-creditor.md).

<figure><img src="../.gitbook/assets/image (319).png" alt="Hotel autobilling settings with creditor and schedule options"><figcaption><p>Enable hotel Autobilling, link a creditor, and choose how hotel supplier invoices are generated.</p></figcaption></figure>

### Scheduling options

Invoices can be generated on the following schedules:

* **Daily**
* **Weekly** – select the weekday.
* **Monthly** – select the day of the month.
* **Days After Departure** – generate invoices a set number of days after guest departure.

***

### Invoice information fields

The following fields appear on the generated invoice:

* **Department Code**
* **Account Deposit**
* **Account Debit**

***

### Pre-arrival schedules

Invoices can also be scheduled **before the guest's arrival** at the hotel.\
The same scheduling options apply:

* Daily
* Weekly
* Monthly

***

#### Generating past invoices

You can create invoices for **past periods** by entering the desired dates in the settings.

***

#### Finalizing settings

After all configurations are made, click **Save** to apply the changes.

***

### FAQ

* **Do I need to enable Autobilling for every hotel?**\
  Yes. Hotel Autobilling is configured per hotel. Enable **Automatic Billing** on each hotel that should generate invoices.
* **Why can’t I enable Autobilling without a creditor?**\
  Autobilling needs a creditor to know who the invoice is issued to, which currency to use, and which accounting settings to export. Create and link a creditor first: [How to create a creditor](how-to-create-a-creditor.md).
* **Where do generated hotel invoices show up?**\
  In **Finance → Invoice**. See [Invoice](../invoice.md).
* **When are invoices actually generated?**\
  Based on your selected schedule (daily/weekly/monthly/after departure). The exact runtime is typically handled by a scheduled job (often overnight), depending on your setup.
* **What’s the difference between “pre-arrival schedules” and “days after departure”?**\
  Pre-arrival schedules generate invoices before arrival on a recurring cadence (daily/weekly/monthly). **Days After Departure** generates invoices a set number of days after the guest departs.
* **Can I create invoices for past periods?**\
  Yes. Use **Generating past invoices** and enter the dates for the period you want to invoice, then **Save**.
* **The schedule is set, but no invoices are created. What should I check?**\
  Confirm the hotel has:
  1. a linked **Creditor**, 2) **Automatic Billing** enabled, and 3) cost data available for the invoiced items.\
     Also check **Finance → Invoice** and filter by invoice type/creditor/date.
* **How does supplier approval work?**\
  If your Autobilling flow uses approvals, suppliers receive an email link to approve or reject invoices. See [Autobilling](./).
