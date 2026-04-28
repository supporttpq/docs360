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

#### Export filters

#### Export Configuration (Top Section)

Used for:

* manual export
* defining filters for scheduled exports

Fields:

| Field                                                      | Description                          |
| ---------------------------------------------------------- | ------------------------------------ |
| Export Type                                                | Defines dataset (e.g. Bookings XLSX) |
| Booking Start / End                                        | Filters by booking creation date     |
| Departure Start / End                                      | Filters by travel date               |
| More Filters                                               | Additional filtering options         |
| Include Cancelled Bookings and Details                     | Includes cancelled bookings          |
| Include Moved Bookings and Details                         | Includes rebooked bookings           |
| Include past bookings with changes in the departure period | Tracks historical updates            |

***

#### Schedules section

Used to configure automated exports.

Each row represents a **scheduled export configuration**.

Each schedule contains:

| Column        | Description        | Behavior                             |
| ------------- | ------------------ | ------------------------------------ |
| Enabled       | Activates schedule | If unchecked → export will not run   |
| Description   | Custom name        | Should describe purpose              |
| Schedule Type | Frequency          | Monthly / Weekly / Daily             |
| Departure     | Time filter logic  | Defines data window (e.g. Last week) |
| Day           | Execution day      | Depends on schedule type             |

#### Schedule Types

**Daily**

* Runs every day
* Uses selected **Departure filter**

**Weekly**

* Runs once per week
* Requires **Day selection** (e.g. Wednesday)

**Monthly**

* Runs once per month
* Uses selected **Day (1–31)**

#### Departure Filter Logic

This field defines **what data is included**, not when it runs.

Examples:

| Value       | Meaning                  |
| ----------- | ------------------------ |
| Last month  | Data from previous month |
| Last week   | Data from previous week  |
| Last 7 days | Rolling window           |
| Yesterday   | One-day snapshot         |
| Custom      | Manual date logic        |

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

### Example Scenarios

#### Scenario 1 — Weekly Finance Report

* Schedule Type: Weekly
* Day: Monday
* Departure: Last week

Result:

* weekly dataset for accounting

***

#### Scenario 2 — Daily Operational Tracking

* Schedule Type: Daily
* Departure: Yesterday

Result:

* daily snapshot of bookings

***

#### Scenario 3 — Monthly Reporting

* Schedule Type: Monthly
* Day: 1
* Departure: Last month

Result:

* full monthly dataset

***

<img src="../.gitbook/assets/file.excalidraw (1) (1).svg" alt="Manual vs Schedule Export" class="gitbook-drawing">

### Common Mistakes

* Confusing **Departure** with execution date
* Forgetting to click **Save**
* Not enabling schedule
* Using wrong filters → incorrect exports
* Not checking auto-disabled schedules

{% hint style="warning" %}
Schedules not used for **7 days are automatically disabled**
{% endhint %}

***

### Troubleshooting

| Issue             | Cause                | Solution          |
| ----------------- | -------------------- | ----------------- |
| No file generated | Schedule disabled    | Enable schedule   |
| Wrong data        | Incorrect filters    | Review filters    |
| Empty export      | No data in period    | Adjust date range |
| Schedule stopped  | Auto-disabled        | Re-enable         |
| Missing bookings  | Filters exclude them | Check options     |

***

### Best Practices

* Use clear descriptions (e.g. “Weekly Finance Export”)
* Validate filters before saving
* Use “Last week” instead of fixed dates
* Monitor schedules weekly
* Avoid duplicate schedules

### Daily finance export file

Some setups generate a separate **Finance export file** on a fixed nightly run.

Email recipients for the finance export can be configured in `Setup → System Setup → General Information → Settings`.

<figure><img src="../.gitbook/assets/image (351).png" alt="Finance export schedule configuration"><figcaption><p>Finance export configuration: recipients and scheduling are maintained separately from Export schedules.</p></figcaption></figure>

* Each user only sees the schedules they created.
* Changing filters does not update existing schedules. Create a new schedule if the filters change.
