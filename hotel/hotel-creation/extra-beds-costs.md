# Extra Beds Costs

### Overview

Extra Bed Costs are hotel cost adjustments used when passengers occupy extra beds.\
They are typically used as discounts from the hotel to the agency.\
You can also treat the value as a normal price, depending on your checkbox settings.

### Purpose

Use this to manage hotel-provided extra bed costs in a consistent way.\
It reduces manual corrections in bookings.\
It also supports multiple extra beds in the same room.

### Conditions of Application

Extra Bed Costs are applied only when:

* Extra beds are used by passengers.
* Room cost prices are set **per passenger**.

If these conditions are not met, the extra bed cost value will remain **0**.

<figure><img src="../../.gitbook/assets/image (63) (1).png" alt=""><figcaption></figcaption></figure>

### Field Explanations

* **Age** – Define the age of the passenger who will use the extra bed.
* **Arrival Start / End Date** – Set the date range for valid guest arrivals.
* **Booking Start / End Date** – Set the booking period during which the discount is applicable.
* **Cost Columns**:
  * **Cost Price** – Value applied for the first extra bed.
  * **Second / Third / Fourth Price** – Values applied for additional extra beds in the same room.
* **PD (Per Day)** – If checked, the value is applied **per day** instead of per interval.
* **NP (Normal Price)** – If checked, the value is treated as a **price** (supplement), not a discount.
* **% (Percent)** – If checked, the value is treated as a **percentage**.
* **Room Type** – Select the room types to which the rule applies.
* **Period** – Define the applicable period for the extra bed discount.
* **EBD (Extra Bed Discount)** – Links the entry to the [Discount Extra Beds](discount-extra-beds.md) configuration.

### Instructions of Use

1. Open the **Extra Bed Costs** configuration panel.
2. Define the **age group** eligible for extra bed usage.
3. Set the **arrival** and **booking date ranges**.
4. Enter the **cost values** in the respective columns:
   * Use the **Cost Price** column for the first extra bed.
   * Use the additional columns for second, third, or fourth extra beds if needed.
5. Configure discount behavior using the checkboxes:
   * Enable **PD** for per-day application.
   * Enable **NP** if treating the value as a price.
   * Enable **%** if defining the value as a percentage.
6. Assign the rule to specific **room types** and **periods**.
7. Link to an **Extra Bed Discount (EBD)** if required.
8. Save the configuration to activate the discount logic.
