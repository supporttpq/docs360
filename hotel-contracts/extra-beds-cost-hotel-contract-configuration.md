# Extra Beds Cost – Hotel Contract Configuration

### Overview

The **Extra Beds Cost** section within the “Edit Hotel Contract” module is used to define pricing rules for extra beds based on guest categories (e.g., infant, child), age, stay period, and room types. This helps ensure that the correct extra bed charges are applied during booking and invoicing processes.

***

### Purpose

Use this tab when extra bed pricing depends on:

* **Who**: category (Infant/Child/Adult) and age range.
* **Where**: one room type or all rooms.
* **When**: one or more contract periods.
* **How it’s calculated**: fixed amount vs percentage, and supplement vs discount.

***

### Preconditions

Before configuring Extra Beds Cost, ensure that:

* The **hotel contract** is already created.
* The **Periods** are already defined within the contract.
* At least one **room type** is configured under the “Rooms” tab.
* Guest categories (Infant, Child, Adult) are defined if they differ from defaults.

***

### Fields

| Field              | Description                                                                                                         |
| ------------------ | ------------------------------------------------------------------------------------------------------------------- |
| **Category**       | Defines the guest type for which the extra bed cost applies (e.g., Infant, Child, Adult).                           |
| **Age – From/To**  | Age range where this rule applies. Keep ranges unique for the same room selection to avoid conflicts.               |
| **Rank – From/To** | Which extra bed(s) this rule covers. `1–1` = first extra bed. `1–2` = first and second extra beds.                  |
| **Per Pax/Day**    | If checked, applies per person per day. If unchecked, applies once per interval/period row.                         |
| **Normal**         | If checked, the value is a supplement (normal price). If unchecked, the value is a discount.                        |
| **% (Percentage)** | If checked, the cost will be applied as a percentage of the room price instead of a fixed amount.                   |
| **Room**           | Specifies the room type(s) to which this extra bed cost applies. Selecting “All rooms” applies it globally.         |
| **Period ID**      | Displays the period(s) from the contract to which the cost rule applies. Each row corresponds to a contract period. |
| **Cost**           | The actual cost value in the selected currency (e.g., USD). Can vary per period.                                    |

***

### How it works

{% stepper %}
{% step %}
### Create the rule header

Pick **Category**, set **Age – From/To**, and set **Rank – From/To**.
{% endstep %}

{% step %}
### Choose calculation type

Decide if the cost is **Per Pax/Day**.

Choose **Normal** (supplement) or discount.

Enable **% (Percentage)** if it should follow the room price.
{% endstep %}

{% step %}
### Scope it to rooms

Select a specific **Room**, or choose **All rooms**.
{% endstep %}

{% step %}
### Enter costs per period

Fill the **Cost** column for each **Period ID** row you want active.
{% endstep %}
{% endstepper %}

***

### Tips

{% hint style="info" %}
Avoid overlapping age ranges for the same **Category** and **Room** selection. Overlaps can create unpredictable pricing.
{% endhint %}

* Use **All rooms** only when the supplier uses one extra-bed policy.
* Prefer **% (Percentage)** when extra beds should scale with seasonal prices.
* Use `Rank 2–2` when the second extra bed has a different price than the first.

***

### Related workflows

* [Hotel contract - General](hotel-contract-general.md)
* [Rooms – Hotel Contract Configuration](rooms-hotel-contract-configuration.md)
* [Periods – Hotel Contract Configuration](periods-hotel-contract-configuration.md)

***

### FAQ

**What does “Rank – From/To” mean?**\
It targets the extra bed position.\
`1–1` prices the first extra bed only.\
`1–2` prices the first and second extra beds.

**How do I price the second extra bed differently?**\
Create a separate rule with `Rank 2–2`.

**Should I use fixed amounts or “% (Percentage)”?**\
Use fixed amounts for stable fees.\
Use percentage when the price should follow room cost.

**Why do I see multiple rows under Period ID?**\
Each row maps to one contract period.\
It lets you change extra bed cost by season.

**What happens if age ranges overlap?**\
Rules can conflict.\
Keep ranges unique per Category + Room scope.
