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

#### Changing the cost if a number of rooms has been sold​ <a href="#changing-the-cost-if-a-number-of-rooms-has-been-sold" id="changing-the-cost-if-a-number-of-rooms-has-been-sold"></a>

It is possible to change the cost of the rooms with the usage of the **Up to rooms** and **Price2** columns. The feature is set to work in the way that if a number of rooms has been set in the **Up to rooms** column and that number of rooms has been booked, the new cost will be taken from **the Price2** column.

### Early booking cost-discount rules​ <a href="#early-booking-cost-discount-rules" id="early-booking-cost-discount-rules"></a>

#### **Overview**

The **Early Booking Cost Discount Rules** section within the **Room Costs** tab allows you to configure and manage early booking discounts for hotels. These rules apply when bookings are made a set number of days in advance, offering discounted rates to incentivize early reservations.

***

#### **Purpose**

To define and automate early booking discount conditions based on:

* Stay booking dates
* Room type
* Board type
* Pricing and deposit conditions

These configurations ensure proper cost calculation and promotional accuracy for early-bird bookings.

***

<figure><img src="../../../.gitbook/assets/image (315).png" alt=""><figcaption></figcaption></figure>

#### **Instructions**

#### **Filters Section**

* **Contract**: Dropdown to select the contract for which you want to define early booking rules.
* **Show all**: Checkbox to display all existing rules.
* **+ More Filters**: Allows advanced filtering options (not fully visible in the screenshot).
* **Clear**: Resets all filters and fields.
* Room Code:  Select a specific room code to define EBD
* Period: Select the interval
* Booking date
* Departure date

***

#### **Grid Fields**

| **Field**               | **Description**                                                                                                                                                            |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Stay **Start / End**    | Defines the stay date range for which the early booking discount is valid.                                                                                                 |
| **Booking Start / End** | Specifies when the booking must be made for the discount to apply.                                                                                                         |
| **Room**                | Allows selection of one or multiple room types.                                                                                                                            |
| **Board**               | Select the board type (e.g., Bed & Breakfast, Half Board, etc.) the discount applies to.                                                                                   |
| **Price**               | The specific price code or rate this rule applies to.                                                                                                                      |
| **BDNBA**               | Booking Days No Before Arrival.                                                                                                                                            |
| **IS %**                | Checkbox indicating if the discount is a percentage.                                                                                                                       |
| **PR**                  | Checkbox for "Per Room" discount.                                                                                                                                          |
| **S\&P**                | Checkbox for "Stay & Pay" rules (e.g., Stay 7 Pay 6).                                                                                                                      |
| **BC**                  | Apply on Extra Bed Cost                                                                                                                                                    |
| **BB**                  | Apply on Board basis                                                                                                                                                       |
| **Days of the Week**    | Select days of the week the discount is valid.                                                           ![](<../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png>) |
| **Min Days**            | Minimum number of days in advance the booking must be made to qualify for the discount.                                                                                    |
| **Deposit Date**        | The cutoff date for the deposit to be paid to validate the discount.                                                                                                       |
| **DDNBA**               | Deposit days no before stay                                                                                                                                                |
| **OB**                  | Checkbox indicating if the rule applies to "On Booking"  - Deposit on Booking Final save                                                                                   |
| **Deposit %**           | Discount percentage that applies for the deposit payment.                                                                                                                  |
| **Send List Date**      | Date when the rate list or contract was sent, used for administrative tracking.                                                                                            |
| **SLDNBA**              | Send list days number before arrival stay                                                                                                                                  |
| **EBP Discount**        | Customer Early Booking Discount                                                                                                                                            |
| **Contract**            | Displays the selected contract ID or name that the rule belongs to.                                                                                                        |
| From age/To age         | Specify an optional age range for the Early Booking Discount (Leave the field empty to accept any age).                                                                    |

There are two rules that apply. They cannot be applied at the same time and are governed by the **IS PERCENT** check box:

* Percent - the value inserted in the PRICE case is used as a percent of the total value if the check box is used
* Price - the value inserted in the PRICE case is used as it is if the check box is not used. Also, this rule has two additional exceptions because of the **PER ROOM** check box:
  * Per passenger - if the check box is not used
  * Per room - if the check box is used
* Customer Early booking discount - the value inserted in this case is used in the calculation of the pricelist price. If this value is completed, the normal price will be taken into account when calculating the profit of the room on the booking, and the value for the price list will be taken into account when calculating the price Pricelist prices.

<figure><img src="../../../.gitbook/assets/image (316).png" alt=""><figcaption></figcaption></figure>

This rule can be combined with the **Stay and Pay cost rules** if the **S\&P** check box is used. Filters used:

* Stay Date Start and End
* Booking Start and End date
* Room
* Days no before arrival The rest of the filters are used in **invoices** and will be explained there.

Early Booking Discount with Board Type as a filter

<figure><img src="../../../.gitbook/assets/image (317).png" alt=""><figcaption></figcaption></figure>

In Hotel - Room Costs (Early Booking Cost Discount Rules)  it was added a new field called BOARD, containing all the Board Types defined for the company.

When saving a booking, the cost rules that will be added to the hotel cost calculation will also be filtered by the board types chosen by the passengers.

A board type is set on a product (Basic setup - Board Supplements), so for a passenger to select a board type they should select a product that has the required board type.

If a rule meets all the requirements for a booking, including the board type filter, then the system will also check that every passenger in the room will have the same board type (mixing board types on a passenger will return no rules with board type filters).

If a rule meets all the requirements for a booking but it has no board type filter, it will be applied only to passengers that have no board type selected.

### Stay and Pay cost rules

#### **Overview**

