# Room cost

### Overview

Room Cost rules let you define hotel cost conditions per hotel. They keep cost and profit calculations consistent across bookings.

### Purpose

Use Room Cost rules to adjust hotel costs by rules and date windows. This supports correct allocation and reliable profit reporting.

### How it works

* Rules can target:
  * A single hotel
  * A departure (stay) date range
  * A booking date range
  * One room type or all room types for the hotel
* Costs can be calculated:
  * **Per passenger**: applied to each passenger
  * **Per room**: applied once per room and split across occupants

#### Test a rule

1. Create a booking using the hotel and room type.
2. Open the **Profit** tab to see cost and profit.
3. Some values update after **Total Cost Service** recalculates.
4. Use the info icon to see the cost breakdown.

### Room cost rules​ <a href="#room-cost-rules" id="room-cost-rules"></a>

#### Overview

Room Cost Rules define the base cost your agency pays the hotel. They define how cost is calculated and when it changes.

#### Purpose

Use Room Cost Rules to keep hotel costs correct across scenarios. Use thresholds to switch cost after a number of rooms are sold.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### How it works

* **Stay Type** (from the _Stay Type_ dropdown):
  * **Per Room Per Night**
    * The amount is split between passengers in the room.
    * The rule applies per night within the stay period.
    * It can apply on overlapping days within the booking.
  * **Per PAX Per Room**
    * The amount applies per passenger.
  * **Per Room Per Stay**
    * The amount is split across passengers and stay days.
    * The rule applies when arrival is inside the stay interval.
* **Single Price**
  * Adds an extra amount when a room has exactly one passenger.
* **Extra Cost Included**:
  * Subtracts **Extra Cost Included** from **Price**.
  * This happens only when Early Booking or Stay & Pay applies.

**Filters**\
Rules can be restricted based on the following conditions:

* Stay start and end dates
* Booking start and end dates
* Room type

**Changing Costs Based on Number of Rooms Sold**\
It is possible to adjust room costs dynamically using the **Up to rooms** and **Price2** fields:

* If **Up to rooms** is set, the system switches to **Price2** after the threshold.

### Early booking cost-discount rules​ <a href="#early-booking-cost-discount-rules" id="early-booking-cost-discount-rules"></a>

#### **Overview**

Use **Early Booking Cost Discount Rules** to discount hotel costs. The discount applies when a booking is made far enough in advance.

#### **Purpose**

Apply consistent early booking discounts by room, board, and date range. This supports accurate price calculation and profit reporting.

#### **System Setup Requirement**

Before early booking discounts appear in the price list, a specific setting must be enabled in **System Setup**:

**Path:**\
`System Setup → General → Settings`

**Setting name:**\
✅ **Use Early Booking and Stay and Pay for Discount**

**Purpose of the setting:**

* Controls how the discounted cost is used in price calculations.
* Includes Room Discount, Early Booking, and Stay & Pay reductions.
* Ensures profit margin discount reflects the final discounted cost.

<figure><img src="../../../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure>

This setting decides **how** discounted cost is handled. Early Booking rules can still be configured without it. Uses discounted into account Room Discount Early Booking and Stay\&Pay for calculating Discount via Profit Margin

<figure><img src="../../../.gitbook/assets/image (423).png" alt=""><figcaption></figcaption></figure>

* If this setting is **disabled**, rules still show in the screen. They do **not** affect calculated prices in the price list.

{% hint style="warning" %}
This checkbox will not trigger the service automatically; you will need to either have to change the cost in the hotel or change the Profit Margin in the price list, changing the price or saving on the price list will change the price as well.

Also, the profit margin service will not change the price instantly on modification; it may take up to 30 minutes for the price to be changed in the price list. This depends on how many tasks need to be processed by the service.
{% endhint %}

#### Field Explanation

<figure><img src="../../../.gitbook/assets/image (425).png" alt=""><figcaption></figcaption></figure>

#### **Filters Section**

