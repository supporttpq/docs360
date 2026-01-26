# Editable releases in Allotment per Day

### Overview

**Allotment per Day** lets you override hotel release values per room and date.

Use it when release deadlines change late, or when a release must be undone.

### Purpose

Use editable releases to:

* Change the **DAYS** value per date (release deadline).
* Undo a release by unchecking **R**.
* Restore rooms (fully or partially) using **AR** and **SR**.
* Override contract-level release settings for specific dates.

This is operational tooling. It avoids changing the underlying contract.

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### Screen structure

The screen is divided into three main areas:

1. Search and control area (top)
2. Allotment table (center)
3. Release columns (grouped inside the table)

### 1. Search and control area

* **Period**: Date range shown in the table.
* **Room Type**: Filter by one room type. Leave blank for all.
* **Week Days**: Optional weekday filter.
* **Search**: Loads allotment data for the selected filters.
* **Search with Stay Length**: Applies stay-length logic. This search does **not** include transports.
* **Search with Allotment Control**: Includes full allotment control logic and **includes transports**.
* **Display Names**: Toggles between internal codes and readable names.
* **Save**: Saves changes.
* **Cancel**: Discards unsaved changes.
* **Allotment History**: Opens the change log for this hotel and period.

### 2. Allotment table – common columns

These columns are standard availability data:

* **Room Type**: Room category for the row.
* **Date**: Arrival date.
* **Day**: Day of week.
* **No.**: Total rooms allocated for that date.
* **Secured**: Secured rooms. Not automatically released.
* **Guaranteed**: Rooms you pay for, regardless of sales.
* **Book**: Rooms already booked.
* **Free**: Rooms available to sell.

### 3. RELEASE section

The **RELEASE** header groups all release-related columns.

These columns have a grey background to separate them from availability data.

Release handling here applies to **daily releases only**.

#### Field reference (release columns)

**DAYS**: Days before arrival when the release is executed.

* Initial value comes from the Release rule in the contract
* Editable if a release rule exists
* Empty and not editable if no release rule is defined
* Can be changed to extend or shorten the release deadline

**R**: Release executed flag.

* Checked: the release is executed
* Unchecked: the release is not executed or has been undone
* Unchecking **undoes the release** and makes **AR** and **SR** editable

**AR (Allotment Released)**: Number of **allotment rooms** released.

* Filled automatically when a release is executed
* Editable only when undoing a release
* Controls how many allotment rooms are restored

**SR (Secured Released)**: Number of **secured rooms** released.

* Filled automatically when a release is executed
* Editable only when undoing a release
* Controls how many secured rooms are restored

**PAX1–PAX4**: Max rooms by occupancy (1–4 pax).

* Used for pax-based control and limits per room.

**MIN**: Minimum stay (nights).

### How to work with releases

#### Execute a release

1. Ensure **DAYS** has the correct value.
2. Wait for the automated daily release to run. See [Hotel release - Reporting](../releases/hotel-release-reporting.md).
3. Confirm the **R** checkbox becomes checked.
4. Confirm **AR** and **SR** are filled with released values.

### Release logic

* When a release is executed, the system stores how many **allotment** and **secured** rooms were released
* When a release is revoked:
  * Rooms are restored by default
  * AR and SR become editable to allow partial restoration
* Allotment per Day values override the release defined in the contract

#### Undo a release

1. Uncheck **R**.
2. Edit **DAYS** if you need a new release deadline.
3. Adjust **AR** and **SR** to control how many rooms to restore.
4. Click **Save**.

By default, undoing a release restores all released rooms unless adjusted.

***

### Bulk updates (Change Value tool)

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

The Change Value tool can be used to:

* Edit **DAYS** for multiple rows
* Uncheck **R** for multiple rows
* Adjust **AR** and **SR** for multiple rows

This is useful when correcting releases across many dates or room types.

***

### Activity log

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

All changes made to release data in Allotment per Day are logged.

* Activity name: **Release update**
* Includes changes to **DAYS**, **R**, **AR**, and **SR**
* Used for auditing and troubleshooting

***

### Permissions

Release columns are visible and editable only if the user or supplier has:

* Access to Allotment per Day
* Access to Release management

Without both rights, release data is hidden or read-only.

### FAQ

<details>

<summary>Why is <strong>DAYS</strong> empty or not editable?</summary>

There is no release rule on the contract for that room/date.

In that case, Tourpaq has nothing to override at day level.

</details>

<details>

<summary>What happens when I uncheck <strong>R</strong>?</summary>

You undo the release for that room/date.

Tourpaq restores rooms by default.

You can then fine-tune the restoration using **AR** and **SR**.

</details>

<details>

<summary>Can I restore only some rooms after undoing a release?</summary>

Yes.

Uncheck **R**, then edit **AR** and **SR** to restore a partial amount.

</details>

<details>

<summary>Does editing releases change the hotel contract?</summary>

No.

It only overrides release values per day in **Allotment per Day**.

</details>

<details>

<summary>Why can’t I see the release columns?</summary>

Your user (or supplier login) lacks one of these permissions:

* **Allotment per Day**
* **Release management**

</details>
