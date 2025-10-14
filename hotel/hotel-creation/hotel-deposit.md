# Hotel Deposit

#### **Overview**

The _Deposit_ section is used to manage and track deposit rules and payments between the hotel and the system. Deposits ensure that a financial commitment is secured for reservations and can be linked to invoices and repayment terms. This module provides an overview of all deposits, amounts, dates, and repayment status.

#### **Purpose**

* To record and manage hotel deposit agreements.
* To track payment dates, amounts, and repayment obligations.
* To connect deposits with invoices for proper financial reconciliation.
* To provide transparency on outstanding and completed financial obligations.

#### Fields and Explanations

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Filter Options (Top Section)**

1. **Deposit Date From / To**
   * Filters deposits by their effective start and end dates.
   * Useful for reviewing deposits in a specific period.
2. **Invoice Date From / To**
   * Filters by invoice issue dates.
   * Helps match deposits against issued invoices.
3. **Invoice No**
   * Search deposits linked to a specific invoice number.
4. **Display / Clear Buttons**
   * **Display** → Applies the chosen filters.
   * **Clear** → Resets filters to show all deposits.

***

**Deposits Table**

1. **Deposit Date -** The date the deposit is registered.
   * Example: _01-11-2025_.
2. **Payment Type -** The category of the deposit (e.g., _NormalDeposit_).
3. **Amount -** The value of the deposit for that entry.
   * Example: _500_.
4. **Total Amount -** Sum of deposits recorded.
   * Ensures visibility of the overall financial commitment.
5. **Payback Date - T**he date when the payment is made. At the final payment, the deposit is deducted from the hotel invoice, only if it's in the paid status.
   * Example: _30-11-2025_.
6. **Payback On -** The system field to indicate when repayment occurred (if applicable).
7. **Invoice No -** Links the deposit to a specific invoice, if one has been issued.
8. **Deduction -** Field where deductions from the deposit can be entered.
   * Used to record amounts subtracted for costs or adjustments.
9. **Delete (Trash Icon) -** Removes a deposit entry.
   * Use carefully, as financial records may need to be retained for audit purposes.

***

**Invoices Section (Bottom Table)**

1. **Date - D**ate of the invoice related to the deposit.
2. **Deposit Paid -** Amount paid by the customer as a deposit.
3. **Deposit Payback -** Amount refunded or adjusted back to the customer.
4. **Rest Payment -** Remaining balance to be paid after deducting deposit and adjustments.
5. **Invoice No -** Reference number of the linked invoice.
6. **Archived -** Indicates whether the invoice record is archived.
7. **Status -** Shows the current processing status of the invoice.

***

**Buttons & Options**

* **New Deposit** → Add a standard deposit entry.
* **New Special Deposit Rule** → Create a custom rule (e.g., different amounts, exceptions, or conditions).
* **Archived also (dropdown)** → Controls whether archived invoices are visible.

Deposits are paid at a date agreed upon in the contract between companies/agencies and creditors

A feature has been added: the **Special Deposit Rule**. It is used to pre-calculate the deposit amount for multiple deposit dates. It requires the allotments and costs of the rooms to be set in the hotel

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
