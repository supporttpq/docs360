# Extra Beds Cost – Hotel Contract Configuration

### Overview

The **Extra Beds Cost** section within the “Edit Hotel Contract” module is used to define pricing rules for extra beds based on guest categories (e.g., infant, child), age, stay period, and room types. This helps ensure that the correct extra bed charges are applied during booking and invoicing processes.

### Purpose

This configuration allows pricing flexibility by setting up extra bed costs that vary based on:

* Age range of the guest
* Category (e.g., Infant, Child, Adult)
* Room types
* Specific time periods (contract periods)
* Cost type (per person/day, normal, percentage)

### Preconditions

Before configuring Extra Beds Cost, ensure that:

* The **hotel contract** is already created.
* The **Periods** are already defined within the contract.
* At least one **room type** is configured under the “Rooms” tab.
* Guest categories (Infant, Child, Adult) are defined if they differ from defaults.

### Field-by-Field Explanation

| Field              | Description                                                                                                           |
| ------------------ | --------------------------------------------------------------------------------------------------------------------- |
| **Category**       | Defines the guest type for which the extra bed cost applies (e.g., Infant, Child, Adult).                             |
| **Age – From/To**  | The age rank for which the Extra Bed Cost is applied. The age range must be unique in combination with the rooms.     |
| **Rank – From/To** | The rank of the guests using extra beds. From 1 to 1 is the first extra bed. From 1 to 2 is the first two extra beds. |
| **Per Pax/Day**    | If checked, the cost is applied per person per day. If unchecked, it may be applied per interval                      |
| **Normal**         | If checked, the value is a supplement (normal price). If unchecked, the value is a discount.                          |
| **% (Percentage)** | If checked, the cost will be applied as a percentage of the room price instead of a fixed amount.                     |
| **Room**           | Specifies the room type(s) to which this extra bed cost applies. Selecting “All rooms” applies it globally.           |
| **Period ID**      | Displays the period(s) from the contract to which the cost rule applies. Each row corresponds to a contract period.   |
| **Cost**           | The actual cost value in the selected currency (e.g., USD). Can vary per period.                                      |
