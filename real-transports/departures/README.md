# Departures

### Overview

**Departures** (under _Real Transports_) shows every planned departure for a specific real transport.

Each row is one departure. It includes the date, times, airline, flight number, seats, prices, and status.

You can edit one row at a time. You can also update many rows at once.

### Purpose

Use this page to keep departures correct and up to date.

This helps your bookings match what the supplier will actually operate.

### Before you start

Make sure these are in place:

* You have confirmed times, seats, and prices with the supplier.

### View departures

1. Open **Transports → Real Transports → Departures**.
2. Review the list for the selected real transport.
3. Turn on **Show Older** if you also need past departures.

### Page layout

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Filters and tools

Use these filters at the top of the page:

* **Date / End** – Choose the date range to display.
* **Week Days** – Filter by day of the week (you can pick more than one).
* **Flight No** – Search by flight number.
* **Show Older** – Include departures from the past.
* **Clear** – Reset all filters.
* **Run** – Apply the filters.

#### Buttons and actions

* **Create** – Opens a new line to create a departure manually.
* **Send Flight Change** – Sends updated flight details to connected systems. It also saves your edits.
* **Queue Flight Change** – Saves your edits and puts the change in a queue for later processing.

### Select rows (row selector)

Located on the left of the table.

* You can select **one**, **many**, or **all** departures.
* The header shows **“N of M selected”**.
* **Select All** selects all rows in the current result set.

Row selection is required for:

* Updating many rows at once
* Running the **Change Value** tool
* Sending or queueing flight changes

### Change Value tool (update many rows)

Use **Change Value** when you need the same change on several departures.

#### Available options

* **Column**: Choose which column to update
* **Operation**: Add, subtract, or replace
* **Value**: Numerical or text, depending on the field
* Press **Run** to apply the change to all selected rows

#### Examples

* Add +10 to PR Seat
* Replace Airline with “Airseven”
* Subtract 5 minutes from Departure Time

Some columns do not support Change Value. Those fields must be edited per row.

### Table columns

These are the most common columns on this page.

| Column                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Departure**          | The planned departure date                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Flight Change Type** | <p>Displays the type of flight change for the given date based on what changed at the respective departure.<br>Flight change types are configured in System Setup -> Flight Change Queue. (See <a href="../../flight-change/">Flight Change</a>)</p>                                                                                                                                                                                                                                                                                                                                      |
| **Day**                | Weekday of the departure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Departure Time**     | Planned time of departure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Arrival Time**       | Planned time of arrival                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Airline**            | Airline operating the flight                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Stop Sale**          | If checked, then the departure is no longer available for sale. Existing bookings on the departure are not affected.                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Days**               | If the arrival passed midnight, specify the number of days added                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Offset**             | Is used to adjust hotel check-in or hotel check-out. For an outbound, the offset determines the hotel check-in, and for a homebound, the check-out is adjusted. A positive value adjusts the check-in/out later, and a negative value adjusts the check-in/out earlier.                                                                                                                                                                                                                                                                                                                   |
| **Flight No**          | Flight number (editable)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Class**              | Flight class                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Transport Supplier** | Supplier configuration                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Seats**              | Total seats on the departure. Allotment seats = Seats − (Guaranteed + Pro Rate).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Allotment (seats)**  | Seats available as allotment seats                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Guaranteed (seats)** | Seats you have guaranteed with the supplier                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Pro Rate (seats)**   | Seats handled as pro rate seats                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Allotment cost**     | Cost per allotment seat                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Guaranteed cost**    | Cost per guaranteed seat                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Pro Rate cost**      | Cost per pro rate seat                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Tax**                | Tax amount per passenger                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Base cost**          | <p>If a base cost is specified, it will be used as the transport cost when calculating the price in the price list. The load factor will not impact the base cost. Note: The transport cost used in a booking is the actual cost of a seat (calculated based on the load factor, etc.).</p><p>If Base Cost is specified:</p><ul><li>It overrides Guaranteed, Allotment, and Pro-rate seat costs in the Price List</li><li>The Load Factor does not affect this value</li></ul><p>If Base Cost is empty:</p><ul><li>The system uses the current transport cost calculation logic</li></ul> |
| **Load Factor (%)**    | Expected percentage of seats that will be filled                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Booked**             | Number of booked passengers                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **PNR**                | Booking reference (PNR), if used for this departure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Booked Attached**    | If enabled, the departure is linked to the parent transport                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |

You can edit most fields directly in the table. Some fields may be locked.

### Sorting

Columns marked as **sortable** can be clicked to reorder departures:

* Ascending
* Descending

Useful for:

* Grouping by airline
* Sorting by date
* Finding high load factor departures

### Create departures

