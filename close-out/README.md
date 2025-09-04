# Close Out

### Overview

The **Close Out** functionality is used to restrict availability for specific transports, destinations, resorts, hotels, or room types within a selected time period. This ensures that no new bookings can be made for the defined combinations once a close-out rule is applied.

### Purpose

This feature is used by **travel coordinators, back-office staff, and product managers** to:

* Define and review **Close Out rules** that affect sales and availability.
* Filter and identify rules by date range, transport, destination, hotel, or room type.
* Confirm when and by whom rules were created.
* Quickly enable/disable rules or edit them when required.

### Preconditions

* The user must have access rights to the **Hotel → Close Out** menu.
* Close-out rules should be created carefully, as they may override availability settings in other modules.
* Relevant transport, hotel, or room type must already exist in the system.

### **Step-by-Step Instructions**

#### **Step 1: Access Close Out**

* Navigate to the **Hotel menu**.
* Confirm that the **Close Out** option is displayed right below **Stop Sales**.

#### **Step 2: Open Close Out Page**

* Click on **Close Out**. - The **Close Out page** opens, showing all defined rules.
* Each rule has a dedicated **Edit** button.
* Rules are created on **company level** (not per brand).

Step 3: Fields

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

*   **Apply Filters**

    Fill in the required fields to refine search:

    * **Start date** (default today)
    * **End Date** (default one year ahead)
    * **Transport type** (multi-select)
    * **Transports** (multi-select, with options: _Select all_, _Show hidden_, _Show code_; default display by name; _Show code_ displays only code)
    * **Destination** (multi-select, options: _Select all_, _Show code_)
    * **Resort** (multi-select, options: _Select all_, _Show hidden_, _Show code_)
    * **Hotel** (multi-select, options: _Select all_, _Show hidden_, _Show code_)
    * **Room type** (multi-select, options: _Select all_, _Show hidden_, _Show code_)
* Display Results

| **Field/Option**          | **Description**                                                            |
| ------------------------- | -------------------------------------------------------------------------- |
| **Start Date / End Date** | Date interval for rule validity (departure date range).                    |
| **Transport Type**        | Filters rules by type of transport (e.g., charter, dynamic).               |
| **Transports**            | Specific transports where rule applies;                                    |
| **Destination**           | Destination filtering                                                      |
| **Resorts**               | Filter by resort                                                           |
| **Hotels**                | Filter by hotel;                                                           |
| **Room Type**             | Filter by specific room types;                                             |
| **Note**                  | Additional description set on the rule (truncated, full text on hover).    |
| **Enabled**               | Shows whether the rule is active.                                          |
| **Created / Created By**  | Date, time, and user who created the rule. Username links to user details. |
| **Display Button**        | Executes the filter search.                                                |
| **Clear Button**          | Removes all applied filters and reloads full list.                         |
| **Pagination**            | Navigates results (25 rules per page by default).                          |

#### **Step 4: Explore/Sort Results (Optional)**

* Navigate through multiple pages using **pagination**.
* Sort results by **Start Date** or **End Date** (ascending/descending).

#### **Step 5: Clear Filters**&#x20;

* Click **Clear** to reset all filter inputs.

### Notes

* Each rule is displayed in the list with details such as **Start Date, End Date, Transport, Destination, Resort, Hotel, Room Type, Note, Status (Enabled/Disabled), Created Date, and Created By**.
* Rules can be enabled/disabled or edited later if adjustments are needed.
* Filtering by **brand** is not available, as close-outs are created on company level.
