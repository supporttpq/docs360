# Transport creation

This feature is available for administrator user type.

More information can be found in [Transport](https://docs.tourpaq.com/docs/transport/transport)

### General <a href="#general" id="general"></a>

Mandatory fields:

* Code - name of the transport, mostly it's the abbreviation of the departure and arrival names.
* Return - return code
* Departure - place from which the transport leaves
* Arrival - place where the transport arrives
* Cancelation condition
* Transport mode
* Travel lenght (in minutes)
* Dynamic itineraries (only if you are using real transport feature or GDS)

Other fields:

* Infant price - price the infants pay
* Payment rule
* Use Change Rule Service
* Seat map (only if transport layout is enabled) - allows for guest the select their seats
* Airline (only if Transport mode is FLY)
* Transport type
* Pickup point - please check \[\[Routes]]
* Show on dashboard
* Shift checkin date by +/- days - controls checking days in the hotel
* Estimated seats sale percentage
* Hotel nights correction +/- days -
* Tour operator
* Reporting type
* Dynamic Itineraries - setting for Real Transports and GDS
* Use real transport allotments (only if Dynamic itineraries is checked)
* Status
* Outbound parent transport - select a transport from which the created transport can draw seats. (**Example**: Transport1 departs from DepartureA, has a stop in PointB and then goes to DestinationC. The two transports DepA-DestC and PointB-DestC indeed share the same transport seats allotment); the new created transport will share the alltoments and layout with the parent set for outbound flight.
* Homebound parent transport - select a transport from which the created transport can draw seats. Cand be a different transport for the homebound flight. (**Example**: P1: charter transport (7 days) that departs every Wednesday, (01.01.2025 - 31.12.2025), P2: charter transport (7 days) that departs every Saturday, (04.01.2025 - 27.12.2025), C1 - child transport having P1 outbound parent and P2 homebound parent - charter transport (3 days) that departs every Wednesday (homeboud is every Saturday) (01.01.2025 - 27.12.2025), C2 - child transport having P2 outbound parent and P1 homebound parent - charter transport (4 days) that departs every Saturday (homebound is every Wednesday) (04.01.2025 - 31.12.2025) ). Once "outbound parent transport" is set, is mandatory to have also homebound parent. You cannot set one without the other. So if there are no different parent transports for outbound and homebound, just set the same one on both legs.

<figure><img src="../.gitbook/assets/ParentTransport-8a32e65eb158c08eebd7443e07c63fa3.png" alt=""><figcaption></figcaption></figure>

* Dynamic Transport Supplement - when checked, transport price will be added as a supplement to guests in the booking (needs DTS supplement)

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

### Brands <a href="#brands" id="brands"></a>

Select a brand for the transport

### Interval Def <a href="#interval-def" id="interval-def"></a>

Set the interval between flights.

* Interval
* Date From - start date
* Date To - end date
* Days - days between the flights
* API Text It's used in setting the fix quota. Multiple intervals can be set.

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

### Timetable <a href="#timetable" id="timetable"></a>

Used to set the date and time of the flights.

* Out/Home - flight type
* Start period
* End period
* Departure time (hour)
* Arrival time (hours)
* Airline
* Flight number
* Days - the transport arrives at the destination with a delay of x days from the departure date (eg: departure 01-05-2025 00:00, arrival 02-05-2025 00:00)
* Land days (should be disabled for travel out)
* Extra day out - controls hotel check-in days
* FL - flinght changes (After changing time and date of a flight, check this and update; an e-mail will be sent to all bookings made on this flight that the flight hours have been changed. Requires **Flight change e-mail** template
* Alternative Airport - this can be set only for the Travel home lines and can change the returning airport. It will be shown on booking and ticket. (Example: Flight leaves from Billund to Krete and returns to Kobenhavn instead of Billund)

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

#### Fix quota <a href="#fix-quota" id="fix-quota"></a>

Used to generate and divide the places on the transport between flights and intervals.

* Start Date
* End Date
* Place Number - number of seats in the transport (Place number = I1 + I2 + I3 + I4 + One way out)
* Period - sets trip lenght
* Override Period - is used to generate departure dates using the same interval but with a gap of x days between departures
* Simple cost - is used to calculate transport cost per passenger (superadmin setting; when active removes Transport All Price, Guaranteed Seats, Tax and ProRate columns)
* Transport All. Price
* Guaranteed seats - number of seats that will be paid wheter they will be booked or not
* Tax
* ProRate1
* ProRate2
* ProRate3
* ProRate4
* I1 - number of seats for interval 1
* I2 - number of seats for interval 2
* I3 - number of seats for interval 3
* I4 - number of seats for interval 4
* One way out - number of seats for one way out
* One way home - number of seats for one way home

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

To finish click on Insert and then Generate. The end result is:

<figure><img src="../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

or

<figure><img src="../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

This depends on the simple cost being active or not In fix quota you can control the number of seats to be sold, costs, etc. For more information please check \[\[Transport]] and \[\[Transport dashboard]]

In case of a **child transport** creation (that has one or two different transports set as outbound and homebound parent transport) fix quota definition depends on the fixquotas of the parent transports. The start and end date must be included in the corresponding dates from parent transports. Otherwise fix quota will no be generated

<figure><img src="../.gitbook/assets/ChildTransportFixQuota-90a88a655e66bee5d547c3cb9be26636.png" alt=""><figcaption></figcaption></figure>

### Layout <a href="#layout" id="layout"></a>

Used for seating passengers in bookings. Available only if agency transport layout service is activated.
