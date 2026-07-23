---
description: >-
  Configure extra-level customer information (errata) in Tourpaq Office. Add
  guest notices for excursions/transfers on tickets/WebBooking, with
  travel/booking periods and optional acknowledgment.
---

# Customer Information on Extra setup

{% hint style="info" %}
**How to access:** **Extras Setup → Extras** → open an extra → **Passengers Information**.

Use this area to add **customer information / errata** (guest notifications) for an extra, optionally limited by travel dates and booking dates.
{% endhint %}

### Overview

You can add **Passenger Information** rules to an **extra** so important messages are shown during booking. In some setups, the message also appears on tickets/vouchers.

Typical use cases:

* Conditions or restrictions for an excursion or transfer
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

### See also

* [Extras](../extras-setup/extras-general-page/extras.md)
* [Customer Information Booking Flow](customer-information-booking-flow.md)
