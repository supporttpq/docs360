# Business Intelligence – Accommodation

#### **Overview**

The _Business Intelligence – Accommodation_ page provides detailed analytics on hotel allotments and booking performance for each week within a defined travel period.\
It helps users track available versus sold rooms, analyze occupancy per allotment type, and monitor booking progress to optimize accommodation inventory and performance.

This report consolidates sales data by **country**, **resort**, **hotel**, **room type**, and **date range**, displaying weekly capacity utilization and sales progression trends.

***

#### **Purpose**

The purpose of this page is to:

* Monitor room allotment usage and occupancy levels per hotel and room type.
* Identify sales performance by allotment type (Commitment, Allotment, Hotel Bed Bank).
* Support revenue optimization by tracking sold percentages and available capacity.
* Provide visibility into booking speed and progression over previous weeks.

***

#### **Preconditions**

Before using the _Accommodation_ Business Intelligence report:

1. Ensure that **hotel allotments** and **stat weeks** are correctly configured for the selected travel period and year(s).
2. The selected **country**, **resort**, and **hotel** must have valid accommodation data for the chosen date range.
3. The user must have access to the **Business Intelligence** module and relevant hotel data.

{% hint style="warning" %}
💡 **Tip:** To have results listed according to the filters set, make sure _departure stat weeks_ are defined for the year(s) used.\
See here how: [**Departure stat weeks**](../setup/departure-stat-weeks.md)
{% endhint %}

***

#### **Field Descriptions and Sections**

<figure><img src="../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

**1. Filters (Top Section)**

* **Country:** Select the destination country where the accommodation is located.\
  &#xNAN;_&#x45;xample:_ GR – Greece.
* **Resort:** Choose the specific resort area.\
  &#xNAN;_&#x45;xample:_ PVK–PARG – Parga.
* **Hotel:** Select the hotel for which you want to view sales data.\
  &#xNAN;_&#x45;xample:_ Diogenis Studios.
* **Room:** Select a specific room type or use “Room -” to view all rooms.\
  &#xNAN;_&#x45;xample:_ 1-var. lej. (studio) – 2 pers.
* **Date Period:** Defines the analysis period by setting a start and end date.\
  &#xNAN;_&#x45;xample:_ 01-04-2024 → 01-06-2024.
* **Hotel Allotment / Booking Date:**
  * _Hotel Allotment:_ Filters the report based on allotment type (e.g., Commitment, Allotment).
  * _Booking Date:_ Filters results by when bookings were made.
* **Rooms No / Beds No:** Allows inclusion or exclusion of rooms/beds in the report metrics.
* **Display / More Filters / Clear:**
  * **Display:** Generates the report based on selected filters.
  * **More filters:** Opens additional filtering options (Hotel allotment, Booking date)
  * **Clear:** Resets all filters to default values.
* **Show Guarantee Rooms / Show Codes:** Toggles to display guaranteed rooms /show internal room codes.

***

**2. Report Summary (Left Panel)**

* **Report Generated Date:** Displays the date when the report was generated.\
  &#xNAN;_&#x45;xample:_ 21-10-2025.
* **% of Total Capacity Sold to Date:** Shows the total sold percentage across all listed accommodations.\
  &#xNAN;_&#x45;xample:_ 100.00%.

***

**3. Weekly Data Table**

| **Column**                   | **Description**                                                                                                       |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **Week No**                  | Calendar week number for the displayed period.                                                                        |
| **Date**                     | The specific date (within that week) of the room allotment or booking.                                                |
| **Resort**                   | The resort where the hotel is located.                                                                                |
| **Hotel**                    | The hotel name.                                                                                                       |
| **Allotment Type**           | Defines the contract type with the hotel (e.g., **Commitment**, **Allotment**, or **Hotel Bed Bank**).                |
| **Room**                     | The room type                                                                                                         |
| **Available**                | Number of unsold rooms for that week.                                                                                 |
| **Sold**                     | Number of rooms sold.                                                                                                 |
| **Total**                    | Total number of rooms (Available + Sold).                                                                             |
| **Guarantee Rooms**          | Displays the number of guaranteed rooms (if applicable).                                                              |
| **Sold %**                   | Percentage of rooms sold relative to total available.                                                                 |
| **Price EUR**                | Displays the average selling price per room (if available).                                                           |
| **Sold % 1W / 2W / 3W / 4W** | Tracks percentage sold compared to 1, 2, 3, or 4 weeks before departure — used to monitor booking progress over time. |
