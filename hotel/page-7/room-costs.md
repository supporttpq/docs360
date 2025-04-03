# Room costs

It must be possible to insert cost prices per room for different periods of time. There will be 2 types of cost prices:

* Per room
* Per passenger

Example:

Let’s consider //Room A//, a room with 2 ordinary beds and 2 extra beds, and //Room B// a room with 3 ordinary beds.

| Start period | End period | Room type  | Price | Per passenger |
| ------------ | ---------- | ---------- | ----- | ------------- |
| 01/01/2011   | 31/01/2011 | //Room A// | 200   | True          |
| 01/01/2011   | 31/01/2011 | //Room B// | 500   | False         |

For a certain booking, we are interested in the cost price for each passenger. Taking the example given above, let’s suppose we have a booking for which the transport arrives at the destination in January 2011. The booking has 7 passengers with 4 passengers (//Passenger1// and //Passenger2//, //Passenger3//, //Passenger4//) in //Room A// and 3 passengers (//Passenger5//, //Passenger6//, //Passenger7//) in //Room B//. Let’s also suppose that the trip’s length is 7 days (for the next 2 sections, we will consider this example as a default one)

The cost price will be calculated for each day of the period, like this:

* for each of the 4 passengers from //Room A: cost price = cost price \* trip length// = 200 x 7 = 1400
* for each of the 3 passengers from //Room B : cost price=(cost price \* trip length)/passengers number// = (500 x 7) / 3 = 1167 (//Per passenger// is set to false; as we are interested in the cost price for one passenger, we divide the cost price by the number of passengers from the room)

From this section there will also be established the extra prices. There will be 2 types of extra prices:

* Per passenger per night
* Per room

Let’s suppose we have these values inserted:

| Start age | End age | Extra price/night/passenger | Extra price/room |
| --------- | ------- | --------------------------- | ---------------- |
| 0         | 50      | 100                         | 12               |

If Passenger1’s age is between 0 and 50 years

* Extra price per night per passenger = extra price x trip length = 100 x 7 = 700. There is one //Room A// booked for this trip. The value for the second extra price would be calculated like this:
* Extra price per room for one passenger = (extra room price x booked rooms number) / passengers number from the booked room

For //Passenger1// that stays in //Room A//, the value would be

* Extra price per room for one passenger = (12 x 1)/4 = 3

The total cost price for //Passenger1// (and also for the others passengers from //Room A//) is obtained by adding all these 3 prices:

* Total cost for Passenger1 = 1400 + 700 + 7 = 2107

The conclusion would be that for each passenger the cost price is calculated like this:

* Total cost price = cost price + extra price per night per passenger + extra price per room for one passenger
