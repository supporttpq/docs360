# Special Offers

### **Overview**

The **Special Offers** page provides an overview of all active and upcoming promotional offers applied to hotels and room types. These offers may include early booking discounts, room cost adjustments, or seasonal promotions.\
Users can search, filter, and export special offers for specific hotels, resorts, or periods.

#### **Purpose**

The purpose of this page is to allow users to:

* View existing special offers configured for hotels.
* Filter offers based on booking or departure periods.
* Analyze discount rules and validity intervals.
* Export offers for reporting or verification purposes.

This feature ensures that sales and operations teams have full visibility into the pricing strategies and conditions applied to hotel rooms.

#### **Field Description**

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Filter Section**

| **Field**                          | **Description**                                                                                     |
| ---------------------------------- | --------------------------------------------------------------------------------------------------- |
| **Select Type**                    | Defines the offer category to display. Examples: _Early Booking_, _Room Cost_, etc.                 |
| **Select Resort**                  | Filters offers by resort. Only hotels belonging to the selected resort will be listed.              |
| **Select Hotel**                   | Filters results to a specific hotel. Useful for reviewing offers configured for one property.       |
| **Booking Period (From / To)**     | Defines the reservation period in which bookings must be made to qualify for the offer.             |
| **Departure Period (Start / End)** | Defines the actual travel or stay period during which the offer applies.                            |
| **Select Stars**                   | Filters hotels by their official star rating (e.g., 3★, 4★, 5★).                                    |
| **Semicolon for Export**           | When checked, exported CSV files will use semicolons (;) instead of commas (,) as field separators. |
| **Display**                        | Refreshes the results list according to the selected filters.                                       |
| **+ More Filters**                 | Expands additional filter criteria, if available.                                                   |
| **Clear**                          | Resets all filters to default values and clears the current selection.                              |

**Result Table Fields**

| **Column**                     | **Description**                                                                  |
| ------------------------------ | -------------------------------------------------------------------------------- |
| **Rule Type**                  | Type of promotion (e.g., _Early Booking_, _Room Cost_).                          |
| **Hotel**                      | Code of the hotel where the offer is applied.                                    |
| **From Date / To Date**        | The arrival period during which the offer is active.                             |
| **Bkg From / Bkg To**          | Booking period defining when reservations must be made to qualify for the offer. |
| **Days Number Before Arrival** | Minimum number of days before arrival required to benefit from the offer.        |
| **Room**                       | The room type(s) covered by the special offer.                                   |
| **Price**                      | The main promotional price or discount applied to the room.                      |
| **2nd / 3rd / 4th**            | Additional pricing columns for extra persons in the room                         |

#### **Instructions**

**1. Filtering Special Offers**

1. Select the desired filters (offer type, resort, hotel, booking period, etc.).
2. Click **Display** to update the results table.
3. Use **+ More Filters** for advanced filtering options.
4. To reset your search, press **Clear**.

***

**2. Viewing Results**

The table displays a list of all special offers that match the selected filters.\
Each row represents a distinct promotional rule with details about validity periods, rooms, and pricing.

Use the columns to:

* Verify if promotions overlap.
* Check that the booking and stay periods align.
* Confirm pricing and rule types per room category.

***

**3. Exporting Data**

Two export options are available:

* **Export CSV** – Generates a CSV file for analysis in Excel or other spreadsheet tools.
* **Export PDF** – Creates a formatted PDF report suitable for printing or sharing.

If **Semicolon for Export** is checked, the exported CSV will use “;” instead of “,” as a separator — useful for regional settings like Europe.

***

#### **How to Use – Example**

To review all _Early Booking_ offers for 4-star hotels:

1. Select **Type → Early Booking**.
2. Set **Select Stars → 4**.
3. Define a **Booking Period** and **Departure Period** if needed.
4. Press **Display** to show the results.
5. Export the table as **PDF** or **CSV** for reporting.

***

#### **Tips**

💡 _When multiple offers apply to the same room, verify that the date ranges do not overlap to avoid pricing conflicts._\
💡 _Use the “Export PDF” option for quick sharing with management or external partners._
