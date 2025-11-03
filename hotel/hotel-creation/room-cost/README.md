# Room cost

**Overview**\
Room Cost rules allow you to define additional cost conditions for a specific hotel. These rules provide flexibility in how costs are applied, ensuring accurate pricing and profit calculations across different booking scenarios.

**Purpose**\
The main purpose of Room Cost rules is to adjust hotel costs based on defined criteria, such as travel dates, booking dates, and room types. This ensures that costs are distributed correctly per passenger or per room, supporting both fair allocation and transparent profit reporting.

**How it works**

* Rules can be applied to:
  * A specific hotel
  * A departure date range
  * A booking date range
  * A single room type or all room types linked to the hotel
* Cost calculation options:
  * **Per passenger** – cost applies individually to each traveler
  * **Per room** – cost is applied once per room and divided among its occupants
* Testing a rule:
  1. Create a booking with the selected hotel and room type.
  2. Open the **Profit** tab to view real-time calculations of cost and profit.
  3. Some cost figures update only after the **Total Cost Service** recalculates.
  4. In the **Profit** tab, the hotel cost is displayed as a single value, with an information icon providing a detailed breakdown of how the cost was calculated.

### Room cost rules​ <a href="#room-cost-rules" id="room-cost-rules"></a>

**Overview**\
Room Cost Rules define the base value that the agency pays to the hotel for reserved rooms. These rules establish how costs are calculated (per room or per passenger), whether extra cost adjustments apply, and how costs may change when a certain number of rooms are sold.

**Purpose**\
The purpose of Room Cost Rules is to ensure accurate and flexible cost allocation in different booking scenarios. By applying configurable conditions, the system can adjust how costs are calculated and update them automatically when thresholds are reached.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**How It Works**

* **Stay Type setting** (controlled by the _Stay Type_ dropdown):
  * Per Room Per Night&#x20;
    * 1\. the amount is split between the passengers in room.&#x20;
    * 2\. the rule is applying per day for example: booking with arrival on the period 01-01-2025 - 06-01-2025 a rule can apply if is defined between 04-01-2025 - 09-01-2025 on the booking regardless of arrival date of the booking.
  * Per PAX Per Room - the amount applies per PAX
  * Per Room Per Stay &#x20;
    * 1\. the amount is spited between PAX in room and between days to stay.&#x20;
    * 2\. the rule is apply if arrival date is in stay interval
* **Single Price** - If we have the amount set and we have a room with one passenger in room the single price will be added to the price of the rule.
* **Extra Cost Included**:
  * The value entered in the **Extra Cost Included** field is subtracted from the **Price** value, but **only if** an Early Booking or an S\&P Rule cost is applied.

**Filters**\
Rules can be restricted based on the following conditions:

* Stay start and end dates
* Booking start and end dates
* Room type

**Changing Costs Based on Number of Rooms Sold**\
It is possible to adjust room costs dynamically using the **Up to rooms** and **Price2** fields:

* If a threshold is set in the **Up to rooms** column, once that number of rooms is booked, the system automatically switches to the new cost defined in the **Price2** column.

### Early booking cost-discount rules​ <a href="#early-booking-cost-discount-rules" id="early-booking-cost-discount-rules"></a>

#### **Overview**

The **Early Booking Cost Discount Rules** section within the **Room Costs** tab allows you to configure and manage early booking discounts for hotels. These rules apply when bookings are made a set number of days in advance, offering discounted rates to incentivize early reservations.

#### **Purpose**

The purpose of these rules is to automatically apply early booking discounts to the selected rooms, board types, and date periods, ensuring consistent and accurate price calculation in the system and towards the customer.

#### **System Setup Requirement**

Before early booking discounts appear in the price list, a specific setting must be enabled in **System Setup**:

**Path:**\
`System Setup → General → Settings`

**Setting name:**\
✅ **Use Early Booking and Stay and Pay for Discount**

**Purpose of the setting:**

* The **User’s Discounted Cost** represents the calculated cost of a booking after applying all relevant discounts. This value takes into account **Room Discount**, **Early Booking**, and **Stay & Pay** offers. This calculation ensures that the **Discount via Profit Margin** reflects the final, accurate cost after all applicable reductions have been applied.



<figure><img src="../../../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure>

