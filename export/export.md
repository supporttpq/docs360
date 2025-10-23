# Export - Scheduled Reports

### **Overview**

The **Export – Schedules** allows users to configure and manage automatic data exports from the system. Exports can be scheduled to run at specific intervals (daily, weekly, or monthly), using predefined filters such as booking or departure dates. The purpose of this page is to automate report generation and distribution, ensuring that data is consistently updated and available without manual export actions.

### **Purpose**

This functionality helps users save time and maintain consistency by:

* Automating repetitive export tasks.
* Ensuring data reports (e.g., bookings, departures) are generated regularly.
* Allowing different configurations for various reporting needs (e.g., last week, last month, custom ranges).
* Managing and monitoring all scheduled exports from a single view.

***

### **Export Scheduling Options**

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

Using the three buttons located next to the **Export** button, you can:

* **View** all previously scheduled exports
* **Create** new export schedules based on selected filters

#### **Page Structure and Fields**

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

**Export Filters (Top Section)**

These filters define the base parameters for what will be included in the exported data.

| Field                               | Description                                                                       |
| ----------------------------------- | --------------------------------------------------------------------------------- |
| **Export Type**                     | Defines the format and type of data to export. Example: **Bookings (XLSX)**.      |
| **Booking Start / Booking End**     | Specifies the booking date range to include in the export.                        |
| **Departure Start / Departure End** | Specifies the departure date range (optional filters).                            |
| **+ More filters / Clear**          | Additional filtering options can be added; the “Clear” button resets all filters. |
| **Export**                          | Runs the export immediately based on the current filters.                         |

***

**Schedules Section**

This table lists all configured automatic exports. Each row represents a schedule with customizable options.

| Column                          | Description                                                                                                                                                                                  |
| ------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Enabled**                     | Checkbox to activate or deactivate the schedule. Only enabled schedules will run automatically.                                                                                              |
| **Description**                 | A user-defined name or label for the schedule (e.g., “test15Mel”). Useful for identifying different exports.                                                                                 |
| **Schedule Type**               | Defines how often the export runs. Options include:• **Once a day**• **Once a week**• **Once a month**                                                                                       |
| **Departure**                   | Specifies which departure period the export will cover. Options include:• **Custom**• **Last month**• **Last week**• **Last 7 days**• **Yesterday**                                          |
| **Day**                         | Defines the exact day or frequency when the export should occur.Examples:• For monthly schedules: day of the month (1–31).• For weekly schedules: a specific weekday (e.g., Monday, Friday). |
| **Get Latest Result (🗎 icon)** | Opens or downloads the latest generated export file for this schedule.                                                                                                                       |
| **Delete (🗑️ icon)**           | Removes the selected schedule.                                                                                                                                                               |

***

### **Export Button (Top Right)**

Initiates a **manual export** using the current filters and options selected, independent of the schedule.

#### **Instructions**

1. **Add a New Schedule**
   * Click on the last empty row in the schedule list.
   * Enter a **Description** (e.g., “Monthly Booking Export”).
   * Choose a **Schedule Type** (daily, weekly, monthly).
   * Define the **Departure** period:&#x20;
     * Custom - use the filters set in the general field without Export Type.  The export will generate 2 different exports (one for Booking and one for Cost);
     * Yesterday - will generate an export from the previous day before the day when the scheduler was created;
     * Last 7 days - Used for weekly reports, exporting the last 7 days
     * Last week -  Used for weekly reports, exporting the previous week
     * Last month - Used for monthly reports, exporting last month.
   * Select the appropriate **Day** for the export.
   * Check **Enabled** to activate it.
2. **Disable or Delete a Schedule**
   * Uncheck **Enabled** to pause an export without deleting it.
   * Click the **🗑️** icon to permanently remove a schedule.
3. **Manual Export**
   * Use the filters in the top section and press **Export** to generate a one-time file manually.

***

#### **Notes**

* Only **enabled** schedules will run automatically.
* You can manage multiple schedules for different purposes (e.g., weekly sales, monthly statistics).
* Ensure your selected **Export Type** supports the desired data format.
* Each schedule is generated only once a day (the time is set by the Super Admin and is usually at night). The resulting file can be downloaded manually using the Get Latest Result button.

The finance export file is generated each night but, the export is dependent on the schedule set, e.g daily, yes, then it is for this night, but if weekly it will take the export from that specific, day scheduled in the schedule. The Super Admin collaborates with the developer to determine the specific hour for scheduling tasks.&#x20;

### Daily export of  the Financial Export

Additionally, the scheduling of the Finance export file is separate from the time set for the scheduler. It is also worth noting that email addresses for the Finance Export can be configured in Setup / System Setup / General Information / Settings.&#x20;

<figure><img src="../.gitbook/assets/image (352).png" alt=""><figcaption></figcaption></figure>

* Each user only sees the schedulers defined by him/her (he/she cannot see other schedulers defined by other users).
* The filters set do not affect already created schedulers. They can only be generated with the Export button, or to create a new scheduler using the filters.
