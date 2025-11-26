# Flight Transfer Export

**Available to:** Admin and Guide user types

### Overview

The **Flight Transfer Export** function enables users to generate reports based on data from the **Flight Transfer Settings**. These reports provide detailed information about flight-related transfers and can be exported in different formats depending on operational needs.

### Purpose

This feature supports both administrators and guides in managing and monitoring passenger transfers between flights and resorts. By exporting the relevant lists, users can ensure smooth coordination of transfers and accurate communication with transport operators.

### Filters

The available **filters** vary depending on the type of list selected for export. Each export type provides its own filtering options to tailor the output to the required data.

### Airport Plan Overview​ <a href="#airport-plan-overview" id="airport-plan-overview"></a>

Generates a list which will contain (for homebounds and outbounds):

* departure date and agency
* Legend detailed below
* all airports/or the selected one from the filters, with flights outbound and homebound
* estimated time of arrival and departure for flights(A, B columns)
* flight number (C column)
* IATA code (D column)
* number of seats booked on the outbound/homebound flights (E column)
* number of free seats on the homebound/outbound flights (F column)
* number of booked transfers (G column)
* resorts columns with the total number of transfers assigned (starts with H and ends depending on the number of resorts)
* arrival column with number of passengers with flight only without transfer booked (last Column)

(Legend) The background is colored accordingly:

* green- if bus capacity is adequate/seating on a bus is smaller than the allocation of a bus
* red- if the bus capacity is too low/seating on a bus is bigger than the allocation of the bus
* no background- if there are no buses assigned/no bus and allocation created so far
* bold value- if buses are confirmed/confirmation is checked
* underlined value- if all pax are seated/if there are still pax booked on a given flight/resort transfer

<figure><img src="../.gitbook/assets/ftr10-e5d703ed162ac3696181e4d9df53d415.png" alt=""><figcaption></figcaption></figure>

Filters:

* Departure Date From
* Departure Date To
* Arrivals

<figure><img src="../.gitbook/assets/image (24) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Transfer Airport Report PDF/Excel​ <a href="#transfer-airport-report-pdfexcel" id="transfer-airport-report-pdfexcel"></a>

It is a list of all transfers serving an airport, their load capacity, and the route plan. The list can be exported in PDF or Excel versions, is divided into 2 parts, and contains:

**Part 1 contains**:

* Agency details (name, phone number, email address)
* Arrival airport and date
* ETD- estimated time of departure of the flight
* ETA- estimated time of arrival of the flight
* Departure- Homebound Flight number
* Arrival- Outbound Flight number
* Pax- total number of allocated pax on the corresponding flight having a flight transfer booked (extras on the booking selected)
* Homebound Bus Schedule
* Time of the flight arrival at the airport
* Passengers with a transfer and their route
* Passengers without transfer
* Total number of passengers

<figure><img src="../.gitbook/assets/ftr11-eea478144ae8f0ff57404bbbac9a590a.png" alt=""><figcaption></figcaption></figure>

**Part 2 contains**:

* Bus details - name, number, time it leaves the home resort, and time it returns to it, route name
* Route plan to the airport - resorts on the route and their stop times, flight number of the passengers, and number of passengers to pick up from each resort
* Route plan from the airport - resorts on the route and their stop times, flight number of the passengers, and number of passengers to leave at each resort
* Bus company details - bus driver name, guide name, phone, email
* Guides on the bus

<figure><img src="../.gitbook/assets/ftr12-f0165c6cd987e013abbe89ab4fed80b2.png" alt=""><figcaption></figcaption></figure>

Filters:

* Departure Date From
* Arrivals
* Resorts

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (2).png" alt=""><figcaption></figcaption></figure>

### Transfer Bus Report​ <a href="#transfer-bus-report" id="transfer-bus-report"></a>

Generates a list that gives an overview of the buses in the airport, either homebound or outbound.

Information is grouped by:

