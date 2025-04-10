# Dynamic transport baggage

The dynamic transport baggage allows the system to reserve also the baggage for a flight ( on ACH - Low Cost Carriers) and to display in the office if the flight contains already a baggage ( on 1G).

**How to activate the dynamic baggage?​**

You can activate this new feature only for the dynamic transports. Go in "Legs" tab and check the box "Dynamic Baggage" from "General dynamic information" section. After that you have to update the flights for this transport, so the service could find and include the baggage also in the flight and in the price.

<figure><img src="../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>

**How it works?​**

After the dynamic baggage is activated, the service will find the baggage price and quantity for earch airline, save it in memory and add it in the price of the flight. The price and the quantity will be displayed in the "Test search" from "Configure" -> "Leg" section and in the "View Flights" from "Fix Quota"

**"Test Search"**

<figure><img src="../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

**"View Flights"**

When a booking is made, on take allotment the baggage price will be checked again. On the GDS tab, when the booking is created the baggage will be booked as a optional service and after it will be displayed in the "Successfully submited bookings" section.

On "Load PNR" the optional services will be loaded again.
