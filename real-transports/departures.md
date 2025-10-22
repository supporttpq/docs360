# Departures

### **Overview**

The **Departures** section under _Real Transports_ displays all scheduled departures connected to a real (operational) transport setup.\
It provides detailed information such as departure dates, times, airlines, seat capacity, and related suppliers.\
This view ensures that all departures linked to the real transport are correctly defined and synchronized with the system data.

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

<figure><img src="../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

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

### Departure Table Columns

| Column                   | Description                                                      |
| ------------------------ | ---------------------------------------------------------------- |
| **Departure**            | The departure date for the flight                                |
| **Day**                  | Automatically displays the weekday of the departure.             |
| **Departure Time**       | Time when the flight leaves the departure location.              |
| **Arrival Time**         | Time when the flight arrives at the destination.                 |
| **Airline**              | The airline operating the flight. Select from available options. |
| **Flight No**            | The assigned flight number.                                      |
| **Transport Supplier**   | The supplier responsible for the transport operation.            |
| **Seats**                | Number of available seats for this departure.                    |
| **Allotment Seat Price** | The cost per seat allocated for this flight or transport.        |

**Create  Departures**

1.  Click **Create** to add a new departure line.&#x20;

    <figure><img src="../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
2.  Fill in the following fields:

    * **Type** – Select the type of departure (Daily / Weekly).
    * Frequency - If Daily is selected, insert the Every N days

    &#x20;                          \- If Weekly is selected, then insert the number of weeks and choose a specific day(s)

    * **Period -** Define the period for departures.
    * **Seats** – Total number of Available / Guaranteed seats and the price for each seat.
    * **Flight Info** – Set the Airline, Flight number and the Transport supplier
      * **Airline** – Airline operating the flight.
      * **Transport Supplier** – Supplier responsible for the real transport.
      * **Departure / Arrival Time** – Scheduled times for take-off and landing.
3. Save the changes.
