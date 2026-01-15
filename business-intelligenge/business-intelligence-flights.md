# Business Intelligence – Flights

#### **Overview**

The _Business Intelligence – Flights_ report shows flight capacity and sales by week for a travel period.\
Use it to track sold seats, remaining capacity, and sales pace over time.\
This helps you spot slow-selling routes early and react faster.

You can filter by **departure**, **arrival**, **transport**, and **date period**.\
Results show how much of the total capacity is sold per week.

***

#### **Purpose**

The purpose of this page is to:

* Offer insights into flight seat utilization and sales dynamics.
* Track weekly sales performance versus total flight capacity.
* Identify underperforming or oversold flights.
* Support data-driven decisions for capacity adjustments, pricing, or marketing strategies.

***

#### **Preconditions**

Before using the _Flights_ Business Intelligence report, make sure:

1. [Departure stat weeks](../setup/departure-stat-weeks.md) are defined for the selected year(s).\
   They are required to aggregate and display weekly sales data correctly.
2. The selected **departure and arrival airports** must have valid flight data for the chosen period.
3. The user must have access to the **Business Intelligence** module.

{% hint style="warning" %}
**Tip:** If results don’t match your filters, check **departure stat weeks** first.\
Setup guide: [Departure stat weeks](../setup/departure-stat-weeks.md)
{% endhint %}

***

#### **Field Descriptions and Sections**

<figure><img src="../.gitbook/assets/image (3) (1) (1) (3) (1).png" alt=""><figcaption></figcaption></figure>

**1. Filters (Top Section)**

* **Departures:** Select the departure airport for the flight data to be displayed.\
  Example: `BLL – Billund`.
* **Arrivals:** Choose the destination airport.\
  Example: `CHQ – Chania (Crete)`.
* **Transports:** Select the transport code.\
  Example: `All transports`.
* **Date Period:** Defines the time range of flights being analyzed. Select a start and end date.\
  Example: `01-04-2024 → 01-08-2024`.
* **Display / More Filters / Clear:**
  * **Display:** Refreshes the report with the selected filters.
  * **More filters:** Opens additional filtering options (Transport mode, Transport type).
  * **Clear:** Resets all filters to their default state.

***

**2. Report Summary (Left Panel)**

* **Report Generated Date:** Displays the date on which the report was generated.\
  Example: `21-10-2025`.
* **% of Total Capacity Sold to Date:** Shows the overall percentage of sold capacity across all listed weeks.\
  Example: `94.96%`.

***

**3. Weekly Data Table**

| **Column**                      | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Week No**                     | The calendar week number for the displayed travel period. The arrow (›) allows expanding to view detailed data for that week.                                                                                                                                                                                                                                                                                                                                                                                      |
| **Available**                   | Number of remaining unsold seats for that week.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Sold**                        | Number of sold seats. Negative values can appear if cancellations exceed sold seats in the selected scope.                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Total**                       | The total number of seats available for that week (Available + Sold).                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Sold %**                      | Percentage of total seats sold.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Sold 1D / 1W / 2W / 3W / 4W** | <p>Represents additional seats sold compared to previous days or weeks(1 day, 1 week, 2–4 weeks).                                                                • <strong>Sold 1D</strong> – The number of seats sold on the last day before departure. </p><p>• <strong>Sold 1W</strong> – The number of seats sold 1 week before departure. </p><p>• <strong>Sold 2W–4W</strong> – The number of seats sold 2 to 4 weeks before departure.</p><p>These columns show booking velocity and sales progression.</p> |



***

#### **How to use this report**

{% stepper %}
{% step %}
### Set your filters

Pick **Departures**, **Arrivals**, and a **Date Period**.\
Use **More filters** if you need **Transport mode** or **Transport type**.
{% endstep %}

{% step %}
### Generate results

Click **Display** to refresh the report.
{% endstep %}

{% step %}
### Drill down by week

Use the arrow (›) on a **Week No** row to expand details.
{% endstep %}
{% endstepper %}

***

#### **FAQ**

<details>

<summary><strong>Why is my report empty after I click Display?</strong></summary>

Most empty reports come from missing **departure stat weeks** for the selected year.\
Also verify the route has flight data inside the selected **Date Period**.

</details>

<details>

<summary><strong>Why is “Sold” negative?</strong></summary>

Negative values can happen when cancellations exceed sold seats for your filter scope.\
This is common if you filter a small route, week, or transport subset.

</details>

<details>

<summary><strong>How are weeks calculated in this report?</strong></summary>

Weeks come from your **Departure stat weeks** setup.\
If week boundaries look wrong, verify that setup for the year.

</details>

<details>

<summary><strong>What do “Sold 1D / 1W / 2W / 3W / 4W” mean?</strong></summary>

They show sold seats at fixed cutoffs before departure (1 day, 1 week, 2–4 weeks).\
Use them to compare booking pace across weeks and routes.

</details>

<details>

<summary><strong>What’s the difference between “Transports” and “Transport type”?</strong></summary>

**Transports** is the specific transport code (or all transports).\
**Transport type** is a classification used for broader grouping and filtering.

</details>
