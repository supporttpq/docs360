---
description: Configure cost reductions based on stay length, such as Stay 7 Pay 6.
---

# Stay and Pay Cost Rules

### Introduction

The **Stay and Pay Cost Rules** page is part of the **Hotel → Room Costs** configuration in **Tourpaq Office**. It allows the definition of promotions where a guest stays a certain number of nights but pays for fewer nights.

This functionality supports common hotel promotions such as **“Stay 7 nights, Pay 6”** or **“Stay 14 nights, Pay 12.”**

Stay and Pay Cost Rules work together with several other Tourpaq components:

* **Room Cost Rules** (base hotel costs)
* **Early Booking Cost Discount Rules**
* **Price Lists**
* **Profit Margin rules**
* **Hotel Contracts**

These components together determine the **final hotel cost and selling price** used in bookings and price lists.

### **Overview**

**Stay and Pay Cost Rules** define cost reductions based on the length of stay.\
When a booking satisfies the configured conditions, the system recalculates the hotel cost so that only the configured **Pay Days No** are charged even though the guest stays longer.

Example:

* **Stay Days No:** 7
* **Pay Days No:** 6

The booking stays for **7 nights**, but the hotel cost is calculated as **6 nights**.

The cost reduction occurs at the **hotel cost level**. If the selling price is calculated using **Profit Margin rules**, the reduced cost may also produce a **lower selling price toward the guest**.

### **Purpose**

Stay and Pay Cost Rules are used to:

* Encourage **longer stays**
* Support hotel promotions defined in contracts
* Automate cost recalculation based on stay length
* Maintain consistent pricing across bookings and price lists

This functionality allows promotional hotel deals to be implemented directly within the Tourpaq cost calculation system.

### **System Setup**

The following conditions must exist before Stay and Pay Cost Rules can function correctly:

1. A **Hotel** must be configured.
2. **Room Cost Rules** must exist for the hotel.
3. **Room Types** must be configured in the contract.

#### System Setup Behavior for Early Booking and Stay and Pay for Discount

Path to system setting: **System Setup → General → Settings**

Setting name: **Use Early Booking and Stay and Pay for Discount**

**Purpose of the setting:**

The setting **Use Early Booking and Stay and Pay for Discount** uses discounted cost that also takes into account Room Discount Early Booking and Stay an Pay for calculating Discount via Profit Margin

<figure><img src="../../../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (713).png" alt=""><figcaption></figcaption></figure>

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

### Related pages

* [Room cost](./)
* [Early Booking Cost Discount Rules](early-booking-cost-discount-rules/)
