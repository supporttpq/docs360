# All bookings

### **Overview**

The **All Bookings** tab is the central place for **finding, filtering, and analyzing bookings** in Tourpaq. From here you can:

* See a list of all bookings matching your filters.
* Quickly check key KPIs (bookings, passengers, turnover, profit).
* Open a booking directly from the list.
* Jump into more detailed statistics and totals.

Filters are grouped by purpose:

* **Booking retrieval** – who booked, when, and for which brand.
* **Transport / hotel configuration** – which flights, resorts, and hotels are included.
* **Analysis** – statistics per passenger, profit, turnover, and more.

This section supports both daily operations and management reporting for **agents, operations, finance, and management**.

For detailed sub‑features, see:

* [View all bookings](view-all-bookings.md)
* [Statistic in All bookings](statistic-in-all-bookings.md)
* [All bookings Totals](all-bookings-totals.md)

***

### **Purpose**

The goal of **All Bookings** is to let you:

* Retrieve, view, and analyze bookings based on precise criteria.
* Generate statistics such as **profit**, **turnover**, **booking trends**, and **customer distributions**.
* Work faster with **saved views** and **hideable filters** that keep the interface clean.

***

### **Preconditions**

To use this section effectively, make sure:

* You are logged in with an account that has appropriate access rights.
* You select at least one **Brand** before displaying bookings or statistics.
* Date filters that work in pairs (e.g., _Booking Start_ & _Booking End_) are **used together**.
* All statistics are calculated **per passenger**, and **a brand must be selected**.

{% hint style="info" %}
If no results appear, first check that a **Brand** is selected and that both dates are filled in for any date range you use.
{% endhint %}

***

### **Quick start**

{% stepper %}
{% step %}
#### 1. Open **All Bookings**

* Go to **Booking → All Bookings**.
* Select the **Brand** you want to work with.
{% endstep %}

{% step %}
#### 2. Apply filters and display

* Set the **Booking Period** or **Departure/Arrival/Return Periods**.
* Optionally filter by **Hotel**, **Transport**, **Owner**, **Bonus Code**, etc.
* Click **Display** to load the bookings list.
{% endstep %}

{% step %}
#### 3. Analyze and drill down

* Review the bookings in the **table** and open any booking by clicking its **Booking No.**
* Use the **statistics bar** at the bottom for quick KPIs.
* Click **Statistics** to open detailed reports (see [Statistic in All bookings](statistic-in-all-bookings.md)).
{% endstep %}
{% endstepper %}

***

### **Instructions & Field Explanations**

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

#### **Booking & General Filters**

These filters control **which bookings** are shown.

| Field                            | Description                                                                   | Example                                                                                                                                                                             |
| -------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Brands**                       | Brand(s) included in the search. **At least one brand is required.**          | `Tourpaq DK`                                                                                                                                                                        |
| **Booking Period**               | Date range in which the booking was created.                                  | `15-09-2025 – 21-09-2025`                                                                                                                                                           |
| **Departure Period**             | Date range for the trip departure.                                            | `Start: 19-09-2025`                                                                                                                                                                 |
| **Arrival Period**               | Date range for the trip arrival.                                              | `21-09-2025`                                                                                                                                                                        |
| **Return Period**                | Date range for return trips.                                                  | `End: 29-09-2025`                                                                                                                                                                   |
| **Pax No.**                      | Search by number of passengers in a booking.                                  | `3`                                                                                                                                                                                 |
| **Status**                       | Filter bookings by status (e.g., _OK_, _Cancelled_, _Error_, _Locked_).       | `OK`                                                                                                                                                                                |
| **GDS Status**                   | Filter by GDS status if you use a Global Distribution System integration.     | `GDSTKOK`                                                                                                                                                                           |
| **Internal Comment**             | Search bookings based on internal notes.                                      | `Voucher issued`                                                                                                                                                                    |
| **Bonus Code**                   | Filter by promotional or bonus codes used in bookings.                        | `SUMMER25`                                                                                                                                                                          |
| **Hotels**                       | Filter by hotel names or assigned accommodations.                             | `Grand Hotel Budapest`                                                                                                                                                              |
| **Transports / Real Transports** | Filter by transport types and specific real transports assigned to bookings.  | `Flight DK123`                                                                                                                                                                      |
| **Extra**                        | Filter by extras and/or a specific extra category.                            | <div><figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div> |
| **Owners**                       | Filter bookings by the responsible agent, user, or company (booking “owner”). | `RW/TPQ`                                                                                                                                                                            |
| **All Bookings**                 | Ignores date ranges and shows **all** bookings for the selected brand(s).     | _Checked_                                                                                                                                                                           |

