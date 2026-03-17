---
description: >-
  Schedule automatic Excel (XLSX) exports in Tourpaq Office. Create recurring
  booking/cost reports (daily, weekly, monthly), manage schedules, and download
  the latest export result.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# Export - Scheduled Reports

### Overview

**Export schedules** let you automate recurring **Excel (XLSX) exports** from Tourpaq Office.

Schedule booking, discount, cost, or finance reports to run **daily**, **weekly**, or **monthly**, based on your export filters (booking and departure periods).

This is used for **scheduled reports** and **recurring exports** without manual downloads.

### Purpose

This functionality helps users save time and maintain consistency by:

* Automating repetitive export tasks.
* Generating updated reports on a fixed schedule (daily/weekly/monthly).
* Supporting common periods like yesterday, last 7 days, last week, and last month.
* Keeping all scheduled exports in one place for monitoring and download.

***

### Export scheduling options

<figure><img src="../.gitbook/assets/image (8) (3).png" alt="Export schedules actions next to the Export button"><figcaption><p>Use schedules to view existing exports, create a new schedule, and manage recurring XLSX reports.</p></figcaption></figure>

Using the buttons next to **Export**, you can:

* **View** all previously scheduled exports
* **Create** new export schedules based on selected filters

### Page structure and fields

<figure><img src="../.gitbook/assets/image (9) (3).png" alt="Export filters and schedules table"><figcaption><p>Top: export filters. Bottom: the schedules table where you enable, configure, and download scheduled exports.</p></figcaption></figure>

#### Export filters (top section)

These filters define the base parameters for what will be included in the exported data.

| Field                               | Description                                                                       |
| ----------------------------------- | --------------------------------------------------------------------------------- |
| **Export Type**                     | Defines the format and type of data to export. Example: **Bookings (XLSX)**.      |
| **Booking Start / Booking End**     | Specifies the booking date range to include in the export.                        |
| **Departure Start / Departure End** | Specifies the departure date range (optional filters).                            |
| **+ More filters / Clear**          | Additional filtering options can be added; the “Clear” button resets all filters. |
| **Export**                          | Runs the export immediately based on the current filters.                         |

***

#### Schedules section

This table lists all configured automatic exports. Each row represents a schedule with customizable options.

| Column                          | Description                                                                                                             |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **Enabled**                     | Checkbox to activate or deactivate the schedule. Only enabled schedules will run automatically.                         |
| **Description**                 | A user-defined name or label for the schedule (e.g., “test15Mel”). Useful for identifying different exports.            |
| **Schedule Type**               | How often the export runs: **Once a day**, **Once a week**, or **Once a month**.                                        |
| **Departure**                   | Which departure period the export covers: **Custom**, **Yesterday**, **Last 7 days**, **Last week**, or **Last month**. |
| **Day**                         | When the export runs. Monthly schedules use a day of month (1–31). Weekly schedules use a weekday (for example Monday). |
| **Get Latest Result (🗎 icon)** | Opens or downloads the latest generated export file for this schedule.                                                  |
| **Delete (🗑️ icon)**           | Removes the selected schedule.                                                                                          |

***

### Export button (top right)

Initiates a **manual export** using the current filters and options selected, independent of the schedule.

### Instructions

1. **Add a New Schedule**
   * Click on the last empty row in the schedule list.
   * Enter a **Description** (e.g., “Monthly Booking Export”).
   * Choose a **Schedule Type** (daily, weekly, monthly).
   * Define the **Departure** period:
     * **Custom**: use the filters you set in the top section. Depending on your setup, Custom schedules can generate separate exports (for example Bookings and Cost).
     * **Yesterday**: export for the previous day.
     * **Last 7 days**: rolling 7-day export.
     * **Last week**: previous calendar week export.
     * **Last month**: previous calendar month export.
   * Select the appropriate **Day** for the export.
   * Check **Enabled** to activate it.
2. **Disable or Delete a Schedule**
   * Uncheck **Enabled** to pause an export without deleting it.
   * Click the **🗑️** icon to permanently remove a schedule.
3. **Manual Export**
   * Use the filters in the top section and press **Export** to generate a one-time file manually.

***

### Notes

* Only **enabled** schedules will run automatically.
* You can manage multiple schedules for different purposes (e.g., weekly sales, monthly statistics).
* Ensure your selected **Export Type** supports the desired data format.
* Schedules are generated once per day at a time set by the Super Admin (usually at night).
* Download the latest scheduled file using **Get Latest Result**.

The exact runtime is configured centrally. It can vary by environment and setup.

### Daily finance export file

Some setups generate a separate **Finance export file** on a fixed nightly run.

Email recipients for the finance export can be configured in `Setup → System Setup → General Information → Settings`.

<figure><img src="../.gitbook/assets/image (352).png" alt="Finance export schedule configuration"><figcaption><p>Finance export configuration: recipients and scheduling are maintained separately from Export schedules.</p></figcaption></figure>

* Each user only sees the schedules they created.
* Changing filters does not update existing schedules. Create a new schedule if the filters change.
