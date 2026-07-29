# Daily Programs

## Daily Programs

### Overview

The **Daily Programs** module manages and organizes daily itineraries associated with different travel products.\
Each program is defined with a unique code, name, and validity interval.

### Purpose

* To provide structured daily itineraries for tours, packages, or destinations.
* To ensure that programs are valid only during defined travel periods.
* To simplify the management of multiple programs across different destinations.

### Requirements

* Permissions to view and manage Daily Programs.
* Programs should be linked to relevant offers or packages where applicable.

### Interface overview

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1).png" alt="Daily Programs overview page"><figcaption></figcaption></figure></div>

#### Filters

Filter Daily Programs by:

* **Code** – Enter the program’s unique code.
* **List name** – Search by program name.
* **From date** / **To date** – Filter by program validity interval.
* **Display** – Applies the selected filters.
* **Clear** – Resets all filters.

#### Table columns

| Column       | Description                                           |
| ------------ | ----------------------------------------------------- |
| **Code**     | Unique identifier for the daily program.              |
| **Name**     | The descriptive name of the daily program.            |
| **Interval** | Start and end date during which the program is valid. |

#### Actions

* **Create** – Opens a form to create a new daily program.
* **Delete (🗑️)** – Removes the selected program permanently.
* **Copy (📑)** – Creates a duplicate of the selected program, which can be modified.

#### Pagination

Select the number of records displayed per page, for example 25.

### Create a daily program

#### Overview

The **New Daily Program** page is used to create and configure a new daily itinerary.\
Each program must have a unique code, a descriptive name, and a validity period (start and end date).

This information defines the availability of the program and ensures that it can be linked to travel offers and packages within the system.

#### Field descriptions

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="New Daily Program fields"><figcaption></figcaption></figure></div>

| Field            | Description                                                | Notes                                           |
| ---------------- | ---------------------------------------------------------- | ----------------------------------------------- |
| **Code**\*       | Unique identifier for the program (e.g., BCH).             | Mandatory. Must be unique.                      |
| **Name**\*       | Descriptive title of the program (e.g., “Bucharest Tour”). | Mandatory. Shown in listings and linked offers. |
| **Start Date**\* | The date when the program becomes active.                  | Mandatory. Selected using the date picker.      |
| **End Date**\*   | The date when the program expires.                         | Mandatory. Selected using the date picker.      |

\*Mandatory fields must be completed before saving.

#### Workflow

1. Go to **Daily Programs** → **Create**.
2. Enter a unique **Code**.
3. Enter a **Name**.
4. Set **Start Date**.
5. Set **End Date**.
6. Click **Save**.

The program appears in the **Daily Programs** list after saving. It can then be edited or linked to offers.

### Days tab

The **Days** tab defines the daily itinerary for a program. Each row represents one day.

#### Field descriptions

1. **Day No.**
   * Represents the sequential number of the day in the program (e.g., 1 for the first day, 2 for the second).
   * Used for ordering the activities chronologically.
   * This number is automatically assigned but can be edited if needed.
2. **Title**
   * A short title summarizing the activity planned for that day.
   * Should be concise and easy to understand at a glance.
3. **Latitude**
   * The geographical latitude of the activity location.
4. **Longitude**
   * The geographical longitude of the activity location.
5. **Description**
   * A detailed explanation of the activity for the given day.
   * Can include information such as the purpose of the visit, special instructions, or highlights.
   * Example: _Visit Bucharest Opera for a guided cultural experience_.
6. **Photos**
   * A link to view and manage photos associated with that day’s activity.
   * Clicking **View Photos** opens the photo gallery for the selected day.
   * Helps visually represent what the participants will experience.

#### Actions

* **Edit (✎ icon)**\
  Opens the edit mode for the selected day, allowing you to update the title, description, location, and photos.
* **Delete (🗑️ icon)**\
  Permanently removes the day from the program. Use with caution, as this action cannot be undone.
* **Add Day (button)**\
  Creates a new entry in the daily program. The system will automatically assign the next available **Day No.**, but this can be adjusted.

### Resources

Resources assign specific availability to the Daily Program.

#### Field descriptions

* **Arrivals**
  * Dropdown list where you can select arrival airports
* **Resorts**
  * Dropdown list of available resorts.
  * Used to assign the resort where the guests are staying or activities are planned.
* **Hotels**
  * Dropdown list of hotels connected to the brand and resort.
  * Defines which hotel the daily program applies to.
* **Rooms**
  * Two dropdown lists for selecting specific room types and categories.
  * Helps in managing room allocation for the daily program.
