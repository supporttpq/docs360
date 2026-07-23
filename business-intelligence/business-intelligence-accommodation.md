---
description: >-
  Analyze hotel and accommodation performance in Tourpaq, including occupancy,
  allotment usage, and stay trends.
---

# Business Intelligence – Accommodation

### **Overview**

The _Business Intelligence – Accommodation_ report shows hotel allotment capacity and sales by week for a travel period.\
Use it to track available vs. sold rooms, compare allotment types, and follow booking pace over time.

You can filter by **country**, **resort**, **hotel**, **room type**, and **date period**.\
Results show weekly capacity utilization and sales progression trends.

***

### **Purpose**

The purpose of this page is to:

* Monitor room allotment usage and occupancy levels per hotel and room type.
* Identify sales performance by allotment type (Commitment, Allotment, Hotel Bed Bank).
* Support revenue optimization by tracking sold percentages and available capacity.
* Provide visibility into booking speed and progression over previous weeks.

***

### **Preconditions**

Before using the _Accommodation_ Business Intelligence report, make sure:

1. [Departure stat weeks](../setup/departure-stat-weeks.md) are defined for the selected year(s).\
   They are required to aggregate and display weekly sales correctly.
2. The selected **country/resort/hotel** has allotments inside the chosen **Date Period**.
3. You have access to the **Business Intelligence** module and hotel data.

{% hint style="warning" %}
**Tip:** If results don’t match your filters, check **departure stat weeks** first.\
Setup guide: [Departure stat weeks](../setup/departure-stat-weeks.md)
{% endhint %}

***

### **Field Descriptions and Sections**

<figure><img src="../.gitbook/assets/image (4) (1) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

**1. Filters (Top Section)**

* **Country:** Select the destination country where the accommodation is located.\
  Example: `GR – Greece`.
* **Resort:** Choose the specific resort area.\
  Example: `PVK–PARG – Parga`.
* **Hotel:** Select the hotel for which you want to view sales data.\
  Example: `Diogenis Studios`.
* **Room:** Select a specific room type or use “Room -” to view all rooms.\
  Example: `1-var. lej. (studio) – 2 pers.`
* **Date Period:** Defines the analysis period by setting a start and end date.\
  Example: `01-04-2024 → 01-06-2024`.
* **Hotel Allotment / Booking Date:**
  * _Hotel Allotment:_ Filters the report based on allotment type (e.g., Commitment, Allotment).
  * _Booking Date:_ Filters results by when bookings were made.
* **Rooms No / Beds No:** Allows inclusion or exclusion of rooms/beds in the report metrics.
* **Display / More Filters / Clear:**
  * **Display:** Generates the report based on selected filters.
  * **More filters:** Opens additional filtering options (Hotel allotment, Booking date).
  * **Clear:** Resets all filters to default values.
* **Show Guarantee Rooms / Show Codes:** Toggles guaranteed rooms and internal room codes.

***

**2. Report Summary (Left Panel)**

* **Report Generated Date:** Displays the date when the report was generated.\
  Example: `21-10-2025`.
* **% of Total Capacity Sold to Date:** Shows the total sold percentage across all listed accommodations.\
  Example: `100.00%`.

***

**3. Weekly Data Table**

| **Column**                   | **Description**                                                                                         |
| ---------------------------- | ------------------------------------------------------------------------------------------------------- |
| **Week No**                  | Calendar week number for the displayed period. The arrow (›) allows expanding details for that week.    |
| **Date**                     | The specific date (within that week) of the room allotment or booking.                                  |
| **Resort**                   | The resort where the hotel is located.                                                                  |
| **Hotel**                    | The hotel name.                                                                                         |
| **Allotment Type**           | Defines the contract type with the hotel (e.g., **Commitment**, **Allotment**, or **Hotel Bed Bank**).  |
| **Room**                     | The room type.                                                                                          |
| **Available**                | Number of unsold rooms for that week.                                                                   |
| **Sold**                     | Number of rooms sold.                                                                                   |
| **Total**                    | Total number of rooms (Available + Sold).                                                               |
| **Guarantee Rooms**          | Displays the number of guaranteed rooms (if applicable).                                                |
| **Sold %**                   | Percentage of rooms sold relative to total available.                                                   |
| **Price EUR**                | Displays the average selling price per room (if available).                                             |
| **Sold % 1W / 2W / 3W / 4W** | Sold percentage measured 1–4 weeks earlier for the same week. Use it to compare booking pace over time. |

***

### **How to use this report**

{% stepper %}
{% step %}
**Set your filters**

Select **Country**, **Resort**, **Hotel**, and **Date Period**.\
Use **Room** if you want a single room type.
{% endstep %}

{% step %}
**Generate results**

Click **Display** to refresh the report.
{% endstep %}

{% step %}
**Review sales pace**

Compare **Sold %** with **Sold % 1W–4W**.\
This shows if sales are accelerating or slowing down.
{% endstep %}
{% endstepper %}