* Transfer number
* Operator
* Transfer type
* Route
* Resort departure hour
* Airport hour
* Resort arrival hour
* Passenger number on departure from the resort
* Passenger number on return to the passenger resort
* Number of passengers per flight for each transfer
* Cost per transfer

<figure><img src="../.gitbook/assets/ftr13-4e3a0bdcee6bba1279b3627c740e401b.png" alt=""><figcaption></figcaption></figure>

Filters:

* Departure Date From
* Arrivals
* Resorts
* Operators
* Buses

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Flight Transfer Order​ <a href="#flight-transfer-order" id="flight-transfer-order"></a>

Generates a list that contains information about the transfers of a transfer operator for a certain date:

* transfer details - bus name, type and route
* outbound information - passengers number, flight number, flight time
* home information - passengers number, flight number, flight time
* transfer operator details - driver name, guide name

<figure><img src="../.gitbook/assets/ftr14-0fe94cc2ea1748ec3158d6ecd67d3cf5.png" alt=""><figcaption></figcaption></figure>

Filters:

* Departure Date From
* Arrivals
* Resorts
* Operators
* Buses

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Transfer Seating/Pax PDF/Excel​ <a href="#transfer-seatingpax-pdfexcel" id="transfer-seatingpax-pdfexcel"></a>

The list can be exported in PDF or Excel version and contains information about:

* total number of passengers for either outbound or homebound
* passenger names
* booking number of the passenger
* resort of the passenger
* bus number of the passenger
* flight number
* airports
* stops

<figure><img src="../.gitbook/assets/ftr15-4421be07b9a0772e61f649afc9f25e34.png" alt=""><figcaption></figcaption></figure>

Filters:

* Departure Date From
* Outbound/Homebound
* Arrivals
* Resorts
* Operators
* Buses

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Transfer Seating/Bus + Stop PDF/Excel​ <a href="#transfer-seatingbus--stop-pdfexcel" id="transfer-seatingbus--stop-pdfexcel"></a>

A list containing detailed information about each bus and their route grouped by the stops made and bookings. Can be exported in PDF or Excel versions.

Details:

* Transfer number
* Transfer type
* Flight details
* Number of passengers
* Stops and bookings assigned to it

<figure><img src="../.gitbook/assets/ftr16-6bc362d0f365f31fa85e0033aa724293.png" alt=""><figcaption></figcaption></figure>

Filters:

* Departure Date From
* Outbound/Homebound
* Arrivals
* Resorts
* Operators
* Buses

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Transfer Seating/Bus + Pax PDF/Excel​ <a href="#transfer-seatingbus--pax-pdfexcel" id="transfer-seatingbus--pax-pdfexcel"></a>

A list detailing all passengers by bus that can be exported as a pdf or excel file and contains:

* Passenger name
* Booking number
* Flight number
* Departure and Arrival for flight
* Resort of the passenger
* Hotel of the passenger

<figure><img src="../.gitbook/assets/ftr17-2beca1b4cdb5b2eab22f6a9e365b53c8.png" alt=""><figcaption></figcaption></figure>

Filters:

* Departure Date From
* Outbound/Homebound
* Arrivals
* Resorts
* Operators
* Buses

<figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Departure information​ <a href="#departure-information" id="departure-information"></a>

Exports the information set in **Flight Transfer/Departure information** in a pdf file for each booking and the data is displayed in this order:

* Booking details (customer name, booking number, accomodation place, number of passengers on the booking, flight number) -> taken from the booking
* Customer name -> taken from the booking
* Destination Text - Beginning
* Departure Information Text for Hotels
* Destination Text - Transport type
* Desination Text - Closing

<figure><img src="../.gitbook/assets/ftr9-2359af526a57a62f2b7f59dfb7878635.png" alt=""><figcaption></figcaption></figure>

Filters:

* Departure Return Date
* Arrivals
* Resorts

<figure><img src="../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
