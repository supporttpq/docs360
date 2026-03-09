---
description: >-
  Add hotel costs on top of the base room cost by age, date, room, or booking
  period.
---

# Hotel Extra Cost Rules

**Overview**\
Hotel Extra Cost Rules define additional costs that the agency pays to hotels. These rules are applied automatically to bookings when specific conditions are met. Both types of rules are always applied, ensuring that extra costs are accurately reflected in the booking’s financial calculations.

**Purpose**\
The purpose of these rules is to ensure that hotel-related expenses beyond the base room cost are correctly accounted for. This provides a transparent view of the agency’s expenses and supports more precise profit analysis.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Types of Extra Cost Rules**

1. **Extra price per passenger per night**
   * Formula: _value × number of nights_
2. **Extra price per room**
   * One-time cost per room.
   * The system distributes the cost across room occupants.

#### **Filters for Applying**

Extra costs are applied only when these conditions are met:

* **Age** – Define a start and end age range for which the extra cost applies.
* **Extra P/P/N (Extra Price/Pax/Night)** – Multiplied by the number of nights and applicable guests.
* **Extra P/R (Extra Price/Room)** – One-time charge per room, not per night.
* **Stay/Arrival Period** – Limit the extra cost to bookings with arrivals within specific dates.
* **Booking Period** – Apply the cost only if the booking is created within a defined date range.
* **Room** – Restrict the cost to a specific room type.

#### Creating a New Rule

1. Click **Create** (top right).
2. Set **From age** and **To age**.
3. Set **Extra P/P/N**, **Extra P/R**, or both.
4. Set **Stay/Arrival Start** and **Stay/Arrival End**.
5. Set **Booking Start** and **Booking End**.
6. Select a **Room** (or **All Rooms**).
7. Select a **Contract**, if needed.
8. Save the rule.

#### Editing an Existing Rule

1. Locate the rule you want to modify in the table
2. Click on the row or edit icon (if available)
3. Modify the required fields
4. Ensure date ranges don’t conflict with other rules
5. Save changes

#### Deleting a Rule

1. Locate the rule in the table
2. Click the **delete icon** (trash can) on the right side of the row
3. Confirm the deletion when prompted

### Related pages

* [Room cost](./)
