# Early Booking Discount – Hotel Contract Configuration

### Overview

The **Early Booking Discount** section in the “Hotel Contract” module allows the hotel to reward customers who book early by offering a fixed or percentage-based discount. It helps boost early occupancy and gives customers an incentive to book well in advance.

### Purpose

This configuration allows contract managers to define rules for early booking incentives that apply during specific travel and booking periods, for certain room and board combinations. These settings are applied automatically during the booking process if the criteria are met.

### Preconditions

Before configuring early booking discounts:

* The **hotel contract** must be created.
* **Periods**, **room types**, and **board types** should already be set up.

### Field-by-Field Explanation

| Field                   | Description                                                                                                                                                                                                                    |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Cost Discount**       | The discount amount to be applied. Can be a fixed amount (e.g., 50 USD) or a percentage (if % is checked).                                                                                                                     |
| **%**                   | Check this box to apply the discount as a percentage instead of a fixed amount.                                                                                                                                                |
| **S\&P (Stay & Pay)**   | If checked, the discount combined with stay & pay                                                                                                                                                                              |
| **EBC**                 | Apply on Extra Bed Cost                                                                                                                                                                                                        |
| **Room**                | Select the room(s) the Early booking discount applies to. If left empty, the Early booking discount will be applied to the board suplement                                                                                     |
| **Board**               | If a board is selected in combination with a room, then the Early booking discount only applies to the room if the selected board is used. If no room is selected, the Early booking discount applies to the Board Supplement. |
| **Stay (Start/End)**    | Defines the travel/stay window when the discount is valid. Guests must stay during this period.                                                                                                                                |
| **Booking (Start/End)** | Defines the **booking window**. The guest must book between these dates to be eligible.                                                                                                                                        |
| **Min Days**            | Minimum number of stay days for the Early booking discount to take effect                                                                                                                                                      |
| **Week Days**           | Specify the weekdays where the guests shall arrive, for the Early Booking Discount to be applied. Select specific days or “Selected all (7)”.                                                                                  |
| **Days Before**         | Days before arrival. If set no deposit is used.                                                                                                                                                                                |
| **Deposit**             | The deposit to be paid in a percentage of the cost.                                                                                                                                                                            |
| **Deposit Date**        | Payment of Early booking discount on all bookings agreed on this date.                                                                                                                                                         |

