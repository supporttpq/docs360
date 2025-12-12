# All bookings Totals

### **Overview**

The **All bookings Totals** section gives you a **summarized, booking‑level overview** based on your current filters in [All bookings](./).

It shows:

* Total number of **bookings**
* Total number of **passengers**
* Aggregated **turnover** and **profit** (if enabled)

This functionality is part of the **All bookings** page and is designed for a quick, high‑level view of booking volume and business performance. For more detailed, per‑passenger analytics, use [**Statistics in All bookings**](statistic-in-all-bookings.md).

***

### **Purpose**

Use **All bookings Totals** to:

* Summarize booking data across custom‑defined filters.
* Quickly check totals for **bookings**, **passengers**, and optionally **turnover/profit**.
* Analyze booking behavior by **period**, **transport**, **hotel**, **status**, and more.
* Get a compact overview before drilling down into individual bookings or statistics.

***

### **Preconditions**

To use **All bookings Totals** effectively, make sure:

* You have access to the **All bookings** page under the **Booking** menu.
* At least one **Brand** is selected (either all brands or one specific brand).
* You apply at least one **date filter pair** (e.g. **Booking period**, **Departure period**, or **Arrival period** with both `from` and `to` dates).
* You click **Display** in **All bookings** to refresh the result list.

The Totals section shows **aggregated values** (counts and sums). For **per‑passenger averages and detailed breakdowns**, use [Statistics in All bookings](statistic-in-all-bookings.md).

{% hint style="info" %}
If totals show `0` or appear empty, first check that a **Brand** is selected and that all date filters you use have both **from** and **to** dates. Then click **Display** again.
{% endhint %}

***

### **Quick start**

{% stepper %}
{% step %}
### 1. Open **All bookings**

1. Go to **Booking → All bookings**.
2. Select at least one **Brand**.
3. Make sure you have the necessary access rights to see financial data (if you want turnover/profit).
{% endstep %}

{% step %}
### 2. Apply filters for the totals

1. Set at least one **date period**:
   * **Booking period** – when the booking was created, or
   * **Departure period** – when the trip starts, or
   * **Arrival period** – when customers arrive at the destination.
2. Always use date filters as **pairs** (`from` + `to`).
3. Optionally add more filters such as **Owner**, **Transport**, **Real Transport**, **Hotel**, or **Status**.
{% endstep %}

{% step %}
### 3. Click **Display** and read the totals

1. Click **Display** in **All bookings**.
2. At the bottom (or in the relevant totals area), review the **Totals**:
   * Total **bookings**
   * Total **passengers**
   * **Turnover** and **profit** aggregates (if enabled).
3. Adjust filters and click **Display** again to update the totals.
{% endstep %}
{% endstepper %}

***

### **Filters for Totals**

Use filters in **All bookings** to control which bookings are included in the totals.

| Filter Type          | Description                                                                                        |
| -------------------- | -------------------------------------------------------------------------------------------------- |
| **Brand**            | Select one or more brands to include. At least one brand must be selected.                         |
| **Booking period**   | `From` and `To` dates for when the bookings were **created**.                                      |
| **Departure period** | `From` and `To` dates for when trips **depart**.                                                   |
| **Arrival period**   | `From` and `To` dates for when customers **arrive** at the destination.                            |
| **Owner**            | Filter by booking owner/creator (e.g. a user, office, or agency).                                  |
| **Transports**       | Filter by planned transport services (e.g. specific flights or routes).                            |
| **Real transports**  | Filter by actual assigned transport services (real flights, buses, etc.).                          |
| **Hotels**           | Filter by the hotel or accommodation linked to the booking.                                        |
| **Status**           | Filter by booking status (e.g. **OK**, **Cancelled**, **Error**, **Locked** – depending on setup). |

{% hint style="warning" %}
Date‑based filters (**Booking**, **Departure**, **Arrival**) must always be used as **complete pairs** (`from` and `to`) to give valid totals.
{% endhint %}

***

### **Notes & best practices**

* The **Totals** update **only after** you click **Display** in **All bookings**.
* Combine filters to focus on a specific segment, for example:
  * All bookings for **Resort A** departing in **September** on a specific **Real Transport**.
  * All bookings with **Status = OK** for a given **hotel** and **brand**.
* Use **Saved Views** in All bookings if you often check the same totals (e.g. “This week’s sales”, “Monthly overview per brand”).
* Compare **All bookings Totals** with **Statistics**:
  * **Totals** = high‑level aggregated counts/sums.
  * **Statistics** = per‑passenger breakdowns and averages (profit, turnover, passengers per country/hotel, etc.).

<figure><img src="../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="All bookings Totals overview"><figcaption><p>Example of the Totals overview for a filtered set of bookings.</p></figcaption></figure>

***

### **FAQ**

#### **1. Why do the totals show 0 even though I know there are bookings?**

This is usually caused by one of the following:

* No **Brand** is selected.
* A **date filter** (Booking/Departure/Arrival) is missing either the `from` or `to` date.
* You changed filters but did not click **Display** again in **All bookings**.

Verify these points, click **Display**, and check the Totals again.

***

#### **2. Are totals calculated per booking or per passenger?**

Totals focus on **aggregated booking data**:

* **Bookings** = total number of bookings in the filtered view.
* **Passengers** = total number of passengers across those bookings.
* **Turnover/Profit** = sums across all included bookings.

For per‑passenger statistics and averages (e.g. **Average Turnover per passenger**, **Profit per passenger**), use [**Statistics in All bookings**](statistic-in-all-bookings.md).

***

#### **3. Which date filter should I use for Totals – Booking, Departure, or Arrival?**

Use the date filter that matches your question:

* **Booking period** – when customers made the booking (useful for **sales/campaign analysis**).
* **Departure period** – when trips depart (useful for **operational load** and departure‑based reports).
* **Arrival period** – when customers arrive at the destination (useful for **in‑destination planning**).

You can combine them, but each date type must be used as a **full pair** (`from` + `to`).

***

#### **4. Why do totals differ from the numbers I see in Statistics?**

Differences often come from:

* **Different focus**: Totals show **overall counts/sums**, while Statistics often shows **per‑passenger** averages and breakdowns.
* **Different filters**: If filters (Brand, Status, Hotel, Transport, etc.) are not exactly the same, the results will differ.
* **Different date periods**: For example, Totals filtered by **Booking period** vs Statistics filtered by **Arrival period**.

Align filters and date periods between **All bookings Totals** and **Statistics** to compare results correctly.

***

#### **5. I do not see turnover or profit in my totals – why?**

Possible reasons:

* Your **user role/permissions** does not allow viewing financial data.
* Turnover/profit display may be **disabled** in your company’s configuration.

Contact your **Tourpaq administrator** if you believe you should have access to these financial totals.

***

#### **6. Can I export the totals to Excel or another format?**

If export is enabled for your environment, you may see an **Export** or **Excel** option on the **All bookings** page or related reports. Use this to download the results based on your current filters.

If no export option is visible, ask your **Tourpaq administrator** or support contact whether exports are available for your user.

***

#### **7. When should I use All bookings Totals vs Statistics in All bookings?**

Use **All bookings Totals** when you need:

* A **quick, aggregated overview** of bookings, passengers, turnover, and profit.
* A simple check of **volume and revenue** for a filtered segment.

Use [**Statistics in All bookings**](statistic-in-all-bookings.md) when you need:

* **Per‑passenger** statistics and averages.
* Detailed breakdowns by **country, arrival date, resort, or hotel**.
* Tools like **Compare Statistics**, **Booking Date Statistics**, or **Additional Sales per Seller**.
