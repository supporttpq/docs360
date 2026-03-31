---
description: >-
  Analyse booking trends, passenger volumes, turnover, and profitability —
  broken down by destination, hotel, country, and time period.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# Statistics in All bookings

### **Overview**

The **Statistics** view in All Bookings transforms your filtered booking list into analytical reports. Instead of looking at individual bookings one by one, Statistics aggregates the data and presents it broken down by the dimensions most useful for business decisions — passengers per resort, profit per hotel, turnover per country, and more.

All figures in this view are calculated **per passenger**, not per booking. This is an important distinction when interpreting results.

{% hint style="info" %}
**Need booking-level totals (counts, turnover, profit) rather than per-passenger breakdowns?** Use [All Bookings Totals](https://manual.tourpaq.com/booking/all-bookings/all-bookings-totals) instead.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

***

### Purpose

Use Statistics in All Bookings to:

* Understand **passenger distribution** by country, arrival date, resort, and hotel
* Analyse **average turnover and profit per passenger** across different market segments
* Identify your **most and least profitable hotels, resorts, and countries**
* Compare **capacity vs actual sales** to spot unsold inventory
* Compare **two different time periods** side by side using Compare Statistics
* Evaluate **agent performance** through the Additional Sales per Seller tool

***

### Preconditions

Before using Statistics, ensure the following:

* You have access to **Booking → All Bookings**
* At least one **Brand** is selected — no statistics will generate without a Brand
* You have set your filters in All Bookings and clicked **Display** first — Statistics reads from the current filtered result set
* All date filters are complete pairs (`From` + `To`) — an incomplete date pair will return empty or misleading results
* Statistics are calculated **per passenger** — if you need booking-level totals, use [All Bookings Totals](https://manual.tourpaq.com/booking/all-bookings/all-bookings-totals)

{% hint style="warning" %}
Always click **Display** in All Bookings **before** opening Statistics. If you change filters, click Display again before refreshing Statistics — otherwise the statistics will reflect the previous filter set.&#x20;
{% endhint %}

***

### How to Use Statistics

#### Step 1 — Set filters and click Display

In All Bookings:

1. Select at least one **Brand**
2. Set a **Booking**, **Departure**, or **Arrival** period with both `From` and `To` dates
3. Add any additional filters you need (hotel, transport, owner, status, etc.)
4. Click **Display**

***

#### Step 2 — Open the Statistics view

Click the **Statistics** button in the toolbar. The default view loads immediately, showing a general overview of passenger distribution per week and per month for the current filter set.

***

#### Step 3 — Choose a statistics type and level

In the Statistics view:

1. Select the **Statistics Type** you want to analyse (e.g. Passengers, Profit, Average Turnover)
2. Select the **Level** — how the data is broken down (e.g. Total, Per Country, Per Resort, Per Hotel)
3. Click **Display** within the Statistics view to update the results

***

#### Step 4 — Use additional tools if needed

For deeper analysis, use the additional tools available in the Statistics view — Compare Statistics, Booking Date Statistics, Additional Sales per Seller. See the Field Reference below for details on each tool.

***

#### Step 5 — Adjust and iterate

Change the statistics type, level, or filters as needed. Always click **Display** after any change to refresh the results.

***

### Field Reference

#### Statistics Types and Levels

| Statistics Type       | Available Levels                                       | Use it to answer…                                                       |
| --------------------- | ------------------------------------------------------ | ----------------------------------------------------------------------- |
| **Passengers**        | Total, Per Country, Per Arrival, Per Resort, Per Hotel | "How many passengers do we have per country, resort, or hotel?"         |
| **Average Turnover**  | Total, Per Country, Per Arrival, Per Resort            | "What is the average revenue per passenger across our markets?"         |
| **Profit**            | Total, Per Country, Per Arrival, Per Resort, Per Hotel | "Where do we earn or lose the most?"                                    |
| **Average Profit**    | Total, Per Country                                     | "What is the average profit per passenger overall or per country?"      |
| **Percentage**        | Total                                                  | "What share of total volume does each destination or period represent?" |
| **Possible vs. Sold** | Total, Per Country                                     | "How much capacity remains unsold?"                                     |

***

#### Additional Analysis Tools

| Tool                                       | Description                                                                                                                                         |
| ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Totals / Cost and Profit**               | Shows total cost vs. profit for the current filtered set. Use this for a quick overall profitability check on a specific period, hotel, or campaign |
| **Additional Sales per Seller / Turnover** | Ranks agents by extra sales and turnover generated. Use this to evaluate agent performance and identify strong upsellers                            |
| **Booking Date Statistics**                | Groups bookings by their creation date per day and per week. Use this to identify booking peaks, quiet periods, and lead time patterns              |
| **Compare Statistics**                     | Adds a secondary filter set so you can compare two different periods (Booking, Departure, or Arrival dates) side by side                            |

***

#### How to Use Compare Statistics

1. Set your **primary filters** in All Bookings (Brand, date period, destination, etc.) and click **Display**
2. Open **Statistics** and select the type you want to analyse
3. Enable **Compare Statistics** and define the **comparison period** — choose Booking, Departure, or Arrival date range for the second period
4. Click **Display** to see both periods side by side

Use Compare Statistics to analyse year-on-year performance, compare two campaigns, or evaluate seasonal differences.

***

### FAQ

**Q: Why are my statistics empty even though I know there are bookings?** The most common causes are: no Brand selected, a date filter with only one date filled in (missing `From` or `To`), or filters changed without clicking Display again. Also note: if your departure dates span more than 12 months, some interval-based statistics may not display. Check all these points, click Display in All Bookings, then reopen Statistics.

***

**Q: Are statistics calculated per booking or per passenger?** All statistics in this view are calculated **per passenger**. Totals, averages, and profit figures all reflect passenger-level data. If you need booking-level aggregates, use [All Bookings Totals](https://manual.tourpaq.com/booking/all-bookings/all-bookings-totals).

***

**Q: Which date filter should I use — Booking, Departure, or Arrival?** Use **Booking Period** when you want to analyse when customers made their reservations — ideal for campaign and sales performance analysis. Use **Departure Period** to analyse when customers travel — ideal for operational planning and capacity analysis. Use **Arrival Period** to analyse when customers reach the destination — ideal for in-destination planning. You can combine them, but always use complete pairs.

***

**Q: Why do Statistics numbers differ from All Bookings Totals?** Statistics are **per passenger** — averages and per-pax figures. Totals are **aggregated booking-level** counts and sums. They answer different questions. Also check that the filters and date periods are identical between the two views before comparing numbers.

***

**Q: How do I compare this year's results with last year's?** Use **Compare Statistics**. Set your primary filters to this year's period and click Display. In Statistics, enable Compare Statistics and set the comparison period to the equivalent period last year. Click Display to see both periods side by side.

***

**Q: Can I export statistics to Excel?** If export is enabled in your environment, an **Export** or **Excel** button will be visible in or near the Statistics view. If no export option is visible, contact your Tourpaq administrator to confirm whether this feature is available for your user role and configuration.

***

**Q: How often are statistics updated?** Statistics are generated in real time based on the current filtered result set. Every time you change filters in All Bookings and click Display, the next Statistics view will reflect the latest data.

***

### Related Pages

* [All Bookings](https://manual.tourpaq.com/booking/all-bookings) — set filters and run Display before opening Statistics
* [View All Bookings](https://manual.tourpaq.com/booking/all-bookings/view-all-bookings) — filter management and saved views
* [All Bookings Totals](https://manual.tourpaq.com/booking/all-bookings/all-bookings-totals) — aggregated booking counts, turnover, and profit totals
* [Dashboard](https://manual.tourpaq.com/dashboard/dashboard) — real-time sales and performance overview without needing to set filters
