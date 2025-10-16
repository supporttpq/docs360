# Method of Payment

### **Overview**

The **Payment Types Module** is a core administrative and financial feature of the system, designed to manage and categorize all payment methods accepted within the platform. This module enables the insertion and classification of various **payment types**, ensuring consistent tracking and reporting of financial transactions across bookings, agents, and customers.

Each time a payment is recorded in the system, a **payment type** must be specified to indicate how the transaction was carried out (e.g., via bank transfer, card, online payment, etc.).

***

### **Purpose**

The purpose of this module is to:

* Define and maintain the list of accepted **payment types** in the system.
* Differentiate between **debit** and **credit** transactions for accurate accounting.
* Ensure traceability of all payments made by customers, agents, and guides.
* Identify and flag special types of payments (e.g., bank imports, gift cards).

***

### **Preconditions**

Before configuring or using the Payment Types Module, ensure the following:

* You have access rights as either an **Administrator** or **Financial** user role.
* You understand the financial flow within your department or company (i.e., which payment types are considered debit vs. credit).
* You are aware of any special or custom payment methods used by your organization (e.g., Dankort, Gift Cards, or imported payments).
* The accounting system or ERP (if integrated) is aligned with the same payment classification structure.

***

<figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Payment Type Categories**

There are two main categories of payments:

#### 1. **Debit Payments**

* Represent transactions where money is **received** by the company.

#### 2. **Credit Payments**

* Represent transactions where money is **given** or refunded.

***

### **Special Payment Types**

The following payment types should be specially categorized and identified due to their source or behavior:

| Special Payment Type       | Description                                                                |
| -------------------------- | -------------------------------------------------------------------------- |
| **Online Payments**        | Payments made directly through an integrated online payment gateway.       |
| **Imported Bank Payments** | Payments imported into the system from a bank file or automated sync.      |
| **Dankort Payments**       | Payments made using the Dankort card system (specific to certain markets). |
| **Guide Payments**         | Payments handled and received directly by the travel guide.                |
| **Agent Machine Payments** | Payments made using an agent’s card terminal or in-office POS device.      |
| **Gift Card Payments**     | Payments made using valid company-issued gift cards or vouchers.           |

These special payment methods may affect reporting, reconciliation, or automation and should be flagged accordingly.



### Create a new payment method

### **Overview**

This section explains how to define and insert a new **payment method** into the system. Each payment method determines how a financial transaction is recorded, processed, and reported—whether it's a cash payment, an online transaction, or an import from a bank file.

This process is **applicable for users with Administrator or Financial access**.

***

### **Purpose**

Creating a well-defined payment method ensures:

* Accurate financial tracking and categorization
* Compatibility with integrated systems like DIBS or banking imports
* Clear differentiation between debit (incoming) and credit (outgoing) payments
* Proper association with reporting accounts (credit and debit)

***

### **Preconditions**

Before creating a new payment method, ensure:

* You have **Administrator** or **Financial** permissions.
* You understand the nature of the payment method (cash, card, online, etc.).
* You have the required **accounting codes** (Credit and Debit accounts).
* You are aware of any **system integrations** that may affect the method (e.g., DIBS, bank import, Dankort).
* The payment method is **relevant to the company** you are currently working under in the system.

<figure><img src="../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Instructions: Create a New Payment Method**

1. **Navigate to**: `Admin Panel > Financial Settings > Payment Methods`
2. **Click** the **"Add New Payment Method"** button.
3.  **Fill in the following fields:**

    | **Field**                      | **Description**                                                                                       |
    | ------------------------------ | ----------------------------------------------------------------------------------------------------- |
    | **Payment Code**               | A short identifier for internal use (e.g., `VISA`, `BANK`, `CASH`).                                   |
    | **Payment Full Name**          | The user-friendly name (e.g., _Visa Card_, _Bank Transfer_, _Cash Payment_).                          |
    | **Type of Payment**            | Select **Debit** (money in) or **Credit** (money out).                                                |
    | **Credit Account**             | The accounting code to be credited during the transaction.                                            |
    | **Debit Account**              | The accounting code to be debited during the transaction.                                             |
    | **Is Online Payment?**         | Check this box if the payment is processed via an **online platform** (e.g., DIBS, Stripe).           |
    | **Used for Bank Imports?**     | Check if this method is used for **imported bank transactions**.                                      |
    | **Used for Dankort Payments?** | Check if this payment is made using a **Dankort card**.                                               |
    | **Used for Guide Payments?**   | Check if guides can **receive payments** using this method.                                           |
    | **Is Cash Payment?**           | Check if this method represents a **cash transaction**.                                               |
    | **Active**                     | Enable this option if the method should be **available for use** in bookings or financial operations. |

    > ⚠️ **Note**: If selecting **VISA** as the card type and the customer pays using a **Visa/Dankort** on the **DIBS** platform, DIBS will treat this as a **VISA** transaction. As a result, the payment will be registered using the **VISA** payment method in Tourpaq, not the Visa/Dankort method.


4. Other useful fields:

| Checkbox                                  | **Description**                                                                                                                                                                                                                                                                                                      |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Is GDPR Sensitive                         | Anonymize the payment **type** for a booking of an anonymized customer for users logged with other account than "Administrator" or "Financial"                                                                                                                                                                       |
| **"Pay from home" Payment**               | Allow to be used in the  Guide App for Extra Orders payments;                                                                                    ![](<../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)         |
| **Agent Machine Payment**                 | When checked, it allows guides to pay with the payment machine; ![](<../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)                                                                                                                                  |
| **Booking Gift Card Payment**             | When checked, it allows the gift card to be used for another agency besides the one for which it was created. (Used only  if "All brands" is selected for the giftcard); ![](<../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1).png>)                                     |
| **Booking Gift Card Own Agency Payments** | Allows the gift card to be used only with on your own agency payments (Used when the All brands checkbox it is used on the Giftcard)                                                                                                                                                                                 |

5. **Save** the new payment method.

It will be automatically associated with the **currently selected company** in the system.
