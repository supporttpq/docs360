# Daily Programs

### Overview

The **Daily Programs** module allows you to manage and organize daily itineraries associated with different travel products.\
Each program is defined with a unique code, name, and validity interval.&#x20;

### Purpose

* To provide structured daily itineraries for tours, packages, or destinations.
* To ensure that programs are valid only during defined travel periods.
* To simplify the management of multiple programs across different destinations.

### Preconditions

* User must have permissions to view and manage daily programs.
* Programs should be linked to relevant offers or packages where applicable.

<figure><img src=".gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

#### Filters

At the top of the page, you can filter daily programs by:

* **Code** – Enter the program’s unique code.
* **List name** – Search by program name.
* **From date** / **To date** – Filter by program validity interval.
* **Display** – Applies the selected filters.
* **Clear** – Resets all filters.

#### Table Columns

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

At the bottom of the table, you can select how many records to display per page (e.g., 25 / page).



## Create New Daily Program

### Overview

The **New Daily Program** page is used to create and configure a new daily itinerary.\
Each program must have a unique code, a descriptive name, and a validity period (start and end date).

This information defines the availability of the program and ensures that it can be linked to travel offers and packages within the system.

### Fields Description

<figure><img src=".gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

| Field            | Description                                                | Notes                                           |
| ---------------- | ---------------------------------------------------------- | ----------------------------------------------- |
| **Code**\*       | Unique identifier for the program (e.g., BCH).             | Mandatory. Must be unique.                      |
| **Name**\*       | Descriptive title of the program (e.g., “Bucharest Tour”). | Mandatory. Shown in listings and linked offers. |
| **Start Date**\* | The date when the program becomes active.                  | Mandatory. Selected using the date picker.      |
| **End Date**\*   | The date when the program expires.                         | Mandatory. Selected using the date picker.      |

\*Mandatory fields must be completed before saving.

### Workflow

1. Go to **Daily Programs** → **Create**.
2. Fill in the required fields:
   * Enter a unique **Code**.
   * Provide a **Name** for the program.
   * Set a **Start Date** and **End Date**.
3. Click **Save** to create the program.
4. Once saved, the program will appear in the **Daily Programs** list and can be further edited or linked to offers.

## **Daily Program – Days Tab**&#x20;

The **Days** tab allows you to define the daily itinerary for a program. Each row represents one day, with details about planned activities, descriptions, and related photos. Below is an explanation of each field:

***

#### **Fields Overview**

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

***

#### **Actions**

* **Edit (✎ icon)**\
  Opens the edit mode for the selected day, allowing you to update the title, description, location, and photos.
* **Delete (🗑️ icon)**\
  Permanently removes the day from the program. Use with caution, as this action cannot be undone.
* **Add Day (button)**\
  Creates a new entry in the daily program. The system will automatically assign the next available **Day No.**, but this can be adjusted.



## Resources Section

This section allows the user to assign specific resources to the daily program.&#x20;

### **Fields under Resources:**

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
