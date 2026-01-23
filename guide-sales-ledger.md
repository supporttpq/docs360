# Guide Sales Ledger

The _Guide Sales Ledger_ provides an overview of all payments registered by guides during the selected period. The page consolidates all guide transactions, including debit, credit, commission status, and settlement status, making it easier to validate and reconcile guide-related financial activity.

This page is typically used by accounting teams, destination managers, and administrators responsible for guide settlements.

## **Overview**

The **Guide Sales Ledger** is a financial reporting module used to track and validate all payments, sales, and extras recorded by guides within a selected time period.\
It consolidates **debits, credits, extras sold, payment methods, resort activity, and guide performance** into a single interface.

This tool is essential for:

* Verifying guide transactions
* Reconciling amounts handed in by guides
* Checking extras sold per guide
* Tracking revenue per resort
* Auditing financial activity for a selected period

## **Purpose**

The purpose of the Guide Sales Ledger is to ensure:

* **Transparency** of every transaction registered by guides
* **Accuracy** of payments received, refunds, or outstanding balances
* **Consistency** between bookings and guide-reported payments
* **Support for accounting and commission validation**
* **Monitoring of guide performance and operational activity**

By understanding each field, a user can analyze financial data, detect errors, confirm sales, and communicate efficiently with guides and accounting staff.

## **Preconditions**

Before working with the Guide Sales Ledger, the following conditions must be met:

1.  You must have an **active Tourpaq user account** (admin or guide) with access to  Guide Sales Ledger.      - For an Admin user to have access to the Guide Sales Ledger menu, after this feature has been activated, a System Administrator must grant certain permissions in the User section, to the user who wants to have access to the feature. The Guide Sales Ledgedr activation permission is in the Finance menu.&#x20;

    <figure><img src=".gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>
2. Guide transactions (debit/credit entries) must already be added by the guides in the destination.
3. Bookings, extras, and supplier mappings must be configured correctly in the system.
4. You must know the **payment period** and **allotment period** you are reviewing.
5. Familiarity with basic financial terms (debit, credit, balance) is recommended.

## **How It Works**

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **1. Select Filters**&#x20;

Users can apply filters to narrow down results:

|                                 |                                                                                                                                                                    |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Payment Period                  | Defines when the payment was registered by the guide.                                                                                                              |
| <p></p><p>Allotment Period </p> | Optional filter matching payments with specific departure date ranges.                                                                                             |
| Guide                           | Select a specific guide or guide team.                                                                                                                             |
| Resorts                         | Limit the view to one or more resorts.                                                                                                                             |
| **Payment Methods**             | <p></p><p>The payment method used. Examples:</p><ul><li><strong>CHSING</strong> – Cash in guider</li><li><strong>OTHOUTG</strong> – Other refunds guider</li></ul> |
| **Display**                     | **Display** applies filters                                                                                                                                        |
| **Clear**                       | **Clear** resets all filters to default                                                                                                                            |

#### **Table Columns Explained**

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
| **Comm.**                  | Commited                                                                                                |
| **Dep.Paid**               | Deposit Paid                                                                                            |
| **Guide Payment Comments** | Any comments added by guide or system                                                                   |
| **Resort**                 | The resort where the payment was recorded                                                               |
| **M.O.User**               | Manual Overview User - the name of the user who handles negative extra orders, for credit transactions. |

#### **Row Details**

Each row can be expanded using the **▸** icon on the left.\
Expanded rows show the Connected Extras and information about it.

* Name of the extras
* Allotment date
* Number of the adults & children
* Price per adult & children
* Name of the Creditor
* Name of the Supplier

#### **Totals & Balances**

The **Sales Ledger** provides a consolidated financial overview of all debits, credits, and resulting balances grouped by currency. It helps users understand how much money has been charged (debit), refunded/credited (credit), and what the outstanding balance is for each currency and in total.

At the bottom of the page, totals are grouped by currency, and divided into three main categories repeated for each currency:

* **Debit -** Sum of all debit transactions across all currencies converted into the base currency. Debits usually represent **charges**, **invoices**, or **amounts the customer must pay**.
* **Credit -** Sum of all credits across all currencies, converted into the base currency. Credits usually represent **refunds**, **discounts**, or **payments received**.
* **Balance - Total Debit – Total Credit**, shown in the base currency. Represents the **overall outstanding balance**.

Each currency operates independently in its own ledger line.

#### Currency-Specific Fields

It shows the financial overview of all debits, credits and balances grouped by currency, each currency having the same field structure.

Example:

<table><thead><tr><th width="175.75">Currency</th><th width="182.5">Debit</th><th width="219">Credit</th><th>Ballance</th></tr></thead><tbody><tr><td>THB (Thai Baht)</td><td>All debit transactions recorded in THB.</td><td>All credits/refunds/payments recorded in THB</td><td>THB Debit – THB Credit (in THB).</td></tr><tr><td>DKK (Danish Krone)</td><td>Charges recorded in DKK</td><td>Payments/credits recorded in DKK</td><td>Calculated balance in DKK</td></tr><tr><td>EUR (Euro)</td><td>Charges recorded in Euro</td><td>Payments/credits in Euro.</td><td>Balance remaining in Euro</td></tr></tbody></table>

### **2. Exporting Data**

The **Export** button (top right corner) downloads the data in XLSX format.

The export includes:

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* All displayed columns
* Raw values (no rounding)
* Totals per currency
* Filters applied

This file can be used for:

* Accounting
* Auditing

## **Typical Flow for Using the Guide Sales Ledger**

A simple workflow to follow:

### **Step 1 — Select Payment Period**

Choose the dates where the guide payments were recorded.

### **Step 2 — Narrow Down Filters**

Filter by:

* Guide
* Resort
* Payment Method
* Allotment Period (optional)

### **Step 3 — Review Transactions**

Check:

* Debit and credit values
* Commission status
* Deposit status
* Payment method

### **Step 4 — Expand Extras**

Show more financial details of the Extra(s) by opening the details row.

### **Step 5 — Review Totals**

Validate that:

* Totals match guides' delivered
* Balances are consistent with reports

### **Step 6 — Export**

Use the **Export** button for:

* Bookkeeping
* Internal audit
