# System Setup – Flight Change Queue

### Overview

The **Flight Change Configuration** section allows administrators to define thresholds and notifications for flight schedule changes. These settings classify flight time changes into categories (Tiny, Small, Large), trigger alerts, and set pre-departure warning rules.

This ensures that both the system and relevant staff are aware of schedule modifications early, helping maintain accurate communication with passengers and providers.

### Purpose

The purpose of this configuration is to:

* Categorize flight schedule changes by duration.
* Notify designated staff when changes occur.
* Define a timeframe for warnings before flight departure.

By standardizing thresholds, the system can automatically detect and classify changes, improving efficiency and reducing human error.

***

### Fields & Options

<figure><img src="../../.gitbook/assets/image (359).png" alt=""><figcaption></figcaption></figure>

#### 1. **Earlier (minutes)**

* **Description:** Defines how many minutes earlier a flight can shift for each change category.
* **Example:**
  * _Tiny:_ 10 minutes earlier
  * _Small:_ 20 minutes earlier
  * _Large:_ 60 minutes earlier

#### 2. **Later (minutes)**

* **Description:** Defines how many minutes later a flight can shift for each change category.
* **Example:**
  * _Tiny:_ 20 minutes later
  * _Small:_ 30 minutes later
  * _Large:_ 70 minutes later

#### 3. **Warning – Email**

* **Description:** The email address that receives flight change alerts.
* **Instruction:** Enter the email of the responsible person/team (e.g., operations, customer service).

#### 4. **Warning – Before Departure**

* **Description:** Defines the timeframe (in hours) before departure when the system should issue a warning.
* **Example:** `5 hours` – warnings will be triggered for changes detected within 5 hours of departure.

***

### Instructions for Configuration

1. Navigate to **System Setup > Flight Change Queue > Flight Change Configuration**.
2. Define thresholds for **Tiny, Small, and Large** flight changes by setting the _Earlier_ and _Later_ values in minutes.
   * Example: A flight leaving 15 minutes earlier than planned falls under _Small Change_ if “Tiny” is up to 10 minutes.
3. Enter the **Email address** of the person or department responsible for handling change notifications.
4. Set the **Before Departure (hours)** value to determine how close to departure changes should trigger special warnings.
5. Save the configuration.

Once saved, the system will automatically classify flight time changes and notify the specified contact by email.

***

### Troubleshooting Guide

#### 1. **Not Receiving Flight Change Emails**

* **Cause:** Incorrect or inactive email address entered.
* **Solution:** Verify the email address field and confirm the recipient’s inbox can receive system messages.

#### 2. **Flight Changes Not Classified Correctly**

* **Cause:** Incorrect thresholds set in _Earlier_ or _Later_ fields.
* **Solution:** Review and adjust minute values to match company policy.

#### 3. **Warnings Not Triggered Before Departure**

* **Cause:** _Before Departure_ value set too high or too low.
* **Solution:** Adjust hours to a practical timeframe (e.g., 5 hours ensures timely action).

#### 4. **Overlapping Categories**

* **Cause:** Inconsistent configuration (e.g., Tiny later = 20 min, Small earlier = 20 min).
* **Solution:** Ensure ranges do not overlap between Tiny, Small, and Large.

***

✅ **Tips:**\
Start with company-standard values (Tiny: 10–20 min, Small: 20–30 min, Large: 60–70 min) and only adjust if instructed by management. Always test by simulating a flight change after configuration.
