---
description: >-
  The real-time command centre for your sales, bookings, and operational
  activity.
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

# Dashboard

### Overview

The **Dashboard** is the default landing page of Tourpaq Office. It provides a centralised, real-time snapshot of your business — combining data from Bookings, Offers, Finance, Questionnaires, and Service Cases into a single, filterable view.

It is designed for quick situational awareness: you can assess the health of your sales pipeline, spot operational issues, and monitor financial performance — all without navigating to ind

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (242).png" alt=""><figcaption></figcaption></figure></div>

### Purpose

The Dashboard exists to help sales managers, tour operators, and administrators answer key business questions at a glance:

* How are bookings and revenue performing compared to the previous period?
* Which destinations, resorts, and hotels are selling best?
* How many offers are converting into bookings?
* Are there open service cases or unresolved quality issues?
* What is the current profit and turnover picture?

***

### Preconditions

Before using the Dashboard, ensure the following:

* You are logged in with a user role that has **Dashboard access**. If you cannot see the Dashboard, contact your system administrator to review your permissions under [Users](https://manual.tourpaq.com/users/users).
* Your **Brand** is correctly selected. Dashboard data is scoped to the Brand(s) you have access to.
* Underlying data must exist — a fresh system with no bookings or offers will show empty widgets. This is expected behaviour.

{% hint style="info" %}
If widgets are showing zero values unexpectedly, first check that your **Brand** and **date filters** are set correctly before assuming a data issue.&#x20;
{% endhint %}

***

### How to Use the Dashboard

#### Step 1 — Open the Dashboard

The Dashboard loads automatically when you log in to Tourpaq Office. You can return to it at any time by clicking **Dashboard** in the left sidebar.

***

#### Step 2 — Apply filters

The filter bar at the top of the Dashboard controls the scope of all widgets simultaneously.

| Filter             | What it does                                                       |
| ------------------ | ------------------------------------------------------------------ |
| **Booking Period** | Limits all data to bookings created within the selected date range |
| **Users**          | Filters data to show only activity by the selected user(s)         |
| **Brands**         | Limits the view to one or more specific Brands                     |
| **Clear**          | Resets all filters and reloads the default full-data view          |

{% hint style="warning" %}
All filters apply **globally** — changing one filter updates every widget on the page at the same time.&#x20;
{% endhint %}

***

#### Step 3 — Read the widgets

The Dashboard is divided into several widget groups. Each is described in detail in the Field Reference section below.

Work through the widgets from top to bottom for a full operational picture:

1. **Summary counters** (Offers, Service Cases, Questionnaires, Customers, Notifications) — quick health check
2. **Sales Performance** — bookings and passenger volume trends
3. **Guest on Destinations** — where your customers are going
4. **Destination & Accommodation Insights** — top resorts, hotels, and booking days
5. **Financial Summary** — revenue, profit, and margin overview

***

### Field Reference

#### Filter Controls

| Field              | Type                  | Description                                                                          |
| ------------------ | --------------------- | ------------------------------------------------------------------------------------ |
| **Booking Period** | Date range picker     | Defines the time window for all dashboard data. Defaults to the current month.       |
| **Users**          | Multi-select dropdown | Filter by one or more agent/user accounts. Leave blank to show all users.            |
| **Brands**         | Multi-select dropdown | Filter by one or more Brands. Leave blank to show data across all accessible Brands. |
| **Clear**          | Button                | Resets all three filters to their default (unfiltered) state.                        |

***

#### Offers Widget

Tracks the performance of quotes and offers sent to customers within the selected period.

| Field            | Description                                                                                                        |
| ---------------- | ------------------------------------------------------------------------------------------------------------------ |
| **Total Offers** | Total number of offers created and sent in the selected period                                                     |
| **Active**       | Offers that are still open — the customer has not yet accepted or declined                                         |
| **Unsold**       | Offers that expired or were declined without converting to a booking                                               |
| **Sold**         | Offers that were accepted and converted into confirmed bookings                                                    |
| **Hit Rate**     | Conversion rate: the percentage of total offers that resulted in a booking. Formula: `(Sold ÷ Total Offers) × 100` |

***

#### Service Cases Widget

Provides a real-time count of customer support cases, organised by status.

| Field           | Description                                                              |
| --------------- | ------------------------------------------------------------------------ |
| **New**         | Cases that have been opened but not yet assigned or actioned             |
| **In Progress** | Cases currently being handled by a staff member                          |
| **Waiting**     | Cases on hold, pending a response from the customer or an external party |
| **Closed**      | Cases that have been fully resolved and closed                           |

{% hint style="info" %}
A high number of **New** or **Waiting** cases may indicate a support backlog. Review [Service Cases](https://manual.tourpaq.com/service-cases) for details.&#x20;
{% endhint %}

***

#### Questionnaires Widget

| Field     | Description                                                                             |
| --------- | --------------------------------------------------------------------------------------- |
| **Total** | Total number of post-trip feedback forms received from customers in the selected period |

***

#### Customers Widget

Monitors customer volume and acquisition within the selected period.

| Field         | Description                                                                     |
| ------------- | ------------------------------------------------------------------------------- |
| **Total**     | Total number of customers associated with bookings in the period                |
| **New**       | First-time customers — those who have no previous booking history in the system |
| **Recurring** | Returning customers who have booked at least once before                        |

***

#### Sales Performance — Overview

High-level booking and passenger metrics for the selected period.

| Field        | Description                                                                                                                                        |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Bookings** | Total number of confirmed bookings in the period                                                                                                   |
| **Pax**      | Total number of passengers across all bookings. Will exceed the booking count for bookings with multiple travellers                                |
| **Change %** | Percentage change compared to the equivalent previous period (e.g. same date range last month or last year). Positive = growth, negative = decline |

***

#### Sales Performance — Bar Chart

A visual trend chart showing booking and passenger activity over time.

| Element            | Description                                                                       |
| ------------------ | --------------------------------------------------------------------------------- |
| **X-Axis**         | Weekly time periods (e.g. 17/3–23/3/2025)                                         |
| **Y-Axis**         | Quantity (number of bookings, passengers, or offers)                              |
| **Blue bars**      | PAX — total number of passengers per week                                         |
| **Dark blue bars** | Bookings — total confirmed bookings per week                                      |
| **Green bars**     | New Offers — number of new offers created per week                                |
| **View toggle**    | Switch between weekly, monthly, and yearly views using the toggle above the chart |

***

#### Guest on Destinations

Shows how bookings and passengers are distributed across destinations.

| Field           | Description                                       |
| --------------- | ------------------------------------------------- |
| **Destination** | The travel destination (country or region)        |
| **Bookings**    | Number of bookings travelling to that destination |
| **Pax**         | Total passengers travelling to that destination   |
| **Change %**    | Comparison with the equivalent previous period    |

***

#### Top-Selling Resorts

Lists the resorts with the highest passenger volume in the selected period. Useful for identifying which specific areas within a destination are most popular.

| Field      | Description                            |
| ---------- | -------------------------------------- |
| **Resort** | Name of the resort                     |
| **Pax**    | Total passengers booked to that resort |

***

#### Top-Selling Hotels

Lists the hotels with the highest passenger volume. Useful for understanding accommodation performance and informing contract negotiations.

| Field     | Description                           |
| --------- | ------------------------------------- |
| **Hotel** | Name of the hotel                     |
| **Pax**   | Total passengers booked at that hotel |

***

#### Top-Selling Days

Identifies the days of the week or calendar dates with the highest booking volumes. Useful for staffing and campaign timing decisions.

| Field          | Description                                        |
| -------------- | -------------------------------------------------- |
| **Day / Date** | The day or date in question                        |
| **Pax**        | Total passengers booked for departures on that day |

***

#### Financial Summary

Provides a high-level financial overview of the business within the selected period.

| Field              | Description                                                                                                                                            |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Bookings**       | Total number of confirmed bookings contributing to the financial data                                                                                  |
| **Turnover Total** | Total gross revenue generated before any costs are deducted                                                                                            |
| **DB Total**       | _Direct Booking Total_ — gross profit calculated as Revenue minus direct supplier costs                                                                |
| **Profit Total**   | Net profit after all costs (direct and indirect) are deducted. May show a negative value during periods of high cancellations, refunds, or cost spikes |
| **Profit/Pax**     | Average net profit per passenger. Formula: `Profit Total ÷ Total Pax`                                                                                  |
| **Extra Total**    | Revenue generated from extras (e.g. transfers, insurance, activities, upgrades)                                                                        |

{% hint style="warning" %}
**Negative financial values** are possible and expected in some periods — for example, during high-cancellation months or when large refunds are processed. Always cross-check with the full [Finance](https://manual.tourpaq.com/finance/payment-registration) module before drawing conclusions.
{% endhint %}

***

### FAQ

**Q: Why are all my Dashboard widgets showing zero?** The most common cause is an active filter that doesn't match any data — for example, a Booking Period with no bookings, or a Brand/User combination that has no activity. Click **Clear** to reset all filters and check if data appears. If widgets remain empty after clearing filters, contact your system administrator.

***

**Q: The Change % figure is missing or showing "N/A" — why?** The Change % requires comparable data from a previous equivalent period. If no data exists for the comparison period (e.g. the system was not in use at that time), the field will not display a value.

***

**Q: Can I customise which widgets appear on the Dashboard?** Widget visibility is controlled by your user role and system configuration. Individual widget rearrangement is not currently available as a self-service option. Contact your system administrator if you need a different default view.

***

**Q: The financial figures on the Dashboard don't match my Finance reports — why?** The Dashboard provides a summary view based on booking-level data. Detailed finance reports may use different calculation methods, cost allocations, or include manually registered adjustments not visible in the Dashboard summary. Always use the [Finance module](https://manual.tourpaq.com/finance/payment-registration) for authoritative financial figures.

***

**Q: Can I export the Dashboard data?** The Dashboard itself does not have a direct export button. For exportable reports, use the [Export module](https://manual.tourpaq.com/export-1/export) or the individual finance and booking reports.

***

### Related Pages

* [Notifications](https://manual.tourpaq.com/notifications/notification) — system alerts visible from the Dashboard
* [All Bookings](https://manual.tourpaq.com/booking/all-bookings) — drill into individual bookings behind the Dashboard numbers
* [Offers](https://manual.tourpaq.com/offers) — manage and track the offers counted in the Offers widget
* [Service Cases](https://manual.tourpaq.com/service-cases) — manage the cases shown in the Service Cases widget
* [Finance → Payment Registration](https://manual.tourpaq.com/finance/payment-registration) — full financial detail behind the Financial Summary
* [Export](https://manual.tourpaq.com/export-1/export) — export booking and financial data for external reporting
