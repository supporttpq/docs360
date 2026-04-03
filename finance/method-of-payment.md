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
* [Payment File Import](payment-file-import/)
* [Refund File Import](refund-file-import.md)

Common examples:

* Bank transfer payments (bank import)
* Card and online payments (for example DIBS)
* Cash payments
* Gift card payments
* Refund payment methods (credit)

***

### Purpose

The Method of Payment module defines, controls, and governs all payment types used within Tourpaq Office Finance. This documentation establishes standardized procedures for creating, maintaining, and reviewing payment methods to ensure:

* Accurate financial classification and reporting
* Compliance with internal controls, accounting standards, and regulatory requirements
* Proper segregation of duties
* Consistent handling of payments across bookings, guides, agents, and integrations
* Reliable reconciliation and auditability

This document forms part of the organization’s financial control framework.

***

### Preconditions

Before configuring payment methods, ensure the following:

* You have access rights as either an **Administrator** or **Financial** user role.
* You understand the financial flow within your department or company (i.e., which payment types are considered debit vs. credit).
* You are aware of any special or custom payment methods used by your organization (e.g., Dankort, Gift Cards, or imported payments).
* The accounting system or ERP (if integrated) is aligned with the same payment classification structure.

***

![Method of Payment (payment types) list](<../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

_Payment methods (payment types) define how payments are recorded and reported in Tourpaq Office._

## **Responsibilities**

#### **Roles**

| Role                             | Responsibilities                                                                                  |
| -------------------------------- | ------------------------------------------------------------------------------------------------- |
| **Administrator**                | Create, modify, deactivate payment methods; assign accounting codes; configure integration flags. |
| **Financial User**               | Validate accounting mappings; review payment method usage; support reconciliation.                |
| **Finance Manager / Controller** | Approve creation or modification of payment methods; ensure alignment with accounting policies.   |
| **Internal Audit / Compliance**  | Periodically review configuration, access rights, and audit trails.                               |

#### **Approval Workflow**

All changes to payment methods must follow this workflow:

1. **Request** submitted by Administrator or Financial User
2. **Review** by Finance Manager
3. **Approval** documented and stored (ticket, email, or change log)
4. **Implementation** by Administrator
5. **Post‑implementation validation** by Financial User

No payment method may be created or modified without documented approval.

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

![Create a new payment method form](<../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

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

## **Integration & Automation Controls**

#### **Online Payment Gateways**

Payment methods flagged as online must:

* Match gateway configuration
* Use correct accounting codes
* Be tested before activation

#### **Bank Imports**

Payment methods used for bank imports must:

* Match bank file codes
* Support reconciliation rules
* Be validated during monthly close

#### **Error Handling**

Any failed import or mismatched payment type must be:

1. Logged
2. Investigated
3. Corrected
4. Documented

## **Deactivation of Payment Methods**

A payment method may be deactivated only when:

* It is no longer used operationally
* All open transactions are resolved
* Finance Manager approves deactivation
* Audit logs capture the change

Deactivated methods must remain visible for audit purposes but unavailable for new transactions.
