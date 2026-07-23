---
description: >-
  Configure destination customer information (errata) in Tourpaq Office. Set
  travel and booking periods, guest messages for tickets/WebBooking, and
  required acknowledgment.
---

# Customer Information on Destination setup

{% hint style="info" %}
**How to access:** **Setup → Destinations** → open a destination → **Passenger Information**.

This is where you define destination-specific **customer information** (errata) and **guest notifications** shown in the booking flow and on customer-facing outputs.
{% endhint %}

### Overview

Use **Passenger Information** on a destination to add destination-specific messages (often called **Customer information / errata**) that appear on:

* **Tickets**
* **WebBooking**
* The **booking flow** and **booking confirmation** screens

You can also require the message to be **acknowledged** before the booking can be completed.

### Purpose

Make sure customers (and staff) see the right information for the selected destination, for the correct travel period—and (optionally) confirm they have read it.

### Preconditions

* You have **administrative access** to Tourpaq Office.
* The destination already exists in **Setup → Destinations**.
* If you want brand-specific wording, the brand must have **Use custom text** enabled.

### Navigation path

**Setup → Destinations → (open destination) → Passenger Information**

***

### How it works (what you see on the Passenger Information tab)

On the **Passenger Information** tab you’ll typically see:

* A list of existing rules/entries (or **“There are no entries to show”** if none exist)
* **Create**, **Edit**, and **Delete** actions
* Pagination (25 rows per page)
* A **Default text** tab
* One tab per brand (only for brands where **Use custom text** is enabled)

#### Default text vs. brand-specific text

* **Default text** is the “base” message.
* Brand tabs let you **override only the message text** for that brand, while keeping the same date logic.

***

### Create a new destination message

{% stepper %}
{% step %}
**Open the destination**

1. Go to **Setup → Destinations**.
2. Click the destination you want to configure.

You are now on the destination edit page.
{% endstep %}

{% step %}
**Go to Passenger Information**

Open the **Passenger Information** tab to view existing entries.
{% endstep %}

{% step %}
**Click Create**

Click **Create** to add a new entry.

A form opens with **Save** and **Cancel**.
{% endstep %}

{% step %}
**Fill in the rule fields**

**Travel period (required)**

* **From**: start date of the period where the message applies
* **To**: end date of the period where the message applies

**Booking date period (optional)**

* **Booking date from**: only show/apply the message for bookings created on/after this date
* **Booking date to**: only show/apply the message for bookings created on/before this date

**Message text**

* **Information for the customer on ticket**: the text shown on ticket/WB/booking screens (opens in a pop-up editor)

**Acknowledgement**

* **Acknowledge** (checkbox): when enabled, the user/customer must actively confirm the message during the booking flow (checkout).

<figure><img src="../.gitbook/assets/image (22) (1) (1) (1).png" alt="Destination Passenger Information: create customer information (errata) rule with travel and booking periods"><figcaption><p>Create a destination customer information notice (errata): set travel period, optional booking period, text, and acknowledgment.</p></figcaption></figure>

{% hint style="warning" %}
If you enable **Acknowledge**, the booking flow will block completion until all required messages are confirmed.
{% endhint %}
{% endstep %}

{% step %}
**Save**

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
If you need two different messages, place them in **non-overlapping periods** (for example split the travel period into two ranges).
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

1. Open the destination’s **Passenger Information** tab.
2. Go to the relevant **brand tab**.
3. Click **Edit** on the entry.

You will see the rules from **Default text**, but only **Information for the customer on ticket** is editable.

4. Update the text and click **Save**.
