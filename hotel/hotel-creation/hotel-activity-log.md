# Hotel Activity Log

### Overview

The **Activity Log** provides a detailed record of all changes made to room allotments within the system. It ensures transparency, allows tracking of modifications to hotel room availability, and improves accountability by showing which users performed specific actions.

### Purpose

* Monitor changes to allotments and room availability.
* Identify which users made updates and when.
* Compare original values with new values for auditing purposes.
* Provide a history of allotment modifications for troubleshooting or verification.

<figure><img src="../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

### **Key Elements**

#### Filters & Search

* **Change Date** – Select a date range to filter changes (e.g., 27-02-2025 to 27-03-2025).
* **Room Selection** – Choose a specific room code to view its activity (e.g., "D21").
* **Activity Type** – Dropdown to filter specific types of activities (e.g., updates, releases).
* **Search Button** – Executes the search based on selected filters.
* **Clear Button** – Resets all filters to default values.

#### Activity Log Table

Each record in the table displays details of a logged action:

* **Change Date & Time** – Timestamp of the action.
* **User** – The user who performed the change.
* **Activity** – Type of action (e.g., "Update Hotel Allotment").
* **Room Code** – Identifies the affected room (e.g., "D21").
* **Property Name** – The modified property (e.g., "GuaranteedRoomsNo").
* **Original Value** – The value before the update (e.g., 20).
* **New Value** – The updated value (e.g., 10).
* **Description** – Additional context about the change, if available.

### **Allotment History**

In addition to the Activity Log, the system provides **Allotment History** under **Allotment per Day**.

* To access, click the **Allotment History** button.
* This feature shows a chronological view of allotment changes for a specific day.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Overview**

The **Allotment History** screen provides a detailed audit trail of changes made to hotel allotments. It helps track when allotments were created, updated, or deleted, by whom, and what specific values were modified.\
This ensures transparency, accountability, and the ability to investigate past modifications.

#### **Purpose**

The purpose of this screen is to:

* Record every change made to hotel allotments.
* Allow users to filter and review allotment activities.
* Provide visibility into who made the changes, when, and what values were affected.
* Support troubleshooting and reporting.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Fields Explanation**

#### **Filters (Top of the Page)**

* **Change Date** – Date range when the change was made (e.g., 01-04-2025 → 01-10-2025).
* **Period** – The actual stay period affected by the allotment (e.g., 02-10-2025 → 02-11-2025).
* **Room** – Allows filtering by specific room code.
* **Activity** – Filters the type of action (Create, Update, Delete).
* **Display Names** – Option to show user-friendly names instead of Room codes

***

#### **Table Columns**

1. **Change Date** – The exact timestamp when the change occurred (e.g., 21-08-2025 15:52:04).
2. **Period** – The booking/allotment period the change applies to (e.g., 02-10-2025).
3. **Room Code** – Identifier of the room type (e.g., 31BR).
4. **Activity** – Type of action performed:
   * _Create Hotel Allotment_ – A new allotment was created.
   * _Update Hotel Allotment_ – An existing allotment was modified.
   * _Delete Hotel Allotment_ – An allotment was removed.
5. **User** – The system user who performed the action (e.g., rowebtpq).
6. **Property Name** – The specific field within the allotment that was modified (e.g., Date, RoomsNo, MinStay).
7. **Original Value** – The previous value before the change.
8. **New Value** – The updated value after the change.

### Instructions of Use

1. Open the **Activity Log** section.
2. Apply filters to narrow results:
   * Set a **Change Date range**.
   * Select a **Room Code** (optional).
   * Choose an **Activity Type** (optional).
3. Click **Search** to view filtered results.
4. Review details in the **Activity Log Table** to track changes.
5. Use **Clear** to reset filters and start a new search.
6. For a per-day overview, access **Allotment per Day → Allotment History**.
