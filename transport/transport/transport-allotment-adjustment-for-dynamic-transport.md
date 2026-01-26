# Transport Allotment adjustment for Dynamic Transport

### Overview

This feature manages dynamic transport scenarios where flights arrive very early or depart very late. In such cases, it ensures that an additional hotel night is automatically added—either at the beginning or end of the stay—so that guests have accommodation available upon arrival or before departure.

<mark style="color:red;">NOTE: This feature applies only to the GDS transports.</mark>

### Behavior

The logic handling dynamic transport respects the defined time thresholds and automatically adds an extra day at the beginning or end of the hotel stay, depending on the flight’s arrival or departure time. This ensures guests have proper accommodation coverage for very early arrivals or late departures.

### How It Works

* Configure in Setup -> System Setup ->Transport Providers the Early arrival limit and Late departure limit

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;       \- Early arrival limit - if the arrival time for departure is before the limit, then the guest needs the hotel on the day before the arrival date, adding one extra day (+DAYS) to stay. This applies only to the new bookings

&#x20;      \- Late departure limit - if the departure time for the return home is after the limit, then the guest needs the hotel room one day extra (LAND DAYS), adding one extra day to the stay. This applies only to the new bookings

* Create a booking with a GDS transport

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

In this case there both situation met;

1. The arrival hour is 19:20 and the setup for Early arrival limit is set to 20:00 ⇒ one extra day before the arrival date;

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

2. The departure hour is 10:40 and the setup for Late departure limit is set to 10:00 ⇒ adding one extra day to the stay;

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The results of  this will be that on the hotel will be added 2 extra nights (one for early arrival and one for late departure). The transport has the date departure interval between 01.09 - 08.09, and the guests will stay at the hotel between 31.08 - 09.09.  Also, the total cost in the pricelist will be influenced by the two settings. The cost of one night's accommodation is added to the hotel for each setting.
