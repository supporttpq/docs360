# Special Offers

### Overview

The Special Offers page lists active and upcoming promotions for hotels and room types. Common examples are early booking discounts, room cost rules, and seasonal pricing.

Use filters to narrow results by resort, hotel, dates, and stars. Export results to CSV or PDF when you need to share or validate pricing.

### Purpose

Use this page to:

* Review special offers configured for hotels and rooms.
* Filter offers by booking period and travel period.
* Validate rule coverage, validity intervals, and overlaps.
* Export offers for reporting or verification.

### Related pages

* [Special Offer](hotel/hotel-creation/special-offer.md) (create and edit rules)

### Field description

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Filter Section**

| **Field**                          | **Description**                                                                                     |
| ---------------------------------- | --------------------------------------------------------------------------------------------------- |
| **Type**                           | Defines the offer category to display. Examples: _Early Booking_, _Room Cost_, etc.                 |
| **Resort**                         | Filters offers by resort. Only hotels belonging to the selected resort will be listed.              |
| **Hotel**                          | Filters results to a specific hotel. Useful for reviewing offers configured for one property.       |
| **Booking Period (From / To)**     | Defines the reservation period in which bookings must be made to qualify for the offer.             |
| **Departure Period (Start / End)** | Defines the actual travel or stay period during which the offer applies.                            |
| **Stars**                          | Filters hotels by their official star rating (e.g., 3★, 4★, 5★).                                    |
| **Semicolon for Export**           | When checked, exported CSV files will use semicolons (;) instead of commas (,) as field separators. |
| **Display**                        | Refreshes the results list according to the selected filters.                                       |
| **+ More Filters**                 | Expands additional filter criteria, if available.                                                   |
| **Clear**                          | Resets all filters to default values and clears the current selection.                              |

**Result Table Fields**

| **Column**                     | **Description**                                                                  |
| ------------------------------ | -------------------------------------------------------------------------------- |
| **Rule Type**                  | Type of promotion (e.g., _Early Booking_, _Room Cost_).                          |
| **Hotel**                      | Code and name of the hotel where the offer is applied.                           |
| **From Date / To Date**        | The arrival period during which the offer is active.                             |
| **Bkg From / Bkg To**          | Booking period defining when reservations must be made to qualify for the offer. |
| **Days Number Before Arrival** | Minimum number of days before arrival required to benefit from the offer.        |
| **Room**                       | The room type(s) covered by the special offer.                                   |
| **Price**                      | The promotional price or discount applied to the room.                           |
| **2nd / 3rd / 4th**            | Additional pricing columns for extra persons in the room.                        |

### Instructions

#### Filtering special offers

1. Select the desired filters (offer type, resort, hotel, booking period, etc.).
2. Click **Display** to update the results table.
3. Use **+ More Filters** for advanced filtering options.
4. To reset your search, click **Clear**.

#### Viewing results

Each row represents a promotional rule. Use the columns to confirm dates, room coverage, and price values.

Check overlaps when multiple rules target the same room and period.

#### Exporting data

Two export options are available:

* **Export CSV** – Generates a CSV file for analysis in Excel or other spreadsheet tools.
* **Export PDF** – Creates a formatted PDF report suitable for printing or sharing.

If **Semicolon for Export** is checked, the exported CSV will use `;` instead of `,`. This is useful for locales where Excel expects semicolons.

### How to use (example)

To review all _Early Booking_ offers for 4-star hotels:

1. Select **Type → Early Booking**.
2. Set **Stars → 4**.
3. Define a **Booking Period** and **Departure Period** if needed.
4. Press **Display** to show the results.
5. Export the table as **PDF** or **CSV** for reporting.

### Tips

{% hint style="info" %}
* Avoid overlapping date ranges for the same room and rule type.
* Use PDF for quick sharing. Use CSV for deeper checks.
{% endhint %}
