# Edit Stop Sale

### Overview

The _Stop Sales_ page allows users to manage and modify existing stop sale rules applied to hotels and rooms. A stop sale defines specific periods during which a hotel or room cannot be sold due to operational restrictions or supplier limitations. All lines in the list are open for editing, and you save all changes at once.

### **Purpose**

The purpose of the _Edit Stop Sale_ functionality is to:

* Change the period of an existing stop sale.
* Add or remove room types in an existing stop sale.
* Change the note or the **Hidden** setting.

Edit the existing stop sale instead of creating a new line for each correction.

### When to use it

* The hotel extends or shortens the stop sale.
* The hotel stops or opens again one of the room types.
* The hotel creates a new room type that must also be blocked. New room types are not added to a stop sale automatically.

To remove a stop sale completely, see [Delete Stop Sale](remove-undo-stop-sale.md).

### Edit a Stop Sale

{% stepper %}
{% step %}
**Find the stop sale**

1. Go to **Hotel → Stop Sales**.
2. Use the filters to find the stop sale, and click **Display**.
{% endstep %}

{% step %}
**Change the line**

Change what you need directly in the line:

* **From** / **To**: select the new dates. **To** must be the same as or later than **From**.
* **Room**: click the field, select or clear room types of the hotel and click **Ok**.
* **Note**: click the note, change the text in the **Edit Note** popup and click **Save**.
* **Hidden**: tick or clear the checkbox.
{% endstep %}

{% step %}
**Save or cancel**

Click **Save** at the bottom of the page to save all changed lines. Click **Cancel** to discard changes.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
Dates and room types you remove from a stop sale can be sold again, unless another active stop sale covers them. The Stop Sale service applies the change in the background and writes it to the log.
{% endhint %}

### Verify your changes

After you save, check these spots:

* **Log** on the stop sale line (opens the Releases / Stop Sales Log)
* **Hotel → Allotment per Day** (same room and dates): the yellow warning icon next to **Allotment** shows the stopped dates
* **Pricelist** (same room and dates)
