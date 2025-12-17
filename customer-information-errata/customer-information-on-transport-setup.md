# Customer Information on Transport setup

{% hint style="info" %}
**How to access:** **Transport → Transports** → open a transport → **Passenger Information**.

This is where you define transport-specific messages shown to the customer (and/or booking user) in the booking flow and on customer-facing outputs.
{% endhint %}

### Overview

Use **Passenger Information** on a transport to add important transport-specific text (often called _Customer information/errata_) that should appear on:

* **Tickets**
* **WebBooking (WB)**
* The **booking flow / booking confirmation** screens

You can also make the message **mandatory to acknowledge** before the booking can be completed.

### Purpose

Ensure customers (and staff) see the right information for the selected **transport**, for the correct travel period—and (optionally) confirm they have read it.

### Preconditions

* You have **administrative access** to Tourpaq Office.
* The transport already exists in **Transport → Transports**.
* If you want brand-specific wording, the brand must have **Use custom text** enabled.

### Navigation path

**Transport → Transports → (open transport) → Passenger Information**

***

### How it works (what you see on the Passenger Information tab)

On the **Passenger Information** tab you’ll typically see:

* A list of existing rules/entries (or **“There are no entries to show”** if none exist)
* **Create**, **Edit**, and **Delete** actions
* Pagination (25 rows per page)
* A **Default text** tab
* One tab per brand (only for brands where **Use custom text** is enabled)

<figure><img src="../.gitbook/assets/image (24) (1).png" alt="Passenger Information tab on a transport"><figcaption></figcaption></figure>

#### Default text vs. brand-specific text

* **Default text** is the “base” message.
* Brand tabs let you **override only the message text** for that brand, while keeping the same date logic.

***

### Create a new transport message

{% stepper %}
{% step %}
### Open the transport

1. Go to **Transport → Transports**.
2. Click the transport you want to configure.

You are now on the transport edit page.
{% endstep %}

{% step %}
### Go to Passenger Information

Open the **Passenger Information** tab to view existing entries.
{% endstep %}

{% step %}
### Click Create

Click **Create** to add a new entry.

A form opens with **Save** and **Cancel**.
{% endstep %}

{% step %}
### Fill in the rule fields

#### Travel period (required)

* **From**: start date of the period where the message applies
* **To**: end date of the period where the message applies

#### Booking date period (optional)

* **Booking date from**: only show/apply the message for bookings created on/after this date
* **Booking date to**: only show/apply the message for bookings created on/before this date

#### Message text

* **Information for customer on ticket**: the text shown on ticket/WB/booking screens (opens in a pop-up editor)

#### Acknowledgement

* **Acknowledge** (checkbox): when enabled, the user/customer must actively confirm the message during the booking flow.

{% hint style="warning" %}
If you enable **Acknowledge**, the booking flow will block completion until all required messages are confirmed.
{% endhint %}
{% endstep %}

{% step %}
### Save

Click **Save**.

* If the entry is valid, you’ll see a success message.
* If something is wrong, you’ll see a warning/error explaining what needs to be fixed.
{% endstep %}
{% endstepper %}

***

### Validation rules (important)

#### Date range checks

* **To** must be later than **From**.

#### Overlap checks (to avoid conflicting messages)

The system prevents multiple entries that cover the **same period**.

* Entries **without booking-date limits** are compared only with other entries that also have **no booking-date limits**.
* Entries **with booking-date limits** are compared only with other entries that also have **booking-date limits**.

{% hint style="info" %}
If you need different wording in different periods, split the travel period into **non-overlapping** ranges.
{% endhint %}

***

### Edit or delete an existing entry

#### Edit

1. Click **Edit** on the entry.
2. Update the fields.
3. Click **Save**.

#### Delete

1. Click **Delete** on the entry.
2. Confirm the deletion.

The entry is removed and a success message is shown.

***

### Brand-specific configuration (override the text per brand)

Use this when the **same rule** (same dates) should have different wording for different brands.

1. Open the transport’s **Passenger Information** tab.
2. Go to the relevant **brand tab**.
3. Click **Edit** on the entry.

You will see the rules from **Default text**, but only **Information for customer on ticket** is editable.

4. Update the text and click **Save**.

***

### FAQ

<details>

<summary><strong>What should I write in “Information for customer on ticket”?</strong></summary>

Write short, clear, actionable information—such as:

* baggage or check-in reminders
* meeting time / meeting point instructions
* carrier/operator restrictions
* temporary changes (route changes, check-in rules, etc.)

If the message is long, use short paragraphs and bullet points.

</details>

<details>

<summary><strong>What’s the difference between “Default text” and a brand tab?</strong></summary>

* **Default text** is the standard message.
* A **brand tab** lets you override the message wording for that brand only (the date periods and rule logic stay the same).

</details>

<details>

<summary><strong>When should I use “Booking date from/to”?</strong></summary>

Use booking-date limits when the message should only apply to bookings created during a certain sales period (for example: “Only for bookings made after 1 Jan”).

If you want the message to apply to _all_ bookings for a travel period, leave booking dates empty.

</details>

<details>

<summary><strong>I can’t save my entry. What should I check first?</strong></summary>

Most save issues are caused by:

* **To** being earlier than (or equal to) **From**
* The new entry **overlaps** an existing entry in a way the system does not allow

Adjust the dates (or split the period) and try again.

</details>

<details>

<summary><strong>Can I have multiple transport messages for the same travel period?</strong></summary>

Not if they overlap. The system blocks overlapping rules to prevent conflicting information.

If you need multiple messages, consider:

* Combining them into one message, or
* Splitting the travel period into smaller non-overlapping ranges

</details>

<details>

<summary><strong>I edited the text on a brand tab, but I still see the default text. Why?</strong></summary>

Common causes:

* The brand does not have **Use custom text** enabled
* You edited the wrong brand tab
* The output you’re checking is tied to a different brand than expected

If you’re unsure which brand the booking uses, verify the booking’s brand first.

</details>

<details>

<summary><strong>What happens if I enable “Acknowledge”?</strong></summary>

The message becomes mandatory to confirm during the booking flow. The user/customer must check the confirmation checkbox(es) before they can proceed.

</details>
