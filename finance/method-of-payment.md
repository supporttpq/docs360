---
description: >-
  Configure payment methods (payment types) in Tourpaq Office Finance. Set
  debit/credit, online payment, bank import, gift card, and guide payment flags
  for correct reporting and reconciliation.
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

# Method of Payment

### Overview

**Method of Payment** (also called **Payment Types**) is where you manage the **payment methods** used across Tourpaq Office Finance.

Every payment in Tourpaq uses a **payment code** (payment type). This controls how transactions are tracked for **reporting**, **reconciliation**, and imports.

Related modules:

* [Payment Registration](payment-registration.md)
* [Payment File Import](payment-file-import.md)
* [Refund File Import](refund-file-import.md)

Common examples:

* Bank transfer payments (bank import)
* Card and online payments (for example DIBS)
* Cash payments
* Gift card payments
* Refund payment methods (credit)

***

### Purpose

The purpose of this module is to:

* Define and maintain the list of accepted **payment methods** (payment types).
* Separate **debit** (money in) from **credit** (money out / refund).
* Support automation like **bank payment import** and online payment flows.
* Keep payments consistent across bookings, guides, and exports.

***

### Preconditions

Before configuring payment methods, ensure the following:

* You have access rights as either an **Administrator** or **Financial** user role.
* You understand the financial flow within your department or company (i.e., which payment types are considered debit vs. credit).
* You are aware of any special or custom payment methods used by your organization (e.g., Dankort, Gift Cards, or imported payments).
* The accounting system or ERP (if integrated) is aligned with the same payment classification structure.

***

![Method of Payment (payment types) list](<../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

_Payment methods (payment types) define how payments are recorded and reported in Tourpaq Office._

### Payment type categories

There are two main categories of payments:

#### 1. Debit payments

* Represent transactions where money is **received** by the company.

#### 2. Credit payments

* Represent transactions where money is **given** or refunded.

***

### Special payment types

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

#### Overview

This section explains how to define and insert a new **payment method** into the system. Each payment method determines how a financial transaction is recorded, processed, and reported—whether it's a cash payment, an online transaction, or an import from a bank file.

This process is **applicable for users with Administrator or Financial access**.

***

#### Purpose

Creating a well-defined payment method ensures:

* Accurate financial tracking and categorization
* Compatibility with integrated systems like DIBS or banking imports
* Clear differentiation between debit (incoming) and credit (outgoing) payments
* Proper association with reporting accounts (credit and debit)

***

#### Preconditions

Before creating a new payment method, ensure:

* You have **Administrator** or **Financial** permissions.
* You understand the nature of the payment method (cash, card, online, etc.).
* You have the required **accounting codes** (Credit and Debit accounts).
* You are aware of any **system integrations** that may affect the method (e.g., DIBS, bank import, Dankort).
* The payment method is **relevant to the company** you are currently working under in the system.

![Create a new payment method form](<../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

_Create a payment method with a payment code, debit/credit type, and flags for online payments and imports._

### Instructions: Create a new payment method

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

{% hint style="danger" %}
**Note**: If selecting **VISA** as the card type and the customer pays using a **Visa/Dankort** on the **DIBS** platform, DIBS will treat this as a **VISA** transaction. As a result, the payment will be registered using the **VISA** payment method in Tourpaq, not the Visa/Dankort method.
{% endhint %}

4. Other useful fields:

| Checkbox                                  | **Description**                                                                                                                            |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Is GDPR Sensitive                         | Anonymize the payment **type** on anonymized customers for users with a role other than **Administrator** or **Financial**.                |
| **"Pay from home" payment**               | Allow this payment method in the **Guide App** for Extra Orders payments.                                                                  |
| **Agent machine payment**                 | Allow guides to register payments using a payment terminal (POS).                                                                          |
| **Booking gift card payment**             | Allow the gift card to be used for an agency other than the one it was created for (used when **All brands** is enabled on the gift card). |
| **Booking gift card own agency payments** | Allow the gift card to be used only for your own agency payments (used when **All brands** is enabled on the gift card).                   |

#### Checkbox screenshots

![Pay from home payment checkbox](<../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

_“Pay from home” payment: enable the method for Guide App Extra Orders payments._

![Agent machine payment checkbox](<../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

_Agent machine payment: enable the payment terminal (POS) option for guides._

![Booking gift card payment checkbox](<../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1).png>)

_Booking gift card payment: allow gift cards across agencies when All brands is enabled._

5. **Save** the new payment method.

It will be automatically associated with the **currently selected company** in the system.
