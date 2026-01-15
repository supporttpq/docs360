# Business Intelligence – Allotment Overview

#### **Overview**

The _Business Intelligence – Allotment Overview_ page shows hotel allotment availability and usage for a selected period.\
It helps you monitor remaining capacity per hotel and room type in a day-by-day grid.\
Use it to spot sold-out dates, stop sales, and capacity risks early.

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
💡 **Tip:** To have results listed according to the filters set, make sure departure stat weeks are defined for the year(s) used.\
See how to set them up here: [Departure stat weeks](../setup/departure-stat-weeks.md)
{% endhint %}

**Note:** Cells highlighted in **red** indicate a **stop sale** for that date.

#### **Field Descriptions and Sections**

<figure><img src="../.gitbook/assets/image (427).png" alt=""><figcaption></figcaption></figure>

**1. Filters (Top Section)**

* **Transport:** Defines the transport code associated with the departure and arrival combination. Example: `BLLCHQ-A7-7M`.
* **Real Transport:** Allows selection of a specific real transport (actual flight or transfer connection) used in the calculation.
* **Resort:** Selects the destination resort area to display hotels within that region. Example: `CHQ–AGI3 – Agii Apostoli`.
* **Hotel:** Filters data for a specific hotel or shows all available hotels within the selected resort.
* **Room:** Displays data for a particular room type or all rooms combined.
* **Date Period:** Defines the date range of the overview. Example: `01-09-2025 → 30-09-2025`.
* **Rooms No / Beds No:** Enables or disables the display of rooms and beds in the report.
* **Show Guarantee Beds:** Displays guaranteed bed allocations when enabled.
* **Display / More Filters / Clear:**
  * **Display:** Loads the data for the chosen filter selection.
  * **More filters:** Expands additional configuration filters.
  * **Clear:** Resets all filters to default.

***

#### **2. Data Grid (Main Table)**

The main section displays a **calendar-style grid**.\
Rows represent hotels and room types. Columns represent dates within the selected period.

Each cell shows remaining capacity for that date. The value is shown as **beds** and/or **rooms**, depending on the **Rooms No / Beds No** toggles.

| **Column / Element**        | **Description**                                                                                             |
| --------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **Hotel Name**              | The name of the hotel displayed on the left-hand side.                                                      |
| **Room / Allotment Type**   | Indicates room types and their associated allotment identifiers (e.g., “1/21 ALL”, “2/22-P ALL”).           |
| **Daily Columns (1–30)**    | Each column represents one day within the selected month. Values show available beds or rooms for that day. |
| **Highlighted Cells (Red)** | Indicates a **stop sale** for that date.                                                                    |
| **“Sum ALL” Rows**          | Aggregated totals for each hotel across the selected date range.                                            |

#### **Allotment information**

1. **Beds No:** Shows the number of beds available for the selected period.
2. **Rooms No:** Shows the number of rooms available for the selected period.
   * Optionally, check **Show only parent room** to filter parent rooms only.
3. **Guarantee Rooms:** When enabled, guaranteed room numbers are displayed **below the allotment line** for each room.

<figure><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

#### **FAQ**

<details>

<summary><strong>Why is my report empty after I click Display?</strong></summary>

Most empty reports come from missing **departure stat weeks** for the selected year.\
Also check that the selected **transport/resort/hotel** has allotments for the chosen **date period**.

</details>

<details>

<summary><strong>What do the red cells mean?</strong></summary>

Red cells indicate a **stop sale** on that date.\
The stop sale blocks availability, even if there is allotment capacity.

</details>

<details>

<summary><strong>What does “Sum ALL” mean?</strong></summary>

“Sum ALL” rows are totals per hotel across the selected date range.\
Use them to compare hotels without scanning every day column.

</details>

<details>

<summary><strong>What is the difference between “Transport” and “Real Transport”?</strong></summary>

**Transport** is the planned transport code used for packaging and reporting.\
**Real transport** is the actual flight/connection used in calculations.

</details>

<details>

<summary><strong>Why do I see beds in some cases and rooms in others?</strong></summary>

Use **Rooms No / Beds No** to control what the grid shows.\
Some setups track capacity in beds, others in rooms (or both).

</details>

<details>

<summary><strong>What are “Guarantee Rooms”?</strong></summary>

Guarantee rooms are allocated rooms that are guaranteed by contract.\
When enabled, they are shown as a separate line below the allotment line.

</details>

<details>

<summary><strong>Why don’t I see guaranteed beds/rooms even when I enable them?</strong></summary>

Guaranteed values only appear if they exist in the hotel allotment setup.\
If the setup has no guarantees for that period, nothing is displayed.

</details>