* **Contract**: Select the contract you want to configure.
* **Show all**: Checkbox to display all existing rules.
* **+ More Filters**: Shows more filters.
* **Clear**: Resets filters and fields.
* **Room Code**: Select a room code.
* **Period**: Select the period.
* **Booking date**: Filter by booking dates.
* **Departure date**: Filter by departure/stay dates.

#### **Grid Fields**

| **Field**               | **Description**                                                                                                                                                 |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Stay **Start / End**    | The rule can apply on overlapping stay days. Example: stay 01–07 Oct, rule 05–30 Oct applies on 05–07 Oct.                                                      |
| **Booking Start / End** | Specifies when the booking must be made for the discount to apply.                                                                                              |
| Days of the Week        | Restricts the rule to arrivals on selected weekdays. This has to coincide with the arrival date of the booking. ![](<../../../.gitbook/assets/image (569).png>) |
| **Room**                | Allows selection of one or multiple room types.                                                                                                                 |
| **Board**               | Board type filter. If the booking has a board, the system looks for a matching board rule first. If none exists, it can use a rule without board.               |
| From Age/to Age         | Defines the age interval for which the rule applies.                                                                                                            |
| **Price**               | The specific price code or rate this rule applies to.                                                                                                           |
| **BDNBA**               | Booking Days No Before Arrival.                                                                                                                                 |
| **IS %**                | Treats **Price** as a percent of (Room Cost + Extra Included + Extra Bed + Stay & Pay). The result is subtracted.                                               |
| **PR**                  | Per-room discount. Splits the discount across passengers in the room.                                                                                           |
| **S\&P**                | Allows this rule to combine with Stay & Pay. If unchecked, Stay & Pay is excluded from cost.                                                                    |
| E**BC**                 | Apply on Extra Bed Cost                                                                                                                                         |
| **BB**                  | Apply on Board basis                                                                                                                                            |
| **Min Days**            | Minimum number of days in advance the booking must be made to qualify for the discount.                                                                         |
| **Deposit Date**        | The cutoff date for the deposit to be paid to validate the discount.                                                                                            |
| **DDNBA**               | Deposit days no before stay                                                                                                                                     |
| **OB**                  | Applies on booking final save (deposit on booking).                                                                                                             |
| **Deposit %**           | Discount percentage that applies for the deposit payment.                                                                                                       |
| **Send List Date**      | Date when the rate list or contract was sent, used for administrative tracking.                                                                                 |
| **SLDNBA**              | Send list days number before arrival stay                                                                                                                       |
| **EBP Discount**        | Customer Early Booking Discount                                                                                                                                 |
| **Contract**            | Displays the selected contract ID or name that the rule belongs to.                                                                                             |
| **Invoice List**        | Invoices created according to the rule.                                                                                                                         |

#### Percent vs fixed value

Only one of these applies at a time. It is controlled by **IS %**.

* **Percent**: **Price** is treated as a percentage.
* **Fixed value**: **Price** is treated as a value.
  * If **PR** is unchecked, it is per passenger.
  * If **PR** is checked, it is per room.
* **EBP Discount** affects the selling price in the price list. Profit can still use the “normal” price for cost/profit comparison.

<figure><img src="../../../.gitbook/assets/image (316).png" alt=""><figcaption></figcaption></figure>

This rule can combine with **Stay and Pay cost rules** if **S\&P** is checked.

Filters used:

* Stay Date Start and End
* Booking Start and End date
* Room
* Days no before arrival

Other fields are used for invoices and are explained elsewhere.

Early Booking Discount with Board Type as a filter

<figure><img src="../../../.gitbook/assets/image (317).png" alt=""><figcaption></figcaption></figure>

The Early Booking Cost Discount Rules include a **Board** field. It contains board types defined for the company.

When you save a booking, cost rules are filtered by passenger board type.

Board type comes from the product (Basic setup → Board Supplements). Passengers pick board type by selecting a matching product.

If a board filter is used, all passengers in the room must match it. Mixed board types in the same room will not match board-filtered rules.

If a rule has no board filter, it applies only to passengers without board type.

### Stay and Pay cost rules

#### **Overview**

Stay and Pay Cost Rules support “Stay X, Pay Y” deals. Example: stay 7 nights and pay 6.

