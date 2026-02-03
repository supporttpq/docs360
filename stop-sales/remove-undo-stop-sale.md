# Remove (Undo) Stop Sale

### Overview

Use **Remove (Undo)** to remove a Stop Sale rule and restore availability.

### Purpose

Remove a Stop Sale when the restriction is no longer needed. Tourpaq restores the original allotment and availability for the same dates.

### When to use it

* The hotel/room should be sellable again.
* The supplier lifted a restriction.
* A Stop Sale was created by mistake.

{% hint style="info" %}
You remove Stop Sales from **Hotel → Stop Sales**. Start from [Edit Stop Sale](edit-stop-sale.md) if you are unsure which rule to edit.
{% endhint %}

### Key fields and sections

* **Stop Sales list**: Shows Stop Sale rules. It is filtered by current dates by default.
* **Edit** (pencil icon): Opens the rule in edit mode.
* **Remove or Split**: Expands the section where you can remove or split the rule.
* **Remove** checkbox: Removes the Stop Sale and restores the original allotment.
* **Info** (tooltip): Explains what Remove does.

### Remove a Stop Sale

Only want to undo part of the date range? Use [Split the Stop Sale Rule](split-the-stop-sale-rule.md).

{% stepper %}
{% step %}
### Open the rule in edit mode

1. Go to **Hotel → Stop Sales**.
2. Find the rule you want to undo.
3. Click **Edit** (pencil icon).

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Only **enabled** rules can be removed or split.
{% endhint %}
{% endstep %}

{% step %}
### Open “Remove or Split”

Click **Remove or Split**. The section opens under the rule.
{% endstep %}

{% step %}
### Select “Remove”

Check the **Remove** box. If the checkbox is disabled, you are not in edit mode yet.
{% endstep %}

{% step %}
### Save or cancel

Click **Save** to apply the removal. Click **Cancel** to discard changes.

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

### Verify availability was restored

After you save, check these spots:

* **Stop Sales Logs → View details**
  * `Initial r.No`: the record number created when the Stop Sale was enabled.
  * `Final r.No`: the original allotment record number restored after removal.
* **Hotel → Allotment per Day** (same room and dates)
  * Allotment values should match the pre-Stop Sale values.
* **Pricelist** (same hotel, room type, and dates)
  * `FHA` (free-hotel-allotment) should show the restored availability.

### FAQ

#### Why is the “Remove” checkbox disabled?

The rule is not in edit mode yet. Click **Edit** first, then open **Remove or Split**.

#### Is “Disable” the same as “Remove (Undo)”?

No. **Disable** stops applying the rule going forward. **Remove (Undo)** restores the original allotment that the Stop Sale replaced.

#### Does removing a Stop Sale change existing bookings?

No. It changes availability calculations for the dates and rooms covered by the rule.

#### Can I undo a removal?

Not directly. Create a new Stop Sale for the same period if you need to block sales again.

#### Where should I verify the result first?

Start with **Stop Sales Logs**. Then check **Allotment per Day** and **Pricelist**.
