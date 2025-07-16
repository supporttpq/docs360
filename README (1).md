# Dashboard

### 🧭 Overview

The **Dashboard** is the default landing page in the Tourpaq Office application. Its purpose is to provide users—especially those in sales, operations, and management—with a **quick, centralized snapshot of system activity**, customer behavior, sales data, and operational metrics.

<figure><img src=".gitbook/assets/image (5) (2).png" alt=""><figcaption></figcaption></figure>

This dashboard provides a comprehensive overview of the sales and customer activity. The data is segmented into various widgets, offering insights into bookings, destinations, revenue, top-performing entities, and operational alerts.

### 🎯 Purpose

The dashboard aggregates and visualizes critical business data from multiple modules (Bookings, Offers, Questionnaires, Service Cases, and Finance). This allows users to:

* Track sales performance at a glance
* Monitor customer and destination trends
* React to service and support metrics
* Identify top-performing products and problem areas

### ✅ Preconditions

* The user must have access to the dashboard page (depending on user role/permissions).
* Real-time or near-real-time data must be available in the database.
* System filters must be configured properly for user-specific views (e.g., agency or brand access).

### 🛠️ How to Use the Dashboard

#### 🔍 Filter Controls

These control the **scope of the data** shown in the dashboard widgets.

* **Booking Period**: Select a date range to view bookings created during that period.
* **Users**: Filter the data to reflect actions made by selected users.
* **Brands**: Choose one or more brands to limit the report to specific company identities.
* **Clear**: Resets all filters and reloads default data.

***

### 📦 Dashboard Widgets & Field Explanations

#### 🔹 Offers Section

Tracks the effectiveness of quotes/offers sent to customers.

| Field            | Description                                                                    |
| ---------------- | ------------------------------------------------------------------------------ |
| **Total Offers** | The number of offers sent in the selected period.                              |
| **Active**       | Offers still pending customer decision.                                        |
| **Unsold**       | Offers that were not converted into bookings.                                  |
| **Sold**         | Offers that turned into successful bookings.                                   |
| **Hit Rate**     | Percentage of sold offers out of total offers. Formula: `(Sold / Total) * 100` |

***

#### 🔹 Service Cases Section

Tracks the health of customer support operations.

| Field           | Description                                               |
| --------------- | --------------------------------------------------------- |
| **New**         | Recently opened or reported service cases.                |
| **Closed**      | Resolved and completed cases.                             |
| **In Progress** | Currently being worked on by staff.                       |
| **Waiting**     | On hold, awaiting action from client or external parties. |

***

#### 🔹 Questionnaires Section

Provides feedback quantity collected from clients.

| Field     | Description                                                                     |
| --------- | ------------------------------------------------------------------------------- |
| **Total** | The number of survey forms received from clients, including post-trip feedback. |

***

#### 🔹 Customers Section

Monitors customer engagement.

| Field         | Description                                            |
| ------------- | ------------------------------------------------------ |
| **Total**     | Total number of customers in the selected time frame.  |
| **New**       | First-time bookers in the period.                      |
| **Recurring** | Repeat customers who previously used Tourpaq services. |

***

#### 🔹 Notifications Section

* A system-level alert for notable events or changes (not further detailed in this section).

***

### 💸 Sales Performance

#### 📌 Sales Overview

| Field        | Description                                                                               |
| ------------ | ----------------------------------------------------------------------------------------- |
| **Bookings** | Total number of confirmed bookings.                                                       |
| **Pax**      | Total number of passengers (can exceed bookings if bookings contain multiple passengers). |
| **Change %** | Change compared to the previous equivalent time period (e.g., last week or month).        |

#### 📊 Bar Chart (Performance Trends)

* **X-Axis**: Weekly time periods (e.g., 17/3–23/3/2025)
* **Y-Axis**: Quantity

| Color         | Metric                     |
| ------------- | -------------------------- |
| **Blue**      | PAX – Number of passengers |
| **Dark Blue** | Bookings                   |
| **Green**     | New Offers                 |

***

### 🌍 Guest on Destinations

Tracks guest distribution by destination.

| Field        | Description                           |
| ------------ | ------------------------------------- |
| **Bookings** | Number of bookings per destination    |
| **Pax**      | Total passengers for each destination |
| **Change %** | Comparison with previous period       |

***

### 🏖️ Destination & Accommodation Insights

#### 🥇 Top-Selling Resorts

* Shows resorts with the most passengers booked.

#### 🏨 Top-Selling Hotels

* Highlights the most-booked hotels by total passengers.

#### 📅 Top-Selling Days

* Identifies the most popular booking dates (by number of passengers).

***

### 💰 Financial Summary

| Field              | Description                                                               |
| ------------------ | ------------------------------------------------------------------------- |
| **Bookings**       | Confirmed reservations.                                                   |
| **Profit Total**   | Net profit (Revenue – Total Costs). May show loss (e.g., DKK -1,727,600). |
| **Profit/Pax**     | Net profit per passenger.                                                 |
| **Extra Total**    | Income from extra services like upgrades, VIP packages, or tours.         |
| **DB Total**       | Gross profit (Revenue – Direct Costs).                                    |
| **Turnover Total** | Total gross revenue before costs are subtracted.                          |

> ⚠️ **Note on Negative Values**: Financial values may sometimes be negative due to refunds, high cancellations, or cost spikes. Always cross-check with the finance module for full context.
