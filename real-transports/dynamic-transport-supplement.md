# Dynamic transport supplement

The dynamic transport supplement allows the service to find the cheapest flight for a departure, even if the price is bigger then the maximum price set for that transport departure, converting the difference in a supplement added on passenger.

**How to activate the dynamic supplement?​**

You can activate this new feature only for the dynamic transports. Go in "Legs" tab and check the box "Dynamic Supplement" from "General dynamic information" section. After that you have to update the flights for this transport, so the service could find the cheapest flights ignoring the "Max return price per person from GDS".

**How it works?​**

After the option is selected, the service will find the cheapest flights for that transport, ignoring the max. price, and save those in database. When the user set this flight for a booking, click take allotment and save passengers, the system will add a dynamic supplement with code "DTS" from a category "DT", that represents the difference between the flight price and the maximum price set on departure/transport, on each passenger.

The supplement "DTS" must be specificate and permanent. The supplement "DTS" and the category "DT" are added manually for each company, and can't be deleted.

DTS for Charter: -when we are using DTS for charter transport always Transport Cost will be 0, and DTS Cost = Transport Price.

DTS for Gds Transport: -when we are using Gds Transport, DTS is calculated raported to "Max return price per person from GDS:"

Example: Max return price per person from GDS = 100 Gds real flight price is 1720 DKK. Transport Cost = 100 DKK (maximum value between Max return price per person from GDS and Gds real flight price) Dts Price => 1720 - 100 = 1620 DKK Dts Cost stored in AlternativeCost => 1720 - 100 = 1620 DKK TransportGDSCost from Passenger table = 100 DKK