The **Stay and Pay Cost Rules** screen is part of the **Room Costs** module, and it allows configuration of promotional offers where guests pay for fewer nights than they stay — commonly referred to as "Stay X, Pay Y" deals (e.g., Stay 7 nights, Pay only 6).

***

#### **Purpose**

The purpose of this interface is to:

* Define promotional offers that reduce the effective cost of stays.
* Encourage longer bookings by offering free nights.
* Apply rules based on room types, periods, and booking/stay dates.

***

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Instructions**

#### **Top Filter Section**

| **Field**          | **Description**                                                     |
| ------------------ | ------------------------------------------------------------------- |
| **Contract**       | Dropdown to select the applicable contract.                         |
| **Show All**       | Checkbox to show all existing stay and pay rules.                   |
| **+ More Filters** | Expands additional filter options.                                  |
| **Clear**          | Clears all selected filters.                                        |
| **Room Code**      | Dropdown to filter rules for a specific room type.                  |
| **Period**         | Dropdown to filter by periods.                                      |
| **Booking Date**   | Date filter to find rules within specific booking date ranges.      |
| **Departure Date** | Date filter to search for rules active for certain departure dates. |
| **Display**        | Applies all filters and shows matching records.                     |
| **Clear**          | Clears the results from the grid.                                   |

***

#### **Rule Configuration Grid**

| **Field**               | **Description**                                                                |
| ----------------------- | ------------------------------------------------------------------------------ |
| **Stay Start / End**    | Defines the check-in (stay) period the rule applies to.                        |
| **Booking Start / End** | Defines the window in which the booking must be made for the rule to be valid. |
| **Room**                | Dropdown to select one or more room types the rule applies to.                 |
| **Period**              | Select a system-defined period                                                 |
| **Days of the Week**    | Restrict the rule to stays that start on specific days (e.g., Mon-Fri).        |
| **Stay Days No**        | Number of nights the guest must stay to qualify for the promotion.             |
| **Pay Days No**         | Number of nights the guest actually pays for.                                  |
| **EB**                  | Checkbox to indicate if this is combined with Early Booking                    |
| **Contract**            | Dropdown to associate this rule with a specific contract.                      |
| **Trash Icon**          | Allows deletion of a specific rule.                                            |
| **Save**                | Commits all newly added or updated rules to the database/system.               |

They are governed by two cases:

* Stay days no.
* Pay days no. The company uses the room for several days and can pay for a lesser amount of days. The number inserted in the **Pay days no.** cannot be greater than **the Stay days no.**, and both must be greater than 0.

Filters used:

* Stay Start and End date
* Booking Start and End date
* Room
* Period

### Special offer cost​ <a href="#special-offer-cost" id="special-offer-cost"></a>

Special offers are rules setup by hotel owners capable of overriding any other cost rules setup in the hotels.

<figure><img src="../../../.gitbook/assets/image (318).png" alt=""><figcaption></figcaption></figure>

There are 4 rules:

* Room cost
* Extra bed cost
* Early booking
* Stay and pay

Filters used to set up the rules:

* Approved
* Rule Type - select the rule type for the  special offer to be applied (Room cost, Extra bed cost, Stay\&Pay, Early booking);

&#x20;            When the **Rule Type** is set to **Early Booking**, an additional field named **BOARD** becomes available. This field displays all board types defined for the company. For other rule types, the **BOARD** field remains disabled in the _Special Offers_ configuration.

During the booking process, any applicable cost rules used in hotel price calculations will be filtered based on the board types selected by the passengers.\
Board types are assigned to products in the **Basic Setup > Board Supplements** section. To select a board type, passengers must choose a product that includes the desired board type.

If a cost rule includes a board type filter and all other rule conditions are met, the system will apply the rule only if **all passengers in the same room** have the **same board type**. If different board types are assigned to passengers sharing a room, the rule will not be applied.

If a rule does **not** include a board type filter, it will only apply to passengers who have **no board type** selected.

* Stay start date / Stay end date: Defines the stay date range for which the early booking discount is valid.
* Booking start date / Booking end date: Specifies when the booking must be made for the discount to apply.
* Days before arrival
* Room: Allows selection of one or multiple room types.
* Price for each interval
* Days of the week: Select days of the week the Special Offer is valid. (It is applied only when the rule typoe is set as Stay and Pay or Early booing;    &#x20;
* Per day check box (if checked, the price will be applies per day, not per interval)
* Add to default rule (for Early booking only) - if "on", the Special Offer Early Booking rule will not overwrite the contract Early Booking rule, but add to it. It will add in the following manner:
  * contract Early Booking rule will apply first
  * and the Special Offer Early Booking rule will be applied on that result
  * **Please note**! - if the cost of a particular day would be 0 (for various reasons, may be the last 2 days of a Stay 7 pay 5 days rule), then the adding of a discount (Early booking or other) will not result in a negative amount cost but still zero.
* Normal price check box (if checked, it behaves as a price, not as a discount)
* Per pax check box (if checked it applies to each passenger)
* Percent check box (if checked it turns the value into a percent)
* Period
* From age / To age: Specify an optional age range for the Early Booking Discount (Leave the field empty to accept any age).
* Stay (duration of the stay)
* Pay (duration of the pay, works with the **Stay** filter)
* Combine with **Early booking** - dictates if an EB rule will combine with an S\&P rule. If not, the EB rule wins, and S\&P is not taken into account.
* Combine with **Stay and pay** - dictates if an S\&P rule will combine with an EB rule. If not, the S\&P rule wins, and EB is not taken into account.

### Partial mind map of Hotel Cost rule interactions <a href="#partial-mindmap-of-hotel-cost-rule-interractions" id="partial-mindmap-of-hotel-cost-rule-interractions"></a>

This is a mind map trying to cover the various interactions between hotel

<figure><img src="../../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>