#### **Purpose**

Encourage longer stays by lowering cost on specific nights. The system recalculates cost using the stay/pay definition.

#### **System Setup Requirement**

Stay & Pay must be enabled to affect the selling price and the price list.

**Path:**\
`System Setup → General → Settings`

**Setting name:**\
✅ **Use Early Booking and Stay and Pay for Discount**

**Purpose of the setting:**

* Enables Stay & Pay rules in the price list.
* Makes them affect guest price calculation.

<figure><img src="../../../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (423).png" alt=""><figcaption></figcaption></figure>

* If disabled, rules still show in configuration. They do not affect price list calculations.

{% hint style="warning" %}
This checkbox does not trigger recalculation jobs. Change hotel cost or profit margin to trigger updates.

Price updates can take up to 30 minutes. Timing depends on service load.
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
| **Period**              | Select a system-defined period.                                                |
| **Stay Days No**        | Number of nights the guest must stay to qualify for the promotion.             |
| **Pay Days No**         | Number of nights the guest actually pays for.                                  |
| **EB**                  | Allows combination with Early Booking.                                         |
| **Contract**            | Dropdown to associate this rule with a specific contract.                      |
| **Trash Icon**          | Allows deletion of a specific rule.                                            |
| **Save**                | Commits all newly added or updated rules to the database/system.               |

#### Validation rules

* **Stay days no.** must be greater than 0.
* **Pay days no.** must be greater than 0.
* **Pay days no.** cannot be greater than **Stay days no.**

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

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Types of Extra Cost Rules**

1. **Extra price per passenger per night**
   * Formula: _value × number of nights_
2. **Extra price per room**
   * One-time cost per room.
   * The system distributes the cost across room occupants.

#### **Filters for Applying**

Extra costs are applied only when these conditions are met:

* **Age** – Define a start and end age range for which the extra cost applies.
* **Extra P/P/N (Extra Price/Pax/Night)** – Multiplied by the number of nights and applicable guests.
* **Extra P/R (Extra Price/Room)** – One-time charge per room, not per night.
* **Stay/Arrival Period** – Limit the extra cost to bookings with arrivals within specific dates.
* **Booking Period** – Apply the cost only if the booking is created within a defined date range.
* **Room** – Restrict the cost to a specific room type.

#### Creating a New Rule

1. Click **Create** (top right).
2. Set **From age** and **To age**.
3. Set **Extra P/P/N**, **Extra P/R**, or both.
4. Set **Stay/Arrival Start** and **Stay/Arrival End**.
5. Set **Booking Start** and **Booking End**.
6. Select a **Room** (or **All Rooms**).
7. Select a **Contract**, if needed.
8. Save the rule.

#### Editing an Existing Rule

1. Locate the rule you want to modify in the table
2. Click on the row or edit icon (if available)
3. Modify the required fields
4. Ensure date ranges don’t conflict with other rules
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

This mind map highlights common interactions between hotel cost rules.

<figure><img src="../../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

***

### FAQ

#### Why doesn’t my Room Cost rule apply?

Most misses come from date filters. Check stay dates, booking dates, and room type first.

#### What’s the difference between **Per room** and **Per passenger**?

**Per room** applies once per room and is split across occupants. **Per passenger** applies to each passenger individually.

#### Why did the price list not update after I changed a rule?

Rule edits do not trigger recalculation jobs automatically. Price list updates can take up to 30 minutes.

#### Why do I see the hotel cost as one value in Profit?

The Profit tab shows a single total by default. Use the info icon for the detailed breakdown.

#### What does **Extra Cost Included** do?

It reduces the base **Price** value. It only applies when EB or S\&P cost applies.

#### Why is my Early Booking rule with **Board** not applied?

All passengers in the same room must have the same board type. Mixed board types will not match board-filtered rules.

#### Can Early Booking and Stay & Pay combine?

Yes, if the relevant “combine” checkbox is enabled in the rule. Otherwise, one discount can override the other.

#### What happens if a day becomes **0 cost** due to discounts?

Cost will never go below 0. Additional discounts keep it at 0.
