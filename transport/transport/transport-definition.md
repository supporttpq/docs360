# Transport Definition

### General <a href="#general" id="general"></a>

When creating a transport user can choose if he wants to use dynamic itineraries. Setting this transport can be configured to use GDS flights and own real transport for departures it has defined. To do this, legs definitions is enabled on transport.

### Legs <a href="#legs" id="legs"></a>

We can define a list of city pairs that will make up the itinerary of this transport.

<figure><img src="../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

For each leg we can define the filters used to search GDS and own real transports. User can press search button to preview search results. When setting is done he can save the filters.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Once filters are set on leg user can press „Update flight data” button to have the system search for available flights. How search is made is described on “flight search” section.

### Flight Search <a href="#flight-search" id="flight-search"></a>

Every night the system is checking for the best flight available for each departure on all transport that is using dynamic itineraries. The system will store timetables, flight numbers and airlines. When a transport is using OWN real transports and GDS flights, the following list of rules that decides when GDS segments are booked instead of OWN segments is used:

1. Selling of guarantee seats in according to load matrix (see below)
2. Cost price is lower on GDS
3. GDS price is lower that “Max price from GDS

The flight found can be views under fix quota/view fligths:

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Load factor <a href="#load-factor" id="load-factor"></a>

Load factor matrixes can be created and on a transport we can choose the one we want to use.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
