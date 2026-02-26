---
description: >-
  Use the Tourpaq Office Dashboard to track bookings, offers, customers, service
  cases, and financial KPIs with widgets and filters.
---

# Dashboard

### Overview

The **Dashboard** is the default landing page in Tourpaq Office. It gives sales, operations, and managers a fast overview of activity, trends, and alerts.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (242).png" alt=""><figcaption></figcaption></figure></div>

The dashboard is split into widgets. They summarize bookings, destinations, revenue, top performers, and operational warnings.

### Purpose

The dashboard aggregates data from key modules like **Bookings**, **Offers**, **Questionnaires**, **Service Cases**, and **Finance**.

Use it to:

* Track sales performance at a glance
* Monitor customer and destination trends
* React to service and support metrics
* Identify top-performing products and problem areas

### Preconditions

* You must have access to the Dashboard (role and permissions).
* Data must be available in the database (near real time).
* Filters must be configured for your scope (for example, agency or brand access).

### How to Use the Dashboard

#### Filter Controls

Filters control the **scope** of data shown in the widgets.

* **Booking Period**: Select a date range for bookings created in that period.
* **Users**: Filter data to actions made by selected users.
* **Brands**: Choose one or more brands to limit the report to specific company identities.
* **Clear**: Reset all filters and reload the default view.

***

### Dashboard Widgets & Field Explanations

#### Offers Section

Tracks the effectiveness of quotes and offers sent to customers.

| Field            | Description                                                                    |
| ---------------- | ------------------------------------------------------------------------------ |
| **Total Offers** | The number of offers sent in the selected period.                              |
| **Active**       | Offers still pending customer decision.                                        |
| **Unsold**       | Offers that were not converted into bookings.                                  |
| **Sold**         | Offers that turned into successful bookings.                                   |
| **Hit Rate**     | Percentage of sold offers out of total offers. Formula: `(Sold / Total) * 100` |

***

#### Service Cases Section

Tracks the health of customer support operations.

| Field           | Description                                               |
| --------------- | --------------------------------------------------------- |
| **New**         | Recently opened or reported service cases.                |
| **Closed**      | Resolved and completed cases.                             |
| **In Progress** | Currently being worked on by staff.                       |
| **Waiting**     | On hold, awaiting action from client or external parties. |

***

#### Questionnaires Section

Shows the amount of feedback collected from clients.

| Field     | Description                                                                     |
| --------- | ------------------------------------------------------------------------------- |
| **Total** | The number of survey forms received from clients, including post-trip feedback. |

***

#### Customers Section

Monitors customer engagement.

| Field         | Description                                            |
| ------------- | ------------------------------------------------------ |
| **Total**     | Total number of customers in the selected time frame.  |
| **New**       | First-time bookers in the period.                      |
| **Recurring** | Repeat customers who previously used Tourpaq services. |

***

#### Notifications Section

* System alerts for notable events or changes (not detailed in this section).

***

### Sales Performance

#### Sales Overview

| Field        | Description                                                                        |
| ------------ | ---------------------------------------------------------------------------------- |
| **Bookings** | Total number of confirmed bookings.                                                |
| **Pax**      | Total passengers (PAX). This can exceed bookings.                                  |
| **Change %** | Change compared to the previous equivalent time period (e.g., last week or month). |

#### Bar Chart (Performance Trends)

* **X-Axis**: Weekly time periods (e.g., 17/3–23/3/2025)
* **Y-Axis**: Quantity

| Color         | Metric                     |
| ------------- | -------------------------- |
| **Blue**      | PAX – Number of passengers |
| **Dark Blue** | Bookings                   |
| **Green**     | New Offers                 |

***

### Guests by destination

Tracks passenger distribution by destination.

| Field        | Description                           |
| ------------ | ------------------------------------- |
| **Bookings** | Number of bookings per destination    |
| **Pax**      | Total passengers for each destination |
| **Change %** | Comparison with previous period       |

***

### Destination & Accommodation Insights

#### Top-Selling Resorts

* Shows resorts with the most passengers booked.

#### Top-Selling Hotels

* Highlights the most-booked hotels by total passengers.

#### Top-Selling Days

* Identifies the most popular booking dates (by number of passengers).

***

### Financial Summary

| Field              | Description                                                               |
| ------------------ | ------------------------------------------------------------------------- |
| **Bookings**       | Confirmed reservations.                                                   |
| **Profit Total**   | Net profit (Revenue – Total Costs). May show loss (e.g., DKK -1,727,600). |
| **Profit/Pax**     | Net profit per passenger.                                                 |
| **Extra Total**    | Income from extra services like upgrades, VIP packages, or tours.         |
| **DB Total**       | Gross profit (Revenue – Direct Costs).                                    |
| **Turnover Total** | Total gross revenue before costs are subtracted.                          |

{% hint style="danger" %}
**Note on Negative Values**: Financial values may sometimes be negative due to refunds, high cancellations, or cost spikes. Always cross-check with the finance module for full context.
{% endhint %}
