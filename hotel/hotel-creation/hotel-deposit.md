---
description: Manage hotel deposits and payback against invoices.
---

# Hotel Deposit

### Overview

The **Deposit** section tracks deposit agreements with a hotel supplier.

It helps you register deposits, link them to invoices, and track payback/deductions.

Where to find it: **Hotel → Deposit**.

### Purpose

* To record and manage hotel deposit agreements.
* To track payment dates, amounts, and repayment obligations.
* To connect deposits with invoices for proper financial reconciliation.
* To provide transparency on outstanding and completed financial obligations.

### Screen overview

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Filters (top section)

1. **Deposit Date From / To**
   * Filters deposits by their effective start and end dates.
   * Useful for reviewing deposits in a specific period.
2. **Invoice Date From / To**
   * Filters by invoice issue dates.
   * Helps match deposits against issued invoices.
3. **Invoice No**
   * Searches deposits linked to a specific invoice number.
4. **Display / Clear**
   * **Display** → Applies the chosen filters.
   * **Clear** → Resets filters to show all deposits.

***

#### Deposits table

1. **Deposit Date** – The date the deposit is registered.
   * Example: _01-11-2025_.
2. **Payment Type** – The deposit type (for example, _NormalDeposit_).
3. **Amount** – The amount for this deposit entry.
   * Example: _500_.
4. **Total Amount** – Total of all deposit entries in the list.
5. **Payback Date** – Planned payback date.
   * On the final payment, the deposit can be deducted from the hotel invoice.
   * The deposit must be in **Paid** status.
   * Example: _30-11-2025_.
6. **Payback On** – Actual payback date/time (set when payback happens).
7. **Invoice No** – Links the deposit to a specific invoice (if available).
8. **Deduction** – Amount deducted from the deposit (costs, corrections, adjustments).
9. **Delete (trash icon)** – Deletes the deposit entry.

{% hint style="warning" %}
Be careful with deletions. Your accounting or audit process may require keeping deposit history.
{% endhint %}

***

#### Invoices section (bottom table)

1. **Date** – Invoice date linked to the deposit.
2. **Deposit Paid** – Amount paid by the customer as a deposit.
3. **Deposit Payback** – Amount refunded or adjusted back to the customer.
4. **Rest Payment** – Remaining balance to be paid after deducting deposit and adjustments.
5. **Invoice No** – Reference number of the linked invoice.
6. **Archived** – Indicates whether the invoice record is archived.
7. **Status** – Shows the current processing status of the invoice.

***

#### Actions

* **New Deposit** → Add a standard deposit entry.
* **New Special Deposit Rule** → Create multiple deposit dates and amounts from a rule.
* **Archived also (dropdown)** → Controls whether archived invoices are visible.

### How it works (typical flow)

1. Agree deposit terms with the hotel supplier (date, amount, payback logic).
2. Register the deposit with **New Deposit** (or use **New Special Deposit Rule**).
3. Link the deposit to the relevant invoice when available.
4. When final payment is processed, the deposit can be deducted from the hotel invoice.

Deposits are typically paid on the date agreed in the supplier contract.

### Special Deposit Rule

Use **Special Deposit Rule** to pre-calculate deposit amounts across multiple deposit dates.

Prerequisites:

* Room **allotments** are set for the hotel.
* Room **costs** are set for the hotel.

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### FAQ

**Q: What’s the difference between “Payback Date” and “Payback On”?**\
**A:** **Payback Date** is the planned date. **Payback On** is the actual date/time when it happened.

**Q: Why isn’t the deposit deducted from the hotel invoice?**\
**A:** The deposit must be in **Paid** status. The deduction happens on the final payment run.

**Q: I created a Special Deposit Rule, but the amounts look wrong. Why?**\
**A:** The rule uses the hotel’s room allotments and room costs. Missing data changes the calculation.

**Q: What does “Archived also” do?**\
**A:** It toggles whether archived invoices appear in the invoice list at the bottom.

**Q: Can I delete a deposit entry?**\
**A:** Yes, via the trash icon. Confirm your internal audit/accounting requirements first.
