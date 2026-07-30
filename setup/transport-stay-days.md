---
description: >-
  Define the stay lengths available for transport rules and stay-length
  allotment.
---

# Transport Stay Days

## Transport Stay Days

**Transport Stay Days** defines the stay lengths used in transport planning. These values support [Transport Rules](../transport-rules/edit-transport-rule.md) and [Allotments per day](../hotel/hotel-creation/allotments-per-day/).

### Overview

Each row defines one stay length with a **Name** and **Days** value. For example, a seven-day stay can use the name `7d` and value `7`.

### Purpose

Use consistent stay lengths to:

* Select stay durations in Transport Rules.
* Reserve rooms by stay length in daily allotment.
* Apply consistent stay-duration labels across transport planning.

### Requirements

Define a stay length before selecting it in a Transport Rule. Coordinate new values with transport and allotment planning.

### Navigation

In Tourpaq Office, open **Setup → Transport Stay Days**.

### Interface overview

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (2) (1) (1) (1) (1).png" alt="Transport Stay Days list with Name, Days, Edit, Delete, and Create"><figcaption></figcaption></figure></div>

The page lists existing stay lengths and provides actions for their maintenance.

### Field descriptions

| Field      | Description                                                                                                                   |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Name**   | Identifies the stay length in Tourpaq Office. Use a consistent label, such as `3d`, `7d`, or `Weekend`.                       |
| **Days**   | Defines the stay duration in days. This value controls the selected stay length in related transport and allotment workflows. |
| **Edit**   | Opens an existing stay length for changes. Review related Transport Rules before changing **Days**.                           |
| **Delete** | Removes the stay length from the list. Confirm that no active Transport Rule requires the value.                              |
| **Create** | Opens a new stay-length record.                                                                                               |

### Configuration steps

{% stepper %}
{% step %}
#### Open Transport Stay Days

In Tourpaq Office, open **Setup → Transport Stay Days**.
{% endstep %}

{% step %}
#### Create a stay length

Click **Create**.
{% endstep %}

{% step %}
#### Enter Name

Enter a consistent label in **Name**.
{% endstep %}

{% step %}
#### Enter Days

Enter the duration in **Days**.
{% endstep %}

{% step %}
#### Save the stay length

Click **Save**.
{% endstep %}
{% endstepper %}

### System behavior

Transport Rules use the configured stay-day values when defining a season. Adding a stay day to a Transport Rule preselects the first available value.

Daily hotel allotment can reserve rooms by the selected stay length. Stay-length reservations can also affect multiples of the configured duration.

### Examples

The following entries use clear, consistent names:

{% hint style="info" %}
Use one naming convention for all stay lengths:
{% endhint %}

* **Name**: `Weekend`; **Days**: `3`
* **Name**: `One week`; **Days**: `7`
* **Name**: `Two weeks`; **Days**: `14`

### Related pages

* [Edit Transport Rule](../transport-rules/edit-transport-rule.md) assigns stay days to transport rule seasons.
* [Allotments per day](../hotel/hotel-creation/allotments-per-day/) uses stay lengths for room allocation by transport duration.
