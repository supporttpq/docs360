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