> **Tip:** Use as few filters as possible when troubleshooting (e.g., searching for a missing booking), then add more filters to narrow down the result set.

***

#### **Bookings Table (Main Section)**

The table lists all bookings that match your filters.

| Column                  | Description                                                                                                                                                                                                                                                                                                                                                        |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Booking No.**         | Unique booking identification number. Click to open the **booking details** page.                                                                                                                                                                                                                                                                                  |
| **Customer**            | Name of the customer or system automation related to the booking.                                                                                                                                                                                                                                                                                                  |
| **Transport**           | Transport type and code.                                                                                                                                                                                                                                                                                                                                           |
| **Resort**              | Destination resort.                                                                                                                                                                                                                                                                                                                                                |
| **Hotel**               | Hotel assigned to the booking.                                                                                                                                                                                                                                                                                                                                     |
| **Bkg. Date**           | Date when the booking was created.                                                                                                                                                                                                                                                                                                                                 |
| **Bkg. Time**           | Time when the booking was created.                                                                                                                                                                                                                                                                                                                                 |
| **Nights/No**           | Number of nights booked.                                                                                                                                                                                                                                                                                                                                           |
| **Phone**               | Customer’s phone number.                                                                                                                                                                                                                                                                                                                                           |
| **Pax No.**             | Number of passengers in the booking.                                                                                                                                                                                                                                                                                                                               |
| **Owner**               | Responsible agent, user, or system owner of the booking.                                                                                                                                                                                                                                                                                                           |
| **Departure**           | Departure date for the trip.                                                                                                                                                                                                                                                                                                                                       |
| **Extras**              | <p>Lists all extras associated with the booking.</p><p>Hover to see a tooltip with a table showing which extras belong to which passenger and the full extra names. The <strong>Extras</strong> column can be turned on from the column selector.</p><p><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1).png" alt=""></p> |
| **⋮ (Column selector)** | Opens the column selector so you can show or hide additional columns in the table.                                                                                                                                                                                                                                                                                 |

***

### **Toolbar Actions**

<figure><img src="../../.gitbook/assets/image (550).png" alt=""><figcaption></figcaption></figure>

#### **Display**

Runs the search using the currently selected filter criteria and refreshes the bookings list.

#### **More Filters**

Expands additional filtering options.

* A green badge indicates the **number of active additional filters**.

#### **Clear**

Resets all filters back to their default (empty) state.

#### **Save View**

Saves the current combination of filters as a **reusable view**.

* Useful for daily workflows such as **“Today’s arrivals”**, **“Last week’s sales”**, or **“Brand X / Hotel Y performance”**.

#### **Today’s Bookings**

Shortcut that automatically sets the **Booking Period** to today and displays all bookings created **today**.

#### **Statistics Bar (Bottom)**

At the bottom of the page, a statistics bar shows a quick summary for the filtered bookings:

| Metric             | Description                                               | Example          |
| ------------------ | --------------------------------------------------------- | ---------------- |
| **Bookings**       | Total number of bookings in the filtered view.            | `72`             |
| **Total Pax**      | Total passengers across all bookings.                     | `208`            |
| **Pax / Booking**  | Average number of passengers per booking.                 | `2.9`            |
| **Total Turnover** | Total revenue generated from the bookings.                | `DKK 539,773`    |
| **Turnover / Pax** | Average revenue per passenger.                            | `DKK 2,595`      |
| **Profit Total**   | Total profit (revenue minus costs) for filtered bookings. | `DKK -2,751,155` |
| **Profit / Pax**   | Profit per passenger.                                     | `DKK -13,227`    |

> For an in‑depth breakdown of these numbers, use the **Statistics** button and see [Statistic in All bookings](statistic-in-all-bookings.md).

***

### **Hide Filters Functionality**

The **Hide filters** feature helps keep the interface clean by hiding filters you rarely use.

