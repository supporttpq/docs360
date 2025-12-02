# Double as Single – Hotel Contract Configuration

#### Purpose

The **Double as Single** tab is used to define additional costs (or discounts) when a double room is occupied by a single person. This is especially relevant for pricing logic and ensures fair cost allocation when occupancy is reduced.

***

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

#### How It Works

**Top Section – Cost Percentage per Period**

You can configure percentage adjustments for each defined **contract period**.

| Field               | Description                                                                                                                                                                                                                            |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Period ID**       | Corresponds to the contract period (from the _Periods_ tab).                                                                                                                                                                           |
| **Cost (%)**        | Defines how much is added (or discounted) when the room is used as a single.                                                                                                                                                           |
|  **Per Pax**        | Set the cost per pax                                                                                                                                                                                                                   |
| %                   | Unchecked: The cost is added on top of the cost for the parent room;                                                                                  Checked: The cost is the percentage added on top of the cost for the parent room |
| **Trash icon (🗑)** | Deletes the row.                                                                                                                                                                                                                       |

***

**Bottom Section – Room Configuration**

This section lists all the **room types** and their parameters to manage base and derived rooms for occupancy and cost logic.

| Field                           | Description                                                                 |
| ------------------------------- | --------------------------------------------------------------------------- |
| **Room Code**                   | Internal system code for the room type.                                     |
| **List Text Name**              | Display name used for dropdowns or customer-facing elements.                |
| **Name**                        | Room name or description.                                                   |
| **Minimum / Maximum**           | Allowed occupancy limits for the room.                                      |
| **Max Extra / Max Extra Child** | Limits for additional adult or child guests.                                |
| **Room Above**                  | Parent room                                                                 |
| **Parent Room**                 | Defines a fallback or inheritance relationship.                             |
| **Delete Icon (🗑)**            | Removes the room entry from the list.                                       |
| Period ID                       | Corresponds to the contract period (from the _Periods_ tab).                |
| Allotments                      | Number of rooms available for sale.                                         |
| Guarantee                       | Number of guaranteed rooms the agency commits to sell.                      |
| Stay Type                       | Defines if the cost is **Per Pax**, **Per Room**, or **Per Pax Per Night**. |
| Tr. Length                      | Transport length                                                            |
| Cost                            | Amount charged to applicable guests.                                        |
