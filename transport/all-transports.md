# All Transports

<figure><img src="../.gitbook/assets/image (18) (2).png" alt=""><figcaption></figcaption></figure>

### Overview

The **All Transports** page provides a comprehensive overview of scheduled transport operations. Users can filter, review, and analyze transport records, including departures, arrivals, seat usage, and costs.

### Filters & Controls

* **Transport -** Filter transports by transport code.
* **Transport Date (Start - End) -** Select a specific date range to narrow down the results.
* **Departure / Arrival -** Filter by departure and arrival points.
* **Flight No -** Search by flight or transport number.
* **Weekdays -** Limit results to specific days of the week.
* **Drop Arrival Country -** Filter based on arrival country.
* **Transport Type -** Choose the type of service (Charter, Dynamic, Sys-real, System Transports, or All Transport Types).
  * Charter Transports - are transports using Fix Quotas to define all flights
  * Dynamic Transports - uses Dynamic Itineraries for their legs. The legs may use Real Transport or use external providers (GDS)
  * Sys-real Transports - are generated from a Transport Rule, and both legs use Real Transports
  * System Transports - are generated from a Transport Rule, and at least one of the legs uses an external provider (GDS)&#x20;
* **Transport Mode -** Additional filtering for transportation category (Boat, Bus, Car, Fly Train).
* **Direction -** Options: Travel Home, Travel Out, or Both Ways.
* **More Filters -** Access advanced filter options for precise data control.
* **Clear -** Reset all active filters.
*   **Use Real Transports -** Shows only the real transports&#x20;

    <figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
* **Save View -** Save the current filter setup as a reusable custom view.

### Table Columns

| Column        | Description                                                                     |
| ------------- | ------------------------------------------------------------------------------- |
| **Date**      | The scheduled date of the transport.                                            |
| **Transport** | The transport code.                                                             |
| **Dep. Time** | Departure time                                                                  |
| **Arr. Time** | Arrival time                                                                    |
| **Seats**     | Total number of available seats for the transport.                              |
| **GES**       | Typically refers to a group or seat class metric (e.g., guarantee empty seats). |
| **AOT**       | Allotment seats total                                                           |
| **BOT**       | Booked seats total – total passengers with reservations.                        |
| **Cost**      | Cost of the transport, shown in the local currency (e.g., DKK - kr.).           |

* Click on column headers to **sort** (e.g., by Date, Cost).
*   Click on the right three dots to add other columns to the table&#x20;

    <figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
*   Use **checkboxes** on the left to select multiple transports for export.&#x20;

    <figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
