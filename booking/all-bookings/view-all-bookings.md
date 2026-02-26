---
description: >-
  Use Tourpaq Office View all bookings to search the All bookings list, apply
  booking filters, save views, and open booking details for reporting.
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

# View all bookings

### **Overview**

The **View all bookings** page is your main **booking search** view inside **Tourpaq Office → All bookings**. Use it to **search, filter, and review bookings** across one or more brands.

From this booking list, you can open booking details and continue to [Statistics in All bookings](statistic-in-all-bookings.md) or [All bookings Totals](all-bookings-totals.md) for reporting.

Access this page from **Booking → All Bookings**.

***

### **Purpose**

Use **View all bookings** to:

* Work with a centralized **All bookings list** for the selected brand(s).
* Apply **booking filters** on **dates, transports, hotels, users, brands**, and status.
* Prepare the filtered result set used by **Statistics** and **Totals**.
* Save filter combinations as **saved views** for recurring **booking reporting**.

***

### **Preconditions**

Before using **View all bookings**, make sure that:

* You are logged in with an account that has permission to view bookings.
* At least one **Brand** is selected – otherwise no bookings or statistics will be shown.
* Date range filters (for example **Booking Start/End** or **Departure From/To**) must be used **as pairs**, with both **From** and **To** filled in.

{% hint style="info" %}
If you get no results, first check that a **Brand** is selected and that any date filters you use have **both** a start and an end date.
{% endhint %}

***

### **How to use View All Bookings**

#### 1. Open the page

* Go to **Booking → All Bookings**.
* Select the **Brand** you want to work with (required).

#### 2. Set your filters

Filters narrow down which bookings are shown in the booking list.

| **Filter name**              | **Description**                                                               |
| ---------------------------- | ----------------------------------------------------------------------------- |
| **Brands**                   | Select one or more brands. **Required** to display any results.               |
| **Booking Start & End Date** | Shows bookings created in this period. Must be used together.                 |
| **Departure Date From & To** | Filters bookings by departure date range. Must be used as a pair.             |
| **Arrival Date From & To**   | Filters bookings by arrival date range. Must be used as a pair.               |
| **Return From & To**         | Filters bookings by return date range. Must be used as a pair.                |
| **All Bookings**             | Ignores date ranges and shows **all** bookings for the selected brand(s).     |
| **Filter by Bonus Code**     | Shows only bookings where a specific bonus code was used.                     |
| **User Owners**              | Filters bookings by the users/owners responsible for the booking.             |
| **Transports**               | Filters by transport (for example flight, bus) used in the booking.           |
| **Real Transports**          | Filters by specific real transport departures linked to bookings.             |
| **Hotels**                   | Shows only bookings with the selected hotel(s).                               |
| **Status**                   | Filters by booking status, for example **OK**, **Pending**, or **Cancelled**. |
| **GDS Status**               | Filters by Global Distribution System (GDS) status, if GDS is used.           |

You can combine **one, several, or all** filters as needed.

#### 3. Display the results

* After setting your filters, click **Display**.
* The bookings list is updated to show only bookings that match your criteria.
* Click a **Booking No.** (booking number) in the list to open booking details.

#### 4. Save a view (optional)

If you use the same filter combination regularly, you can save it as a view:

1. Set your filters and click **Display** so the list matches what you want to reuse.
2. Click **Save View** in the toolbar at the top of the page.
3. Enter a name (for example, `Today's arrivals` or `Last week – Brand DK`) and confirm.

Next time, select this saved view from the list to automatically re‑apply the same filters.

#### 5. Manage saved views (rename or delete)

To change or remove an existing saved view:

<figure><img src="../../.gitbook/assets/image (561).png" alt="Manage Views dialog in All bookings"><figcaption><p>Manage saved views in All bookings.</p></figcaption></figure>

1. In the views bar, click the **three dots (⋯)** button to open **Manage Views**.
2. In the **Manage Views** dialog:
   * **Rename a view** by editing its name directly in the text field.
   * **Delete a view** by clicking the **trash can** icon on the row.
   * (Optional) Use **Multiple delete** if you want to remove several views at once.
3. Click **Save** to apply your changes.

***

### **Hide filters (optional)**

If you work with many filters, you can hide the ones you rarely use:

* Use **Hide filters** to collapse less-used filters and keep the panel clean.
* A hidden filter is still included when you choose **Select all** inside that filter.
* To show a hidden filter temporarily, use the **Show hidden** checkbox for that filter.
* Administrators can also hide filters automatically based on inactivity using **System Setup → Hide Filter**.

For a more detailed description of all filters and statistics tools, see [All bookings](./).

***

### **Best practices**

* Always confirm that a **Brand** is selected before clicking **Display** or opening **Statistics**.
* Use complete **date ranges** (both From and To) to avoid empty or misleading results.
* Start with **a few filters** when troubleshooting (for example, looking for a missing booking), then narrow down.
* If the filter area feels cluttered, use **Hide filters** to focus only on what you need.

<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="View all bookings filter panel and booking list"><figcaption><p>View all bookings: filters on top, booking list below.</p></figcaption></figure>

***

### **FAQ**

#### Why do I get no results?

In most cases, no **Brand** is selected. Also check that any date filter has both **From** and **To** filled in.

#### Why do some date filters require both From and To?

These filters are designed to work as a range. If you set only one side, the system won’t apply the filter.

#### Who can create, rename, or delete saved views?

Saved views are typically tied to your user. If you can’t save or manage views, check your role permissions.
