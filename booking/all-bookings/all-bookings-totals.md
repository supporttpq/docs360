---
description: >-
  A fast, aggregated summary of booking counts, passenger volumes, turnover, and
  profit for any filtered set of bookings.
---

# All bookings Totals

### Overview

**All Bookings Totals** provides a high-level financial and operational summary based on the filters currently active in All Bookings. Where Statistics breaks data down per passenger across multiple dimensions, Totals keeps things simple — giving you the headline numbers for the filtered booking set at a glance.

It answers questions like: _"How many bookings and passengers do we have for this departure period?"_ or _"What is the total turnover and profit for this hotel across the summer season?"_

{% hint style="info" %}
**Need per-passenger breakdowns by country, resort, or hotel?** Use [Statistics in All Bookings](https://manual.tourpaq.com/booking/all-bookings/statistic-in-all-bookings) instead.
{% endhint %}

***

### Purpose

Use All Bookings Totals to:

* Get a quick **aggregated count** of bookings and passengers for a filtered segment
* Review **total turnover and profit** for a specific period, brand, hotel, or transport
* Validate data before exporting or reporting
* Compare filter segments rapidly without navigating to the full Statistics view

***

### Preconditions

Before using All Bookings Totals, ensure the following:

* You have access to **Booking → All Bookings**
* At least one **Brand** is selected
* You have applied at least one **date filter pair** (`From` + `To`) — Booking Period, Departure Period, or Arrival Period
* You have clicked **Display** in All Bookings — Totals reads from the current filtered result set

{% hint style="warning" %}
Totals update **only after** you click **Display** in All Bookings. If you change filters, always click Display again before reading the Totals to ensure you are seeing current data.
{% endhint %}

***

### How to Use All Bookings Totals

#### Step 1 — Open All Bookings and select a Brand

Go to **Booking → All Bookings** and select at least one Brand.

***

#### Step 2 — Apply filters

Set the filters that define the segment you want to summarise. At minimum, set one complete date pair:

| Goal                                    | Recommended filter           |
| --------------------------------------- | ---------------------------- |
| Sales performance in a period           | Booking Period (From + To)   |
| Operational load for a departure window | Departure Period (From + To) |
| In-destination planning                 | Arrival Period (From + To)   |
| Revenue from a specific hotel           | Hotels + any date pair       |
| Agent performance                       | Owners + any date pair       |

You can combine multiple filters for more granular totals — for example, all confirmed (Status = OK) bookings for a specific hotel departing in a given month.

***

#### Step 3 — Click Display

Click **Display** in All Bookings to execute the search. The totals for the filtered set appear at the bottom of the page (or in the Totals area, depending on your screen layout).

***

#### Step 4 — Read the Totals

Review the aggregated figures shown:

* **Bookings** — total number of bookings in the filtered set
* **Passengers** — total number of passengers across those bookings
* **Turnover** — total gross revenue before costs
* **Profit** — total net profit (revenue minus costs). May be negative in periods with high cancellations or refunds

***

#### Step 5 — Adjust and compare

Change filters and click Display again to update the Totals for a different segment. Use **Saved Views** to quickly switch between common filter combinations.

***

### Field Reference

#### Totals Metrics

| Metric         | Description                                                                                                                                                                              |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Bookings**   | Total number of bookings in the current filtered result set                                                                                                                              |
| **Passengers** | Total number of passengers across all filtered bookings. One booking may contain multiple passengers                                                                                     |
| **Turnover**   | Total gross revenue from all filtered bookings before any costs are deducted                                                                                                             |
| **Profit**     | Total net profit: Revenue minus all costs (direct and indirect). A negative value indicates the filtered set is running at a loss — common in periods with high cancellations or refunds |

***

#### Filters That Drive Totals

| Filter                           | Description                                                                                       |
| -------------------------------- | ------------------------------------------------------------------------------------------------- |
| **Brand**                        | Required. Select one or more Brands                                                               |
| **Booking Period**               | Date range for when bookings were created. Must be a complete pair                                |
| **Departure Period**             | Date range for outbound travel dates. Must be a complete pair                                     |
| **Arrival Period**               | Date range for arrival at destination. Must be a complete pair                                    |
| **Hotels**                       | Limit totals to bookings for specific hotels                                                      |
| **Room Types**                   | Limit totals to bookings for a specific room types. Works only if at least one hotel is selected. |
| **Transports / Real Transports** | Limit totals to bookings on specific transports                                                   |
| **Owners**                       | Limit totals to bookings owned by specific agents or users                                        |
| **Status**                       | Limit totals to bookings of a specific status (e.g. OK only, or Cancelled only)                   |

{% hint style="warning" %}
Date filters (**Booking**, **Departure**, **Arrival**) must always be used as complete pairs — both `From` and `To` must be filled in. An incomplete pair will return empty or incorrect totals.
{% endhint %}

***

### Totals vs. Statistics — When to Use Which

|                          | All Bookings Totals             | Statistics in All Bookings                                 |
| ------------------------ | ------------------------------- | ---------------------------------------------------------- |
| **What it shows**        | Aggregated counts and sums      | Per-passenger averages and breakdowns                      |
| **Calculation basis**    | Per booking                     | Per passenger                                              |
| **Best for**             | Quick volume and revenue checks | Detailed analysis by country, hotel, resort                |
| **Breakdowns available** | None — headline figures only    | Country, arrival, resort, hotel                            |
| **Additional tools**     | None                            | Compare Statistics, Booking Date Stats, Seller Performance |

<figure><img src="../../.gitbook/assets/image (794).png" alt=""><figcaption></figcaption></figure>

***

### Related Pages

* [All Bookings](https://manual.tourpaq.com/booking/all-bookings) — parent page and filter reference
* [View All Bookings](https://manual.tourpaq.com/booking/all-bookings/view-all-bookings) — filter setup, saved views, and bookings table
* [Statistics in All Bookings](https://manual.tourpaq.com/booking/all-bookings/statistic-in-all-bookings) — per-passenger analytics and breakdowns
* [Dashboard](https://manual.tourpaq.com/dashboard/dashboard) — real-time financial and sales summary without manual filtering
* [Finance → Payment Registration](https://manual.tourpaq.com/finance/payment-registration) — authoritative financial records for individual bookings
