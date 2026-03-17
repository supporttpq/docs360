# Room cost

### Introduction

The **Room Cost Rules** page is located in **Hotel Contract → Room Costs** in **Tourpaq Office**. This functionality defines the **base hotel cost structure** used during booking cost calculation.

Room Cost Rules are a central component of the Tourpaq pricing architecture. They determine the base hotel cost before other adjustments such as:

* **Early Booking Cost Discount Rules**
* **Stay and Pay Cost Rules**
* **Hotel Extra Cost Rules**
* **Profit Margin rules**
* **Price List calculations**

Because many Tourpaq pricing mechanisms depend on the base hotel cost, Room Cost Rules play an important role in maintaining consistent cost calculations and reliable financial reporting across bookings.

### Overview

**Room Cost Rules** define the base hotel cost conditions per hotel contract. These rules determine how the cost of a room is calculated for bookings depending on specific rule conditions.

Each rule can define:

* The **hotel** to which the cost applies
* The **stay period** for which the cost is valid
* The **booking period** during which the rule applies
* The **room type** affected by the rule
* Whether the cost is applied **per passenger** or **per room**

During booking creation or recalculation, Tourpaq evaluates the configured Room Cost Rules and determines the correct cost based on the booking details.

### Purpose

The purpose of Room Cost Rules is to ensure that **hotel costs are calculated consistently across all bookings**.

These rules support:

* Accurate **hotel cost allocation**
* Reliable **profit margin calculations**
* Consistent pricing across **contracts and price lists**
* Correct financial reporting for hotel bookings

Because other pricing mechanisms operate on top of the base hotel cost, Room Cost Rules act as the **foundation of the hotel pricing structure** in Tourpaq.

### How Room Cost Rules Work

Room Cost Rules determine the base hotel cost using rule conditions.

A rule can target:

* A **single hotel contract**
* A **departure (stay) date range**
* A **booking date range**
* A **specific room type**
* **All room types** within the contract

Costs can be calculated in two ways:

#### - Per passenger

The cost is applied **to each passenger in the room**.

Example:

Cost per passenger: 100\
Passengers: 2

Total room cost: 200

#### - Per room

The cost is applied **once per room** regardless of the number of occupants.

Tourpaq internally distributes the cost across passengers for calculation and reporting purposes.

### Testing a Room Cost Rule

Room Cost Rules can be verified using a booking test.

Recommended procedure:

1. Create a **booking** using the relevant hotel and room type.
2. Open the **Profit tab** in the booking.
3. Review the **hotel cost and profit values**.
4. Use the **information icon** to view the cost breakdown.

Some values may update after the **Total Cost Service** recalculates the booking.

The recalculation service runs asynchronously, meaning that cost updates may not appear immediately after modifying a rule.

#### Important Notes

Certain rule interactions may influence the final calculated cost.

If the calculated cost for a particular day becomes **0**, additional discounts cannot reduce the value below zero.

Example:

A **Stay 7, Pay 5** rule results in zero cost for two nights.\
If an **Early Booking Discount** or other discount is applied to those nights, the cost remains **0** and will not become negative.

This behavior prevents invalid negative hotel cost values.

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
