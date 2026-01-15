# Early Booking Discount – Hotel Contract Configuration

### Overview

The **Early Booking Discount** section in the “Hotel Contract” module allows the hotel to reward customers who book early by offering a fixed or percentage-based discount. It helps boost early occupancy and gives customers an incentive to book well in advance.

***

### Purpose

Use this tab to define discount rules that apply only when:

* The stay falls within a defined **stay period**.
* The booking is made within a defined **booking period**.
* Optional criteria (room, board, weekdays, min days, days-before) match.

The system applies the discount automatically during booking, when criteria match.

***

### Preconditions

Before configuring early booking discounts:

* The **hotel contract** must be created.
* **Periods**, **room types**, and **board types** should already be set up.

***

### Fields

| Field                   | Description                                                                                                                                                                    |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Cost Discount**       | Discount amount. Use a fixed value (for example `50`) or a percentage (when **%** is checked).                                                                                 |
| **%**                   | Check this box to apply the discount as a percentage instead of a fixed amount.                                                                                                |
| **S\&P (Stay & Pay)**   | Enable if this early booking discount should be combined with **Stay & Pay**.                                                                                                  |
| **EBC**                 | Apply the discount to **extra bed cost**.                                                                                                                                      |
| **Room**                | Select the room types the discount applies to. If you leave it empty, the discount applies to the **board supplement** instead.                                                |
| **Board**               | When combined with **Room**, the discount only applies when this board is used. If **Room** is empty, the discount applies to the **board supplement** for the selected board. |
| **Stay (Start/End)**    | Defines the travel/stay window when the discount is valid. Guests must stay during this period.                                                                                |
| **Booking (Start/End)** | Defines the **booking window**. The guest must book between these dates to be eligible.                                                                                        |
| **Min Days**            | Minimum stay length required for the discount to apply.                                                                                                                        |
| **Week Days**           | Arrival weekdays that qualify. Select specific days, or **Select all (7)**.                                                                                                    |
| **Days Before**         | Minimum number of days before arrival that the booking must be made.                                                                                                           |
| **Deposit**             | Deposit percentage required when using this discount.                                                                                                                          |
| **Deposit Date**        | Date when the deposit must be paid for bookings using this discount.                                                                                                           |

***

### How it works

{% stepper %}
{% step %}
### Set what you want to discount

Use **Room** to discount room cost.

Leave **Room** empty to discount a **board supplement** instead.
{% endstep %}

{% step %}
### Limit it to the right dates

Set **Stay (Start/End)** to define the travel window.

Set **Booking (Start/End)** to define when the booking must be created.
{% endstep %}

{% step %}
### Add eligibility rules (optional)

Use **Min Days**, **Week Days**, and **Days Before** to narrow eligibility.

Only add rules you actually need.
{% endstep %}

{% step %}
### Validate with a test booking

Create a booking that matches the stay and booking windows.

Verify the discount appears on the pricing lines you expect.
{% endstep %}
{% endstepper %}

***

### Tips

{% hint style="info" %}
If you want Early Booking to stack with Stay & Pay, ensure both the rule and the contract allow the combination.
{% endhint %}

* Avoid overlapping rules with the same scope. It makes results hard to predict.
* Keep naming and setup consistent across contracts. It helps support and reporting.

***

### Related workflows

* [Hotel contract - General](hotel-contract-general.md)
* [Rooms – Hotel Contract Configuration](rooms-hotel-contract-configuration.md)
* [Periods – Hotel Contract Configuration](periods-hotel-contract-configuration.md)
* [Stay & Pay - Hotel Contract Configuration](stay-and-pay-hotel-contract-configuration.md)

***

### FAQ

**What’s the difference between a fixed discount and a % discount?**\
Fixed discounts subtract a set amount.\
Percentage discounts scale with the priced amount.

**Why is my early booking discount not applied?**\
Check **Booking (Start/End)** first.\
Then check **Stay (Start/End)**.\
Finally, validate **Days Before**, **Min Days**, and **Week Days**.

**What happens if I leave “Room” empty?**\
The discount targets the **board supplement** instead of the room cost.\
Use **Board** to choose which board supplement it applies to.

**Can I restrict the discount to a specific board type?**\
Yes. Set **Board**.\
If you also set **Room**, both must match.

**How does the deposit work with Early Booking Discount?**\
Use **Deposit** to require a deposit percentage.\
Use **Deposit Date** to define when it must be paid.
