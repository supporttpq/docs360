# Tee Time extras list

### Overview

The **Tee Time Export** feature in Tourpaq Office is used to generate structured reports related to golf tee time bookings. It allows users to filter and export data based on supplier, booking details, arrival periods, extras, and more. This tool is valuable for operational teams and golf course suppliers who manage tee time reservations.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Purpose

This tool is designed to:

* Provide real-time and accurate tee time data to suppliers.
* Export booking information filtered by date, supplier, extras, and categories.
* Allow flexible report customization and format selection.
* Support data delivery in ZIP-compressed format for easier sharing or archiving.

***

### Availability

* **User Role**: Administrator only
* **Module Location**: `Export → Tee Time Export`

***

### Main Sections & Field Explanations

#### Supplier Dropdown

* **Function**: Select a specific **golf supplier** or choose **All suppliers**.
* **Use case**: Useful when generating reports for a single golf partner.

***

#### Report Type Dropdown

* **Function**: Select the **format or version** of the report.
* **Examples**: Excel report, PDF version, supplier-customized template.
* **Note**: Templates are pre-configured based on supplier expectations.

***

### Filtering Options

| Filter                               | Description                                                                                 |
| ------------------------------------ | ------------------------------------------------------------------------------------------- |
| **Arrival Period (Start/End Dates)** | Filters bookings based on **check-in/stay** dates.                                          |
| **Booking Period (Start/End Dates)** | Filters bookings created during this interval.                                              |
| **Display All Extras**               | When checked, includes **all extra items or services** (e.g., golf cart, caddy, equipment). |
| **Compress as ZIP**                  | When checked, exports the file as a compressed `.zip` archive.                              |

***

### Customization Options

#### Categories Section

* **Function**: Allows filtering by **specific extra categories**, such as:
  * Tee times
  * Transfer
  * Udflugter

***

#### Extras Section

* **Function**: Lets you include or exclude specific extras from the export.
* **Use case**: Export only tee times **with or without** particular items.

***

#### Columns for Export Section

* **Function**: Lets the user **customize the columns** that appear in the final export file.

***

### Action Button

| Button     | Description                                                                              |
| ---------- | ---------------------------------------------------------------------------------------- |
| **Export** | Initiates the export process using the selected filters, customization, and report type. |

***

### Export Button

**Purpose:** Generates and downloads the export file based on your selected filters.

* After setting all filters and options, click **Export** to generate the file.
* The file will be downloaded automatically in **.XLS**  / **PDF** format.

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The export file include the following columns:

| Column                  | Description                                                                              |
| ----------------------- | ---------------------------------------------------------------------------------------- |
| **Date**                | The date when the tee time is scheduled.                                                 |
| **Tee Time**            | The specific time slot available for booking (e.g., 08:00, 08:08, etc.).                 |
| **Status**              | Indicates the availability of the slot (e.g., _Available_, _Reserved_).                  |
| **Booking No**          | Displays the booking reference number if the tee time is already reserved.               |
| **Hotel Name**          | Shows the hotel linked to the booking, if applicable.                                    |
| **Agency**              | The agency that made or manages the booking.                                             |
| **Name**                | The name of the customer or booking contact.                                             |
| **Status (Booking)**    | Shows the booking state, such as _Confirmed_, _Pending_, or _Cancelled_.                 |
| **Confirmed by Agency** | Indicates whether the booking has been confirmed by the agency managing the reservation. |

### Tips&#x20;

* Always double-check the **supplier** and **date filters** to ensure data relevance.
* Use **“Display All Extras”** to prevent missing tee-time-related extras.
* For recurring supplier needs, confirm the preferred **report format** (e.g., PDF, Excel).
* Use **ZIP compression** when sending large reports by email or uploading to portals.
