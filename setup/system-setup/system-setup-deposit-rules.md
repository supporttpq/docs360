---
description: >-
  Configure deposit amounts and payment deadlines for Tourpaq booking payment
  plans.
---

# System Setup – Deposit Rules

### Overview

**Deposit Rules** control payment amounts and deadlines for booking payment plans.

They work with [Payment Rate Rules](system-setup-payment-rate-rules.md). Payment Rate Rules define payment stages. Deposit Rules define their amounts and deadlines.

{% hint style="warning" %}
Changes apply to new bookings and can affect payment reminders, exports, and cash flow.

Validate changes with a test booking before using them in production.
{% endhint %}

### Requirements

Configure Deposit Rules only when these requirements are met:

* **Administrator** rights for **System Setup**.
* An approved payment structure in [Payment Rate Rules](system-setup-payment-rate-rules.md).
* Approved deposit amounts, percentages, and payment deadlines.
* A test booking for validation.

### Navigation

Open Deposit Rules:

1. In Tourpaq Office, open **Setup**.
2. Click **System Setup**.
3. Click **Deposit Rules**.

### Purpose

Use Deposit Rules to:

* Define the deposit as a fixed amount or a percentage.
* Set a second payment (optional) and its due date.
* Define the final payment deadline (relative to departure).
* Enable or disable rules without deleting them.
* Keep payment terms consistent across bookings.

### Interface overview

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (355).png" alt="Deposit Rules configuration showing booking dates, deposit amounts, payment due dates, the Disabled setting, and delete controls."><figcaption></figcaption></figure></div>

Each row defines a payment rule for bookings. The rule combines payment values, due dates, and activation status.

### Field descriptions

The configuration includes these fields:

| Field                    | Description                                                                               |
| ------------------------ | ----------------------------------------------------------------------------------------- |
| **Booking Date**         | The booking date the rule applies to.                                                     |
| **Deposit Value**        | Fixed deposit amount due at booking or by the **Deposit Due** date.                       |
| **Deposit Percentage**   | Deposit percentage of the booking total. This value is used instead of **Deposit Value**. |
| **Second Payment Value** | The amount required as the second payment, if applicable.                                 |
| **Disabled**             | Turns the rule off. Disabled rules are not applied to new bookings.                       |
| **Deposit Due**          | Days after booking when the deposit must be paid.                                         |
| **Second Payment Due**   | Days after booking when the second payment must be paid.                                  |
| **Last Payment Due**     | Days before departure when the final payment must be completed.                           |
| **Delete (Trash Icon)**  | Deletes the selected deposit rule. Deleted rules cannot be recovered.                     |

### Configuration workflow

Configure a deposit rule in this order:

1. Review existing rules for dates, values, due dates, and status.
2. Click **Create**.
3. Enter **Booking Date**.
4. Enter **Deposit Value** or **Deposit Percentage**.
5. Enter **Second Payment Value** when a second payment applies.
6. Set **Deposit Due**.
7. Set **Second Payment Due** when a second payment applies.
8. Set **Last Payment Due**.
9. Select **Disabled** when the rule should remain inactive.

To update an existing rule:

1. Open the rule row.
2. Update the required values.

To remove an existing rule:

1. Click the trash icon.
2. Confirm the deletion.

{% hint style="info" %}
Prefer disabling old rules over deleting them.

It keeps history clearer and avoids accidental loss.
{% endhint %}

### System behavior

Deposit Rules affect booking payment behavior in these ways:

* Tourpaq applies active rules to new bookings.
* **Disabled** rules do not apply to new bookings.
* **Deposit Percentage** calculates from the booking total.
* Changes to payment deadlines can affect reminders and financial exports.

### Examples

#### Percentage deposit

A booking uses a 20% deposit. Set **Deposit Percentage** to `20`. Set **Deposit Due** to the approved payment deadline.

#### Two-stage payment

A booking requires a deposit and second payment. Set **Second Payment Value** and **Second Payment Due**. Set **Last Payment Due** for the final balance.

#### Retiring a rule

An old payment plan must remain available for historical reference. Select **Disabled** instead of deleting the rule.

### Related settings

* [System Setup](./)
* [System Setup – Payment Rate Rules](system-setup-payment-rate-rules.md)
* [System Setup – General Information Settings](system-setup-general-information-settings.md)

### Troubleshooting

Check these items when payment behavior is unexpected:

* **Payments are not split as expected:** Check the configured [Payment Rate Rules](system-setup-payment-rate-rules.md).
* **The rule doesn’t apply to new bookings:** Ensure it is not **Disabled**, and confirm the **Booking Date** rule match.
* **Due dates look wrong:** Verify day offsets (after booking vs before departure).
