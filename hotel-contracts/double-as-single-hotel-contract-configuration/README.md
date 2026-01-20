# Double as Single – Hotel Contract Configuration

### Overview

The **Double as Single** tab is used to define additional costs (or discounts) when a double room is occupied by a single person. This is especially relevant for pricing logic and ensures fair cost allocation when occupancy is reduced.

### Screenshot

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Preconditions

Before you start:

* The hotel contract exists and is open for editing.
* Room types exist in [Rooms – Hotel Contract Configuration](../rooms-hotel-contract-configuration.md).
* Period IDs exist in [Periods – Hotel Contract Configuration](../periods-hotel-contract-configuration.md).

***

### Cost adjustment per period (top section)

Add one row per **Period ID**.

The system applies the row when the room is booked as single occupancy.

| Field          | Description                                                                             |
| -------------- | --------------------------------------------------------------------------------------- |
| **Period ID**  | Period the adjustment belongs to. It maps to the **Periods** tab.                       |
| **Cost**       | Adjustment value. Use positive for surcharge. Use negative for discount.                |
| **Per Pax**    | Applies the adjustment per passenger instead of per room.                               |
| **%**          | When enabled, **Cost** is treated as a percentage. When disabled, it is a fixed amount. |
| 🗑️ **Delete** | Deletes the row.                                                                        |

#### How it works

1. The room price is calculated from the parent room setup.
2. The Double as Single adjustment is applied for the matching **Period ID**.
3. **Per Pax** multiplies the adjustment by passenger count.

{% hint style="info" %}
If nothing changes in pricing, check the **Period ID** first.
{% endhint %}

***

### Room configuration (bottom section)

This list shows the room codes available in the contract.

It also shows period-based allotment and cost fields.

| Field                           | Description                                            |
| ------------------------------- | ------------------------------------------------------ |
| **Room Code**                   | System code for the room type.                         |
| **List Text Name**              | User-facing label in dropdowns and lists.              |
| **Name**                        | Internal name. Often used in supplier communication.   |
| **Minimum / Maximum**           | Allowed occupancy limits for the room.                 |
| **Max Extra / Max Extra Child** | Limits for extra adults and children.                  |
| **Room Above**                  | Higher-level grouping room (when used).                |
| **Parent Room**                 | Inheritance link to the base room type.                |
| **Period ID**                   | Period row reference, from the **Periods** tab.        |
| **Allotments**                  | Rooms available for sale in the period.                |
| **Guarantee**                   | Guaranteed rooms for the period.                       |
| **Stay Type**                   | Pricing basis (for example **Per Pax**, **Per Room**). |
| **Tr. Length**                  | Transport length (when used).                          |
| **Cost**                        | Base cost for the room and period.                     |
| 🗑️ **Delete**                  | Removes the room entry from the contract.              |

***

### Related workflows

* [Hotel contract - General](../hotel-contract-general.md)
* [Rooms – Hotel Contract Configuration](../rooms-hotel-contract-configuration.md)
* [Periods – Hotel Contract Configuration](../periods-hotel-contract-configuration.md)
* [Board Basis Inheritance Rule](board-basis-inheritance-rule.md)

***

### FAQ

**What is “Double as Single” used for?**\
It prices a double room when only one guest stays.\
It prevents undercharging compared to double occupancy.

**Can I create a discount instead of a surcharge?**\
Yes. Enter a negative **Cost** value.\
Example: `-10` or `-15%`.

**What does the “%” checkbox change?**\
It changes how **Cost** is interpreted.\
Enabled means percentage. Disabled means fixed amount.

**When should I enable “Per Pax”?**\
Enable it when the adjustment is per person.\
Leave it off for per-room adjustments.

**Why does my Double as Single rule not apply?**\
Most cases are a wrong **Period ID**.\
Also check the booking dates match that period.

**Do I need to configure rooms again here?**\
No. Room codes come from the contract room setup.\
This tab only adds single-occupancy pricing logic.