| Option                               | Description                                                                                                                                                                             |
| ------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Hide filters**                     | Hides all inactive or unused filters for cleaner navigation.                                                                                                                            |
| **Show hidden**                      | Checkbox on each filter – temporarily reveals or hides that specific filter.                                                                                                            |
| **Choose all**                       | Selects all items in a filter, including hidden ones.                                                                                                                                   |
| **Hide as filter on lists**          | Manually hide specific filters, for example a transport you no longer want to see as a filter option.                                                                                   |
| **System Setup → Hide Filter input** | Global setting that automatically hides outdated filters (e.g., transports or users) based on inactivity (number of days). Example: `10` hides transports not used in the last 10 days. |

<figure><img src="https://sonat.com/api/Document/Image/19670ef0-8b8a-4cda-8eb6-249681e07016/60a72aeb-a272-4428-a118-b6074b1b35b5/ec44a3d0-8810-4253-b486-355b314877ba.webp?width=898" alt="" height="200"><figcaption></figcaption></figure>

<figure><img src="https://sonat.com/api/Document/Image/19670ef0-8b8a-4cda-8eb6-249681e07016/60a72aeb-a272-4428-a118-b6074b1b35b5/f3b2074c-944c-4260-a801-0a280f9da0af.webp?width=933" alt="" height="300" width="400"><figcaption></figcaption></figure>

***

### **Statistics Filters and Tools**

<figure><img src="https://sonat.com/api/Document/Image/19670ef0-8b8a-4cda-8eb6-249681e07016/60a72aeb-a272-4428-a118-b6074b1b35b5/5f9160ba-43aa-4d8f-9f35-bbbdc227a335.webp?width=1854" alt="" width="400"><figcaption></figcaption></figure>

**Important:**

* To access statistics, you must **select a Brand** and set your filters.
* Click **Display** to refresh the list.
* Then click **Statistics** to open the Statistics view.

All statistics are **per passenger** by default.

#### **Available Statistics Types**

| Category              | Levels                                                 |
| --------------------- | ------------------------------------------------------ |
| **Passengers**        | Total, Per Country, Per Arrival, Per Resort, Per Hotel |
| **Average Turnover**  | Total, Per Country, Per Arrival, Per Resort            |
| **Profit**            | Total, Per Country, Per Arrival, Per Resort, Per Hotel |
| **Average Profit**    | Total, Per Country                                     |
| **Percentage**        | Total                                                  |
| **Possible vs. Sold** | Total, Per Country                                     |

#### **Additional Tools for Statistics**

| Tool                                       | Description                                                                  |
| ------------------------------------------ | ---------------------------------------------------------------------------- |
| **Totals / Cost and Profit**               | Displays overall cost vs. profit based on selected filters.                  |
| **Additional Sales per Seller / Turnover** | Shows extra sales generated by individual sellers.                           |
| **Booking Date Statistic**                 | Breaks down bookings by creation date, per day or per week.                  |
| **Compare Statistics**                     | Adds a secondary filter set (Booking, Departure, Arrival) to compare trends. |

For detailed examples, screenshots, and recommended usage, see [Statistic in All bookings](statistic-in-all-bookings.md).

![](https://docs.tourpaq.com/assets/images/vab2-2ae8937c8c58496300b15fff0f0dbbf8.jpg?width=1857)

***

### **Turnover**

The **Turnover** view gives you a compact economic overview based on your current filters, showing how revenue and profit are distributed across the selected bookings.

<figure><img src="https://sonat.com/api/Document/Image/19670ef0-8b8a-4cda-8eb6-249681e07016/60a72aeb-a272-4428-a118-b6074b1b35b5/363d971e-5618-449b-aea7-3624b5a4097f.webp?width=1807" alt="" width="800"><figcaption></figcaption></figure>

Use this to quickly answer questions like:

* “What is the total turnover for this campaign period?”
* “How much revenue does this hotel or resort generate in the selected period?”

For a more detailed, totals‑focused explanation, see [All bookings Totals](all-bookings-totals.md).

***

### **Example Workflow**

1. Select a **Brand**.
2. Define a **Booking Period** using _Booking Start Date_ and _End Date_.
3. (Optional) Add filters like **Transport**, **Hotel**, **Status**, or **Owner**.
4. Click **Display** to see the booking results.
5. Review the **statistics bar** for a quick overview.
6. Click **Statistics** to view a detailed analytical breakdown by passengers, profit, turnover, and more.
