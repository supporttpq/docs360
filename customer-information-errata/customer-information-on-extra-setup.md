# Customer Information on Extra setup

{% hint style="info" %}
**How to access:** **Extras Setup → Extras** → open an extra → **Passengers Information**.

Use this area to add **customer information / errata** for an extra, optionally limited by travel dates and booking dates.
{% endhint %}

### Overview

You can add **Passenger Information** rules to an **extra** so that important messages are shown during booking (and in some setups on documents).

Typical use cases:

* Important conditions or restrictions for an excursion/transfer
* What’s included/not included in an extra
* Meeting point / meeting time information
* Mandatory terms the customer must acknowledge before the booking can be completed

***

### Step-by-step: add customer information to an extra

#### 1) Open the Extras list

1. Go to **Extras Setup → Extras**.
2. Find the extra you want to edit.

#### 2) Open the extra and go to **Passengers Information**

1. Click the extra.
2. Open the **Passengers Information** tab.

On this tab you’ll see:

* A list of existing entries (or **There are no entries to show** if none exist)
* Pagination (25 rows per page)
* Entries sorted with the newest first
* Actions per entry: **Edit** and **Delete**
* A **Default text** tab
* Brand tabs (only for brands where **Use custom text** is enabled)

***

### Create a new rule

#### 3) Click **Create**

A new editable row opens with **Save** and **Cancel**.

#### 4) Fill in the fields

* **From / To (Departure date interval)** _(required)_
  * Defines when the message applies based on travel dates.
  * **To** must be later than **From**.
* **Booking Date From / To** _(optional)_
  * Limits the message to bookings created in a specific booking period.
  * Leave empty if booking date should not matter.
* **Information for customer on ticket** _(required)_
  * The message text (opens in a pop-up editor; multi-line supported).
* **Acknowledge**
  * If enabled, the message becomes mandatory to confirm in the booking flow (tooltip explains the behavior).

#### 5) Click **Save**

* If validation passes, the entry is saved and a success message is shown.
* If validation fails, you’ll see a warning and the entry will not be saved.

#### 6) Click **Cancel** (optional)

Discards the new row without saving.

***

### Manage existing rules

#### Edit

1. Click **Edit** on the entry.
2. Update the fields.
3. Click **Save**.

#### Delete

1. Click **Delete**.
2. Confirm in the dialog.

***

### Brand-specific text (override per brand)

If a brand has **Use custom text** enabled, it appears as its own tab.

* **Default text** is the baseline rule.
* On a **brand tab**, you typically only edit the **message text** (not the date logic).

***

### Validation rules (important)

* **To** must be later than **From**.
* The system prevents conflicting rules by checking for **overlaps**.
  * If you don’t use booking dates, the system compares against rules where booking dates are also empty.
  * If you use booking dates, the system compares against rules with booking-date limits.

If you need different messages, split the travel period into **non-overlapping** ranges.

***

### Notes

* Entries apply across brands unless a brand-specific text overrides the default.
* Booking dates are optional but useful when the message depends on when the booking was created.
* Use **Acknowledge** only when you truly want to block booking completion until the message is confirmed.

***

### FAQ

<details>

<summary><strong>What does “Acknowledge” do?</strong></summary>

When **Acknowledge** is enabled, the user/customer must confirm they have read the message (typically via a checkbox) before the booking can proceed.

Use it for mandatory terms or critical information.

</details>

<details>

<summary><strong>When should I use booking dates?</strong></summary>

Use **Booking Date From/To** when the message should only apply to bookings made in a specific sales period.

Example: “Bookings made before 1 May include free equipment rental.”

If the message should apply to everyone traveling in the period, leave booking dates empty.

</details>

<details>

<summary><strong>Why can’t I save my rule?</strong></summary>

Common reasons:

* **To** date is earlier than (or the same as) **From**.
* Your new rule overlaps an existing rule in a way that isn’t allowed.
* A required field is missing (especially the message text).

</details>

<details>

<summary><strong>What’s the difference between “Default text” and a brand tab?</strong></summary>

* **Default text** is the standard message.
* A **brand tab** lets you override the message wording for that brand only.

</details>

<details>

<summary><strong>I don’t see any brand tabs. Why?</strong></summary>

Brand tabs only appear when the brand is configured with **Use custom text**.

If you expect brand tabs and don’t see them, check the brand configuration or ask your system administrator.

</details>

<details>

<summary><strong>Is this the same as the extra’s “Custom Text” description?</strong></summary>

Not necessarily:

* **Passenger/Customer information (errata)** is rule-based (date-driven) and can be mandatory to acknowledge.
* **Custom Text** on the extra is typically general descriptive content (and can be used in other channels like apps), depending on configuration.

</details>

***

### See also

* [Extras](../extras-setup/extras/)
* [Customer Information Booking Flow](customer-information-booking-flow.md)
