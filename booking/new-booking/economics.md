# Economics

### Overview

The **Economics** section provides a comprehensive financial summary and transaction tools for a selected booking. It displays **payment stages, due dates, refund options**, and **booking metadata** such as internet access credentials, update history, and account data. Additionally, it serves as a gateway to initiate payments through various methods.

***

### Purpose

This section helps users:

* Track all stages of booking payment (deposit, second payment, rest).
* Monitor due dates and current payment statuses.
* Record cancellation and update history.
* Access customer account and registration information.
* Process payments via **card, gift card, or cash**.
* Enable refunds through the **release payment** option.

***

### Preconditions

Before using this section:

* The booking must exist and be open (unless reviewing cancellation data).
* The user must have permission to **view financial data** and **process payments**.
* A customer account should be assigned during booking creation or updated manually.
* Payment methods must be configured in the system (for the payment window to function).

***

### Using Economics

#### Payment breakdown

The payment process is typically divided into up to three stages.

**Deposit**

| Field                | Description                                        |
| -------------------- | -------------------------------------------------- |
| **Deposit to pay**   | The total deposit amount required for the booking. |
| **Deposit paid**     | The amount already paid from the deposit.          |
| **Deposit due date** | The deadline for paying the full deposit.          |

**Second payment**

| Field                       | Description                                  |
| --------------------------- | -------------------------------------------- |
| **Second payment to pay**   | The required second payment (if applicable). |
| **Second payment paid**     | The amount received from the second payment. |
| **Second payment due date** | The deadline for the second instalment.      |

**Rest of payment**

| Field                        | Description                                   |
| ---------------------------- | --------------------------------------------- |
| **Rest of payment to pay**   | Remaining balance after previous instalments. |
| **Rest of payment paid**     | Amount paid toward the remaining balance.     |
| **Rest of payment due date** | Deadline to finalize the rest of the payment. |

These values are usually calculated from the **payment rules** configured for the Brand (deposit rules, payment rate rules, etc.).

***

#### Release payment

* A checkbox or action to **allow money to be returned to the customer** (typically used in cancellation scenarios or manual refund cases).
* Once enabled, it marks the booking as **eligible for refund** through the system.
* Actual refund posting is handled via your normal **Payment Registration** or finance process.

***

#### Other financial and metadata fields

| Field                 | Description                                                                           |
| --------------------- | ------------------------------------------------------------------------------------- |
| **Internet password** | Temporary password generated for the customer to log into the **web booking portal**. |
| **Cancellation date** | The official cancellation date, shown only if the booking has been cancelled.         |

***

#### Last booking update info

This block provides traceability by showing:

* **Username** of the last person who modified the booking.
* **Date** of the last update.
* **Time** (hour and minute) of the last update.

Use this to identify who changed payment terms, due dates, or other financial details.

***

#### Customer & accounting information

| Field                            | Description                                                                |
| -------------------------------- | -------------------------------------------------------------------------- |
| **Branch (registration number)** | ID representing the agency branch that registered the booking.             |
| **Account (customer account)**   | Internal account reference used for payment tracking and customer records. |

These values are important for finance and reporting, especially when exporting data or reconciling payments.

***

#### Payment actions

In the Economics area you will find **links/buttons** for processing payments. These open a **new window** or modal to complete the transaction securely.

**Available payment methods**

* **Card** – Credit or debit card transactions.
* **Gift card** – Apply a gift voucher code.
* **Cash** – Manual recording of a physical cash payment.

> Note: These links rely on system configuration and open a secure pop‑up for completing the transaction. Ensure pop‑ups are not blocked in your browser.

***

#### Other fields and actions

* **Web Booking** – Redirects to the web booking page for the selected booking/customer.
* **Save** – Saves the information and changes made in the **Economics** tab.

***

#### Best practices

* Always verify **due dates** before initiating a payment or promising anything to the customer.
* If refunding, confirm with a supervisor before activating **Release payment**.
* Ensure the customer's **email** and **phone** are updated to avoid web access issues (e.g. for Internet password use).
* Use the **last update info** to trace who made financial changes if there are questions or disputes.

<figure><img src="https://sonat.com/api/Document/Image/19670ef0-8b8a-4cda-8eb6-249681e07016/60a72aeb-a272-4428-a118-b6074b1b35b5/055f9e6a-1e8f-4b00-a685-f03c27defc33.webp?width=1864" alt=""><figcaption></figcaption></figure>

***

### FAQ

#### 1. Why are some payment fields (second payment or rest) empty or zero?

This usually means that the **payment rules** for the Brand only define certain stages (for example, only **deposit + rest**, without a second payment). It can also happen if:

* The booking is fully paid and remaining stages are no longer relevant, or
* The payment rules were changed after the booking was created.

Check your Brand’s **deposit rules** and **payment rate rules** if the structure looks unexpected.

#### 2. Can I edit due dates and amounts directly in Economics?

Depending on your permissions, you may be able to adjust **due dates** or **amounts**. Keep in mind:

* Changes here can affect reminders, exports, and financial reporting.
* Your organisation may require that changes to payment structure are approved or only done by finance.

Always follow internal procedures before changing payment terms.

#### 3. What does “Release payment” actually do?

**Release payment** marks the booking as **eligible for refund**. It does **not** automatically send money back to the customer. You still need to:

* Register the refund in **Payment Registration** (or your payment provider), and
* Follow your internal refund workflow.

Use this flag when you intend to return money, for example after cancellations handled under your cancellation rules.

#### 4. I cannot open the card payment window – what should I check?

If the card payment window does not open:

* Make sure your browser allows **pop‑ups** from Tourpaq.
* Confirm that **payment methods** are correctly configured for the Brand.
* Check if there are any **ad‑blockers** or browser extensions blocking the window.

If the issue persists, contact your internal IT/support to check the payment configuration.

#### 5. How does Economics relate to Payment Registration and Finance?

* **Economics** shows the **planned** payment structure and current status for an individual booking.
* **Payment Registration** and finance tools handle the **actual posting** of payments, imports, and refunds.

If there is a mismatch between Economics and financial reports, verify:

* That all payments and refunds are correctly registered, and
* That the booking’s payment structure (deposit, second, rest) matches your company’s payment rules.
