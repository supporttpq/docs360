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

* The **Real Transport** is created and linked to a Transport Rule.
* The **Airline** and **Transport Supplier** exist in the system.
* You have confirmed times, seats, and prices with the supplier.

### View departures

1. Open **Transports → Real Transports → Departures**.
2. Review the list for the selected real transport.
3. Turn on **Show Older** if you also need past departures.

### Page layout

<figure><img src="../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

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

| Column                 | Description                                                                                                                                                                                                                                                                          |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Departure**          | The planned departure date                                                                                                                                                                                                                                                           |
| **Flight Change Type** | Option for selecting a predefined flight change scenario                                                                                                                                                                                                                             |
| **Day**                | Weekday of the departure                                                                                                                                                                                                                                                             |
| **Departure Time**     | Planned time of departure                                                                                                                                                                                                                                                            |
| **Arrival Time**       | Planned time of arrival                                                                                                                                                                                                                                                              |
| **Airline**            | Airline operating the flight                                                                                                                                                                                                                                                         |
| **Stop Sale**          | If checked, then the departure is no longer available for sale. Existing bookings on the departure are not affected.                                                                                                                                                                 |
| **Days**               | If the arrival passed midnight, specify the number of days added                                                                                                                                                                                                                     |
| **Offset**             | Is used to adjust hotel check-in or hotel check-out. For an outbound, the offset determines the hotel check-in, and for a homebound, the check-out is adjusted. A positive value adjusts the check-in/out later, and a negative value adjusts the check-in/out earlier.              |
| **Flight No**          | Flight number (editable)                                                                                                                                                                                                                                                             |
| **Class**              | Flight class                                                                                                                                                                                                                                                                         |
| **Transport Supplier** | Supplier configuration                                                                                                                                                                                                                                                               |
| **Seats**              | Total seats on the departure. Allotment seats = Seats − (Guaranteed + Pro Rate).                                                                                                                                                                                                     |
| **Allotment (seats)**  | Seats available as allotment seats                                                                                                                                                                                                                                                   |
| **Guaranteed (seats)** | Seats you have guaranteed with the supplier                                                                                                                                                                                                                                          |
| **Pro Rate (seats)**   | Seats handled as pro rate seats                                                                                                                                                                                                                                                      |
| **Allotment cost**     | Cost per allotment seat                                                                                                                                                                                                                                                              |
| **Guaranteed cost**    | Cost per guaranteed seat                                                                                                                                                                                                                                                             |
| **Pro Rate cost**      | Cost per pro rate seat                                                                                                                                                                                                                                                               |
| **Tax**                | Tax amount per passenger                                                                                                                                                                                                                                                             |
| **Base cost**          | If a base cost is specified, it will be used as the transport cost when calculating the price in the price list. The load factor will not impact the base cost. Note: The transport cost used in a booking is the actual cost of a seat (calculated based on the load factor, etc.). |
| **Load Factor (%)**    | Expected percentage of seats that will be filled                                                                                                                                                                                                                                     |
| **Booked**             | Number of booked passengers                                                                                                                                                                                                                                                          |
| **PNR**                | Booking reference (PNR), if used for this departure                                                                                                                                                                                                                                  |
| **Booked Attached**    | If enabled, the departure is linked to the parent transport                                                                                                                                                                                                                          |

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

    <figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

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

### FAQ

#### What is the difference between “Send Flight Change” and “Queue Flight Change”?

**Send Flight Change** sends the update right away.

**Queue Flight Change** saves the update and sends it later.

#### What does “Stop Sale” do?

It blocks the departure, is no longer available for sale

It does not cancel existing bookings.

#### How do I update many departures at once?

Select the rows you want to change.

Then use **Change Value** to apply one change to all selected rows.

#### Why can’t I edit some fields?

Some fields may be calculated or controlled by other settings.

If a field is locked, edit the related setup instead.

#### What does “Add days” mean?

It shifts the arrival date forward by the number of days you enter.

Use it for overnight flights where arrival is the next day.
