# System Setup – Deposit Rules

### Overview

Deposit Rules control **how much** customers must pay and **when** they must pay it.

Use them to set deposit amounts, optional second payments, and final payment deadlines.

Go to **Setup → System Setup → Deposit Rules**.

{% hint style="warning" %}
Changes apply to new bookings and can affect payment reminders, exports, and cash flow.

Test changes on a safe booking flow when possible.
{% endhint %}

### Purpose

Use Deposit Rules to:

* Define the deposit as a fixed amount or a percentage.
* Set a second payment (optional) and its due date.
* Define the final payment deadline (relative to departure).
* Enable/disable rules without deleting them.
* Keep payment terms consistent across bookings.

### Screenshot

<figure><img src="../../.gitbook/assets/image (355).png" alt=""><figcaption></figcaption></figure>

### Field descriptions

| Field                    | Description                                                                                                           |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------- |
| **Booking Date**         | The booking date the rule applies to.                                                                                 |
| **Deposit Value**        | Fixed deposit amount due at booking (or by the deposit due date).                                                     |
| **Deposit Percentage**   | Deposit percentage of the booking total (used instead of Deposit Value).                                              |
| **Second Payment Value** | The amount required as the second payment, if applicable.                                                             |
| **Disabled**             | Turns the rule off. Disabled rules are not applied to new bookings.                                                   |
| **Deposit Due**          | Days after booking when the deposit must be paid.                                                                     |
| **Second Payment Due**   | Days after booking when the second payment must be paid.                                                              |
| **Last Payment Due**     | Days before departure when the final payment must be completed.                                                       |
| **Delete (Trash Icon)**  | Allows administrators to delete a specific deposit rule. Use this with caution, as deleted rules cannot be recovered. |

### How to use

1. Go to **Setup → System Setup → Deposit Rules**.
2. Review existing rules (booking date, values, due dates, and status).
3. To create a rule, click **Create** and enter:
   * **Booking Date**
   * **Deposit Value** or **Deposit Percentage**
   * **Second Payment Value** (optional)
   * Due dates: **Deposit Due**, **Second Payment Due**, **Last Payment Due**
   * Set **Disabled** as needed
4. To edit a rule, open the rule row and update the values.
5. To delete a rule, click the trash icon and confirm.

{% hint style="info" %}
Prefer disabling old rules over deleting them.

It keeps history clearer and avoids accidental loss.
{% endhint %}

### Related settings

* [System Setup – Payment Rate Rules](system-setup-payment-rate-rules.md)
* [System Setup – General Information Settings](system-setup-general-information-settings.md)

### Troubleshooting

* **Payments are not split as expected:** Check the configured [Payment Rate Rules](system-setup-payment-rate-rules.md).
* **The rule doesn’t apply to new bookings:** Ensure it is not **Disabled**, and confirm the **Booking Date** rule match.
* **Due dates look wrong:** Verify day offsets (after booking vs before departure).

### FAQ

<details>

<summary><strong>What’s the difference between Deposit Rules and Payment Rate Rules?</strong></summary>

Deposit Rules define **amounts/percentages** and **due dates**.

Payment Rate Rules define **how many payments** are used (one, two, or three).

</details>

<details>

<summary><strong>Do changes apply to existing bookings?</strong></summary>

Typically, changes are intended for new bookings going forward.

Validate on a test booking and confirm your operational process before changing live rules.

</details>

<details>

<summary><strong>Should I use Deposit Value or Deposit Percentage?</strong></summary>

Use **Deposit Percentage** when the deposit should scale with the booking total.

Use **Deposit Value** when you want a fixed amount.

</details>

<details>

<summary><strong>What does “Last Payment Due” mean?</strong></summary>

It’s the number of days **before departure** when the final payment must be completed.

</details>

<details>

<summary><strong>Should I delete old rules?</strong></summary>

Usually no.

Disable old rules instead, unless you are sure you do not need them.

</details>
