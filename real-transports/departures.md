# Departures

### **Overview**

The **Departures** section under _Real Transports_ displays all scheduled departures connected to a real (operational) transport setup.\
It provides detailed information such as departure dates, times, airlines, seat capacity, and related suppliers.\
This view ensures that all departures linked to the real transport are correctly defined and synchronized with the system data.

Each row represents **one specific departure** with all relevant data: times, airline, flight number, provider, seats, costs, taxes, load factor, and more.\
Bulk-edit tools allow operational users to update a full season in a few seconds.

### **Purpose**

The purpose of this page is to manage all real (operational) departures associated with a transport route.\
It allows users to review, verify, and adjust departure details to match actual transport operations and seat availability.

### **Preconditions**

Before viewing or editing departures for real transports, ensure that:

* The **Real Transport** has already been created and connected to a Transport Rule.
* The **Airline** and **Transport Supplier** exists in the system.
* Departure details (time, day, seats, and prices) are confirmed with the supplier.

#### **Instructions**

**Viewing Departures**

* Open **Transports → Real Transports → Departures**.
* The list displays all departures for the selected real transport.
* Use **Show Older** to include past departures in the view.

### Page Layout

<figure><img src="../.gitbook/assets/image (510).png" alt=""><figcaption></figcaption></figure>

#### Filters and Tools

At the top of the page, you can use several filters to search:

* **Date / End** – Define the period for which departures are displayed.
* **Week Days** – Filter by specific days of the week (multiple selection option).
* **Flight No** – Search by flight number.
* **Show Older** – Include older departures in the list.
* **Clear** – Reset all filters.
* **Run** – Execute the selected filter.

#### Buttons

* **Create** – Opens a new line to create a departure manually.
* **Send Flight Change** – Sends updated flight data to connected systems. Sending a Flight Change will also save any modifications made to the selected timetables.
* **Queue Flight Change** – Queues flight changes for later processing. Queuing a Flight Change will also save any modifications made to the selected timetables.

### **Row Selector**

Located on the left of the table.

* You can select **one**, **many**, or **all** departures.
* Header shows **“N of M selected”**.
* **Select All** allows bulk operations across the entire result set.

Row selection is required for:

* Bulk editing
* Running the **Change Value** tool
* Bulk operations for flight changes

### **Change Value Tool**

A powerful mass-edit tool used for changing values on multiple rows at once.

#### **Available Options**

* **Column**: Choose which column to update
* **Operation**: Add, subtract, replace
* **Value**: Numerical or text, depending on the field
* Press **Run** to apply the change to all selected rows

#### **Examples**

* Add +10 to PR Seat
* Replace Airline with “Airseven”
* Subtract 5 minutes from Departure Time

The Change Value Tool supports all columns marked as **Change value supported** in the functional

### **Table Columns**

Below are the most common columns shown on the Real Transport Departures page.

| Column                 | Description                                                                                                 |
| ---------------------- | ----------------------------------------------------------------------------------------------------------- |
| **Departure**          | The planned departure date                                                                                  |
| **Flight Change Type** | Option for selecting a predefined flight change scenario                                                    |
| **Day**                | Weekday of the departure                                                                                    |
| **Departure Time**     | Planned time of departure                                                                                   |
| **Arrival Time**       | Planned time of arrival                                                                                     |
| **Airline**            | Airline operating the flight                                                                                |
| **Flight No**          | Flight number (editable)                                                                                    |
| **Transport Supplier** | Supplier configuration                                                                                      |
| **Seats**              | The total number of seats. Allotment seats are SEATS minus (GUARANTEED + PRO RATE)                          |
| **Allotment**          | Number of Allotments seats                                                                                  |
| **Guaranteed**         | Guaranteed seats                                                                                            |
| **Pro Rate**           | Number of Pro Rate seats                                                                                    |
| **Allotment Cost**     | Cost for one allotment seat                                                                                 |
| **Guaranteed Cost**    | Cost for one Guaranteed seat                                                                                |
| **Pro Rate Cost**      | Cost for one Pro Rate                                                                                       |
| **Tax**                | Tax amount per passenger                                                                                    |
| **Load Factor (%)**    | Expected load factor, used for cost calculation                                                             |
| **Booked**             | Number of booked passengers                                                                                 |
| PNR                    | PNR code support                                                                                            |
| Booked Attached        | Number of booked seats in the parent transport. If checked, the departure is linked to the parent transport |

Each field is inline editable unless specified as calculated (e.g SEATS).

### **Sorting**

Columns marked as **sortable** can be clicked to reorder departures:

* Ascending
* Descending

Useful for:

* Grouping by airline
* Sorting by date
* Finding high load factor departures

## **Create  Departures**

1. Click **Create** to add a new departure line.&#x20;
2.  Fill in the following fields:

    * **Type** – Select the type of departure (Daily / Weekly).

    <figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

    * Frequency - If Daily is selected, insert the Every N days

    &#x20;                          \- If Weekly is selected, then insert the number of weeks and choose a specific day(s)

    * **Period -** Define the period for departures.
    * **Seats** – This section manages seat allocation and pricing:
      * **Guaranteed seats**\* – input for the number of guaranteed seats.
      * **Guaranteed seat cost**\* – input for the cost for a single guaranteed seat.
      * **Allotment seats** – input for allotment seats.
      * **Allotment seat cost** – input for the  cost for a single allotment seat.
    * **Flight Info** – Set the Airline, Flight number and the Transport supplier
      * **Airline** – Airline operating the flight.
      * **Flight no**\* – input field for flight number.
      * **Transport Supplier** – Supplier responsible for the real transport.
      * **Departure / Arrival Time** – Scheduled times for take-off and landing.
      * **Add days** – numeric input for adjusting arrival date.
      * **Class** – input field for class.
      * Departure time UTC icon - shows information about Departure /Arrival time UTC, and Flight time.
3. Save the changes.
