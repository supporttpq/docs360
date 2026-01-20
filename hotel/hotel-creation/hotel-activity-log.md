# Hotel Activity Log

### Overview

The **Activity Log** is an audit view of changes to hotel room allotments.

It helps you track who changed availability, when, and what values changed.

Where to find it: **Hotel → Activity Log**.

### What you can do

* Monitor allotment and room availability changes.
* Identify who made the change and when.
* Compare previous and new values for auditing.
* Investigate issues by reviewing the change trail.

<figure><img src="../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

### Key elements

#### Filters and search

* **Change Date** – Filter by when the change was made (example: `27-02-2025` → `27-03-2025`).
* **Room** – Filter by a room code (example: `D21`).
* **Activity Type** – Filter by the type of action (example: updates, releases).
* **Search** – Run the search with the selected filters.
* **Clear** – Reset filters back to default values.

#### Activity Log Table

Each row represents one logged action:

* **Change Date & Time** – Timestamp of the change.
* **User** – The user who performed the change.
* **Activity** – Action type (example: `Update Hotel Allotment`).
* **Room Code** – The affected room (example: `D21`).
* **Property Name** – The field that changed (example: `GuaranteedRoomsNo`).
* **Original Value** – Value before the change (example: `20`).
* **New Value** – Value after the change (example: `10`).
* **Description** – Extra context, if available.

### Allotment history (per day)

For a day-by-day view, use **Allotment History** in **Allotments per day**.

* Go to **Hotel → Allotments per day** ([Allotments per day](allotments-per-day/)).
* Click **Allotment History**.
* Review the chronological list of create/update/delete actions.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### What you’ll see

The **Allotment History** screen is a detailed audit trail of allotment changes.

It shows when allotments were created, updated, or deleted, and what changed.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Filters (top of the page)

* **Change Date** – Date range when the change was made (e.g., 01-04-2025 → 01-10-2025).
* **Period** – The actual stay period affected by the allotment (e.g., 02-10-2025 → 02-11-2025).
* **Room** – Allows filtering by specific room code.
* **Activity** – Filters the type of action (Create, Update, Delete).
* **Display Names** – Shows user-friendly names instead of room codes.

***

#### Table columns

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

### How to use

1. Open the **Activity Log** section.
2. Apply filters to narrow results:
   * Set a **Change Date range**.
   * Select a **Room** (optional).
   * Choose an **Activity Type** (optional).
3. Click **Search** to view filtered results.
4. Review the **Activity Log** rows to track changes.
5. Use **Clear** to reset filters and start a new search.
6. For a day-by-day view, use **Allotments per day → Allotment History**.

### FAQ

<details>

<summary>What’s the difference between <strong>Activity Log</strong> and <strong>Allotment History</strong>?</summary>

**Activity Log** gives a quick audit of availability changes.

**Allotment History** is designed for a day-by-day audit trail in **Allotments per day**.

</details>

<details>

<summary>Why don’t I see any results?</summary>

Widen the **Change Date** range.

Clear the **Room** filter.

Verify the hotel has allotments in the selected period.

</details>

<details>

<summary>What does <strong>Property Name</strong> mean?</summary>

It’s the exact field that changed in the allotment record.

Use it to understand what was edited, not just that something changed.

</details>

<details>

<summary>Why do I see multiple rows for the same room and time?</summary>

A single user action can update several fields.

Each field change can be logged as a separate row.

</details>