1. Click **Create** to add a new departure.
2.  Fill in the fields below. Fields marked with `*` are required.

    * **Type** – Select **Daily** or **Weekly**.

    <figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (17).png" alt=""><figcaption></figcaption></figure>

    * **Frequency**
      * If **Daily**: set **Every N days**.
      * If **Weekly**: set **Every N weeks**, then select the weekday(s).
    * **Period** – Set the date period you want to create departures for.
    * **Seats and pricing**
      * **Guaranteed seats** `*` – Number of guaranteed seats.
      * **Guaranteed seat cost** `*` – Cost per guaranteed seat.
      * **Allotment seats** – Number of allotment seats.
      * **Allotment seat cost** – Cost per allotment seat.
    * **Flight info**
      * **Airline** – Airline operating the flight.
      * **Flight no** `*` – Flight number.
      * **Transport Supplier** – The supplier responsible for the transport.
      * **Departure / Arrival Time** – Planned take-off and landing times.
      * **Add days** – Add days to the arrival date (for overnight flights).
      * **Class** – Travel class, if used.
      * **Departure time UTC** icon – Shows the UTC times and flight time.
3. Click **Save** to store the departure.

## Real Transport Cost Calculation

The Real Transport cost represents the cost allocated to each passenger based on the transport's guaranteed commitment and the number of passengers booked on the corresponding departure.

The cost is calculated separately for the **outbound** and **homebound** flights. The resulting costs are then combined to determine the total transport cost for the passenger's round trip.

### Cost configuration

The Real Transport departure contains the values used as the basis for the cost calculation.

In the **Departures** tab, the relevant cost fields are displayed in the **Cost (EUR)** section:

| Field           | Description                                                                                                                      |
| --------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **Allotment**   | The number of seats allocated to the departure.                                                                                  |
| **Guaranteed**  | The guaranteed number of seats committed for the departure. This value is used to calculate the guaranteed transport commitment. |
| **Pro Rate**    | The pro-rata cost associated with the departure, when applicable.                                                                |
| **Base Cost**   | The base cost used for the transport cost calculation.                                                                           |
| **Load Factor** | The load factor applied to the transport cost, when configured.                                                                  |
| **Booked**      | The number of passengers booked on the departure.                                                                                |

{% hint style="info" %}
The guaranteed commitment is calculated from the guaranteed seats and the applicable cost per guaranteed seat.
{% endhint %}

### How the passenger cost is calculated

The cost is calculated separately for each flight direction.

#### 1. Calculate the guaranteed commitment

The guaranteed commitment is calculated as:

**Guaranteed seats × Cost per guaranteed seat**

For example:

**174 seats × EUR 1,283.00 = EUR 223,242.00**

#### 2. Divide the commitment by the actual number of booked passengers

The guaranteed commitment is distributed across the passengers booked on that departure.

**Guaranteed commitment ÷ Actual booked passengers = Cost per passenger**

For example:

**EUR 223,242.00 ÷ 171 passengers = EUR 1,305.51**

#### 3. Add applicable tax

Any applicable tax is added to the calculated passenger cost.

**Passenger cost + Tax = Final cost per passenger**

#### 4. Calculate the round-trip cost

For a round trip, the outbound and homebound costs are calculated independently and then added together.

**Outbound cost + Homebound cost = Round-trip cost per passenger**

#### 5. Calculate the booking cost

The round-trip passenger cost is multiplied by the number of passengers included in the booking.

**Round-trip cost per passenger × Number of passengers = Total booking transport cost**

The final booking amount is rounded according to the applicable currency rounding rules.

***

### Example

Consider the following two departures:

#### Outbound flight

**Departure:** 09 May 2026

* Guaranteed seats: **174**
* Cost per guaranteed seat: **EUR 1,283.00**
* Actual booked passengers: **171**
* Tax: **EUR 316.00**

**Guaranteed commitment**

174 × EUR 1,283.00 = **EUR 223,242.00**

**Cost allocated per passenger**

EUR 223,242.00 ÷ 171 = **EUR 1,305.51**

**Final outbound cost**

EUR 1,305.51 + EUR 316.00 = **EUR 1,621.51**

**Outbound cost per passenger: EUR 1,621.51**

***

#### Homebound flight

**Departure:** 16 May 2026

* Guaranteed seats: **174**
* Cost per guaranteed seat: **EUR 1,283.00**
* Actual booked passengers: **173**
* Tax: **EUR 0.00**

**Guaranteed commitment**

174 × EUR 1,283.00 = **EUR 223,242.00**

**Cost allocated per passenger**

EUR 223,242.00 ÷ 173 = **EUR 1,290.42**

**Final homebound cost**

EUR 1,290.42 + EUR 0.00 = **EUR 1,290.42**

**Homebound cost per passenger: EUR 1,290.42**

***

### Round-trip cost

The two flight costs are added together:

**EUR 1,621.51 + EUR 1,290.42 = EUR 2,911.93**

Therefore:

**Round-trip transport cost per passenger = EUR 2,911.93**

#### Cost for two passengers

For a booking containing two passengers:

**EUR 2,911.93 × 2 = EUR 5,823.86**

After rounding:

**Total transport cost = EUR 5,824**

***

### When is the cost updated on the booking?

The transport cost on the booking is based on the cost calculated for the relevant Real Transport departures and is update when the cost is changed.
