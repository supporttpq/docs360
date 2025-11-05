# Communication

### Overview

The **Communication Service** is a Windows service designed to send information from Tourpaq to various vendors (e.g., airlines, hotels, transport companies). A common use case is transmitting **flight information**, such as periodic passenger name lists (PNL), directly to the airline company.

### Purpose

The purpose of this service is to automate vendor communication, ensuring timely and accurate transfer of passenger and booking data. This reduces manual work, increases reliability, and ensures vendors receive the necessary information to deliver their services.

### Preconditions

* Each **reporting type** requires its corresponding service to be enabled.
* To activate a reporting type, you must contact **Tourpaq Support** to ensure the service is enabled for your company.

### **Transport Reporting**

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Configuration

* Under **Transport Settings**, the **Reporting type** drop-down defines how passenger information will be sent.
* Some reporting types require a **Tour Operator Code**.
* A default reporting method can be set in **Transport → General tab**.
* The method can be overridden per timetable in **Transport → Timetable tab**.
* Reporting is managed by the **Communication Service**, which checks schedulers every **9 minutes**.
* Schedulers are configured in **Transport → Communication tab**.

***

#### Passenger Name List (Air)

The **Passenger Name List (PNL)** reporting type generates a **PDF file** that is sent via email to the airline.\
The columns included are:

* **Resort** – Passenger’s resort.
* **Hotel** – Passenger’s hotel.
* **First Name / Last Name**
* **Gender** – Passenger gender.
* **Age** – Shown for children.
* **Phone** – Customer phone number (usually the first passenger in booking).
* **Voucher** – Booking number.
* **Catering** – `"MF"` if the passenger has catering; otherwise blank.
* **Seat Out** – Assigned outbound seat (e.g., A03).
* **Seat Home** – Assigned inbound seat.

***

#### Pick-up List (Bus)

* Please refer to the **Routes** section for details.

***

#### Train Reporting

* Similar to other transport types; configured in Transport Settings.

***

#### Paxport Reporting

The **Paxport** reporting type generates an **ASCII text file**, grouped by header, and sent via email.

**Fields included:**

* Tour Operator (from **Transport → General tab**)
* Outbound Departure Date / Flight Number
* Inbound Departure Date / Flight Number
* IATA codes for departure and arrival airports
* Passenger details: First Name, Last Name, Gender, Age, Booking No., Remarks
* Outbound Seat Number / Inbound Seat Number

***

#### Radixx / DAT / Air Berlin

* Specific file formats used for these vendors.

***

#### Inflight Service Reporting

Files include detailed passenger and customer data, such as:

* Booking Date / Booking No. / Booking Version
* Passenger Name, Gender, Language Code
* Customer Name, Address, Postcode, Country, Contact Info
* Flight details (Outbound & Inbound)
* Operator and Comments

***

#### World Ticketing

* Used for sending PNL to **Norwegian Airlines**.

***

#### AirSeven

* Sends passenger names, gender, booking number, and seat number.
* The list is divided across several emails.

***

### Hotel Reporting

* The system sends passenger lists to hotels based on configured intervals.

***

### Extras Reporting

* Sends lists of passengers who purchased extras from specific categories.
* Example: Daily reporting, 4 days before passengers return from their trip.

***

### Supplier Reporting

* Handles reporting to suppliers depending on configured rules.

***

### Release Reporting

* Used to manage and communicate release-related data (details vary by vendor setup).
