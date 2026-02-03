# System Setup Groups

### Overview

The **System Setup Groups** page lets admins define group rules for bookings.

Each rule is linked to a **Destination** and a **Brand**. This lets the system apply group-specific conditions for that destination.

### Purpose

* Standardize group configurations across agencies and brands.
* Apply minimum passenger requirements and special offers for group bookings.
* Centralize management of group rules to prevent duplication and ensure consistency.

### Permissions

Admins can:

1. **View** all system setup groups that belong to their company.
2. **Edit** existing system setup groups.
3. **Insert** new system setup groups.
4. **Delete** system setup groups.

### Behavior rules

* A group rule is unique per **Brand + Destination**.
* If you insert a rule that already exists, the system updates the existing rule.
  * It does not create a duplicate entry.

### Fields

| **Field**                        | **Description**                                                           |
| -------------------------------- | ------------------------------------------------------------------------- |
| **Brand**                        | The brand to which the group belongs.                                     |
| **Destination**                  | The destination associated with the group rule.                           |
| **Minimum Number of Passengers** | The minimum passenger count required to qualify for the group conditions. |

### How to create or update a group rule

1. Go to **Setup → System Setup → Groups**.
2. Click **Insert**.
3. Select the **Brand** and **Destination**.
4. Set **Minimum Number of Passengers**.
5. Save.

If a rule already exists for the same **Brand + Destination**, saving updates it.

{% hint style="info" %}
Keep **Minimum Number of Passengers** aligned with your sales policy.

If you change it, re-check any flows that depend on group qualification.
{% endhint %}

### FAQ

<details>

<summary><strong>What makes a group rule “unique”?</strong></summary>

The combination of **Brand** and **Destination**.

You can only have one rule per Brand + Destination.

</details>

<details>

<summary><strong>Why did my new rule overwrite an existing one?</strong></summary>

Because a rule already existed for that **Brand + Destination**.

The system updates instead of creating duplicates.

</details>

<details>

<summary><strong>What does “Minimum Number of Passengers” affect?</strong></summary>

It controls when a booking qualifies for the group conditions for that destination.

Use the smallest passenger count that should be treated as a group.

</details>

<details>

<summary><strong>Should we delete group rules we no longer use?</strong></summary>

Delete only if you are sure it should never be used again.

Otherwise, consider keeping the rule and adjusting the minimum passenger count.

</details>
