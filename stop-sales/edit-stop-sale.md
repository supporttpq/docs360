# Edit Stop Sale

### Overview

The _Stop Sales_ page allows users to manage and modify existing stop sale rules applied to hotels, rooms, or suppliers. A stop sale defines specific periods during which a hotel or room cannot be sold due to operational restrictions or supplier limitations. The _Edit Stop Sale_ function provides tools to adjust, remove, or split existing stop sale records to better match business requirements.

### **Purpose**

The purpose of the _Edit Stop Sale_ functionality is to:

* Modify the details of an existing stop sale period.
* Remove an active stop sale when it is no longer required.
* Split a stop sale period into multiple intervals for more granular control. This feature ensures flexibility in managing sales restrictions and maintains accurate availability data for partners and customers.

### When to use it

* Adjust a date range or other rule values.
* Undo a Stop Sale that is no longer needed.
* Split one long period into smaller periods.

### Edit a Stop Sale

{% stepper %}
{% step %}
### Open the rule in edit mode

1. Go to **Hotel → Stop Sales**.
2. Find the rule you want to change.
3. Click **Edit** (pencil icon).

<figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Only enabled rules can be removed or split.
{% endhint %}
{% endstep %}

{% step %}
### Open “Remove or Split”

Click **Remove or Split** above the rule. This opens an extra section under the list.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Choose what you want to do

You have two common paths:

* **Remove (Undo)**: remove the Stop Sale and restore availability.
* **Split**: create multiple Stop Sale periods from one rule.

Use these pages for the detailed flow:

* [Remove (Undo) Stop Sale](remove-undo-stop-sale.md)
* [Split the Stop Sale Rule](split-the-stop-sale-rule.md)
{% endstep %}

{% step %}
### Save or cancel

Click **Save** to apply changes. Click **Cancel** to discard changes.
{% endstep %}
{% endstepper %}

### Example

You have one Stop Sale from `2019-07-06` to `2029-07-06`. You want two periods instead.

1. Click **Edit**.
2. Click **Remove or Split**.
3. Enter `2` as the number of split records.
4. Adjust dates for each row.
5. Apply the split and save.

{% hint style="info" %}
Before you save, ensure periods do not overlap. Ensure periods still cover the original date range.
{% endhint %}

### Verify your changes

After you save, check these spots:

* **Stop Sales Logs → View details**
* **Hotel → Allotment per Day** (same room and dates)
* **Pricelist** (same room and dates)

### FAQ

#### Why is the “Remove” checkbox disabled?

The rule is not in an editable state yet. Click **Edit** first, then open **Remove or Split**.

#### What is the difference between “Removed” and “Enabled”?

**Enabled** turns the rule on or off. **Removed** undoes the Stop Sale and restores availability.

#### Can I split a Stop Sale into more than two periods?

Yes. Enter the number of periods you need.

#### What validations apply when splitting?

Periods must not overlap. Periods must cover the original date range.

#### Where do I confirm the system updated availability?

Check **Stop Sales Logs** first. Then verify **Allotment per Day** and **Pricelist**.
