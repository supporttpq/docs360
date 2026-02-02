# System Setup – Payment Rate Rules

### Overview

Payment Rate Rules define how a booking is split into one or more payments.

Use them to decide whether customers pay everything at once or in installments.

Go to **Setup → System Setup → Payment Rate Rules**.

{% hint style="warning" %}
Changes can impact your payment flow system-wide.

Validate changes on a test booking when possible.
{% endhint %}

### Purpose

Use payment rate rules to:

* Standardize how payments are split across bookings.
* Offer deposit-based and installment-based payments.
* Keep payment behavior consistent across brands and agencies.

### Configuration options

| **Rule Type**           | **Description**                                                                     |
| ----------------------- | ----------------------------------------------------------------------------------- |
| **Single-rate payment** | The full booking amount is paid in one payment.                                     |
| **Two-rate payments**   | The payment is split into a deposit and a final balance payment.                    |
| **Three-rate payments** | The payment is split into a deposit, a second payment, and a final balance payment. |

### How it works

* The **deposit** is collected at booking time, or by a defined due date.
* The **second payment** (if used) is due later, based on your policy.
* The **final balance** is due by the last payment deadline.

You typically configure **amounts/percentages** and **due dates** in related settings like [System Setup – Deposit Rules](system-setup-deposit-rules.md).

### Related settings

* [System Setup – Deposit Rules](system-setup-deposit-rules.md)
* [System Setup – General Information Settings](system-setup-general-information-settings.md)

### FAQ

<details>

<summary><strong>What’s the difference between Payment Rate Rules and Deposit Rules?</strong></summary>

Payment Rate Rules define **how many payments** a booking can have.

Deposit Rules define **how much** is due and **when** it’s due.

</details>

<details>

<summary><strong>When should I use three-rate payments?</strong></summary>

Use three-rate payments if you want a deposit, a mid-point payment, and a final balance.

This is common for longer lead-time bookings.

</details>

<details>

<summary><strong>Do these rules affect all brands and agencies?</strong></summary>

These settings are typically used as company-wide defaults.

If your setup varies by brand, validate the behavior per brand after changes.

</details>

<details>

<summary><strong>What should I test after changing a payment rate rule?</strong></summary>

Create a test booking and verify:

* Which payments are created (deposit/second/balance).
* Due dates and amounts/percentages.
* Any related emails, reminders, and exports.

</details>

<details>

<summary><strong>Why can’t I see or edit the due dates or percentages here?</strong></summary>

In many setups, due dates and amounts are configured in [System Setup – Deposit Rules](system-setup-deposit-rules.md) instead.

</details>