The above setting decide "HOW" the discount is applied. The Early Booking Discount has an impact on the price regardless of whether this checkbox is selected or not

<figure><img src="../../../.gitbook/assets/image (423).png" alt=""><figcaption></figcaption></figure>

* If this setting is **disabled**, EBD rules will still appear in the configuration screen but will **not be reflected** in the calculated prices or displayed to users in the price list.

{% hint style="warning" %}
Note: This checkbox will not trigger the service automatically; you will need to either have to change the cost in the hotel or change the Profit Margin in the price list, changing the price or saving on the price list will change the price as well.

Also, the profit margin service will not change the price instantly on modification; it may take up to 30 minutes for the price to be changed in the price list. This depends on how many tasks need to be processed by the service.
{% endhint %}

#### Field Explanation

<figure><img src="../../../.gitbook/assets/image (425).png" alt=""><figcaption></figcaption></figure>

#### **Filters Section**

* **Contract**: Dropdown to select the contract for which you want to define early booking rules.
* **Show all**: Checkbox to display all existing rules.
* **+ More Filters**: Allows advanced filtering options (not fully visible in the screenshot).
* **Clear**: Resets all filters and fields.
* Room Code:  Select a specific room code to define EBD
* Period: Select the interval
* Booking date
* Departure date

#### **Grid Fields**

| **Field**               | **Description**                                                                                                                                                                                                                                                                                                                                          |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Stay **Start / End**    | The early booking can be applicable in any day of the stay period example: booking stay period 01 Oct to 07 Oct and a rule with period 05 Oct to 30 Oct will apply on the days 05 Oct 06 Oct and 07 Oct                                                                                                                                                  |
| **Booking Start / End** | Specifies when the booking must be made for the discount to apply.                                                                                                                                                                                                                                                                                       |
| Days of the Week        | Select the days of the week on which the discount is valid.   This has to coincide with the arrival date of the booking                                                        ![](<../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>) |
| **Room**                | Allows selection of one or multiple room types.                                                                                                                                                                                                                                                                                                          |
| **Board**               | Select the board type (e.g., Bed & Breakfast, Half Board, etc.) the discount applies to. If the booking has a board type will look for a rule with board type; if there is none, it will settle with a rule that has no board type at all.                                                                                                               |
| From Age/to Age         | Defines the age interval for which the rule applies.                                                                                                                                                                                                                                                                                                     |
| **Price**               | The specific price code or rate this rule applies to.                                                                                                                                                                                                                                                                                                    |
| **BDNBA**               | Booking Days No Before Arrival.                                                                                                                                                                                                                                                                                                                          |
| **IS %**                | If checked, then the amount will be a percentage calculated from the sum between Room Cost, Extra Included, Extra bed, and Stay & Pay, and this will be subtracted from this amount to calculate the cost.                                                                                                                                               |
| **PR**                  | Checkbox for "Per Room" discount. Will split the price between passengers in the room                                                                                                                                                                                                                                                                    |
| **S\&P**                | Checkbox for "Stay & Pay" rules (e.g., Stay 7 Pay 6). If checked, it will allow the rule to combine with stay and pay rules; otherwise, it will exclude the S\&P rule from the cost.                                                                                                                                                                     |
| E**BC**                 | Apply on Extra Bed Cost                                                                                                                                                                                                                                                                                                                                  |
| **BB**                  | Apply on Board basis                                                                                                                                                                                                                                                                                                                                     |
| **Min Days**            | Minimum number of days in advance the booking must be made to qualify for the discount.                                                                                                                                                                                                                                                                  |
| **Deposit Date**        | The cutoff date for the deposit to be paid to validate the discount.                                                                                                                                                                                                                                                                                     |
| **DDNBA**               | Deposit days no before stay                                                                                                                                                                                                                                                                                                                              |
| **OB**                  | Checkbox indicating if the rule applies to "On Booking"  - Deposit on Booking Final save                                                                                                                                                                                                                                                                 |
| **Deposit %**           | Discount percentage that applies for the deposit payment.                                                                                                                                                                                                                                                                                                |
| **Send List Date**      | Date when the rate list or contract was sent, used for administrative tracking.                                                                                                                                                                                                                                                                          |
| **SLDNBA**              | Send list days number before arrival stay                                                                                                                                                                                                                                                                                                                |
| **EBP Discount**        | Customer Early Booking Discount                                                                                                                                                                                                                                                                                                                          |
| **Contract**            | Displays the selected contract ID or name that the rule belongs to.                                                                                                                                                                                                                                                                                      |
| Invoice List            | List of invoices created according t othe rule                                                                                                                                                                                                                                                                                                           |

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

