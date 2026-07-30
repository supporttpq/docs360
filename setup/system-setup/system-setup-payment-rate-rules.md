# System Setup – Payment Rate Rules

### Overview

**Payment Rate Rules** define how Tourpaq splits a booking into payments.

They control whether a booking uses one, two, or three payment stages.

They work with [Deposit Rules](system-setup-deposit-rules.md), which define payment amounts and deadlines.

### Requirements

* Access to **System Setup** is required.
* A test booking is recommended before changing live payment behavior.

### Navigation

In Tourpaq Office, go to **Setup → System Setup → Payment Rate Rules**.

{% hint style="warning" %}
Changes can impact your payment flow system-wide.

Validate changes on a test booking when possible.
{% endhint %}

### Purpose

Use payment rate rules to:

* Define the number of payment stages for each booking.
* Support full payments, deposits, and installments.
* Keep payment behavior consistent across brands and agencies.

### Configuration options

The available payment structures are:

| **Rule Type**           | **Description**                                                                     |
| ----------------------- | ----------------------------------------------------------------------------------- |
| **Single-rate payment** | The full booking amount is paid in one payment.                                     |
| **Two-rate payments**   | The payment is split into a deposit and a final balance payment.                    |
| **Three-rate payments** | The payment is split into a deposit, a second payment, and a final balance payment. |

### How it works

Payment Rate Rules use these payment stages:

* A **deposit** is collected at booking time or by its due date.
* A **second payment** is optional and follows the deposit.
* A **final balance** is due by the final payment deadline.

Configure payment amounts, percentages, and due dates in [Deposit Rules](system-setup-deposit-rules.md).

### Configuration workflow

Configure payment behavior in this order:

1. In **Payment Rate Rules**, select the required payment structure.
2. In [Deposit Rules](system-setup-deposit-rules.md), define amounts or percentages.
3. Set the deposit, second-payment, and final-payment due dates.
4. Create a test booking and validate the payment schedule.

### Examples

#### Single-rate payment

A customer pays the full booking amount in one payment.

#### Two-rate payments

A customer pays a deposit, then the remaining balance.

#### Three-rate payments

A customer pays a deposit, a second payment, and the remaining balance.

### Related settings

* [Deposit Rules](system-setup-deposit-rules.md)
* [General Information Settings](system-setup-general-information-settings.md)
