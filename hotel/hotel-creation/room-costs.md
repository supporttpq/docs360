# Room costs

### Overview

Room costs let you define the **cost price** your agency pays for hotel rooms. You can set costs for specific date ranges. Costs can be calculated **per room** or **per passenger**.

### Purpose

* Set cost prices for rooms over defined time periods.
* Support two calculation methods: **per room** and **per passenger**.
* Add optional extra costs on top of the base room cost.
* Allocate costs consistently across passengers and bookings.

### Cost Price Types

1. **Per room**
   * A fixed cost for the room.
   * The system splits it across the room occupants.
2. **Per passenger**
   * A cost applied to each passenger.
   * The system multiplies it by the stay length.

### Extra Prices

You can add **extra prices** on top of the base room cost. These extras can depend on passenger age and date filters.

* **Per Passenger per Night** – Extra cost added to each passenger’s price per night of the stay.
* **Per Room** – Extra cost applied per room, distributed equally among all passengers in the room.

### Worked example

Room A has 2 ordinary beds and 2 extra beds. Room B has 3 ordinary beds.

| Start period | End period | Room type | Price | Per passenger |
| ------------ | ---------- | --------- | ----- | ------------- |
| 01/01/2011   | 31/01/2011 | _Room A_  | 200   | True          |
| 01/01/2011   | 31/01/2011 | _Room B_  | 500   | False         |

Assume a booking in January 2011 with a 7-night stay. The booking has 7 passengers:

* Room A: 4 passengers (Passenger1–Passenger4)
* Room B: 3 passengers (Passenger5–Passenger7)

#### Base room cost per passenger

* Room A is **per passenger**:
  * Cost per passenger = `200 × 7 = 1400`
* Room B is **per room**:
  * Total room cost = `500 × 7 = 3500`
  * Cost per passenger = `3500 ÷ 3 ≈ 1166.67` (rounded by currency rules)

#### Extra prices

Assume this extra price setup:

| Start age | End age | Extra price/night/passenger | Extra price/room |
| --------- | ------- | --------------------------- | ---------------- |
| 0         | 50      | 100                         | 12               |

If Passenger1 is 0–50 years old:

* Extra price per night per passenger = `100 × 7 = 700`
* Extra price per room per passenger:
  * Extra room price total = `12 × 1 room = 12`
  * Extra per passenger = `12 ÷ 4 = 3`

#### Total cost for Passenger1

Passenger1 stays in Room A:

* Total cost = `1400 + 700 + 3 = 2103`

#### Summary formula

* Total cost price = cost price + extra price per night per passenger + extra price per room for one passenger

### Related pages

* [Room cost](room-cost/)

### FAQ

#### What’s the difference between **per room** and **per passenger**?

**Per room** applies once per room and is split across occupants. **Per passenger** applies to each passenger individually.

#### Why do passengers in the same room sometimes get different costs?

Age filters can apply different extra prices per passenger. Board type rules can also impact cost in some setups.

#### How does the system split a per-room cost?

It splits the room cost evenly across room occupants. The split is recalculated if room occupancy changes.

#### Why does my number look “rounded”?

Splits can create decimals. Rounding depends on your currency settings and where totals are displayed.

#### I changed a room cost setup, but the booking didn’t update. Why?

Some totals update only after cost/profit recalculation runs. Re-open the booking and check the cost breakdown after recalculation.
