# Economics

### **Overview**

The **Economics** section provides a comprehensive financial summary and transaction tools for a selected booking. It displays **payment stages, due dates, refund options**, and **booking metadata** such as internet access credentials, update history, and account data. Additionally, it serves as a gateway to initiate payments through various methods.

***

### **Purpose**

This section helps users:

* Track all stages of booking payment (deposit, second payment, rest).
* Monitor due dates and current payment statuses.
* Record cancellation and update history.
* Access customer account and registration information.
* Process payments via **card, gift card, or cash**.
* Enable refunds through the **release payment** option.

***

### **Preconditions**

Before using this section:

* The booking must exist and be open (unless reviewing cancellation data).
* The user must have permission to **view financial data** and **process payments**.
* Customer account must be assigned during booking creation or updated manually.
* Payments methods must be configured in the system (for the new window payment form to function).

***

### **Instructions & Field Descriptions**

***

### 💳 **Payment Breakdown**

The payment process is divided into three stages:

| Field                | Description                                        |
| -------------------- | -------------------------------------------------- |
| **Deposit to pay**   | The total deposit amount required for the booking. |
| **Deposit paid**     | The amount already paid from the deposit.          |
| **Deposit due date** | The deadline for paying the full deposit.          |

| Field                       | Description                                  |
| --------------------------- | -------------------------------------------- |
| **Second payment to pay**   | The required second payment (if applicable). |
| **Second payment paid**     | The amount received from the second payment. |
| **Second payment due date** | The deadline for the second installment.     |

| Field                        | Description                                    |
| ---------------------------- | ---------------------------------------------- |
| **Rest of payment to pay**   | Remaining balance after previous installments. |
| **Rest of payment paid**     | Amount paid toward the remaining balance.      |
| **Rest of payment due date** | Deadline to finalize the rest of the payment.  |

***

### 💸 **Release Payment**

* A checkbox or action to **allow money to be returned to the customer** (typically used in cancellation scenarios or manual refund cases).
* Once enabled, it marks the booking as **eligible for refund** through the system.

***

### 🌐 **Other Financial and Metadata Fields**

| Field                 | Description                                                                           |
| --------------------- | ------------------------------------------------------------------------------------- |
| **Internet Password** | Temporary password generated for the customer to log into the **web booking portal**. |
| **Cancellation Date** | The official cancellation date, shown only if the booking has been canceled.          |

***

### 🕓 **Last Booking Update Info**

This block provides traceability by showing:

* **Username** of the last person who modified the booking.
* **Date** of the last update.
* **Time** (hour and minute) of the last update.

***

### 🏢 **Customer & Accounting Information**

| Field                            | Description                                                                |
| -------------------------------- | -------------------------------------------------------------------------- |
| **Branch (Registration Number)** | ID representing the agency branch that registered the booking.             |
| **Account (Customer Account)**   | Internal account reference used for payment tracking and customer records. |

***

### 💵 **Payment Actions**

At the bottom or side of the section, you will find **links/buttons** for processing payments. These open a **new window** or modal to complete the transaction securely.

#### Available Payment Methods:

* **Card** – Credit or debit card transactions.
* **Gift Card** – Apply a gift voucher code.
* **Cash** – Manual recording of a physical cash payment.

> 🧩 _Note: These links rely on system configuration and open a secure pop-up for completing the transaction. Ensure pop-ups are not blocked in your browser._

***

#### ✅ Best Practices

* Always verify due dates before initiating payment.
* If refunding, confirm with a supervisor before activating **release payment**.
* Ensure the customer's email and phone are updated to avoid web access issues.
* Use the **update history** to trace who made changes in case of issues.

<figure><img src="https://sonat.com/api/Document/Image/19670ef0-8b8a-4cda-8eb6-249681e07016/60a72aeb-a272-4428-a118-b6074b1b35b5/055f9e6a-1e8f-4b00-a685-f03c27defc33.webp?width=1864" alt="" width="900"><figcaption></figcaption></figure>
