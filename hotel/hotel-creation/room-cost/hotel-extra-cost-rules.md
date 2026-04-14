---
description: >-
  Add hotel costs on top of the base room cost by age, date, room, or booking
  period.
---

# Hotel Extra Cost Rules

### Introduction

The **Hotel Extra Cost Rules** page is located in **Hotel → Room Costs** in **Tourpaq Office**. This functionality allows configuration of additional costs that the agency must pay to the hotel beyond the base room cost.

Hotel Extra Cost Rules complement the standard **Room Cost Rules** by adding extra amounts when specific booking conditions are met. These rules are evaluated automatically during the cost calculation process and are applied to bookings whenever the defined conditions match.

Hotel Extra Cost Rules interact with several other Tourpaq components:

* **Room Cost Rules** (base hotel cost configuration)
* **Early Booking Cost Discount Rules**
* **Stay and Pay Cost Rules**
* **Profit Margin Rules**
* **Price Lists**
* **Booking cost calculation**

Because these rules affect the **hotel cost**, they may also influence the **selling price** shown to the guest if selling prices are calculated from costs using **Profit Margin rules**.

### **Overview**

Hotel Extra Cost Rules define additional costs that the agency pays to hotels. These rules are applied automatically to bookings when specific conditions are met. Both types of rules are always applied, ensuring that extra costs are accurately reflected in the booking’s financial calculations.

### **Purpose**

The purpose of these rules is to ensure that hotel-related expenses beyond the base room cost are correctly accounted for. This provides a transparent view of the agency’s expenses and supports more precise profit analysis.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Types of Extra Cost Rules**

1. **Extra price per passenger per night**
   * Formula: _value × number of nights_
2. **Extra price per room**
   * One-time cost per room.
   * The system distributes the cost across room occupants.

#### **Filters for Applying**

Extra costs are applied only when the rule conditions match the booking.

The following filters determine when a rule is applied:

* **Age** – Defines the passenger age range that triggers the extra cost.
* **Extra P/P/N (Extra Price/Pax/Night)** – Multiplied by the number of nights and the number of applicable passengers.
* **Extra P/R (Extra Price/Room)** – One-time charge applied per room.
* **Stay/Arrival Period** – Limits the rule to bookings with arrivals within a specific date range.
* **Booking Period** – Applies the rule only to bookings created within a defined date range.
* **Room** – Restricts the rule to a specific room type or applies it to all rooms.

### Top Filter Section

The filter section allows the list of rules to be restricted to specific contracts or date ranges.

* Contract - Dropdown used to select the **hotel contract** for which Hotel Extra Cost Rules are displayed. Only rules associated with the selected contract appear in the grid.
* Show all - Checkbox that displays **all configured rules**, including rules that may not match the selected filters.
* \+ More Filters - Expands the filter area and displays additional filtering options such as:
  * **Room Code**
  * **Period**
  * **Booking date**
  * **Departure date**

These filters are useful when contracts contain many rules.

* Clear - Resets all filter fields and returns the grid to the default display.
* Room Code - Dropdown used to filter rules by **room type**.&#x20;

Room codes originate from: **Hotel  → Room Types**

* Period - Dropdown used to filter rules by **period number** configured in the hotel contract. Periods usually represent seasonal ranges in the contract.
* Booking date - Date filter used to locate rules based on the **booking date validity period**.&#x20;
* Departure date - Date filter used to locate rules based on the **stay or arrival period**.
* Display - Applies the selected filters and refreshes the results displayed in the grid.
* Clear - Resets the filter fields.

### Rule Configuration Grid

Each row represents a **Hotel Extra Cost Rule**.

* FROM AGE - Defines the **minimum passenger age** for which the rule applies. Passengers younger than this value will not trigger the rule.
* TO AGE - Defines the **maximum passenger age** for which the rule applies. Passengers older than this value will not trigger the rule.

Together, **FROM AGE** and **TO AGE** define the eligible age range.

* EXTRA P/P/N - Defines the **Extra Price/Pax/Night**.

This value represents the extra cost charged:

* per passenger
* per night

The value is multiplied by the number of nights and applicable passengers.

* EXTRA P/R - Defines the **Extra Price/Room**.

This value represents a **one-time extra cost applied per room**.

The cost is added once when the rule conditions are satisfied.

* STAY/ARRIVAL START - Defines the **first stay or arrival date** when the rule becomes valid. Bookings with arrival dates before this date do not qualify.
* STAY/ARRIVAL END - Defines the **last stay or arrival date** when the rule remains valid. Bookings with arrival dates after this date do not qualify.
* BOOKING START DATE - Defines the **first booking date** when the rule can apply. Bookings created before this date will not trigger the rule.
* BOOKING END DATE - Defines the **last booking date** when the rule remains valid. Bookings created after this date will not trigger the rule.
* ROOM TYPE - Dropdown used to select the **room type** to which the rule applies. Possible values include:
  * A specific room type (e.g., **0D21**)
  * **All Rooms**                                                                                                                                      &#x20;
* CONTRACT - Displays the **contract identifier** associated with the rule. This helps identify the rule when multiple contracts exist for the same hotel.&#x20;
* Delete (Trash Icon) - Deletes the selected rule. Deleting a rule removes it from future calculations but does not affect historical bookings.&#x20;
* Create - Button used to **create a new Hotel Extra Cost Rule**. Selecting this option adds a new row in the grid where rule parameters can be defined.

### Creating a New Rule

1. Click **Create** (top right).
2. Set **From age** and **To age**.
3. Set **Extra P/P/N**, **Extra P/R**, or both.
4. Set **Stay/Arrival Start** and **Stay/Arrival End**.
5. Set **Booking Start** and **Booking End**.
6. Select a **Room** (or **All Rooms**).
7. Select a **Contract**, if needed.
8. Save the rule.

### Editing an Existing Rule

1. Locate the rule you want to modify in the table
2. Click on the row or edit icon (if available)
3. Modify the required fields
4. Ensure date ranges don’t conflict with other rules
5. Save changes

### Deleting a Rule

1. Locate the rule in the table
2. Click the **delete icon** (trash can) on the right side of the row
3. Confirm the deletion when prompted

### Related pages

* [Room cost](./)
