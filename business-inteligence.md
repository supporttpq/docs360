# Business Intelligence – Allotment Overview

#### **Overview**

The _Business Intelligence – Allotment Overview_ page provides a visual overview of hotel allotment availability and usage across a selected period.\
It enables users to monitor the distribution and occupancy of room allotments per hotel and room type, displayed in a day-by-day grid format.\
The page offers insight into remaining capacities, highlighting potential shortages or overbooked periods.

#### **Purpose**

The purpose of this report is to:

* Give a clear overview of daily allotment usage for all hotels within a transport or resort.
* Help identify dates or hotels with high occupancy or zero availability.
* Provide an overview of total commitments and remaining capacities at a glance.
* Assist in monitoring bed and room utilization for operational and commercial planning.

#### **Preconditions**

Before using the _Allotment Overview_ report:

1. **Hotel allotments** and **departure stat weeks** must be defined for the selected year(s) and period.
2. Ensure the **transport, resort, and hotels** have valid allotment data configured in the system.
3. The user must have access to the **Business Intelligence** module.

{% hint style="warning" %}
💡 **Tip:** To have results listed according to the filters set, make sure departure stat weeks are defined for the year(s) used. See here how: [Departure stat weeks](setup/departure-stat-weeks.md)
{% endhint %}

**Note:** Cells highlighted in **red** indicate a **stop sale** for that date.

#### **Field Descriptions and Sections**

<figure><img src=".gitbook/assets/image (427).png" alt=""><figcaption></figcaption></figure>

**1. Filters (Top Section)**

* **Transport:** Defines the transport code associated with the departure and arrival combination.\
  &#xNAN;_&#x45;xample:_ BLLCHQ-A7-7M.
* **Real Transport:** Allows selection of a specific real transport (actual flight or transfer connection) used in the calculation.
* **Resort:** Selects the destination resort area to display hotels within that region.\
  &#xNAN;_&#x45;xample:_ CHQ–AGI3 – Agii Apostoli.
* **Hotel:** Filters data for a specific hotel or shows all available hotels within the selected resort.
* **Room:** Displays data for a particular room type or all rooms combined.
* **Date Period:** Defines the date range of the overview.\
  &#xNAN;_&#x45;xample:_ 01-09-2025 → 30-09-2025.
* **Rooms No / Beds No:** Enables or disables the display of rooms and beds in the report.
* **Show Guarantee Beds:** Displays guaranteed bed allocations when enabled.
* **Display / More Filters / Clear:**
  * **Display:** Loads the data for the chosen filter selection.
  * **More filters:** Expands additional configuration filters.
  * **Clear:** Resets all filters to default.

***

#### **2. Data Grid (Main Table)**

The main section displays a **calendar-style grid** with rows representing hotels and room types, and columns representing dates within the selected period.

| **Column / Element**        | **Description**                                                                                             |
| --------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **Hotel Name**              | The name of the hotel displayed on the left-hand side.                                                      |
| **Room / Allotment Type**   | Indicates room types and their associated allotment identifiers (e.g., “1/21 ALL”, “2/22-P ALL”).           |
| **Daily Columns (1–30)**    | Each column represents one day within the selected month. Values show available beds or rooms for that day. |
| **Highlighted Cells (Red)** | Indicates a **stop sale** for that date                                                                     |
| **“Sum ALL” Rows**          | Aggregated totals for each hotel across the selected date range.                                            |

#### Allotment Information

1. **Bed Number -** Shows the number of beds available for the selected period.
2. **Rooms Number -** Displays all rooms available for sale during the selected period.
   * Optionally, check **Show only parent room** to filter parent rooms only.
3. **Guarantee Rooms -** By checking the **Guarantee Rooms** box, guaranteed room numbers are displayed **below the allotment line** for each room.

<figure><img src=".gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
