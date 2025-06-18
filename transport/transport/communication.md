# Communication

Communication is a windows service that has the purpose to sent information to various vendors. For example the flight information, where a list of passenger is periodically sent to the airline company.

IMPORTANT: For each reporting type, there is a service that needs to be enabled. You have to contact Tourpaq Support to make sure that the specific service is enabled for the company.

**Transport Reporting**

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Under Transport Settings the reporting type drop down list will decide how the reporting will be send. Tour operator cod is required for some reporting types.

Transport Reporting is a way to communicate the passenger name list PNL to the airline company. There are more methods to sent the PNL. The reporting method type can be sent in Transport in Transport/General tab as a default or it can be overwrite in the Transport/Timetable tab. The reporting is managed by a Windows Service that is searching for schedulers every 9 minute. The schedulers are set up in the Transport/Communication tab

**Passenger Name List (Air)**

Passenger Name list is a reporting type that sends a PDF file by email. The column are as follow:

* Resort - The name of the resort where the passengers are staying.
* Hotel - The name of the hotel where the passengers are staying.
* First Name -
* Last Name -
* Gender - Gender of the passenger
* Age - Age of the passenger if he is children
* Phone - Customer phone number usually is the first passenger in the booking
* Voucher - Booking No.
* Catering - the value of the catering is ''MF'' if the passenger has catering otherwise is black
* Seat Out - Number of the seat something like A03 for the outbound flight
* Seat Home - Number of the seat for the inbound flight

**Pick up list (Bus)**

Please check [Routes](https://docs.tourpaq.com/docs/documentation/routes/)

**Train**

**Paxport**

Paxoprt is a file format for the Paxport PNL system. The file is a ASCII text file format and is sent by email. The file are grouped by a header.

* Tour Operator - The tour operator is set up in the \[\[Transport#General\_tab|General Tab]]
* Outbound Departure Date
* Outbound Flight Number
* Inbound Departure Date
* Inbound Flight Number
* Inbound Airport Departure \[\[IATA]] code
* Inbound Airport Arrival \[\[IATA]] code
* Outbound Airport Arrival \[\[IATA]] code
* First Name
* Last Name
* Gender
* Booking No.
* Passenger Remarks - This can be set in the \[\[Booking Page]]
* Age - The age of the passenger
* Outbound Seat Number -
* Inbound Seat Number -

**Radixx**

**DAT**

**Air Berlin**

**Inflight Service**

Files from This Communication Contain the following Columns:

* Booking Date
* Booking No
* Booking Version
* Passenger Language Code (taken from customer country)
* Passenger First Name
* Passenger Last Name
* Customer Gender
* Passenger ID
* Customer First Name
* Customer Last Name
* Customer Address
* Customer Postcode
* Customer Postal Address
* Customer Country Code
* Customer Phone
* Customer Mobile Phone
* Flight No Out
* Departure Code Out
* Arrival Code Out
* Flight No Home
* Departure Code Home
* Arrival Code Home
* Operator
* Customer Email
* Comments

**World Ticketing**

This reporting type is used to communicate the \[\[PNL]] to Norwegian Airline

**AirSeven**

This reporting type sends pax names, gender, booking number and seat number. The list is divided into a few emails.

**Hotel Reporting**

The sistem sends lists based on the interval used.

**Extras Reporting**

**Extras Company Reporting**

//Main article:// \[\[Extras Company Reporting]]

A list of passengers that purchased extras from a specific extras category are sent for ex. every day 4 days before arriving home from the trip.

**Supplier Reporting**

**Release Reporting**