#### **Purpose**

This functionality provides flexible discounting for long stays, encouraging longer bookings while automatically adjusting the price based on the defined “stay” and “pay” conditions.

#### **System Setup Requirement**

Before Stay\&Pay cost rules  can affect the selling price or appear in the price list, a specific setting must be enabled in **System Setup**:

**Path:**\
`System Setup → General → Settings`

**Setting name:**\
✅ **Use Early Booking and Stay and Pay for Discount**

**Purpose of the setting:**

* This setting must be **enabled** for Stay & Pay  (S\&P) rules to be **visible in the Price List** and to have an **actual impact on the guest price calculation**.&#x20;



<figure><img src="../../../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (423).png" alt=""><figcaption></figcaption></figure>

* If this setting is **disabled**, S\&P rules will still appear in the configuration screen, but will **not be reflected** in the calculated prices or displayed to users in the price list.

{% hint style="warning" %}
Note that this checkbox will not trigger the service automatically; you will need to either have to change the cost in the hotel or change the Profit Margin in the price list, changing the price or saving on the price list will change the price as well.

Also, the profit margin service will not change the price instantly on modification; it may take up to 30 minutes for the price to be changed in the price list. This depends on how many tasks need to be processed by the service.
{% endhint %}

#### Field Explanation

<figure><img src="../../../.gitbook/assets/image (426).png" alt=""><figcaption></figcaption></figure>

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

#### **Rule Configuration Grid**

| **Field**               | **Description**                                                                |
| ----------------------- | ------------------------------------------------------------------------------ |
| **Stay Start / End**    | Defines the check-in (stay) period the rule applies to.                        |
| **Booking Start / End** | Defines the window in which the booking must be made for the rule to be valid. |
| **Days of the Week**    | Restrict the rule to stays that start on specific days (e.g., Mon-Fri).        |
| **Room**                | Dropdown to select one or more room types the rule applies to.                 |
| **Period**              | Select a system-defined period                                                 |
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

### Hotel extra cost rules <a href="#hotel-extra-cost-rules" id="hotel-extra-cost-rules"></a>

**Overview**\
Hotel Extra Cost Rules define additional costs that the agency pays to hotels. These rules are applied automatically to bookings when specific conditions are met. Both types of rules are always applied, ensuring that extra costs are accurately reflected in the booking’s financial calculations.

**Purpose**\
The purpose of these rules is to ensure that hotel-related expenses beyond the base room cost are correctly accounted for. This provides a transparent view of the agency’s expenses and supports more precise profit analysis.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Types of Extra Cost Rules**

1. **Extra price per passenger per night**
   * Formula: _value × number of nights_
2. **Extra price per room**
   * Formula: _value × number of passengers in the room_

#### **Filters for Applying**

&#x20;**Costs**Extra costs are only applied when the following conditions are met:

* **Age** – Define a start and end age range for which the extra cost applies.
* **Extra P/P/N (Extra Price/Pax/Night) -** This amount is multiplied by the number of nights and applicable guests
* **Extra P/R (Extra Price/Room) -** This is a one-time charge per room, not dependent on stay duration
* **Stay/Arrival Period** – Limit the extra cost to bookings with arrivals within specific dates.
* **Booking Period** – Apply the cost only if the booking is created within a defined date range.
* **Room** – Restrict the cost to a specific room type.

#### Creating a New Rule

1. Click the **"Create"** button (top right)
2. Define the age range using FROM AGE and TO AGE fields
3. Set either EXTRA P/P/N (per night) or EXTRA P/R (per room) or both
4. Specify the stay period using STAY/ARRIVAL START and END dates
5. Specify the booking period using BOOKING START and END dates
6. Select the applicable room type or "All Rooms"
7. Select the relevant contract if applicable
8. Save the new rule

#### Editing an Existing Rule

