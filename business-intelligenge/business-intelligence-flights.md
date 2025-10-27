# Business Intelligence – Flights

#### **Overview**

The _Business Intelligence – Flights_ page provides an analytical overview of flight capacity and sales performance across different weeks within a defined travel period. It allows users to monitor sold seats, remaining capacity, and the progression of sales over time, helping to identify trends and optimize flight inventory management.

This module enables users to analyze flight data by **departure**, **arrival**, **transport type**, and **date range**, displaying the percentage of total capacity sold per week.

***

#### **Purpose**

The purpose of this page is to:

* Offer insights into flight seat utilization and sales dynamics.
* Track weekly sales performance versus total flight capacity.
* Identify underperforming or oversold flights.
* Support data-driven decisions for capacity adjustments, pricing, or marketing strategies.

***

#### **Preconditions**

Before using the _Flights_ Business Intelligence report:

1. Ensure the [**Departure Stat Weeks**](../setup/departure-stat-weeks.md) are defined for the selected year(s).\
   These weeks are necessary for the system to aggregate and display weekly sales data correctly.
2. The selected **departure and arrival airports** must have valid flight data for the chosen period.
3. The user must have access to the **Business Intelligence** module.

{% hint style="warning" %}
💡 **Tip:** To have results listed according to the filters set, make sure _departure stat weeks_ are defined for the year(s) used.\
See here how: [**Departure stat weeks**](../setup/departure-stat-weeks.md)
{% endhint %}

***

#### **Field Descriptions and Sections**

<figure><img src="../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

**1. Filters (Top Section)**

* **Departures:** Select the departure airport for the flight data to be displayed.\
  &#xNAN;_&#x45;xample:_ BLL – Billund.
* **Arrivals:** Choose the destination airport.\
  &#xNAN;_&#x45;xample:_ CHQ – Kreta Chania.
* **Transports:** Select the transport code \
  &#xNAN;_&#x45;xample:_ All transports
* **Date Period:** Defines the time range of flights being analyzed. Select a start and end date.\
  &#xNAN;_&#x45;xample:_ 01-04-2024 → 01-08-2024.
* **Display / More Filters / Clear:**
  * **Display:** Refreshes the report with the selected filters.
  * **More filters:** Opens additional filtering options (Transport mode, Transport type).
  * **Clear:** Resets all filters to their default state.

***

**2. Report Summary (Left Panel)**

* **Report Generated Date:** Displays the date on which the report was generated.\
  &#xNAN;_&#x45;xample:_ 21-10-2025.
* **% of Total Capacity Sold to Date:** Shows the overall percentage of sold capacity across all listed weeks.\
  &#xNAN;_&#x45;xample:_ 94.96%.

***

**3. Weekly Data Table**

| **Column**                      | **Description**                                                                                                                                                                                                                                                                                                                                                                                                    |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Week No**                     | The calendar week number for the displayed travel period. The arrow (›) allows expanding to view detailed data for that week.                                                                                                                                                                                                                                                                                      |
| **Available**                   | Number of remaining unsold seats for that week.                                                                                                                                                                                                                                                                                                                                                                    |
| **Sold**                        | Number of sold seats. Negative numbers in sold columns denotes negative balance between sold and canceled pax                                                                                                                                                                                                                                                                                                      |
| **Total**                       | The total number of seats available for that week (Available + Sold).                                                                                                                                                                                                                                                                                                                                              |
| **Sold %**                      | Percentage of total seats sold                                                                                                                                                                                                                                                                                                                                                                                     |
| **Sold 1D / 1W / 2W / 3W / 4W** | <p>Represents additional seats sold compared to previous days or weeks:<br>• <strong>Sold 1D</strong> – The number of seats sold on the last day before departure.<br>• <strong>Sold 1W</strong> – The number of seats sold 1 week before departure.<br>• <strong>Sold 2W–4W</strong> – The number of seats sold 2 to 4 weeks before departure. <br>These columns show booking velocity and sales progression.</p> |

