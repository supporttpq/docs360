# Activity Log - Hotel Contract Configuration

### Overview

The **Activity Log** tab shows an audit trail for a hotel contract. It logs inserts, updates, and deletions. It also shows who changed what and when.

Use it for troubleshooting, compliance, and change tracking.

***

### Purpose

The purpose of the **Activity Log** is to:

* Monitor changes made to hotel contracts.
* Provide accountability by showing which user made specific changes.
* Help identify data discrepancies or errors.
* Enable agencies and internal teams to audit past modifications.

***

### Preconditions

Before accessing the Activity Log:

* You must have the necessary **permissions** to view hotel contracts and audit logs.
* At least one **hotel contract** must exist.
* The contract must have logged changes in the selected date range.
* You should know the **date range** and (optionally) the **user** you want to review.

***

### How to use

{% stepper %}
{% step %}
### Open the Activity Log

1. Go to the **Hotel Contract** module.
2. Open the contract you want to review.
3. Select the **Activity Log** tab.
{% endstep %}

{% step %}
### Filter and display results

1. Select the **date period** (top left).
2. Optional: select a specific **user** from the dropdown.
3. Click **Display** to show entries.
4. Click **Clear** to reset filters.
{% endstep %}
{% endstepper %}

***

### Screenshot

<figure><img src="../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

### Field descriptions

| Field Name         | Description                                                                                              |
| ------------------ | -------------------------------------------------------------------------------------------------------- |
| **KEYID**          | A unique identifier for the contract entry. Rows with the same KEYID belong to the same contract record. |
| **ACTION**         | The type of change performed. Example: `Insert`, `Update`, `Delete`.                                     |
| **ENTITY NAME**    | The entity that was changed (typically `HotelContract`).                                                 |
| **PROPERTY NAME**  | The specific attribute/property of the entity that was modified.                                         |
| **ORIGINAL VALUE** | The previous value before the change. For `Insert` actions, this may be empty.                           |
| **NEW VALUE**      | The new value after the change was made.                                                                 |
| **AGENCY**         | Indicates the agency/brand context of the change. `All brands` means it applies across all brands.       |
| **DESCRIPTION**    | A brief text summarizing or categorizing the change.                                                     |

***

### Tips

* One save can create multiple log rows. Each field change is logged separately.
* Use **PROPERTY NAME** to pinpoint what was edited.
* If you see no results, widen the date range first.

***

### Related pages

* [Hotel contract - General](hotel-contract-general.md)
* [Rules - Hotel Contract Configuration](rules-hotel-contract-configuration.md)
* [Hotel Activity Log](../hotel/hotel-creation/hotel-activity-log.md) (hotel allotment changes, not contract changes)

***

### FAQ

**Why don’t I see any entries?**\
Widen the date range.\
Verify you have access to audit logs.\
Confirm the contract was actually changed in that period.

**Why do I see multiple rows with the same KEYID?**\
KEYID groups changes for the same contract entry.\
Each changed field is logged as a separate row.

**What’s the difference between ORIGINAL VALUE and NEW VALUE?**\
ORIGINAL VALUE is the value before the change.\
NEW VALUE is the value after the change.

**What does AGENCY = “All brands” mean?**\
It means the change applies across all brands, not a single brand.

**Can I undo changes from Activity Log?**\
No. The Activity Log is read-only.\
To revert a change, edit the contract back to the correct values.
