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

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

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

The **Early Booking Cost Discount Rules** page allows the creation of rules that reduce hotel costs when bookings are made within a defined **advance booking window**.

The rule applies when the following conditions are met:

* The **stay period** matches the configured dates.
* The **booking date** falls within the allowed booking window.
* The rule conditions such as **room type**, **board**, **days of week**, and **passenger age** match the booking details.

The discount is applied **to the hotel cost**, not directly to the selling price. However, because selling prices may be calculated from hotel costs (for example through **Profit Margin rules**), the Early Booking discount can indirectly influence the final price presented to the guest.

#### **Purpose**

Early Booking Cost Discount Rules provide a structured method for:

* Offering **lower hotel costs for early bookings**
* Supporting **seasonal sales strategies**
* Adjusting costs depending on **room type, board type, or booking period**
* Maintaining consistent pricing behavior across contracts and price lists

This functionality is commonly used for promotions where bookings made before a defined deadline receive discounted hotel costs.

#### **System Setup Requirement**

The following configuration must exist before Early Booking Cost Discount Rules can function correctly:

1. **Room Cost Rules** must already be defined for the hotel.
2. **Board Supplements** must be configured if board filtering will be used.
3. The **System Setup setting** controlling how discounted costs are used in price calculation must be understood and configured correctly.

Path to system setting: **System Setup → General → Settings**

Setting name: **Use Early Booking and Stay and Pay for Discount**

<figure><img src="../../../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure>

This setting enables the system to automatically apply an **Early Booking Discount (EBD)** within the Price List.

When the option is configured and active, the system performs the following actions:

1. **Creates a discounted price** in the Price List for the defined period.
2. **Adds a discount line in the booking**, clearly showing the **EBD reduction granted to the guest**.

As a result, the guest price is calculated based on the discounted value, while the booking interface transparently displays the **EBD discount line**, making it clear that the reduced price is due to the Early Booking promotion.

This mechanism ensures both:

* **Correct price calculation in the Price List**, and
* **Clear visibility of the discount granted to the guest in the booking details**.

**Purpose of the setting:**

This setting determines how **discounted hotel costs** are reflected in the **Price List** and guest pricing.

When the setting is enabled:

* Early Booking discounts are used when calculating **discount lines in the price list**
* The system can display a **visible Early Booking discount** to the guest
* The final price calculation reflects all cost reductions including:
  * **Room Discount**
  * **Early Booking**
  * **Stay & Pay**

In practice, this means the price list can show a **discounted selling price and a discount line** that represents the Early Booking Discount offered to the guest.

<figure><img src="../../../.gitbook/assets/image (423).png" alt=""><figcaption></figcaption></figure>

When the setting is disabled:

* The Early Booking rule still **reduces the hotel cost**.
* If **Profit Margin rules** are used to calculate the selling price from the cost, the final selling price may still become lower because the cost has decreased.
* However, the system will **not create a visible Early Booking discount line** in the price list.

This setting therefore controls **how the discount is presented**, not whether the cost reduction itself exists.

{% hint style="warning" %}
Changes to Early Booking Cost Discount Rules may require recalculation before they appear in the price list.

Recalculation can be triggered by:

* Updating the **hotel cost**
* Updating the **Profit Margin rule**
* Saving or recalculating the **Price List**

The **Profit Margin service** processes price updates asynchronously.\
Price list updates may take **up to 30 minutes**, depending on the number of tasks currently being processed by the service.,
{% endhint %}

#### Field Explanation

<figure><img src="../../../.gitbook/assets/image (425).png" alt=""><figcaption></figcaption></figure>

#### **Filters Section**

The filter section allows the list of Early Booking rules to be narrowed to specific contracts, rooms, or periods.

* **Contract**: Dropdown used to select the **hotel contract** for which Early Booking rules are displayed or created. Only rules associated with the selected contract will appear in the grid.
* **Show all**: Checkbox that displays **all existing rules**, including those that may not match the current filters. This is useful when reviewing all rules configured for a contract.
*   **+ More Filters**: Expands the filter section and displays additional filtering options such as:

    * Room Code
    * Period
    * Booking Date
    * Departure Date

    These filters help locate specific rules in contracts containing large numbers of cost rules.
* **Clear**: Resets all filters and displays the default rule list.
*   **Room Code**: Filter used to display rules related to a specific **room type** configured in the hotel contract. Room types are defined in:

    **Hotel → Room Types**
