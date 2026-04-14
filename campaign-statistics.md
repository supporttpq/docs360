---
description: >-
  Monitor campaign performance with bookings, pax, sales, discounts, and status
  over time.
---

# Campaign Statistics

### Overview

The **Campaign Statistics Dashboard** offers a centralized interface to monitor and evaluate the **performance of marketing campaigns** across a selected time period. It consolidates data such as bookings, sales revenue, applied discounts, and ongoing campaign statuses—presented through visual graphs and summary cards for clarity and actionable insights.

<figure><img src=".gitbook/assets/image (1) (1) (1) (2).png" alt="Campaign Statistics dashboard overview with KPI cards and chart."><figcaption><p>Campaign Statistics dashboard overview (KPI cards + booking trend chart).</p></figcaption></figure>

### 1. Date Interval Selection

Use the **date range filter** to narrow down statistics and focus on a specific period.

* **Function**: Filters all campaign statistics, graphs, and tables based on selected start and end dates.
* **Example Range**: 01-03-2025 to 31-03-2025

### Campaign Summary Cards

Displayed at the **top of the dashboard**, these KPIs give a snapshot of overall campaign performance:

| Card Title            | Description                                                                                                                    |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **Total Bookings**    | <p>Shows the <strong>number of bookings</strong> generated during the selected period.<br>📌 <em>Example: 24 bookings</em></p> |
| **Pax Count**         | <p>Indicates the <strong>total number of passengers (PAX)</strong> across all bookings.<br>📌 <em>Example: 80 PAX</em></p>     |
| **Total Sales**       | <p>Displays the <strong>total gross revenue</strong> from campaigns.<br>📌 <em>Example: 648,441</em></p>                       |
| **Discounts Applied** | <p>Indicates the <strong>total discount value</strong> applied during the campaigns.<br>📌 <em>Example: 140,000</em></p>       |
| **Total DB**          | <p>Shows the <strong>Direct Budget (DB)</strong> used for campaigns.<br>📌 <em>Example: 0 – no direct budget used</em></p>     |
| **Campaigns Running** | Current status of campaign execution:                                                                                          |

* 🔛 _1 campaign open_
* ✅ _0 fully booked_
* ❌ _0 deleted_

### Graph View – Booking Trends

* **Chart Type**: Line chart with shaded area for volume emphasis.
* **X-Axis**: Dates within the selected range.
* **Y-Axis**: Booking activity volume (number of bookings per day).
* **Insights**:
  * Peaks in the chart indicate **high customer engagement days**.
  * Helps correlate **marketing push periods** (e.g., newsletters, promotions) with booking spikes.

### Campaign Table View

A **tabular list** providing granular details about each campaign within the selected interval.\
Includes key data such as:

* Campaign name
* Duration
* Status (Open, Deleted, Fully Booked)
* Total bookings & PAX
* Revenue and discount breakdowns

Useful for comparing the **individual campaign performance** side-by-side.

| Column                 | Description                                                            |
| ---------------------- | ---------------------------------------------------------------------- |
| **Campaign**           | Name and link to the campaign (e.g., Testfamilie - Gratis helpension). |
| **Status**             | Current status (OPEN).                                                 |
| **Group**              | Target group or category (e.g., Diverse rabatter).                     |
| **Booking Limits**     | Maximum number of bookings allowed (999999999).                        |
| **Discount Limits**    | Maximum allowable discount amount (999999999).                         |
| **Booking From/Until** | Campaign activity window (02/26/2025 - 03/24/2025).                    |
| **Booking Rate**       | Average booking rate (1.04).                                           |
| **Campaign Run**       | Duration or activity run count (0).                                    |
| **Total Bookings**     | Count of all bookings (24).                                            |
| **Turnover**           | Total revenue generated (648,441).                                     |
| **Total Discount**     | Total value of discounts given (43,200).                               |
| **Total Profit**       | Profit generated after discounts (651,772.845).                        |

### Action Button – “View”

Each campaign row includes a **"View"** button:

* Opens a **detailed analytics page** for that specific campaign.
* Allows further breakdown by destination, customer segment, channel, and more.

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)   (7).png" alt="Campaign table view with View button per campaign row."><figcaption><p>Campaign table with per-campaign drill-down via <strong>View</strong>.</p></figcaption></figure>

### Conclusion

The **Campaign Statistics Dashboard** enables marketing teams to:

* Monitor campaign progress and success in real time
* Identify which campaigns generate the most engagement and revenue
* Make **data-driven adjustments** to active or future marketing efforts

The combination of **summary metrics**, **trend graphs**, and **drill-down tables** ensures a **holistic view** of campaign health and efficiency.

### FAQ

<details>

<summary>What controls the numbers shown on the dashboard?</summary>

Everything is filtered by the selected **date interval**.

If the range changes, all KPI cards, charts, and the campaign table update.

</details>

<details>

<summary>Do “Total Bookings” and “Pax Count” include all campaigns, or only open ones?</summary>

They include campaigns shown in the list for the selected period.

Use the campaign **Status** in the table to see if a campaign is open, deleted, or fully booked.

</details>

<details>

<summary>Why do “Total Sales”, “Total Discount”, and “Total Profit” not match what I see elsewhere?</summary>

Most mismatches come from using a different date range.

Also check if the other report uses another aggregation level (booking date vs departure date).

</details>

<details>

<summary>What is the difference between “Discounts Applied” and “Total DB”?</summary>

**Discounts Applied** is the total value of discounts granted in bookings.

**Total DB** reflects direct budget tracked for campaigns (if used in your setup).

</details>

<details>

<summary>What does “Campaigns Running” mean?</summary>

It is a quick status split of campaigns in the selected period.

It helps you see how many are still open vs completed or removed.

</details>
