# Periods – Hotel Contract Configuration

### Purpose

The **Periods** tab is where you define the stay intervals (start/end dates) and configure the room pricing and availability rules that apply for each specific time frame. It is essential for implementing seasonal pricing and allocation changes.

***

### Screenshot

<figure><img src="../.gitbook/assets/image (410).png" alt=""><figcaption></figcaption></figure>

***

### Preconditions

* Room types must be defined in the **Rooms** tab.
* Board types (AI, BB, etc.) should be configured in advance.
* Ensure you are aware of any supplier guarantee requirements or minimum stay conditions.

***

### Instructions – Fields and Definitions

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

### Notes (for internal use)

#### Overview

The **Notes** field within Hotel Contract Periods allows company administrators to record internal comments contract period. These notes are visible only within the Tourpaq Office system and are **not shared with hotel suppliers** or external partners.

#### Purpose

The Notes feature is designed to:

* Provide internal context or reminders regarding specific contract periods.
* Help colleagues and administrators track changes and maintain consistency in contract management.

#### Field Explanation

* **Notes (Internal Use Only)** – A free-text field where the administrator can enter comments, clarifications, or reminders related to the hotel contract period.
  * **Visibility**: Notes are strictly internal.
  * **Format**: Free text, no character limit (though concise entries are recommended).

#### Instructions for Use

1. Go to **Hotel Contract → Periods**.
2. Locate the **Notes (Internal Use)** field.
3. Enter the required comments or reminders (e.g., _“Supplier agreed to flexible release rules during peak season”_).
4. Save the contract period. The note will now be stored internally and accessible to other administrators.
