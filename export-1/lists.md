# Lists

### Overview

The **Export/Lists module** in Tourpaq Office allows administrators to generate and schedule exports of booking-related data tailored to specific operational needs. The module supports multiple export types (hotel, passenger, rooming, guide, canceled bookings, and booking changes) and can be used **manually** or with **automated scheduling**.

***

### Purpose

The purpose of this module is to:

* Provide a centralized interface for generating structured booking reports.
* Allow filtering of exports based on various parameters (dates, hotels, rooms, transports, etc.).
* Enable scheduled automatic delivery of reports via email.
* Facilitate communication with hotel partners, guides, airline staff, and internal departments.

***

### Access & Availability

* **Role required**: Administrator
* **Location in UI**: `Export → Lists`

***

### Preconditions

Before using this module:

* User must be assigned the Administrator role.
* Bookings and travel data should exist in the system.
* Export templates and system settings should be preconfigured.
* Email templates and recipients must be properly set for scheduled exports.

***

### Fields & Filters – Export Generation

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

| Field                  | Description                                                                                       |
| ---------------------- | ------------------------------------------------------------------------------------------------- |
| **Report type**        | Choose the export format (see Report Types below).                                                |
| **Arrival period**     | Filters bookings based on **arrival at destination** date range.                                  |
| **Booking period**     | Filters bookings based on **booking creation date**.                                              |
| **Stay period**        | Filters bookings by actual **hotel stay period**.                                                 |
|  Cancel **from**       | Limits **canceled bookings** to those canceled on or after the selected date.                     |
| **Changes since**      | Filters bookings to show only those **changed** after the selected date. Used for “Changes List”. |
| **Transport**          | Select one or more **transport options** (as defined in the booking).                             |
| **Real transport**     | Filter by **real, physical transport services** (e.g., actual bus, flight identifiers).           |
| **Country**            | Filter by one or more **destination countries**.                                                  |
| **Resort**             | Select one or more **resorts** to include bookings from.                                          |
| **Hotel**              | Filter by specific hotels.                                                                        |
| **Room**               | Filter by room type or room codes.                                                                |
| **Columns for export** | Allows selection of specific fields to include in the export.                                     |
| **Compress as ZIP**    | When checked, the exported file will be compressed in `.zip` format.                              |

***

### Report Types Explained

| Report Type             | Description                                                                                                                      |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **Hotel list**          | Bookings grouped by hotel → stay period → room type. Shows room placement and booking totals.                                    |
| **Rooming list**        | Like hotel list, but includes **individual passenger details** (name, age, gender, flight info, extras).                         |
| **Guide list**          | Guide-friendly list with passenger contacts, extras, transfer info, comments, and hotel preferences.                             |
| **Passenger list**      | Flat list of all passengers grouped by **transport interval**, used by airlines or transport providers.                          |
| **Ccl. Bookings List**  | List of canceled bookings matching filter criteria, grouped by hotel, stay, and room type.                                       |
| **Departure Homebound** | Typically used to list passengers returning from holidays.                                                                       |
| **Changes List**        | Tracks all booking changes (e.g., passenger name change, hotel/resort/room changes, extras added/removed) after a selected date. |
| **Transfer List**       | Shows which bookings/passengers have included transport transfers.                                                               |
| **Airport List**        | Export focused on flight/airport-related logistics.                                                                              |
| **Fast Checking**       | Likely used for rapid identity or room allocation validation (company-specific).                                                 |
| **Air List**            | Export for airline use, possibly for check-in or manifest purposes.                                                              |
| **Bus List**            | Export of passengers grouped by bus transport for logistics.                                                                     |
| **Label List**          | Generates label data for baggage, room doors, or luggage tags.                                                                   |

***

### Scheduled Export

You can **automate exports** by setting up schedules.

<figure><img src="../.gitbook/assets/image (23) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Fields

| Field             | Description                                                                                                                                                                                                     |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Enabled**       | When checked, the export schedule becomes active and will begin sending automatically. Schedules not used in 7 days are automatically disabled. For a schedule to be considered used click " Get Latest Result" |
| **Description**   | Textual description of the purpose or content of the export.                                                                                                                                                    |
| **Schedule type** | Choose the recurrence:                                                                                                                                                                                          |
|                   | → Once per day                                                                                                                                                                                                  |
|                   | → Once per week                                                                                                                                                                                                 |
|                   | → Once per month                                                                                                                                                                                                |
| **Day**           |                                                                                                                                                                                                                 |
|                   | → If **weekly**, choose day of the week (e.g., Monday).                                                                                                                                                         |
|                   | → If **monthly**, choose a specific day (e.g., 15th).                                                                                                                                                           |

#### Behavior

* Email is automatically sent to preconfigured recipients.
* Uses same filters and report settings as the on-demand export.
* File format is the same (`Excel XML`), and can be compressed as ZIP.

***

### UI Buttons / Actions

| Button             | Action                                                                                  |
| ------------------ | --------------------------------------------------------------------------------------- |
| **Export**         | Immediately generates an export file based on current filter and sends or downloads it. |
| **Show schedules** | Displays existing scheduled exports and allows editing or creating new ones.            |

