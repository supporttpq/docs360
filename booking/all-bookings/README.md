# All bookings

#### **Overview**

The **All Bookings** tab is a key reporting and monitoring tool within the system. It allows users to access a detailed view of all bookings and extract statistics using a wide array of filters. Filters are grouped by purpose: booking retrieval, transport/hotel configuration, and statistical analysis.

This section is designed for both operational oversight and performance analytics, supporting roles like sales agents, managers, and operations teams.

***

#### **Purpose**

The goal of this feature is to:

* Retrieve, view, and analyze all bookings based on defined criteria.
* Generate insightful statistics such as profit, turnover, booking trends, and customer distributions.
* Enable cleaner filtering and faster workflows with flexible filter visibility and system-wide optimization tools.

***

#### **Preconditions**

To use this section effectively, make sure:

* You are logged in with an account that has appropriate access rights.
* You select at least one **Brand** to begin using the filters.
* Filter pairs (e.g., booking date start & end) are **used together** to function correctly.
* Statistics will only be shown **per passenger** and require **a brand** to be selected.

***

#### **Instructions & Field Explanations**

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**🧩 Booking & General Filters**

| Field                            | Description                                                       | Example                                                                                                                                                                             |
| -------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Booking Period**               | Date range in which the booking was created.                      | `15-09-2025 – 21-09-2025`                                                                                                                                                           |
| **Departure Period**             | Date range for the trip departure.                                | `Start: 19-09-2025`                                                                                                                                                                 |
| **Arrival Period**               | Date range for the trip arrival.                                  | `21-09-2025`                                                                                                                                                                        |
| **Return Period**                | Date range for return trips.                                      | `End: 29-09-2025`                                                                                                                                                                   |
| **Pax No.**                      | Search by number of passengers in a booking.                      | `3`                                                                                                                                                                                 |
| **Status**                       | Filter bookings by status (confirmed, canceled, pending, etc.).   | `OK`                                                                                                                                                                                |
| **GDS Status**                   | Filter by GDS status if integrated.                               |  `GDSTKOK`                                                                                                                                                                          |
| **Internal Comment**             | Search bookings based on internal notes.                          | `Voucher issued`                                                                                                                                                                    |
| **Bonus Code**                   | Filter by promotional or bonus codes used in booking.             | `SUMMER25`                                                                                                                                                                          |
| **Hotels**                       | Filters by hotel names or assigned accommodations.                | `Grand Hotel Budapest`                                                                                                                                                              |
| **Transports / Real Transports** | Filters by transport types and specific assigned real transports. |                                                                                                                                                                                     |
| **Extra**                        | Filter by Extra and a specific Extra Categories                   | <div><figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div> |
| **Owners**                       | Filter bookings by the responsible agent or company.              | `RW/TPQ`                                                                                                                                                                            |

***

**Bookings Table (Main Section)**

| Column             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Booking No.**    | Unique booking identification number.                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Customer**       | Name of the customer or system automation                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Transport**      | Transport type and code.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Resort**         | Destination resort.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Hotel**          | Hotel assigned to the booking.                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Bkg. Date**      | Booking date                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Bk&#x67;**. Time** |  Booking time.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Nights/No**      | Number of nights booked.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Phone**          | Customer’s phone number.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Pax No.**        | Number of passengers in the booking.                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Owner**          | Responsible agent, user, or system owner of the booking.                                                                                                                                                                                                                                                                                                                                                                                      |
| **Departure**      | Departure date                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Extras             | <p>List all extras that are associated with a booking.                                                                   </p><p>At mouse-over, a tool-tip is shown, where a table shows how the extras belong to what passenger and the full name of the extras.    The Extras column is available in the column selector. <img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1).png" alt=""></p><p> </p> |
| ⋮                  | Column selector - add extra coulmns at the table                                                                                                                                                                                                                                                                                                                                                                                              |

***

**Statistics Section (Bottom)**

| Metric             | Description                                               | Example          |
| ------------------ | --------------------------------------------------------- | ---------------- |
| **Bookings**       | Total number of bookings in the filtered view.            | `72`             |
| **Total Pax**      | Total passengers across all bookings.                     | `208`            |
| **Pax / Booking**  | Average passengers per booking.                           | `2.9`            |
| **Total Turnover** | Total revenue generated from the bookings.                | `DKK 539,773`    |
| **Turnover / Pax** | Average revenue per passenger.                            | `DKK 2,595`      |
| **Profit Total**   | Total profit (revenue minus costs) for filtered bookings. | `DKK -2,751,155` |
| **Profit / Pax**   | Profit per passenger.                                     | `DKK -13,227`    |

