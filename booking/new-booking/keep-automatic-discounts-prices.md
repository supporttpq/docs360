# Keep automatic discounts prices

## Keep automatic discount prices

### Overview

When you **edit an existing booking**, Tourpaq can either:

* **Keep the original prices** (so the customer keeps the same discount/extra/insurance prices as when the booking was created), or
* **Recalculate prices** using the **current** prices in the system.

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

On the **booking page** (Back Office), locate the checkbox:

* **Keep automatic discount prices**

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (22).png" alt=""><figcaption><p>Checkbox on the booking page (Back Office).</p></figcaption></figure>

### How it works

#### If the checkbox is checked

Tourpaq will **keep the original prices** for discounts, extras, and insurance—even if those prices have changed in your price lists since the booking was created.

Use this when you want to:

* Preserve the customer’s agreed price
* Avoid unexpected price differences when making small edits (names, contact details, comments, etc.)

#### If the checkbox is unchecked

Tourpaq will **refresh prices** for discounts, extras, and insurance when you modify the booking.

Use this when you want to:

* Ensure the booking matches the **latest** pricing rules and rates
* Intentionally reprice after changes (for example if internal policy requires “current price”)

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

In some changes, Tourpaq will **always update prices** (regardless of checkbox state) because the booking has effectively been rebuilt:

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
