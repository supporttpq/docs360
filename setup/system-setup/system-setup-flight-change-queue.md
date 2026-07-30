---
description: Configure flight-change thresholds and warning notifications.
---

# System Setup – Flight Change Queue

### Overview

**Flight Change Configuration** defines thresholds and warning notifications for flight schedule changes. It forms part of the company-wide settings in [System Setup](./).

Tourpaq classifies changes as **Tiny**, **Small**, or **Large**. It also supports warning emails and departure-related warnings.

### Purpose

Use this configuration to:

* Categorize flight schedule changes by duration.
* Notify designated staff when changes occur.
* Define a timeframe for warnings before flight departure.

Standardized thresholds reduce manual checks and missed changes.

### Requirements

Before configuring Flight Change Queue, confirm these requirements:

* **Administrator** rights for **System Setup**.
* Approved threshold values for **Tiny**, **Small**, and **Large** changes.
* A monitored recipient for **Warning – Email**.

Use a safe test environment for high-impact changes.

### Navigation

In Tourpaq Office, open **Setup → System Setup → Flight Change Queue → Flight Change Configuration**.

### Interface overview

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (359).png" alt="Flight Change Configuration fields for Tiny, Small, and Large thresholds, Warning – Email, and Warning – Before Departure (hours)."><figcaption><p>Flight Change Configuration fields.</p></figcaption></figure></div>

Each change category has **Earlier** and **Later** thresholds. Tourpaq measures both thresholds in minutes.

### Field descriptions

| Field                                  | Description                                                                                                        |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **Tiny**                               | Defines the smallest flight-change category. Configure **Earlier** and **Later** thresholds for this category.     |
| **Small**                              | Defines the intermediate flight-change category. Configure **Earlier** and **Later** thresholds for this category. |
| **Large**                              | Defines the largest flight-change category. Configure **Earlier** and **Later** thresholds for this category.      |
| **Earlier**                            | Defines how many minutes earlier a flight can move for each category.                                              |
| **Later**                              | Defines how many minutes later a flight can move for each category.                                                |
| **Warning – Email**                    | Specifies the email address that receives flight-change alerts. Use a monitored shared inbox where appropriate.    |
| **Warning – Before Departure (hours)** | Defines how close to departure Tourpaq applies before-departure warning logic.                                     |

The screen does not indicate required fields. Configure all categories and warning settings needed by company policy.

### Configuration steps

1. In **Flight Change Configuration**, set the **Earlier** threshold for **Tiny**.
2. Set the remaining **Earlier** thresholds for **Small** and **Large**.
3. Set the **Later** thresholds for **Tiny**, **Small**, and **Large**.
4. In **Warning – Email**, enter the alert recipient.
5. In **Warning – Before Departure (hours)**, enter the warning timeframe.
6. To apply the settings, save the configuration.

### System behavior

After saving, Tourpaq classifies flight time changes using the configured thresholds. It sends alerts to **Warning – Email**.

Tourpaq applies before-departure warning logic inside the configured timeframe.

### Examples

#### Earlier threshold example

The following thresholds classify an earlier flight change:

* **Tiny:** 10 minutes earlier.
* **Small:** 20 minutes earlier.
* **Large:** 60 minutes earlier.

A flight moving 15 minutes earlier is classified as **Small**.

#### Later threshold example

The following thresholds classify a later flight change:

* **Tiny:** 20 minutes later.
* **Small:** 30 minutes later.
* **Large:** 70 minutes later.

#### Departure warning example

Set **Warning – Before Departure (hours)** to `5`. Tourpaq applies before-departure warning logic within five hours of departure.

### Troubleshooting

#### Not receiving flight change emails

* **Cause:** **Warning – Email** contains an incorrect or inactive address.
* **Solution:** Confirm the address and inbox access.

#### Flight changes are not classified correctly

* **Cause:** **Earlier** or **Later** values do not match company policy.
* **Solution:** Review each category threshold.

#### “Before departure” warnings are not triggered

* **Cause:** **Warning – Before Departure (hours)** does not cover the required timeframe.
* **Solution:** Adjust the number of hours.

#### Overlapping categories

* **Cause:** Category thresholds do not increase consistently.
* **Solution:** Keep **Tiny**, **Small**, and **Large** thresholds in ascending order.

{% hint style="info" %}
Start with approved company values.

Test threshold changes with a non-production flight update.
{% endhint %}

### Related pages

* [System Setup](./) describes the company-wide settings area.
