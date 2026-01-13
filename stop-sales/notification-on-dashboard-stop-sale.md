# Notification on Dashboard Stop Sale

### Overview

The **Stop Sale Notifications** section in the Dashboard allows users to view and manage all system notifications related to Stop Sales. This ensures that upcoming or active Stop Sale rules are easily monitored.

### When to use it

* You want to see which Stop Sales will apply soon.
* You want to find Stop Sales with **Agreed Allotment** set.
* You want to review Stop Sales without opening each rule.

### View Stop Sale notifications

{% stepper %}
{% step %}
### Open Stop Sale notifications

1. Go to **Notifications → Stop Sales**.
2. The **Notifications** page opens with the Stop Sales list.

<figure><img src="../.gitbook/assets/image (174).png" alt=""><figcaption><p>Open Stop Sales notifications</p></figcaption></figure>
{% endstep %}

{% step %}
### Understand the default list and columns

* The default date filter shows Stop Sales for the next **2 weeks** (from today).
* The **Agreed Allotment** column shows the agreed allotment value on the rule (if set).

{% hint style="info" %}
If you need older or future periods, expand the date range in the filters.
{% endhint %}
{% endstep %}

{% step %}
### Filter to only rules with Agreed Allotment

1. Enable **Only Agreed Allotment**.
2. The list updates to show only rules with an agreed allotment value.

<figure><img src="../.gitbook/assets/image (175).png" alt=""><figcaption><p>Filter by agreed allotment</p></figcaption></figure>

{% hint style="info" %}
Agreed allotment reopens limited availability while the Stop Sale stays active. See [Agreed Allotment Stop Sale](agreed-allotment-stop-sale.md) for details.
{% endhint %}
{% endstep %}
{% endstepper %}

### Related Stop Sale tasks

* [Edit Stop Sale](edit-stop-sale.md)
* [Agreed Allotment Stop Sale](agreed-allotment-stop-sale.md)
* [Remove (Undo) Stop Sale](remove-undo-stop-sale.md)
* [Split the Stop Sale Rule](split-the-stop-sale-rule.md)

### FAQ

#### Why can’t I see Stop Sales outside the next 2 weeks?

The default filter only shows the next 2 weeks. Expand the date range in the filters.

#### What does **Only Agreed Allotment** do?

It filters the list to Stop Sale rules where an agreed allotment value is set.

#### What is the **Agreed Allotment** column showing?

It shows the agreed allotment value configured on the Stop Sale rule (if any).

#### Is Agreed Allotment the same as removing the Stop Sale?

No. Removing restores the original availability. Agreed allotment keeps the Stop Sale, but reopens some capacity.

#### Where do I change a Stop Sale rule from this list?

Open the rule from **Hotel → Stop Sales** and edit it there. Start from [Edit Stop Sale](edit-stop-sale.md).
