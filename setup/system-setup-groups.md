---
description: >-
  Configure minimum passenger thresholds for group conditions by brand and
  destination.
---

# System Setup Groups

## System Setup Groups

### Overview

**System Setup Groups** defines group qualification thresholds for each **Brand** and **Destination** combination.

Tourpaq uses the same master data as [Brands](../brands/) and [Destination](destination.md).

### Purpose

Use this page to:

* Set the minimum passenger count for group conditions.
* Apply different thresholds for each brand and destination.
* Maintain one rule for each **Brand** and **Destination** combination.

### Requirements

Before creating a rule:

* An administrator needs access to **Setup → System Setup → Groups**.
* The required [Brand](../brands/) must exist.
* The required [Destination](destination.md) must exist.

### Navigation

In Tourpaq Office:

1. Click **Setup**.
2. Click **System Setup**.
3. Click **Groups**.

### Interface overview

The page lists the group rules available for the company.

Each rule combines **Brand**, **Destination**, and **Minimum Number of Passengers**.

Click **Insert** to add a rule. Select an existing rule to edit it.

### Fields

| **Field**                        | **Description**                                                                                                      |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Brand**                        | Selects the brand that owns the group rule. It separates this rule from rules for other brands.                      |
| **Destination**                  | Selects the destination for the group rule. It links the threshold to the destination used in booking-related setup. |
| **Minimum Number of Passengers** | Sets the passenger count required to qualify for group conditions. Align this value with the approved sales policy.  |

### Configure a group rule

{% stepper %}
{% step %}
#### Open Groups

In Tourpaq Office, go to **Setup → System Setup → Groups**.
{% endstep %}

{% step %}
#### Create or select a rule

Click **Insert** to add a rule.

Select an existing rule to change its threshold.
{% endstep %}

{% step %}
#### Select the Brand

Select the **Brand**.
{% endstep %}

{% step %}
#### Select the Destination

Select the **Destination**.
{% endstep %}

{% step %}
#### Set the group threshold

Enter **Minimum Number of Passengers**.

Use the approved sales-policy threshold for this brand and destination.
{% endstep %}

{% step %}
#### Save the rule

Save the rule.
{% endstep %}
{% endstepper %}

### System behavior

Tourpaq permits one rule for each **Brand** and **Destination** combination.

Saving an existing combination updates that rule. Tourpaq does not create a duplicate entry.

{% hint style="info" %}
Keep **Minimum Number of Passengers** aligned with your sales policy.

Review dependent group-qualification flows after changing the threshold.
{% endhint %}

### Example

For a **Brand** and **Destination**, set the approved group threshold.

For example, `10` requires at least 10 passengers for group conditions.

### Related pages

* [System Setup](system-setup/)
* [Brands](../brands/)
* [Destination](destination.md)
