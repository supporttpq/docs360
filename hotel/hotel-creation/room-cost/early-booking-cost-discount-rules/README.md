---
description: >-
  Configure hotel cost discounts for bookings made within a defined booking
  window.
---

# Early Booking Cost Discount Rules

### Introduction

The **Early Booking Cost Discount Rules** page is part of the **Hotel Contract → Room Costs** configuration in **Tourpaq Office**. It defines rules that reduce the **hotel cost** when a booking is made sufficiently in advance.

These rules influence how hotel costs are calculated during the booking process and may also affect the final selling price depending on the pricing configuration used in Tourpaq.

### **Overview**

The **Early Booking Cost Discount Rules** page allows the creation of rules that reduce hotel costs when bookings are made within a defined **advance booking window**.

The rule applies when the following conditions are met:

* The **stay period** matches the configured dates.
* The **booking date** falls within the allowed booking window.
* The rule conditions such as **room type**, **board**, **days of week**, and **passenger age** match the booking details.

The discount is applied **to the hotel cost**, not directly to the selling price. However, because selling prices may be calculated from hotel costs (for example through **Profit Margin rules**), the Early Booking discount can indirectly influence the final price presented to the guest.

### **Purpose**

Early Booking Cost Discount Rules provide a structured method for:

* Offering **lower hotel costs for early bookings**
* Supporting **seasonal sales strategies**
* Adjusting costs depending on **room type, board type, or booking period**
* Maintaining consistent pricing behavior across contracts and price lists

This functionality is commonly used for promotions where bookings made before a defined deadline receive discounted hotel costs.

### **System Setup**&#x20;

System Setup → General → Settings -> Use Early Booking and Stay and Pay for Discount

The setting **Use Early Booking and Stay and Pay for Discount** uses discounted cost that also takes into account Room Discount Early Booking and Stay an Pay for calculating Discount via Profit Margin

EBD rules always affect the **hotel cost** when their conditions are met.

The setting only determines **how the discount is reflected in the selling price and how it is displayed to the guest**.



<figure><img src="../../../../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure>

#### Behavior when the Setting is Enabled

When **Use Early Booking and Stay and Pay for Discount** is enabled, the system explicitly represents the Early Booking Discount in the pricing structure.

The system performs the following actions:

* Creates a **discounted selling price** in the **Price List** for the applicable period.
* Generates a **separate Early Booking Discount line** in the booking calculation.
* Displays the **EBD discount line in the e-ticket**, making the discount clearly visible to the guest.

As a result:

* The selling price reflects the **discounted value**.
* The booking shows a **transparent breakdown** of the discount granted.
* Guests can clearly see that the reduced price is due to an **Early Booking promotion**.

Example system behavior:

Base Price → Early Booking Discount → Final Guest Price

This configuration is commonly used when the agency wants the Early Booking promotion to be **clearly visible in guest-facing documents**.

<figure><img src="../../../../.gitbook/assets/image (716).png" alt=""><figcaption></figcaption></figure>

#### Behavior when the Setting is Disabled

When **Use Early Booking and Stay and Pay for Discount** is disabled, Early Booking Cost Discount Rules still apply to the **hotel cost**.

The system behaves as follows:

* The **hotel cost is reduced** during the Early Booking period.
* If **Profit Margin rules** calculate the selling price based on cost, the **guest selling price becomes lower** because the underlying cost is reduced.
* However, the system **does not create a visible Early Booking discount line**.

As a result:

* Guests still receive the **benefit of the lower price**.
* The discount is **not explicitly displayed** in the booking or e-ticket.

Example system behavior:

Reduced Cost → Profit Margin Calculation → Lower Final Guest Price

In this configuration, the Early Booking promotion is **embedded in the calculated price**, rather than displayed as a separate discount.

{% hint style="warning" %}
Changes to Early Booking Cost Discount Rules may require recalculation before they appear in the price list.

Recalculation can be triggered by:

* Updating the **hotel cost**
* Updating the **Profit Margin rule**
* Saving or recalculating the **Price List**

The **Profit Margin service** processes price updates asynchronously.\
Price list updates may take **up to 30 minutes**, depending on the number of tasks currently being processed by the service.,
{% endhint %}

### Practical Example

Two Tourpaq environments may behave differently depending on the setting:

**Environment with the setting enabled:**

* Discounted price created in the **Price List**
* **EBD discount line visible** in booking and e-ticket

**Environment with the setting disabled:**

* Hotel cost still reduced during the EBD period
* Selling price becomes lower through **Profit Margin calculation**
* **No visible discount line** shown to the guest

### Field Explanation

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
