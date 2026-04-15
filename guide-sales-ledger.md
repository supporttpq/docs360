---
description: >-
  Reconcile guide payments and settlements in Tourpaq Office Finance. Filter by
  payment period, guide, resort, and payment method. Review debits/credits,
  extras, and export XLSX for accounting.
---

# Guide Sales Ledger

The **Guide Sales Ledger** is a finance report for **guide payments**.

Use it to reconcile what guides collected, what was refunded, and what must be settled for **guide settlement**.

It is typically used by finance teams, destination managers, and administrators.

### Overview

The report consolidates **debits**, **credits**, **extras**, **payment methods**, and **resort activity** for a selected period.

Use it to:

* Verify guide transactions
* Reconcile amounts handed in by guides
* Check extras sold per guide
* Track revenue per resort
* Audit guide-related financial activity

### Purpose

The purpose of the Guide Sales Ledger is to ensure:

* **Transparency** of every transaction registered by guides
* **Accuracy** of payments received, refunds, or outstanding balances
* **Consistency** between bookings and guide-reported payments
* **Support for accounting and commission validation**
* **Monitoring of guide performance and operational activity**

You can use the fields to find missing references, validate amounts, and spot abnormal activity.

### Preconditions

Before working with the Guide Sales Ledger:

* You must have an active Tourpaq Office user with **Financial** permissions (or admin access).
* A System Administrator must enable access to **Guide Sales Ledger** in user permissions.

<figure><img src=".gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Guide Sales Ledger permission in Finance menu"><figcaption><p>Enable Guide Sales Ledger in user permissions (Finance) to access the report.</p></figcaption></figure>

* Guide transactions (debit/credit entries) must already exist for the period.
* Bookings, extras, and supplier mappings must be configured correctly.
* You must know the **payment period** you are reviewing.
* Familiarity with debit/credit/balance helps.

### How it works

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (4).png" alt="Guide Sales Ledger filters and results table"><figcaption><p>Filter guide transactions by payment period, guide, resort, and payment method.</p></figcaption></figure>

### 1. Select filters

Users can apply filters to narrow down results:

|                     |                                                                                                 |
| ------------------- | ----------------------------------------------------------------------------------------------- |
| Payment Period      | Defines when the payment was registered by the guide.                                           |
| Allotment Period    | Optional filter matching payments with specific departure date ranges.                          |
| Guide               | Select a specific guide or guide team.                                                          |
| Resorts             | Limit the view to one or more resorts.                                                          |
| **Payment Methods** | The payment method used. Examples: `CHSING` (cash in, guide), `OTHOUTG` (other refunds, guide). |
| **Display**         | Applies filters.                                                                                |
| **Clear**           | Resets all filters to default.                                                                  |

{% hint style="info" %}
If you need to **create** a booking payment (not guide payment), use [Payment Registration](finance/payment-registration.md).
{% endhint %}

#### Table columns explained

| Column                     | Description                                                                                             |
| -------------------------- | ------------------------------------------------------------------------------------------------------- |
| **Pay. Date**              | Payment Date                                                                                            |
| **Method**                 | Payment method used                                                                                     |
| **Bkg. No**                | Booking number related to the payment                                                                   |
| **Departure**              | Departure date of the booking                                                                           |
| **Payment ID**             | Unique ID for the payment                                                                               |
| **Guide Team**             | The guide team linked to the guide                                                                      |
| **Guide Name**             | The guide handling the payment                                                                          |
| **Transport**              | Transport code for the booking                                                                          |
| **Debit**                  | Amount collected from the customer                                                                      |
| **Credit**                 | Refunds or adjustments                                                                                  |
| **O.Amount**               | Original amount paid in basket in the chosen currency                                                   |
| **Ad.**                    | Number of adults in the booking                                                                         |
| **Ch.**                    | Number of children in the booking                                                                       |
| **Tr.Code**                | Transaction Code                                                                                        |
| **Comm.**                  | Committed                                                                                               |
| **Dep.Paid**               | Deposit Paid                                                                                            |
| **Guide Payment Comments** | Any comments added by guide or system                                                                   |
| **Resort**                 | The resort where the payment was recorded                                                               |
| **M.O.User**               | Manual Overview User - the name of the user who handles negative extra orders, for credit transactions. |

#### Row details

Each row can be expanded using the **▸** icon on the left.

Expanded rows show connected extras and details.

* Extra name
* Allotment date
* Number of adults and children
* Price per adult and child
* Creditor name
* Supplier name

#### Totals and balances

The **Sales Ledger** provides a consolidated financial overview of all debits, credits, and resulting balances grouped by currency. It helps users understand how much money has been charged (debit), refunded/credited (credit), and what the outstanding balance is for each currency and in total.

At the bottom of the page, totals are grouped by currency, and divided into three main categories repeated for each currency:

* **Debit -** Sum of all debit transactions across all currencies converted into the base currency. Debits usually represent **charges**, **invoices**, or **amounts the customer must pay**.
* **Credit -** Sum of all credits across all currencies, converted into the base currency. Credits usually represent **refunds**, **discounts**, or **payments received**.
* **Balance - Total Debit – Total Credit**, shown in the base currency. Represents the **overall outstanding balance**.

Each currency operates independently in its own ledger line.

#### Currency-Specific Fields

Totals are grouped by currency. Each currency has the same structure:

Example:

* **Currency**: for example THB, DKK, EUR.
* **Debit**: all debit transactions in that currency.
* **Credit**: all credit/refund transactions in that currency.
* **Balance**: debit minus credit in that currency.

### 2. Exporting data

The **Export** button (top right corner) downloads the data in XLSX format.

The export includes:

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (5).png" alt="Guide Sales Ledger export to XLSX"><figcaption><p>Export the filtered Guide Sales Ledger results to XLSX for accounting and reconciliation.</p></figcaption></figure>

* All displayed columns
* Raw values (no rounding)
* Totals per currency
* Filters applied

This file can be used for:

* Accounting
* Auditing

### Typical flow

{% stepper %}
{% step %}
### Select payment period

Choose the dates where the guide payments were registered.
{% endstep %}

{% step %}
### Narrow down filters

Filter by **Guide**, **Resort**, and **Payment method**.

Use **Allotment period** if you need to match a departure date range.
{% endstep %}

{% step %}
### Review transactions

Check debit/credit values, commission status, deposit status, and payment method.
{% endstep %}

{% step %}
### Expand extras

Open the details row to review connected extras, suppliers, and prices.
{% endstep %}

{% step %}
### Review totals

Validate that totals and balances match the expected settlement per currency.
{% endstep %}

{% step %}
### Export

Export to XLSX for bookkeeping and internal audit.
{% endstep %}
{% endstepper %}
