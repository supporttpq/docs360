---
description: Review system activity by date, agency or brand, user, and action type.
---

# Internal logs

## Internal logs

### Overview

**Internal logs** records activity across Tourpaq.

Use it to investigate changes by date, agency or brand, user, or action type. For changes within one booking, use the [booking History tab](../../booking/new-booking/history.md).

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (361).png" alt="Internal logs filters and activity list"><figcaption></figcaption></figure></div>

### Purpose

Use Internal logs to:

* Identify when an action occurred.
* Identify the user responsible for an action.
* Investigate activity across several records or modules.

### Requirements

Only administrators can open Internal logs.

### Navigation

In Tourpaq Office, open **Setup → Internal Logs**.

### Interface overview

The filter area contains **Start date**, **End date**, **Agency/Brand**, **User**, and **Action type**.

The results list shows activity that matches the selected filters.

### Field descriptions

| **Field**        | **Description**                                      |
| ---------------- | ---------------------------------------------------- |
| **Start date**   | Sets the first date included in the results.         |
| **End date**     | Sets the last date included in the results.          |
| **Agency/Brand** | Limits results to activity for one agency or brand.  |
| **User**         | Limits results to activity performed by one user.    |
| **Action type**  | Limits results to one category of recorded activity. |

### Find an activity record

{% stepper %}
{% step %}
#### Set Start date

Enter **Start date**.
{% endstep %}

{% step %}
#### Set End date

Enter **End date**.
{% endstep %}

{% step %}
#### Select Agency/Brand

Select **Agency/Brand** to investigate one agency or brand.
{% endstep %}

{% step %}
#### Select User

Select **User** to investigate one user.
{% endstep %}

{% step %}
#### Select Action type

Select **Action type** to investigate one activity category.
{% endstep %}

{% step %}
#### Review the results

Review the matching activity records.
{% endstep %}
{% endstepper %}

### System behavior

Internal logs uses the selected date range and filters to narrow the activity list.

The page is read-only. Correct changes in the relevant Tourpaq area.

{% hint style="info" %}
Start with a short date range.

Add **User** or **Action type** if the result set remains large.
{% endhint %}

### Recorded activity

Internal logs can include:

* Exports, including financial files and hotel lists.
* Hotel messages sent from Tourpaq.
* Customer merges.
* Changes to discounts, products, room types, or extra bed discounts.

### Example

An export cannot be located in the expected period.

To find the export activity:

1. Set **Start date** to the first day of the expected period.
2. Set **End date** to the last day of the expected period.
3. Select **Action type** for exports.
4. Review the result list for the matching activity.

### Related pages

* [History](../../booking/new-booking/history.md)
* [All bookings](../../booking/all-bookings/view-all-bookings.md)
* [Export](../../export/)
