# Transport Definition

### Overview

When creating a transport, users have the option to enable **dynamic itineraries**. This configuration allows the system to combine **GDS flights** and **own real transports** for defined departures. To support this setup, the transport includes a **Legs** definition feature.

### Legs

* A **leg** represents a pair of cities that together form part of the transport itinerary.

<figure><img src="../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* For each leg, the user can define **filters** to be applied when searching both GDS and own real transports.
* After setting the filters, the user can press the **Search** button to preview available options.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (3).png" alt=""><figcaption></figcaption></figure>

* Once the configuration is finalized, filters can be saved.
* By pressing the **Update flight data** button, the system will automatically search for available flights based on the defined filters. (Details of this search are described in the _Flight Search_ section.)

### Flight Search <a href="#flight-search" id="flight-search"></a>

* Each night, the system automatically checks for the **best available flight** for every departure associated with transports that use dynamic itineraries.
* The system stores **timetables, flight numbers, and airline information**.
* If a transport uses both **own real transports** and **GDS flights**, the system applies the following rules to determine when GDS segments are booked instead of own segments:
  1. Guarantee seats are sold according to the load matrix.
  2. The cost price is lower on GDS.
  3. The GDS price is lower than the configured _Max price from GDS_.
* Flights found can be reviewed under **Fix Quota → View Flights**.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Load Factor

* **Load factor matrices** can be created and linked to a transport.
* For each transport, users can select which load factor matrix they want to apply.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
