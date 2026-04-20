---
description: >-
  Control repricing when editing bookings in Tourpaq Office. Keep or recalculate
  automatic discount, extras, and travel insurance prices using the “Keep
  automatic discount prices” checkbox.
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

# Keep automatic discount prices

## Keep automatic discount prices (prevent repricing on booking edits)

### Overview

When you **edit an existing booking** in **Tourpaq Office**, the system can either:

* **Keep the original prices** for automatic items (price lock), or
* **Recalculate (reprice)** using the **current** prices and rules.

This behavior is controlled by the checkbox **Keep automatic discount prices** on the booking.

### What this affects

This setting controls how Tourpaq treats **automatically calculated** prices for:

* Discounts / supplements
* Extras
* Travel insurance

{% hint style="warning" %}
If you allow recalculation, the booking total can change. Make sure this matches your agreement with the customer before saving.
{% endhint %}

### Where to find it

On the **booking page** in **Tourpaq Office** (Back Office), locate the checkbox:

* **Keep automatic discount prices**

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (86).png" alt="Booking page in Tourpaq Office showing the “Keep automatic discount prices” checkbox"><figcaption><p>Checkbox on the booking page.</p></figcaption></figure>

### How it works

#### If the checkbox is checked

Tourpaq Office will **keep the original prices** for discounts, extras, and insurance. This applies even if price lists changed after booking creation.

Use this when you want to:

* Preserve the customer’s agreed price
* Avoid unexpected price differences during small edits (names, contact details, comments)

#### If the checkbox is unchecked

Tourpaq Office will **refresh prices** for discounts, extras, and insurance when you modify the booking. This is a **reprice** of automatic items.

Use this when you want to:

* Ensure the booking matches the **latest** pricing rules and rates
* Intentionally reprice after changes (for example if policy requires “current price”)

### Common use cases (when to keep vs reprice)

* **Keep prices**: admin fixes and corrections.
  * Name corrections.
  * Updating email/phone.
  * Internal comments.
* **Reprice**: you want today’s prices.
  * Adding an extra where current pricing should apply.
  * Applying new discount rules after a policy change.

### Recommended workflow

{% stepper %}
{% step %}
### 1. Open the booking and decide your intent

Before changing anything, decide:

* Are you making a **small correction** and want to keep the customer’s price?
* Or are you making a change where you **expect repricing**?
{% endstep %}

{% step %}
### 2. Set the checkbox

* Check **Keep automatic discount prices** to **lock in** the existing prices.
* Uncheck it to **recalculate** to the current prices.
{% endstep %}

{% step %}
### 3. Save and verify the totals

After saving, review the booking totals to confirm the result matches what you intended.
{% endstep %}
{% endstepper %}

### When this setting does not apply

In some changes, Tourpaq Office will **always update prices** (regardless of checkbox state). This happens because the booking was effectively rebuilt:

* Changing the **departure date**
* Changing the **transport**
* Changing the **hotel**

### Notes

* The **default state** of the checkbox is controlled by a **company setting**, but it can typically be overridden per booking.

### Troubleshooting

#### “Prices changed even though the checkbox was checked”

Most commonly this happens because you changed something that forces a full repricing (for example **departure date**, **transport**, or **hotel**).

#### “I’m not sure whether I should check it”

As a rule of thumb:

* **Check it** for corrections and admin updates where the customer price should remain the same.
* **Uncheck it** when you intentionally want the booking to follow today’s pricing.
