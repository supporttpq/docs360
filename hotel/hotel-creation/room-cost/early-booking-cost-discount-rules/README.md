---
description: >-
  Configure hotel cost discounts for bookings made within a defined booking
  window.
---

# Early Booking Cost Discount Rules

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

<figure><img src="../../../../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../../../.gitbook/assets/image (423).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../../../.gitbook/assets/image (425).png" alt=""><figcaption></figcaption></figure>

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
| Days of the Week         | Restricts the rule to arrivals on selected weekdays. This has to coincide with the arrival date of the booking. If no value is selected, the rule applies to **all days**.![](<../../../../.gitbook/assets/image (569).png>)                                                                                |
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

<figure><img src="../../../../.gitbook/assets/image (316).png" alt=""><figcaption></figcaption></figure>

This rule can combine with **Stay and Pay cost rules** if **S\&P** is checked.

Filters used:

* Stay Date Start and End
* Booking Start and End date
* Room
* Days no before arrival

Other fields are used for invoices and are explained elsewhere.

Early Booking Discount with Board Type as a filter

<figure><img src="../../../../.gitbook/assets/image (317).png" alt=""><figcaption></figcaption></figure>

The Early Booking Cost Discount Rules include a **Board** field. It contains board types defined for the company.

When you save a booking, cost rules are filtered by passenger board type.

Board type comes from the product (Basic setup → Board Supplements). Passengers pick board type by selecting a matching product.

If a board filter is used, all passengers in the room must match it. Mixed board types in the same room will not match board-filtered rules.

If a rule has no board filter, it applies only to passengers without board type.

### Related pages

* [Room cost](../)
* [Early Booking Cost Discount Rule – Deletion Behavior](early-booking-cost-discount-rule-deletion-behavior.md)
