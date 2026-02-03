# Extra Beds Costs

### Overview

Extra bed costs adjust hotel costs when passengers use extra beds. Hotels often provide them as a discount to your agency. You can also treat the value as a normal price. This depends on your checkbox settings.

### Purpose

Use this to manage hotel-provided extra bed costs consistently. This reduces manual corrections in bookings. It also supports multiple extra beds in the same room.

### Conditions of Application

Extra bed costs apply only when:

* Extra beds are used by passengers.
* Cost prices are calculated **per passenger**.

If these conditions are not met, the extra bed cost value stays **0**.

<figure><img src="../../.gitbook/assets/image (63) (1).png" alt=""><figcaption></figcaption></figure>

### Field Explanations

* **Age** – Define the passenger age for the extra bed.
* **Arrival Start / End Date** – Set the allowed guest arrival date range.
* **Booking Start / End Date** – Set the booking date range for the rule.
* **Cost columns**
  * **Cost Price** – Value for the first extra bed.
  * **Second / Third / Fourth Price** – Values for additional extra beds in the same room.
* **PD (Per Day)** – Applies the value **per day**, not per interval.
* **NP (Normal Price)** – Treats the value as a **price** (supplement), not a discount.
* **% (Percent)** – Treats the value as a **percentage** (example: `10` = 10%).
* **Room Type** – Select the room types the rule applies to.
* **Period** – Define the stay period where the rule is valid.
* **EBD (Extra Bed Discount)** – Links the entry to the [Discount Extra Beds](discount-extra-beds.md) configuration.

### How to use

1. Open the **Extra Bed Costs** configuration panel.
2. Define the eligible **age**.
3. Set the **arrival** and **booking date ranges**.
4. Enter the **values** in the cost columns:
   * Use **Cost Price** for the first extra bed.
   * Use the other columns for extra beds 2–4.
5. Configure how the value is interpreted:
   * Enable **PD** to apply the value per day.
   * Enable **NP** to treat it as a price.
   * Enable **%** to use a percentage.
6. Assign the rule to specific **room types** and **periods**.
7. Link to an **Extra Bed Discount (EBD)** if required.
8. Save the configuration to activate the pricing logic.

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

When enabled, the value applies **per day** of the stay. When disabled, it applies per configured interval.

#### What does **NP (Normal Price)** mean in practice?

When enabled, the value is treated as a **price/supplement**. When disabled, it is treated as a **discount**.

#### What does **% (Percent)** do?

When enabled, the value is interpreted as a percentage. Example: `10` means **10%**.

#### How do Arrival/Booking dates and Period work together?

All of them must match for the rule to apply:

* Guest arrival must be inside **Arrival Start/End Date**.
* Booking date must be inside **Booking Start/End Date**.
* Stay must match the configured **Period**.

#### Do I have to link an **EBD (Extra Bed Discount)**?

Not always. Use it when you need this entry tied to [Discount Extra Beds](discount-extra-beds.md).
