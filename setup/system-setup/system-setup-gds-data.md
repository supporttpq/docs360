# System Setup – GDS Data

### **Overview**

The **GDS Data** section configures Tourpaq to integrate with Global Distribution Systems (GDS) for transport and ticketing. This allows Tourpaq to create reservations, manage ticketing, and retrieve PNR (Passenger Name Record) information from external providers.

### **Purpose**

* Enable automated booking and ticketing through GDS providers.
* Centralize transport provider credentials and settings.
* Ensure accurate and timely retrieval of booking and ticket data.

### **Configuration Fields**

| **Field**                                   | **Description**                                                         |
| ------------------------------------------- | ----------------------------------------------------------------------- |
| **Currency**                                | Sets the currency for GDS transactions.                                 |
| **User / Password**                         | Credentials provided by the GDS provider for authentication.            |
| **Branch**                                  | Branch code used for ticketing and reporting.                           |
| **Days Number for Ticketing**               | Number of days allowed for ticketing after reservation creation.        |
| **Max GDS Search Results**                  | Maximum number of results returned by GDS queries.                      |
| **Queue Number**                            | Queue to which GDS bookings are assigned for ticketing.                 |
| **Pseudo City Code / Own Pseudo City Code** | Codes used to identify the booking office.                              |
| **Price Change Margin**                     | Margin allowed for price modifications in GDS bookings.                 |
| **Fares Indicator**                         | Indicator used for fare calculations.                                   |
| **Payment Rule**                            | Payment rules applied to GDS reservations.                              |
| **Card Details**                            | Owner, type, number, expiration (year/month), and CVC for payments.     |
| **Confirmation Email**                      | Email address for receiving booking confirmations from Travelport.      |
| **Days Number for Check PNR**               | Number of days before departure to check the PNR status.                |
| **Show Ticket Number on Ticket**            | Option to display ticket numbers on printed tickets.                    |
| **Time Frame Before Departure**             | Minutes before departure to remove flights from bookings automatically. |

### **Transport Selection Rules**

| **Setting**                                    | **Description**                                            |
| ---------------------------------------------- | ---------------------------------------------------------- |
| **Use Division PNR by Classes**                | Divide bookings by classes to optimize pricing.            |
| **Don’t Update DTS on Create GDS Reservation** | Prevents changes to DTS when a GDS reservation is created. |

***

### **Usage Notes**

* All fields are mandatory for proper GDS integration.
* Incorrect credentials or configuration may prevent bookings or ticket generation.
* Administrators should verify all settings before enabling GDS operations.
