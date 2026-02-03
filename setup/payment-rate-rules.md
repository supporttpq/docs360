# Payment rate rules

### Overview

Payment rate rules control **when** customers must pay and **how much** is due at each step.

They usually split the total into:

* a **deposit** (first payment)
* a **second payment**
* a **final payment** (the rest)

### Main fields (what they mean)

* **Deposit value**
  * The deposit amount per passenger.
* **Deposit percentage**
  * If set, the deposit can be calculated as a percentage of the base price.
  * Base price means “without extras and supplements”.
  * Note: payment simulation uses the **deposit value**.
* **Second payment value**
  * A fixed amount due as the second payment (if used in your setup).
* **Deposit due**
  * How many days after booking the deposit must be paid.
* **Second payment due**
  * How many days before departure the second payment must be paid.
* **Last payment due**
  * How many days before departure the final payment must be paid.

### Exception rules (when dates are too close) <a href="#exception-rules" id="exception-rules"></a>

Sometimes the trip is booked close to the departure date. In those cases, Tourpaq moves payment due dates forward to avoid impossible deadlines.

The simplified logic is:

* If departure is **within 3 days** of booking:
  * second and final payments are due **immediately** (same day as booking).
* If departure is **within 14 days** of booking:
  * second and final payments are due **1 day after booking**.
* Otherwise, if the planned second/final payment would be due **before** the deposit deadline:
  * second and final payments are due **2 days after booking**.

Tourpaq also enforces the correct order of payments:

* The second payment due date cannot be earlier than the deposit due date.
* The final payment due date cannot be earlier than the second payment due date.

{% hint style="info" %}
**Note:** the deposit value will be higher since the Cancellation Insurance will also be included, and certain products may be set to be paid within the deposit payment.
{% endhint %}

### Keeping old rules for past bookings (date intervals)

Tourpaq can store a “history” of deposit rules by booking date.

This is useful when deposit levels change by season. If you later update an older booking, Tourpaq can recalculate using the rule that applied for that booking period.

Key points:

* The current default deposit and due dates come from the main fields (shown as **#1** in the screenshots).
*   The **Deposit rules** tab lets you add older default deposit values for earlier booking periods.

    * **Please note!** If we enter a rule today, it will automatically set the rule with today's date.

    <figure><img src="../.gitbook/assets/image (30) (1).png" alt=""><figcaption><p>#1 / #2</p></figcaption></figure>

    <figure><img src="../.gitbook/assets/image (31) (1).png" alt=""><figcaption></figcaption></figure>

How the rules apply:

* Bookings made **up to and including today** follow the relevant rule in the list (**#3**).
* Bookings made **from tomorrow** use the current default values (**#1**).
* You can have multiple rules covering different booking date intervals.

<figure><img src="../.gitbook/assets/image (32) (1).png" alt=""><figcaption><p>#3</p></figcaption></figure>

{% hint style="info" %}
Deposit history is available for the company default rules.
{% endhint %}

### What can override the company default

The company default can be overridden by:

* **Agency-specific** deposit rules:

<figure><img src="../.gitbook/assets/image (33) (1).png" alt=""><figcaption></figcaption></figure>

* **Transport-specific** payment rules (overrides both company and agency):

<figure><img src="../.gitbook/assets/image (34) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
History for past deposit values is not currently supported for agency and transport rules.
{% endhint %}

### FAQ

<details>

<summary><strong>What is the difference between deposit value and deposit percentage?</strong></summary>

**Deposit value** is a fixed amount per passenger.

**Deposit percentage** can calculate the deposit as a percentage of the base price.

</details>

<details>

<summary><strong>Why did Tourpaq move the payment due dates?</strong></summary>

Because the trip was booked close to departure.

Tourpaq avoids due dates that fall before the booking date or before the deposit deadline.

</details>

<details>

<summary><strong>Why is the deposit higher than expected?</strong></summary>

Some items can be included in the deposit.

For example, cancellation insurance and certain products may be required in the first payment.

</details>

<details>

<summary><strong>Do agency or transport rules also support “history” by date?</strong></summary>

Not currently.

Only the company default deposit rules support history by booking date intervals.

</details>

<details>

<summary><strong>Which rule is used if there are company, agency, and transport rules?</strong></summary>

Tourpaq uses the most specific rule:

* Transport rule overrides agency and company.
* Agency rule overrides company.
* Company rule is the fallback.

</details>

<details>

<summary><strong>What does “Deposit due / Second payment due / Last payment due” measure?</strong></summary>

They are deadlines measured in days.

* **Deposit due** is counted from the booking date.
* **Second payment due** and **Last payment due** are counted back from the departure date.

</details>

<details>

<summary><strong>What is the “booking date” used in these rules?</strong></summary>

It is the booking date shown on the booking in Tourpaq.

If you are unsure, open a booking and check the booking date there.

</details>

<details>

<summary><strong>Does a customer have to pay exactly on the due date?</strong></summary>

No. The due date is a deadline.

Customers can usually pay earlier.

</details>

<details>

<summary><strong>Can we use deposit + final payment only (no second payment)?</strong></summary>

Yes, in many setups.

Set the second payment value to `0` (or leave it unused), then verify with a test booking that the plan looks as expected.

</details>

<details>

<summary><strong>What happens if we change the booking (passengers, extras, or dates)?</strong></summary>

Tourpaq can recalculate the payment plan.

Always re-check the payment plan after you save changes, especially when you change passengers or travel dates.

</details>

<details>

<summary><strong>Why does “Deposit percentage” not match what the customer sees?</strong></summary>

Some setups calculate the deposit from a percentage, but still show or simulate payments using the deposit value.

If you use deposit percentage, test a booking end-to-end to confirm the amounts shown to the customer.

</details>

<details>

<summary><strong>How can I test new payment rules safely?</strong></summary>

Use a staging/test environment if you have one.

Create a test booking with:

* a departure date far in the future
* a departure date within 14 days
* a departure date within 3 days

Then confirm the due dates match the exception rules.

</details>
