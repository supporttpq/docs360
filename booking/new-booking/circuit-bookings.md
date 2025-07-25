# Circuit Bookings

#### **Overview**

Circuit bookings enable the creation of **customized multi-component trips** within a single booking. Unlike standard bookings that typically link one hotel and one transport, circuit bookings allow the user to combine:

* Multiple hotels, potentially located in different resorts or even countries.
* Multiple transports, often using one-way flights to accommodate complex itineraries.

***

#### **Purpose**

* To provide greater flexibility in travel planning.
* To accommodate multi-destination trips under one booking record.
* To allow users to tailor customer journeys with varied hotels and transport legs.

***

#### **Preconditions**

* One-way transports must be enabled in the system.
* Custom hotel days must be enabled for hotels.
* Related price lists supporting custom hotel days and multiple one-way flights must be configured.
* Users should refer to:
  * **Custom Hotel Days Bookings** documentation for details on handling hotel durations.
  * **Multiple One-Way Flights Bookings** documentation for transport setup.

***

#### **Key Benefits**

* Combine multiple hotels within a single booking.
* Manage hotels across different resorts or countries seamlessly.
* Use multiple one-way flights to match complex travel itineraries.

An example of a custom hotel days booking

![!](https://docs.tourpaq.com/assets/images/circuit-8d9b468c853f2ffb0e4a767d96942035.png)

* Departure - 21.05.2020 / 09:15 from Billund
* Arrival - 21.05.2020 / 11:15 in Palma - Mallorca
* Stay days - 7 at Hotel Palma Hotel Only (21 - 28 may)
* Departure - 28.05.2020 / 07:15 from Palma - Mallorca
* Arrival - 28.05.2020 / 10:45 in Porto Santo
* Stay days - 7 at Hotel Porto Hotel Only (28 may - 4 june)
* Departure - 04.06.2020 / 09:30 from Porto Santo
* Arrival - 04.06.2020 / 11:00 in Billund

In this example we have 2 different hotels from 2 different countries (Hotel Palma Hotel Only in Palma - Mallorca, and Hotel Porto Hotel Only in Porto Santo). The connection is made by 3 transports (Billund-Palma-Mallorca, Palma-Mallorca-Porto Santo, and Porto Santo-Billund). All of them need to be defined in Tourpaq.

Ticket will look like this

<figure><img src="../../.gitbook/assets/image (249).png" alt=""><figcaption></figcaption></figure>