**🧼 Hide Filters Functionality**

A feature designed to simplify the UI by hiding inactive filters.

| Option                               | Description                                                                                                                                                                               |
| ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Hide filters**                     | Hides all inactive or unused filters for cleaner navigation.                                                                                                                              |
| **Show hidden**                      | Checkbox on each filter – reveals or hides that specific filter.                                                                                                                          |
| **Choose all**                       | Applies selection to all filters, including hidden ones.                                                                                                                                  |
| **Hide as filter on lists**          | Manual way to hide filters — e.g., hide a specific transport from the filter options.                                                                                                     |
| **System Setup → Hide Filter input** | Global setting. Automatically hides outdated filters (e.g., transports, users) based on inactivity (number of days). Example: setting `10` hides transports not used in the last 10 days. |

<figure><img src="https://sonat.com/api/Document/Image/19670ef0-8b8a-4cda-8eb6-249681e07016/60a72aeb-a272-4428-a118-b6074b1b35b5/ec44a3d0-8810-4253-b486-355b314877ba.webp?width=898" alt="" height="200"><figcaption></figcaption></figure>

<figure><img src="https://sonat.com/api/Document/Image/19670ef0-8b8a-4cda-8eb6-249681e07016/60a72aeb-a272-4428-a118-b6074b1b35b5/f3b2074c-944c-4260-a801-0a280f9da0af.webp?width=933" alt="" height="300" width="400"><figcaption></figcaption></figure>

📊 **Statistics Filters and Tools**

<figure><img src="https://sonat.com/api/Document/Image/19670ef0-8b8a-4cda-8eb6-249681e07016/60a72aeb-a272-4428-a118-b6074b1b35b5/5f9160ba-43aa-4d8f-9f35-bbbdc227a335.webp?width=1854" alt="" width="400"><figcaption></figcaption></figure>

**Important:**\
To access statistics, filters must be set and a brand selected. After filtering, click **Display**, then **Statistics**.

**Available Statistics Types**\
All statistics are **per passenger** by default:

| Category              | Levels                                                 |
| --------------------- | ------------------------------------------------------ |
| **Passengers**        | Per Country, Per Arrival, Per Resort, Per Hotel        |
| **Average Turnover**  | Total, Per Country, Per Arrival, Per Resort            |
| **Profit**            | Total, Per Country, Per Arrival, Per Resort, Per Hotel |
| **Average Profit**    | Total, Per Country                                     |
| **Percentage**        | Total                                                  |
| **Possible vs. Sold** | Total, Per Country                                     |

**🛠 Additional Tools for Statistics**

| Tool                                       | Description                                                                  |
| ------------------------------------------ | ---------------------------------------------------------------------------- |
| **Totals / Cost and Profit**               | Displays overall cost vs. profit based on selected filters.                  |
| **Additional Sales per Seller / Turnover** | Shows extra sales generated by individual sellers.                           |
| **Booking Date Statistic**                 | Breaks down bookings by creation date, per day or per week.                  |
| **Compare Statistics**                     | Adds a secondary filter set (Booking, Departure, Arrival) to compare trends. |

![](https://docs.tourpaq.com/assets/images/vab2-2ae8937c8c58496300b15fff0f0dbbf8.jpg?width=1857)

### Turnover

This shows a short economic statistic based on the filters used

<figure><img src="https://sonat.com/api/Document/Image/19670ef0-8b8a-4cda-8eb6-249681e07016/60a72aeb-a272-4428-a118-b6074b1b35b5/363d971e-5618-449b-aea7-3624b5a4097f.webp?width=1807" alt="" width="800"><figcaption></figcaption></figure>

**💡 Example Workflow**

1. Select a **Brand**.
2. Define a **booking date range** using _Booking Start Date_ and _End Date_.
3. Optionally, add filters like **Transport**, **Hotel**, or **Status**.
4. Click **Display** to see the booking results.
5. Click **Statistics** to view the analytical breakdown by passengers, profit, turnover, etc.
