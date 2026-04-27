# Extra Beds Costs

### Introduction

The **Extra Beds Costs** page is used to define pricing rules for additional beds in hotel rooms. These rules determine how extra beds are priced based on age intervals, travel dates, booking periods, and discount structures.

This functionality is closely connected to:

* Room Costs
* Discount Extra Beds
* Allotment
* Booking pricing logic

### Overview

The page allows configuration of **rule-based pricing for extra beds**, ensuring correct pricing during booking creation and calculation.

### Purpose

* Define pricing rules for extra beds
* Support age-based pricing
* Control pricing by travel and booking periods
* Enable complex discount structures

### Requirements

* Hotel must be configured with Room Types
* Contract Periods must exist
* Pricing logic must be enabled for extra beds
* User must have access to the hotel contract configuration

### Navigation

Hotel → Select Hotel → **Extra Beds Costs**

### Conditions of Application

Extra bed costs apply only when:

* Passengers use extra beds.
* Cost prices are calculated **per passenger**.

If these conditions are not met, the extra bed cost value stays **0**.

### Screenshot

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Interface Overview

The interface consists of:

1. Filter section (top)
2. Configuration grid (rules table)
3. Action buttons

### Filter Section

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Field Description – Filters

<table><thead><tr><th width="154.5555419921875"></th><th width="272.2222900390625"></th><th></th></tr></thead><tbody><tr><td>Room Type</td><td>Dropdown used to filter rules by room type</td><td><ul><li>Optional</li><li>Linked to hotel room configuration</li></ul></td></tr><tr><td>Period</td><td>Dropdown used to filter rules by contract period.</td><td><ul><li>Optional</li><li>Related to seasonal pricing</li></ul></td></tr><tr><td>Booking Date</td><td>Date filter for booking creation period.</td><td><ul><li>Optional</li><li>Affects rule visibility</li></ul></td></tr><tr><td>Departure Date</td><td>Date filter for travel period.</td><td><ul><li>Optional</li><li>Used to validate applicable rules</li></ul></td></tr><tr><td>Display</td><td>Applies selected filters and loads results</td><td></td></tr><tr><td>Clear</td><td>Resets all filters</td><td></td></tr></tbody></table>

### Configuration Grid

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Field Explanations

* **From/To Age** – Define the passenger age for the extra bed.
* **Arrival Start / End Date** – Set the allowed guest arrival date range.
* **Booking Start / End Date** – Set the booking date range for the rule.
* **Discount 1 -** The discount for the first extra bed. If C is checked, then it is the fixed cost of the extra bed.
  * **Second / Third / Fourth Discount** – The discount for the second/third/fourth extra bed. If C is checked, then it is the fixed cost of the extra bed.
* **PD (Per Pax/Day)** – If checked, the value is applied per day. If unchecked, the value is applied per interval.
* **C -** Unchecked: The DISCOUNT is a discount of the room cost, and the extra bed cost is the room cost reduced by the DISCOUNT.\
  Checked: The DISCOUNT is the fixed cost of the extra bed.
* **% (Percent)** – Treats the value as a **percentage** (example: `10` = 10%).
  * If checked, the DISCOUNT is a percentage.
  * If unchecked, the DISCOUNT is an amount.
* **Room Type** – Select the room types the rule applies to.
* **Period** – Define the stay period where the rule is valid.
* **EBD (Extra Bed Discount)** – Links the entry to the [Discount Extra Beds](discount-extra-beds.md) configuration.

{% hint style="info" %}
The cost configuration PD, NP, % are applied individually for every cost.
{% endhint %}

### How to use

1. Open the **Extra Bed Costs** configuration panel.
2. Define the eligible **age**.
3. Set the **arrival** and **booking date ranges**.
4. Enter the **values** in the cost columns:
   * Use **Discount 1** for the first extra bed.
   * Use the other columns for extra beds 2–4.
5. Configure how the value is interpreted:
   * Enable **PD** to apply the value per day.
   * Enable **C** to treat it as a price.
   * Enable **%** to use a percentage.
6. Assign the rule to specific **room types** and **periods**.
7. Link to an **Extra Bed Discount (EBD)** if required.
8. Save the configuration to activate the pricing logic.

### Examples

#### Example 1 – Child Pricing

