# Split the Stop Sale Rule

### Overview

Use **Split** to turn one Stop Sale rule into multiple date periods. Each period becomes its own Stop Sale entry.

This is useful when you only want to remove or reopen availability for part of a long range.

### When to use it

* Remove (undo) a Stop Sale for only part of the original period.
* Apply **Agreed Allotment** for only some dates.
* Keep rules easier to read and maintain.

{% hint style="info" %}
Only **enabled** rules can be removed or split.
{% endhint %}

### Access the Stop Sales page

1. Go to **Hotel → Stop Sales**.
2. The Stop Sales list shows all rules.
3. The default filter uses today’s date for **Start/End**.

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

### Split a Stop Sale rule

{% stepper %}
{% step %}
### Filter and select a rule

1. Use filters to narrow down the list.
2. Select an **enabled** Stop Sale rule.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Open the rule in edit mode

Click **Edit** (pencil icon) for the selected rule. This shows the **Remove or Split** button.
{% endstep %}

{% step %}
### Open “Remove or Split”

Click **Remove or Split**. A section called **Remove or Split Stop Sale** opens under the rule.
{% endstep %}

{% step %}
### Choose how many split records you want

Enter the number in **“Record number to split stop sale in”**. Tourpaq creates that many rows.

Each row starts with the original **Start/End** dates. Each row starts as **Enabled**.
{% endstep %}

{% step %}
### Define each period and action

For each row, set:

* **Start/End Date**: the period.
* **Action**: **Remove** or **Agreed Allotment**.

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Split or cancel

* Click **Split** to apply changes.
* Click **Cancel** to discard changes.

If validations fail, Tourpaq shows an error and does not save.
{% endstep %}
{% endstepper %}

### Validations

* Split periods must fully cover the original date range.
* Split periods must not overlap.

### Post-Split Behavior

After splitting, each new rule is independent. You can edit or remove each rule separately.

### Check Results in Stop Sales Logs

After splitting, confirm each new rule in the logs.

1. Click **View details** for each new rule.
2. The **Stop Sales Logs** page opens with filters prefilled.
3. Check **Initial r.No** and **Final r.No**.
4. Confirm the expected action is shown (Removed / Agreed Allotment).

<figure><img src="../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

### Check results in Allotment per Day

1. Open the hotel in edit mode.
2. Go to **Allotment per Day**.
3. Filter on the same room and dates.
4. Confirm daily allotment matches the split setup.

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

### Check Results in Pricelist

1. Go to **Pricelist → Pricelist**.
2. Filter by room and date to match each split rule.
3. Check **FHA** (Free Hotel Allotment).

Formula: `FHA = Final r.No - Booked rooms`.

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

### Notes

* Use splitting to apply different actions across one original date range.
* Start verification in **Stop Sales Logs**.

### FAQ

#### Can I split a disabled Stop Sale rule?

No. The rule must be **enabled** to split it.

#### Can I create gaps in the split periods?

No. The split periods must fully cover the original date range.

#### Can split periods overlap?

No. Overlaps are blocked by validation.

#### What is the difference between **Remove** and **Agreed Allotment** in a split row?

* **Remove** undoes the Stop Sale for that period.
* **Agreed Allotment** keeps the Stop Sale, but reopens limited availability.

See:

* [Remove (Undo) Stop Sale](remove-undo-stop-sale.md)
* [Agreed Allotment Stop Sale](agreed-allotment-stop-sale.md)

#### Does splitting change existing bookings?

No. It changes availability calculations for the dates and room.

#### How do I “undo” a split?

There is no merge button. Edit the split rules or recreate one new rule covering the full period.

#### Where should I verify results first?

Start with **Stop Sales Logs → View details**. Then check **Allotment per Day** and **Pricelist**.
