# Transport Definition

### Overview

When you create a transport, you can enable **Dynamic itineraries**. This lets the system combine **GDS flights** with **your own real transports**. This is done per departure, based on the **Legs** you define.

### Legs

Use **Legs** to define how the itinerary is built.

* A **leg** is one segment in the itinerary. It connects a departure city to an arrival city.

<figure><img src="../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

For each leg, you define **filters**. The filters apply to both **GDS** and **real transports**.

* Click **Search** to preview which options match your filters.

<figure><img src="../../.gitbook/assets/image (605).png" alt=""><figcaption></figcaption></figure>

### Field descriptions and instructions

#### Route information

* **Departure -** Fixed departure airport for this transport (read-only).
* **Arrival -** Fixed arrival airport for this transport (read-only).

#### Time information

* **Departure preferred time -** Optional target departure time.&#x20;
* **Departure earliest time -** Earliest allowed departure time.&#x20;
* **Departure latest time -** Latest allowed departure time.&#x20;

#### Travel limitations

* **Maximum stops number -** Maximum number of stops allowed.
* **Maximum travel time (h) -** Maximum total journey duration in hours, including connections.
* **Maximum connection time (min) -** Maximum allowed layover time between legs, in minutes.

#### Cabin configuration

* **Permitted Cabins -** Cabins that are allowed (for example Economy, Business). Only selected cabins will be returned.
* **Preferred Cabins -** Cabins that should be prioritized when available, but not strictly enforced.

#### Connection points

* **Permitted connection points -** Cities or airports where connections are allowed.\
  Use **Add** to define CITY and/or AIRPORT.
* **Prohibited connection points -** Cities or airports where connections are not allowed.<br>

#### Carrier rules

* **Permitted carriers -** Airlines that are allowed for this transport.
* **Excluded carriers -** Airlines that must never be used.

#### Booking rules

* **Booking Classes**<br>

### Test Search Options

These fields are used **only for testing** and do not affect the saved configuration directly.

* **Search type -** Defines the test search direction, for example One Way.
* **Max result number -**&#x4D;aximum number of results returned by the test search.
* **Pax number -** Number of passengers used in the test search.
* **Date -** Travel date used for the test search.
* **Test Search Button -** Executes a live search using the current Fix Quotas configuration.

{% hint style="info" %}
Always run a test search before saving, especially when using filters like carriers, cabins, or connection limits.
{% endhint %}

* Click **Save** to store your filters.
* Click **Update flight data** to fetch flight data using the saved filters. The selection logic is described in [Flight search](transport-definition.md#flight-search).

{% hint style="info" %}
Use **Search** to validate your filters. Use **Update flight data** when you want the system to refresh the stored flight data.
{% endhint %}

### Flight Search <a href="#flight-search" id="flight-search"></a>

Each night, the system checks for the **best available flight** per departure. This only applies to transports using **Dynamic itineraries**.

The system stores:

* timetables
* flight numbers
* airline information

If a transport can use both **real transport segments** and **GDS segments**, the system uses GDS segments when these rules match:

1. Guaranteed seats must be sold according to the load matrix.
2. The GDS **cost price** is lower.
3. The GDS **sales price** is lower than _Max price from GDS_.

Review the found flights under **Fix quota → View flights**.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Load Factor

You can create **load factor matrices** and link them to a transport. Each transport can use one selected matrix.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### FAQ

<details>

<summary>What is a <strong>leg</strong>?</summary>

A leg is one segment of the itinerary. It’s defined by a departure city and an arrival city.

</details>

<details>

<summary>When should I use <strong>multiple legs</strong>?</summary>

Use multiple legs when the journey has more than one segment. Example: City A → City B → City C.

</details>

<details>

<summary>What’s the difference between <strong>Search</strong> and <strong>Update flight data</strong>?</summary>

* **Search** is for previewing what matches your current filters.
* **Update flight data** refreshes the flight data using your saved filters.

</details>

<details>

<summary>Does <strong>Update flight data</strong> book anything?</summary>

No. It refreshes the stored flight data used by the dynamic itinerary logic. It does not place bookings by itself.

</details>

<details>

<summary>Where do I see the flights the system found?</summary>

Open the transport’s **Fix quota**, then go to **View flights**.

</details>

<details>

<summary>How often does <strong>Flight search</strong> run?</summary>

It runs nightly for transports using **Dynamic itineraries**. Use **Update flight data** if you need a refresh right now.

</details>

<details>

<summary>Why don’t I see any flights in <strong>View flights</strong>?</summary>

Common causes:

* The leg filters are too strict.
* The transport has no generated departures in **Fix quota**.
* No flights are available for the selected dates.
* Flight data has not been refreshed (run **Update flight data**).

</details>

<details>

<summary>What should I do if I get <strong>too many</strong> results in Search?</summary>

Tighten your leg filters. Start with the route, then narrow down step by step.

</details>

<details>

<summary>How does the system choose between <strong>real transports</strong> and <strong>GDS flights</strong>?</summary>

It prefers real transports unless the GDS option meets the configured rules. Those rules include guaranteed seat sales, lower cost, and a max GDS price cap.

</details>

### Related pages

* [Transport creation](transport-creation/)
* [Transport Matrix](transport-matrix.md)
* [Real Transports](../../real-transports/)