* FROM AGE: 0
* TO AGE: 2
* ARRIVAL: 01-07-2026 → 31-10-2026
* BOOKING: 01-01-2026 → 01-07-2026
* DISCOUNT: 1000 EUR

**Result:**\
Extra bed receives fixed discount during booking

***

#### Example 2 – Percentage Discount

* DISCOUNT: 20
* % enabled

**Result:**\
20% discount is applied to the extra bed price

### Discount Extra Beds – Flexibility Improvement

#### Context

Path: **Hotel > Hotels > Extra Bed Cost**

When a rule is created under **Extra Bed Cost** and the **EBD (Link to Extra Beds Discount)** option is enabled:

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* A corresponding rule is automatically generated under **Discount Extra Beds**

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* The rule is currently **locked**
* The **"H" (Hidden)** flag is automatically enabled and cannot be changed

This behavior prevents users from controlling the visibility of the generated discount.

#### Rule Generation (EBD Enabled)

When a rule is generated via EBD:

* The system:
  * Copies the rule into **Discount Extra Beds**
  * Sets **H = checked (default)**
* The generated rule remains **linked to the source rule**

### Functional Rules

#### 1. Default Behavior

* On rule generation:
  * **H = checked**
  * Rule is locked except for "H"

#### 2. User Override

* User can modify only: **"H" (Hidden flag)**
* No other fields can be edited

#### 3. Persistence

* When the user modifies "H":
  * The value will be **saved correctly**
  * The value **persists across sessions and updates**

#### 4. Sync Behavior with Source Rule

When the corresponding **Extra Bed Cost** rule is modified:

* The linked **Discount Extra Beds** rule will be updated according to existing EBD logic (price, dates, etc.)
* **Critical constraint:**
  * The **"H" value will NOT be overwritten**
  * The system preserves the user-defined visibility

### Acceptance Criteria

* When a rule is generated via EBD all fields are **read-only except "H"**
* The **"H" column is editable U**ser can toggle the checkbox
* When the user modifies "H" the value is saved correctly
* When the corresponding Extra Bed Cost rule is modified:
  * The Discount Extra Beds rule is updated as per logic
  * The **"H" value remains unchanged**
* No regression in:
  * EBD rule generation logic
  * Existing Discount Extra Beds behavior

### FAQ

#### Why is the extra bed cost always `0`?

This is expected if either condition is not met:

* No passengers are using an extra bed.
* Room costs are not calculated **per passenger**.

#### How are the second/third/fourth prices used?

They are used when multiple extra beds are placed in the same room.

* Extra bed 1 uses **Cost Price**.
* Extra beds 2–4 use the additional columns.

#### What does **PD (Per Day)** do?

When enabled, the value applies **per day** of the stay. When disabled, it applies per the configured interval.

#### What does **C** mean in practice?

When enabled, the value is treated as a **price/supplement**. When disabled, it is treated as a **discount**.

#### What does **% (Percent)** do?

When enabled, the value is interpreted as a percentage. Example: `10` means **10%**.

#### How do Arrival/Booking dates and Period work together?

All of them must match for the rule to apply:

* Guest arrival must be inside **Arrival Start/End Date**.
* Booking date must be inside **Booking Start/End Date**.
* Stay must match the configured **Period**.

#### What happens if Extra Bed Cost is linked to Extra Bed Discount?

When a rule is created under **Extra Bed Cost** and the **EBD (Link to Extra Beds Discount)** option is enabled:

* A corresponding rule is automatically generated under **Discount Extra Beds**
* The rule is currently **locked**
* The **"H" (Hidden)** flag is automatically enabled and cannot be changed

This behavior prevents users from controlling visibility of the generated discount.

### Related pages

* [Discount Extra Beds](discount-extra-beds.md) — Configure the customer-price discount side that can be linked through **EBD**.
* [Room cost](room-cost/) — Review the base hotel cost logic that extra bed costs build on.
* [Extra Beds Cost – Hotel Contract Configuration](../../hotel-contracts/extra-beds-cost-hotel-contract-configuration.md) — See the contract-level setup page for this same configuration area.
* [Room Cost Rule Interactions and FAQ](room-cost/room-cost-rule-interactions-and-faq.md) — Check how room cost rules interact with other hotel cost rules.