1. Locate the rule you want to modify in the table
2. Click on the row or edit icon (if available)
3. Modify the required fields
4. Ensure date ranges don't create conflicts with other rules
5. Save changes

#### Deleting a Rule

1. Locate the rule in the table
2. Click the **delete icon** (trash can) on the right side of the row
3. Confirm the deletion when prompted

### Special offer cost​ <a href="#special-offer-cost" id="special-offer-cost"></a>

**Overview**\
Special Offer Costs are advanced rules defined by hotel owners that can override any other cost rules configured for a hotel. These rules are designed to manage promotional pricing strategies such as discounts, free nights, or early booking benefits.

**Purpose**\
The purpose of Special Offer rules is to provide flexibility for hotels to apply promotional pricing conditions that take precedence over standard cost rules. This ensures accurate cost handling while allowing hotels to incentivize bookings through discounts or stay-based offers.

<figure><img src="../../../.gitbook/assets/image (318).png" alt=""><figcaption></figcaption></figure>

#### Types of Special Offer Rules

There are four types of rules available:

1. **Room Cost** – Adjusts the base room cost.
2. **Extra Bed Cost** – Applies a discount or adjustment to extra beds.
3. **Early Booking (EB)** – Provides discounts for bookings made in advance.
4. **Stay and Pay (S\&P)** – Offers free nights or reduced costs based on length of stay (e.g., _Stay 7 nights, Pay 5_).

#### Rule Configuration and Filters

* **Approved** – The rule must be approved before it can be applied.
* **Rule Type** – Select the rule type (_Room Cost, Extra Bed Cost, Stay & Pay, Early Booking_).
  * If set to **Early Booking**, the **Board** field becomes available, displaying all board types defined in the company. For other rule types, the field is disabled.
* **Board Types**:
  * Assigned under **Basic Setup > Board Supplements**.
  * Passengers must select a product with the desired board type.
  * If a rule includes a board filter, it only applies when **all passengers in the same room** share the same board type.
  * If different board types exist in one room, the rule is not applied.
  * If no board type filter exists, the rule applies only to passengers with **no board type** selected.

**Date and Time Filters:**

* **Stay Start / Stay End Dates** – Define the stay period when the offer applies.
* **Booking Start / Booking End Dates** – Specify when the booking must be created.
* **Days Before Arrival** – Apply the offer only if the booking is made a certain number of days in advance.
* **Days of the Week** – Restrict validity to selected weekdays (_only for Stay & Pay or Early Booking rules_).

**Room and Price Filters:**

* **Room** – Apply to one or multiple room types.
* **Price per Interval** – Define a cost or discount for each time interval.
* **Per Day** (checkbox) – If enabled, the price is applied per day instead of per interval.
* **Normal Price** (checkbox) – If enabled, the rule behaves as a fixed price rather than a discount.
* **Per Pax** (checkbox) – If enabled, the rule applies per passenger.
* **Percent** (checkbox) – If enabled, the value is treated as a percentage rather than a fixed amount.

**Special Options:**

* **Add to Default Rule (Early Booking only)** – If enabled, the Special Offer EB rule is added on top of the contract EB rule instead of replacing it:
  1. The contract EB rule is applied first.
  2. The Special Offer EB rule is then applied to the resulting value.
* **Stay / Pay Duration** – Define the length of the stay and the payable duration (e.g., _Stay 7, Pay 5_).
* **Combine with Early Booking** – Defines whether an EB rule can be combined with an S\&P rule. If disabled, EB overrides S\&P.
* **Combine with Stay & Pay** – Defines whether an S\&P rule can be combined with an EB rule. If disabled, S\&P overrides EB.
* **From Age / To Age** – Apply the rule only to passengers within the defined age range. Leave empty to allow all ages.

***

#### Important Notes

* If the calculated cost for a particular day is **0** (for example, due to a _Stay 7, Pay 5_ rule), applying an additional discount (EB or otherwise) will not result in a negative value—the cost will remain **0**.

### Partial mind map of Hotel Cost rule interactions <a href="#partial-mindmap-of-hotel-cost-rule-interractions" id="partial-mindmap-of-hotel-cost-rule-interractions"></a>

This is a mind map trying to cover the various interactions between hotel

<figure><img src="../../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>
