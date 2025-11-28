# Flight Change - Configuration

### Feature activation

It can be activated from superadmin per company.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

After the activation, the 1st step is to configure the new flight change process. For this, go to Setup -> System Setup -> Flight Change Queue.&#x20;

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Overview

The **Flight Change Configuration** section in the **System Setup** interface allows administrators to define rules and thresholds for categorizing flight schedule changes. These configurations help determine how flight time modifications are classified and when alerts should be sent out.

### Tabs

* **Flight Change Configuration** – Main configuration panel for setting thresholds.
* **Flight Change Schedules** – All the changes are listed or scheduled.

### Flight Change Configuration - Parameters

#### 1. Flight Change type

Changes are categorized into three types of changes:

| Category | Earlier (minutes) | Later (minutes) |
| -------- | ----------------- | --------------- |
| Tiny     | 10                | 20              |
| Small    | 20                | 30              |
| Large    | 60                | 70              |

* **Earlier (minutes):** used when the flight is scheduled sooner than before
* **Later (minutes):** used when the flight is scheduled later than before

These settings help the system classify the severity of a flight time change.

***

#### 2. Warnings

**Email Notification**

* **Email:** email that the service sends to the administrator, warning, with bookings in which the clients have not confirmed the changes

**Time-based Warning**

* **Before Departure:** Defines how many hours before departure a change should trigger a warning.

This setting ensures that users are notified of changes in sufficient time.



### Flight  Change Schedules

### Overview

The **Flight Change Schedules** interface is a part of the **System Setup** module, under the **Flight Change Queue** section. This module allows administrators to configure automated notification workflows for different types of flight schedule changes. Each entry in the list represents a scheduled action that will occur a set amount of time before the scheduled flight departure.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Interface Sections

#### 🔹 Columns

| Column               | Description                                                                             |
| -------------------- | --------------------------------------------------------------------------------------- |
| ✏️ (Edit Icon)       | Allows editing of the existing schedule entry.                                          |
| **Type**             | Specifies the nature of the flight change (e.g., Tiny, Small, Large, Earlier or Later). |
| **Status**           | Describes the stage of notification: SMS Sent, First Resend, Second Resend.             |
| **Before Departure** | Defines the timing of the notification in relation to the flight departure time.        |
| 🗑️ (Trash Icon)     | Deletes the corresponding schedule entry.                                               |

### Add Schedule

* Use the **Add Schedule** button (top-right) to define a new rule.
* This allows the admin to specify:
  * Change Type
  * Notification Stage
  * Lead Time before departure
