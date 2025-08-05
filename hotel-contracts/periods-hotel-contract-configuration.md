# Periods – Hotel Contract Configuration

#### Purpose

The **Periods** tab is where you define the stay intervals (start/end dates) and configure the room pricing and availability rules that apply for each specific time frame. It is essential for implementing seasonal pricing and allocation changes.

***

#### Screenshot

<figure><img src="../.gitbook/assets/image (288).png" alt=""><figcaption></figcaption></figure>

***

#### Preconditions

* Room types must be defined in the **Rooms** tab.
* Board types (AI, BB, etc.) should be configured in advance.
* Ensure you are aware of any supplier guarantee requirements or minimum stay conditions.

***

#### Instructions – Fields and Definitions

| Field                          | Description                                                                               |
| ------------------------------ | ----------------------------------------------------------------------------------------- |
| **Start Date / End Date**      | Defines the contract validity period. Multiple periods can be added for seasonal pricing. |
| **R**                          | Realese                                                                                   |
| **CD**                         | Checkbox to activate cut down allotment                                                   |
| ➕ **Add Icon**                 | Adds a new interval for the selected period.                                              |
| 🗑️ **Trash Icon (on period)** | Deletes the entire period.                                                                |
| 🗑️ **Trash Icon (on row)**    | Deletes a specific interval.                                                              |
| **Room Code**                  | Pulled from the **Rooms** tab; defines which room the row refers to.                      |
| **Board**                      | Select the applicable board (meal plan) for this room/period.                             |
| **Allotments**                 | Number of rooms available for sale.                                                       |
| **Guarantee**                  | Number of guaranteed rooms the agency commits to sell.                                    |
| **Secured**                    | Number of secured rooms.                                                                  |
| **Min Stay**                   | Minimum number of nights required.                                                        |
| **Cost**                       | Cost price for the room under the specified board.                                        |
| **Single Cost**                | The cost for the room with only a single pax, as a supplement to the room cost            |
| **SP%**                        | Indicates whether the cost is percentage on top of the room cost                          |
| **Stay Type**                  | Defines if the cost is **Per Pax**, **Per Room**, or **Per Pax Per Night**.               |
| **Tr. Length**                 | Transport length reference (e.g., 5d = 5 days).                                           |
