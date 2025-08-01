# Extra Cost – Hotel Contract Configuration

### Overview

The **Extra Cost** section in the “Edit Hotel Contract” module allows the configuration of additional charges that are not directly included in the base room price—such as cleaning fees, resort fees, or optional services. These costs can be applied per person or per room, and they may vary by age and period.

### Purpose

This section ensures that all extra costs associated with a booking are transparently configured and properly applied during pricing and invoicing. It helps the system calculate total costs accurately and provides clarity to the customer.

### Preconditions

Before configuring Extra Costs, ensure the following:

* The **hotel contract** has already been created.
* At least one **Period** is defined in the contract.
* **Room types** are available under the “Rooms” tab.
* If age-based costs are required, the age brackets must be well understood and applicable.

### Field-by-Field Explanation

| Field                    | Description                                                                                                                           |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------- |
| **Type**                 | The type of extra cost to apply. Example: Final Cleaning, Resort Fee, etc. Selected from a dropdown list of predefined types.         |
| **Room**                 | Specifies the room types to which this cost applies. Selecting “All rooms” applies it globally across all room types.                 |
| **From / To (Age)**      | The age range (in years) for which the extra cost is applicable.                                                                      |
| **Period ID**            | Represents a predefined contract period. Each period has its own pricing rules.                                                       |
| **Extra Cost/Pax/Night** | Cost applied **per person per night** within the selected age range and period.                                                       |
| **Extra Cost/Room**      | Cost applied **per room**, regardless of the number of occupants. This is often used for one-time or fixed costs like final cleaning. |
