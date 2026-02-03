# Golf Course Report

### Overview

The **TeeTime List** tool allows you to generate export files containing information about golf course bookings.\
It is designed for reporting, analysis, and communication with golf course suppliers. You can filter bookings by supplier, period, and category, and export the results in Excel format.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Purpose

* To export golf course bookings within a defined period.
* To filter by supplier, arrival or booking dates, and category.
* To generate structured Excel files for internal use or for sending to partners.

***

### Instructions

#### 1. Supplier

**Purpose:** Filter the export by a specific supplier.

* Select a supplier from the dropdown list to include only that supplier’s bookings.
* Choose **All Suppliers** to export all available golf bookings.

***

#### 2. Report Type

**Purpose:** Defines the format and type of report to be generated.

* Select **Golf Course (XLS)** to create an Excel export of all tee time bookings.

***

#### 3. Arrival Period

**Purpose:** Filters bookings based on the passengers’ arrival date.

* Select a **Start** and **End** date to export only bookings where the arrival falls within this range.
* Leave blank to include all arrivals.

***

#### 4. Booking Period

**Purpose:** Filters by the date when the booking was created.

* Choose a **From** and **To** date (e.g., _29-09-2025 to 05-10-2025_).
* This is useful when you want to analyze recent golf course bookings.

***

#### 5. Categories

**Purpose:** Filters by golf-related categories.

* Lists all available categories (e.g., _Golf_, _Golf Courses_).
* Click **Edit** to include or exclude specific categories before export.

***

#### 6. Extras

**Purpose:** Includes or filters additional extras linked to the booking.

* **Show all**: displays all available extras.
* Click **Edit** to filter which extras (if any) should appear in the export.

***

#### 7. Columns for Export

**Purpose:** Allows you to select which columns (fields) should be included in the exported file.

* Click **Edit** to customize the output columns.
* Examples of columns you might include: Passenger Name, Golf Course, Round Date, Price, Supplier, etc.

***

#### 8. Additional Options

| Option                 | Description                                                                                |
| ---------------------- | ------------------------------------------------------------------------------------------ |
| **Display all Extras** | Includes all extras linked to the bookings in the export.                                  |
| **Compress as ZIP**    | Packages the exported Excel file into a ZIP archive. Useful when exporting large datasets. |
| **Use old export**     | Enables the legacy export format (for compatibility with older systems).                   |

***

#### 9. Export Button

**Purpose:** Generates and downloads the export file based on your selected filters.

* After setting all filters and options, click **Export** to generate the file.
* The file will be downloaded automatically in **.XLS** format.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The export file include the following columns:

| COLUMN NAME             | COLUMN                          |
| ----------------------- | ------------------------------- |
| GOLF COURSE             | Golf Course (Name of the Extra) |
| BOOKING NO              | Booking Number                  |
| GENDER                  | Passenger Gender                |
| NAME                    | Passenger Firstname & Surname   |
| HCP                     | Handocap                        |
| CLUB                    | Club                            |
| ROUND                   | Round number                    |
| REQUEST (Date & Time)   | Request time                    |
| CONFIRMED (Date & Time) | Confirmed time                  |



***

### Example Workflow

1. Set **Supplier** to _All Suppliers_.
2. Choose the **Report Type** → _Golf Course (XLS)_.
3. Select a **Booking Period** (e.g., 29-09-2025 to 05-10-2025).
4. Click **Edit** under _Columns for export_ to include Passenger, Golf Course, and Confirmed Time.
5. Check **Compress as ZIP** if you expect a large file.
6. Click **Export** to download the Excel report.

***

#### Notes

* The exported file can be shared with suppliers or used for performance tracking.
* Always verify the selected date range before export to avoid incomplete data.
* The **Edit** buttons allow full control of what is included in the final report.