* **Period**: Filters rules based on the **stay period** defined in the rule.&#x20;
* **Booking date**: Filters rules based on the **booking window** defined in the rule. This allows identification of rules that apply when bookings are made within certain date ranges.
* **Departure date**: Filter by departure/stay dates.
* **Create:** Button used to create a new **Early Booking Cost Discount Rule**. Selecting this option adds a new row in the grid where all rule parameters can be defined.

#### **Grid Fields**

The grid displays all Early Booking Cost Discount Rules configured for the selected hotel contract.

Each column defines conditions or parameters that control when the rule applies.

| **Field**                | **Description**                                                                                                                                                                                                                                                                                             |
| ------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Stay** **Start / End** | Defines the **first stay date/**&#x74;he **last stay date** for which the Early Booking rule is valid. Bookings with arrival dates **before this date/after this date** will not match the rule. The rule can apply to overlapping stay days. Example: stay 01–07 Oct, rule 05–30 Oct applies on 05–07 Oct. |
| **Booking Start / End**  | Specifies when the booking must be made for the discount to apply.                                                                                                                                                                                                                                          |
| Days of the Week         | Restricts the rule to arrivals on selected weekdays. This has to coincide with the arrival date of the booking. If no value is selected, the rule applies to **all days**.![](<../../../.gitbook/assets/image (569).png>)                                                                                   |
| **Room**                 | <p>Defines the <strong>room types</strong> to which the rule applies.</p><p>Room types must exist in:</p><p><strong>Hotel → Room Types</strong></p><p>Selecting <strong>Selected all</strong> means the rule applies to every configured room type.</p>                                                     |
| **Board**                | Board type filter. If the booking has a board, the system looks for a matching board rule first. If none exists, it can use a rule without board.                                                                                                                                                           |
| From Age/to Age          | Defines the age interval for which the rule applies.                                                                                                                                                                                                                                                        |
| **Price**                | <p>Defines the <strong>discount value</strong> applied to the hotel cost.</p><p>How this value is interpreted depends on the <strong>IS %</strong> field.</p>                                                                                                                                               |
| **BDNBA**                | <p>Defines whether the rule should consider <strong>booking days before arrival</strong>.</p><p>This value may be used together with booking date filters to restrict the rule based on how many days in advance the booking is made.</p>                                                                   |
| **IS %**                 | Treats **Price** as a percent of (Room Cost + Extra Included + Extra Bed + Stay & Pay). The result is subtracted.                                                                                                                                                                                           |
| **PR**                   | <p>Defines whether the value is applied <strong>per room</strong> or <strong>per passenger</strong>.</p><ul><li>Enabled → discount applied <strong>per room</strong></li><li>Disabled → discount applied <strong>per passenger</strong></li></ul>                                                           |
| **S\&P**                 | <p>Indicates whether the rule can <strong>combine with Stay and Pay Cost Rules</strong>.</p><p>If enabled, both rules may be applied during cost calculation.</p><p>Stay and Pay rules are configured under:</p><p><strong>Room Costs → Stay and Pay Cost Rules</strong></p>                                |
| E**BC**                  | Apply on Extra Bed Cost                                                                                                                                                                                                                                                                                     |
| **BB**                   | Internal indicator used to identify rules that interact with board-based configurations.                                                                                                                                                                                                                    |
| **Min Days**             | <p>Defines the <strong>minimum number of days before arrival</strong> required for the rule to apply.</p><p>If a booking is created fewer days before arrival than defined here, the rule will not apply.</p>                                                                                               |
| **Deposit Date**         | The cutoff date for the deposit to be paid to validate the discount.                                                                                                                                                                                                                                        |
| **DDNBA**                | Defines the **days before arrival** used for deposit-related conditions.                                                                                                                                                                                                                                    |
| **OB**                   | Applies on booking final save (deposit on booking).                                                                                                                                                                                                                                                         |
| **DEPOSIT %**            | Discount percentage that applies for the deposit payment.                                                                                                                                                                                                                                                   |
| **Send List Date**       | Date when the rate list or contract was sent, used for administrative tracking.                                                                                                                                                                                                                             |
| **SLDNBA**               | Send list days number before arrival stay                                                                                                                                                                                                                                                                   |
| **EBP Discount**         | Customer Early Booking Discount                                                                                                                                                                                                                                                                             |
| **Contract**             | <p>Displays the contract associated with the rule.</p><p>This helps identify the rule when multiple contracts exist for the same hotel.</p>                                                                                                                                                                 |
| **Invoice List**         | <p>Displays the invoice processing status for the rule.</p><p>The message <strong>“Rule not run by service”</strong> indicates that the background service responsible for applying the rule has not yet processed it.</p>                                                                                  |

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

#### Introduction

The **Stay and Pay Cost Rules** page is part of the **Hotel → Room Costs** configuration in **Tourpaq Office**. It allows the definition of promotions where a guest stays a certain number of nights but pays for fewer nights.

This functionality supports common hotel promotions such as **“Stay 7 nights, Pay 6”** or **“Stay 14 nights, Pay 12.”**

Stay and Pay Cost Rules work together with several other Tourpaq components:

* **Room Cost Rules** (base hotel costs)
* **Early Booking Cost Discount Rules**
* **Price Lists**
* **Profit Margin rules**
* **Hotel Contracts**

These components together determine the **final hotel cost and selling price** used in bookings and price lists.

#### **Overview**

**Stay and Pay Cost Rules** define cost reductions based on the length of stay.\
When a booking satisfies the configured conditions, the system recalculates the hotel cost so that only the configured **Pay Days No** are charged even though the guest stays longer.

Example:

* **Stay Days No:** 7
* **Pay Days No:** 6

The booking stays for **7 nights**, but the hotel cost is calculated as **6 nights**.

The cost reduction occurs at the **hotel cost level**. If the selling price is calculated using **Profit Margin rules**, the reduced cost may also produce a **lower selling price toward the guest**.

#### **Purpose**

Stay and Pay Cost Rules are used to:

* Encourage **longer stays**
* Support hotel promotions defined in contracts
* Automate cost recalculation based on stay length
* Maintain consistent pricing across bookings and price lists

This functionality allows promotional hotel deals to be implemented directly within the Tourpaq cost calculation system.

#### **System Setup Requirement**

The following conditions must exist before Stay and Pay Cost Rules can function correctly:

1. A **Hotel** must be configured.
2. **Room Cost Rules** must exist for the hotel.
3. **Room Types** must be configured in the contract.
4. The system behavior for displaying discounts in the **Price List** depends on a configuration in System Setup.

Path to system setting: **System Setup → General → Settings**

Setting name: **Use Early Booking and Stay and Pay for Discount**

**Purpose of the setting:**

This setting controls **how Stay and Pay discounts are represented in the price list and guest pricin**

* Enables Stay & Pay rules in the price list.
* Makes them affect guest price calculation.

<figure><img src="../../../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (423).png" alt=""><figcaption></figcaption></figure>

When the setting is enabled:

* The price list may display a **discount line** representing the Stay and Pay promotion.
* The discount can appear as a **visible reduction toward the guest price**.
* The system considers Stay and Pay together with other discounts such as:
  * **Early Booking**
  * **Room Discounts**

When the setting is disabled:

* Stay and Pay rules still **reduce the calculated hotel cost**.
* If the selling price is calculated from cost using **Profit Margin rules**, the final selling price toward the guest may still become **lower because the underlying cost has decreased**.
* However, the system will **not create a visible Stay and Pay discount line in the price list**.

The setting therefore controls **how the discount is presented in the price list**, not whether the rule affects cost calculation.

#### Price List Recalculation

Changes to Stay and Pay Cost Rules may require price recalculation before appearing in the price list.

Recalculation can occur when:

* **Hotel costs are modified**
* **Profit Margin rules are updated**
* The **Price List** is saved or recalculated

{% hint style="warning" %}
This checkbox does not trigger recalculation jobs. Change hotel cost or profit margin to trigger updates.

Price updates can take up to 30 minutes. Timing depends on service load.
{% endhint %}

#### Field Explanation

<figure><img src="../../../.gitbook/assets/image (711).png" alt=""><figcaption></figcaption></figure>

#### **Top Filter Section**

| **Field**          | **Description**                                                                                                                                                                                                                                                                                                                                                     |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Contract**       | Dropdown used to select the **hotel contract** for which Stay and Pay rules are displayed.                                                                                                                                                                                                                                                                          |
| **Show All**       | <p>Checkbox that displays <strong>all configured Stay and Pay rules</strong>, including rules that may not match the current filters.</p><p>This option is useful when reviewing the complete rule configuration for a contract.</p>                                                                                                                                |
| **+ More Filters** | <p>Expands the filter section and displays additional filtering options.</p><p>These include filters for:</p><ul><li><strong>Room Type</strong></li><li><strong>Period</strong></li><li><strong>Booking date</strong></li><li><strong>Departure date</strong></li></ul><p>These filters help locate specific rules in contracts containing many configurations.</p> |
| **Clear**          | Resets all filters and returns the grid to the default display.                                                                                                                                                                                                                                                                                                     |
| **Room Type**      | <p>The dropdown is used to filter rules by <strong>room type</strong>.</p><p>Room types originate from the configuration in:</p><p><strong>Hotel → Room Types</strong></p>                                                                                                                                                                                          |
| **Period**         | <p>Dropdown used to filter rules by <strong>period number</strong>.</p><p>Periods are used within hotel to define seasonal or contractual cost ranges.</p>                                                                                                                                                                                                          |
| **Booking Date**   | <p>Date selector used to filter rules based on the <strong>booking date range</strong> defined in the rule.</p><p>This filter helps locate rules that apply only to bookings made within a certain period.</p>                                                                                                                                                      |
| **Departure Date** | <p>Date selector used to filter rules by <strong>stay date</strong>.</p><p>This allows quick identification of rules that apply to specific travel periods.</p>                                                                                                                                                                                                     |
| **Display**        | Button that applies the selected filters and refreshes the grid results.                                                                                                                                                                                                                                                                                            |
| **Clear**          | Resets the filter fields to their default state.                                                                                                                                                                                                                                                                                                                    |

#### **Rule Configuration Grid**

The grid displays all configured **Stay and Pay Cost Rules**.

Each row represents a rule defining when and how the Stay and Pay cost reduction applies.

| **Field**               | **Description**                                                                                                                                                                                                                                                                                                                     |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Stay Start / End**    | Defines the check-in (stay) period the rule applies to.                                                                                                                                                                                                                                                                             |
| **Booking Start / End** | Defines the window in which the booking must be made for the rule to be valid.                                                                                                                                                                                                                                                      |
| **Days of the Week**    | <p>Dropdown that restricts the rule to specific <strong>arrival days</strong>.</p><p>Examples include:</p><ul><li>Only weekend arrivals</li><li>Only weekday arrivals</li></ul><p>If <strong>Selected all</strong> is chosen, the rule applies to arrivals on any day of the week.</p>                                              |
| **ROOM TYPE**           | Defines which **room types** are eligible for the Stay and Pay rule. Selecting **Selected all** applies the rule to all configured room types.                                                                                                                                                                                      |
| **Period**              | <p>Defines the <strong>period number</strong> in which the rule applies.</p><p>Periods correspond to seasonal cost configurations within the hotel contract.</p>                                                                                                                                                                    |
| **Stay Days No**        | <p>Defines the <strong>number of nights the guest must stay</strong> for the rule to apply.</p><p>Example:</p><ul><li><strong>Stay Days No:</strong> 7</li></ul><p>The guest must stay <strong>7 nights</strong> to qualify.</p>                                                                                                    |
| **Pay Days No**         | <p>Defines the <strong>number of nights that will be charged</strong>.</p><p>Example:</p><ul><li><strong>Pay Days No:</strong> 6</li></ul><p>Although the guest stays <strong>7 nights</strong>, the cost will be calculated as <strong>6 nights</strong>.</p>                                                                      |
| **EB**                  | <p>Checkbox indicating whether the Stay and Pay rule can be <strong>combined with Early Booking rules</strong>.</p><p>When enabled, both promotions may apply together if their conditions are satisfied.</p><p>Early Booking rules are configured under:</p><p><strong>Room Costs → Early Booking Cost Discount Rules</strong></p> |
| **Contract**            | <p>Displays the <strong>contract identifier</strong> associated with the rule.</p><p>This column is helpful when multiple contracts exist for the same hotel.</p>                                                                                                                                                                   |
| **Trash Icon**          | <p>Icon used to <strong>remove the rule</strong> from the configuration.</p><p>Deleting a rule removes it from future cost calculations but does not modify historical bookings.</p>                                                                                                                                                |
| **Save**                | Commits all newly added or updated rules to the database/system.                                                                                                                                                                                                                                                                    |
| **Create**              | <p>Button used to <strong>create a new Stay and Pay Cost Rule</strong>.</p><p>Selecting this option adds a new row in the grid where rule parameters can be configured.</p>                                                                                                                                                         |

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

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

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
