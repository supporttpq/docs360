# System Setup – Flight Change Queue

### Overview

The **Flight Change Configuration** section lets admins define thresholds and notifications for flight schedule changes.

The system classifies changes as **Tiny**, **Small**, or **Large**. It can also send alerts and trigger extra warnings close to departure.

### Purpose

Use this configuration to:

* Categorize flight schedule changes by duration.
* Notify designated staff when changes occur.
* Define a timeframe for warnings before flight departure.

Standardized thresholds reduce manual checks and missed changes.

***

### Fields and options

<figure><img src="../../.gitbook/assets/image (359).png" alt=""><figcaption></figcaption></figure>

Each change category (Tiny/Small/Large) has its own **Earlier** and **Later** threshold. Thresholds are in minutes.

#### 1. Earlier (minutes)

Defines how many minutes _earlier_ a flight can move and still be classified in each category.

Example:

* Tiny: 10 minutes earlier
* Small: 20 minutes earlier
* Large: 60 minutes earlier

#### 2. Later (minutes)

Defines how many minutes _later_ a flight can move and still be classified in each category.

Example:

* Tiny: 20 minutes later
* Small: 30 minutes later
* Large: 70 minutes later

#### 3. Warning – Email

The email address that receives flight change alerts.

Enter a shared inbox if possible (for example operations or customer service).

#### 4. Warning – Before Departure (hours)

Defines how close to departure the system should apply the “before departure” warning logic.

Example: `5` means “within 5 hours of departure”.

***

### Instructions for Configuration

1. Go to **Setup → System Setup → Flight Change Queue → Flight Change Configuration**.
2. Set **Earlier** and **Later** thresholds for **Tiny**, **Small**, and **Large**.
   * Example: If Tiny is up to 10 minutes earlier, then 15 minutes earlier becomes Small.
3. Enter the **Warning – Email** recipient.
4. Set **Warning – Before Departure (hours)**.
5. Save.

Once saved, the system will automatically classify flight time changes and notify the specified contact by email.

***

### Troubleshooting Guide

#### 1. Not receiving flight change emails

* **Cause:** Incorrect or inactive email address entered.
* **Solution:** Verify the address and confirm the inbox can receive system emails.

#### 2. Flight changes are not classified correctly

* **Cause:** Incorrect thresholds set in _Earlier_ or _Later_ fields.
* **Solution:** Review and adjust minute values to match company policy.

#### 3. “Before departure” warnings are not triggered

* **Cause:** _Before Departure_ value set too high or too low.
* **Solution:** Adjust hours to a practical timeframe (e.g., 5 hours ensures timely action).

#### 4. Overlapping categories

* **Cause:** Inconsistent configuration (e.g., Tiny later = 20 min, Small earlier = 20 min).
* **Solution:** Ensure Tiny < Small < Large for both Earlier and Later.

***

{% hint style="info" %}
Start with company-standard values (for example Tiny: 10–20 min, Small: 20–30 min, Large: 60–70 min).

Test after changes by simulating a flight update in a non-production environment if possible.
{% endhint %}

### FAQ

<details>

<summary><strong>Do I have to configure both Earlier and Later?</strong></summary>

Yes. Flights can move both earlier and later.

Configure both so the system can classify changes consistently in both directions.

</details>

<details>

<summary><strong>Should the thresholds be higher for Large than for Small and Tiny?</strong></summary>

Yes. Keep thresholds increasing from Tiny → Small → Large.

That avoids overlaps and unexpected classification.

</details>

<details>

<summary><strong>What does “Warning – Before Departure” actually control?</strong></summary>

It defines a time window (in hours) before departure.

Changes detected inside that window can trigger extra warning behavior.

</details>

<details>

<summary><strong>What email should I use for “Warning – Email”?</strong></summary>

Use an inbox that is monitored during operating hours.

A shared mailbox usually works better than a single person.

</details>
