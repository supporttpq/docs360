# Transport Dashboard

### Overview

The **Transport Dashboard** provides an at-a-glance view of key selling metrics for each transport, including:

* Number of sold seats per transport allotment
* Percentage of sold seats
* Seats sold in the last week
* Cost price per seat

All values are calculated for each transport, taking into account historical and current sales, guaranteed seats, and transport allotments.

The process to calculate the cost price per seat is elaborate and it will be described further down:

1. The first step is to divide the transport allotments into groups as follows: Considering a selling period and all the transport allotments generated based on it, is taken the first transport allotment for which Total available places for outbound (AOUT) is greater than 0. All the following transport allotments are taken until a transport allotment with AOUT = 0 is found. All these records, including the last one (for which AOUT is 0), are considered a group(named transport allotments group). Thus, a selling period can have several transport allotment groups. The following steps will be made for each group of transport allotments.
2. For each transport allotment from the group, pro seats number is calculated using the next formula:

* Pro seats number = BO1 + BO2 + BO3 + BO4 – Guaranteed seats number

3. For each transport allotment from the group, an intermediary price is calculated for all the interval periods using these formulas:

* Temporary cost price for booked seats for period1 = Transport allotment price + (Pro rate 1 x Pro seats number)
* Temporary cost price for booked seats for period2 = Transport allotment price + (Pro rate 2 x Pro seats number)
* Temporary cost price for booked seats for period3 = Transport allotment price + (Pro rate 3 x Pro seats number)
* Temporary cost price for booked seats for period4 = Transport allotment price + (Pro rate 4 x Pro seats number). There is an important aspect that must be taken into account before making the calculation. If Pro seats number is negative(which means that there have not been bought seats beside the guaranteed ones) the value Pro seats number is considered to be 0. In this case, the total cost price will be, in fact, the price paid for the guaranteed seats.

4. The last transport allotment from the group is selected (the one for which AOUT = 0) and Temporary cost price for booked seats value is calculated for each interval period. Then another intermediary value is calculated using these formulas:

* Cost price for empty leg for period 1= Temporary cost price for booked seats for period1 / (the number of transports allotments from the group – 1)
* Cost price for empty leg for period 2= Temporary cost price for booked seats for period2 /( the number of transports allotments from the group – 1)
* Cost price for empty leg for period 3= Temporary cost price for booked seats for period3/ (the number of transports allotments from the group – 1)
* Cost price for empty leg for period 4= Temporary cost price for booked seats for period4 / (the number of transports allotments from the group – 1)

5. For each interval period, another intermediary value is calculated using this formula:

* Second temporary cost price for booked seats for period 1 = Temporary cost price for booked seats for period 1 + Cost price for empty leg for period 1
* Second temporary cost price for booked seats for period 2 = Temporary cost price for booked seats for period 2 + Cost price for empty leg for period 2
* Second temporary cost price for booked seats for period 3 = Temporary cost price for booked seats for period 3 + Cost price for empty leg for period 3
* Second temporary cost price for booked seats for period 4 = Temporary cost price for booked seats for period 4 + Cost price for empty leg for period 4

6. Another intermediary value is calculated: Passengers number = AO1 + AO2 + AO3 + AO4 – if departure date is in the future Passengers number = BO1 + BO2 + BO3 + BO4 – if departure date is in the past
7. The final value is calculated like this:

* If Passengers number > 0 \_ Final cost price per seat for period 1 = Second temporary cost price for booked seat for period 1 / Passengers number +Tax \_ Final cost price per seat for period 1 = Second temporary cost price for booked seat for period 1 / Passengers number + Tax \_ Final cost price per seat for period 1 = Second temporary cost price for booked seat for period 1 / Passengers number + Tax \_ Final cost price per seat for period 1 = Second temporary cost price for booked seat for period 1 / Passengers number + Tax
* If Passengers number = 0 \_ Final cost price per seat for period 1 = Second temporary cost price for booked seat for period 1 + Tax \_ Final cost price per seat for period 1 = Second temporary cost price for booked seat for period 1 / Passengers number + Tax \_ Final cost price per seat for period 1 = Second temporary cost price for booked seat for period 1 / Passengers number + Tax \_ Final cost price per seat for period 1 = Second temporary cost price for booked seat for period 1 / Passengers number + Tax

For more details regarding the significance of Guarantee seats number, Transport allotment price, Tax, Pro rate 1, AOUT, BOUT, BO1, please refer to section **ALLOTMENTS**.

**Basically, the cost of a seat is calculated like this:**

**\* For future transports**

**Current flight cost + (last flight cost/remaining number of flights)/guaranteed seats.**

**\* For past transports**

**Transport cost + (transport cost/number of flights)/seats occupied.**

> The entire explanation from above is rendered useless if the Company has Simple Cost activated.

Simple cost is a new way of calculating transport cost per passenger.

Simple cost is set for each flight and represents the cost incurred per passenger. It is calculated as a round trip or one way.

<figure><img src=".gitbook/assets/image (106).png" alt=""><figcaption></figcaption></figure>
