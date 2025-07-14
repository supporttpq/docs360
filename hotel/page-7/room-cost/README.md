# Room cost

**Room Cost** rules can apply to a specific hotel. The rule can be configured to apply for a booking within a specific departure date period, a specific booking date period, and by a room type or all room types assigned to the selected hotel. The amount of the **room cost** rule can be calculated per passenger or per room. If the rule is configured per room, the amount will be divided among the passengers staying in that room.

To test the rule, create a booking with the selected hotel and room type. Under the profit tab, you can view real-time calculations of the Cost and profit. Some cost figures will take effect when the **Total Cost Service** recalculates the cost. In the profit tab, the hotel cost is shown as a single figure. Next to it is an information icon, leading to a more detailed view of how the hotel cost

### Hotel extra cost rules <a href="#hotel-extra-cost-rules" id="hotel-extra-cost-rules"></a>

These are costs paid by the agency towards the hotels.

<figure><img src="../../../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

There are 2 rules, and both are applied:

* Extra price/pax/night calculated like this (value \* days)
* Extra price/room calculated like this (value \* passengers per room)

Filters used in applying these costs:

* Age - set the start and end age to which the cost applies
* Stay/Arrival Start and End that limit the cost
* Booking Start and End date where the cost applies
* Room where the cost applies

### Room cost rules​ <a href="#room-cost-rules" id="room-cost-rules"></a>

Represents the basic value paid by the agency to the hotel for the used rooms.

<figure><img src="../../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

**PER PAX**

There are two rules that apply, and each one overrides the other. They are represented by the **PER PAX** check box:

* Per room - the inserted value in the PRICE case is paid for each room (if the box is unchecked)
* Per passenger, the inserted value in the PRICE case is paid for each passenger (if the box is checked)

> 📝 **Note:** Price inserted is per day with the option to be paid by either each passenger or be divided between all passengers that stay in that room

**Extra Cost Included**

The inserted value in the EXTRA COST INCLUDED case is subtracted from the PRICE case ONLY IF AN EARLY BOOKING OR A S\&P RULE COST IS APPLIED!!!

Filters used:

* Stay start and end date
* Booking start and end date
* Room

### Changing the cost if a number of rooms has been sold​ <a href="#changing-the-cost-if-a-number-of-rooms-has-been-sold" id="changing-the-cost-if-a-number-of-rooms-has-been-sold"></a>

It is possible to change the cost of the rooms with the usage of the **Up to rooms** and **Price2** columns. The feature is set to work in the way that if a number of rooms has been set in the **Up to rooms** column and that number of rooms has been booked, the new cost will be taken from **the Price2** column.

### Early booking cost-discount rules​ <a href="#early-booking-cost-discount-rules" id="early-booking-cost-discount-rules"></a>

These are discounts given to agencies by the hotels if certain conditions are met.

<figure><img src="../../../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

There are two rules that apply. They cannot be applied at the same time and are governed by the **IS PERCENT** check box:

* Percent - the value inserted in the PRICE case is used as a percent of the total value if the check box is used
* Price - the value inserted in the PRICE case is used as it is if the check box is not used. Also, this rule has two additional exceptions because of the **PER ROOM** check box:
  * Per passenger - if the check box is not used
  * Per room - if the check box is used
* Customer Early booking discount - the value inserted in this case is used in the calculation of the pricelist price. If this value is completed, the normal price will be taken into account when calculating the profit of the room on the booking, and the value for the price list will be taken into account when calculating the price Pricelist prices.

<figure><img src="../../../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure>

This rule can be combined with the **Stay and Pay cost rules** if the **S\&P** check box is used. Filters used:

* Arrival Date Start and End
* Booking Start and End date
* Room
* Days no before arrival The rest of the filters are used in **invoices** and will be explained there.

Stay and Pay cost rules

These are considered to be more discounts given by the hotel to the agency.&#x20;

<figure><img src="../../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

They are governed by two cases:

* Stay days no.
* Pay days no. The company uses the room for several days and can pay for a lesser amount of days. The number inserted in the **Pay days no.** cannot be greater than **the Stay days no.**, and both must be greater than 0.

Filters used:

* Arrival Start and End date
* Booking Start and End date
* Room
* Period

### Special offer cost​ <a href="#special-offer-cost" id="special-offer-cost"></a>

Special offers are rules setup by hotel owners capable of overriding any other cost rules setup in the hotels.

<figure><img src="../../../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>

There are 4 rules:

* Room cost
* Extra bed cost
* Early booking
* Stay and pay

Filters used to set up the rules:

* Arrival start date
* Arrival end date
* Booking start date
* Booking end date
* Days before arrival
* Room
* Price for each interval
* Per day check box (if checked, the price will be applies per day, not per interval)
* Add to default rule (for Early booking only) - if "on", the Special Offer Early Booking rule will not overwrite the contract Early Booking rule, but add to it. It will add in the following manner:
  * contract Early Booking rule will apply first
  * and the Special Offer Early Booking rule will be applied on that result
  * **Please note**! - if the cost of a particular day would be 0 (for various reasons, may be the last 2 days of a Stay 7 pay 5 days rule), then the adding of a discount (Early booking or other) will not result in a negative amount cost but still zero.
* Normal price check box (if checked, it behaves as a price, not as a discount)
* Per pax check box (if checked it applies to each passenger)
* Percent check box (if checked it turns the value into a percent)
* Period
* From age
* To age
* Stay (duration of the stay)
* Pay (duration of the pay, works with the **Stay** filter)
* Combine with **Early booking** - dictates if an EB rule will combine with an S\&P rule. If not, the EB rule wins, and S\&P is not taken into account.
* Combine with **Stay and pay** - dictates if an S\&P rule will combine with an EB rule. If not, the S\&P rule wins, and EB is not taken into account.

### Partial mind map of Hotel Cost rule interactions <a href="#partial-mindmap-of-hotel-cost-rule-interractions" id="partial-mindmap-of-hotel-cost-rule-interractions"></a>

This is a mind map trying to cover the various interactions between hotel

<figure><img src="../../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>
