# Edit Quota

### **Overview**

The **Edit Quota** page is used to manage seat allotments for transport departures in Tourpaq.\
It provides a unified view of **outbound** and **homebound** departures, allowing transport managers to quickly adjust 7-day rotations, one-way seats, and correct operational deviations such as capacity changes or overbookings.

All departures appear as rows with editable allotment fields. Users can apply individual changes or mass updates using the built-in **Change Values** tool.

This tool is essential for day-to-day management of flights and other transport types that operate with seat allotments.

***

### **Purpose**

The main purpose of the Edit Quota page is to:

* Allow quick correction of allotments when capacity changes occur.
* Support operational changes such as:
  * flight delays, aircraft changes, or cancellations,
  * seasonal adjustments (e.g., higher demand during holidays),
  * re-balancing seats based on bookings.
* Provide a uniform and intuitive interface for adjusting quotas across multiple departure dates.
* Enable bulk modifications across many departures with a single action.

It reduces manual workload and minimizes risk of allotment errors.

## **Field Explanation**

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **1. Change Values Tool**

Used to apply bulk changes across selected departures.

| Field         | Description                                                                                   |
| ------------- | --------------------------------------------------------------------------------------------- |
| **Column**    | Selects which allotment field to update (e.g., OUT: 7D, OUT: Oneway, HOME: 7D, HOME: Oneway). |
| **Operation** | Defines the action: **+** (add), **–** (subtract), **=** (set value).                         |
| Weekday       | Select the weekday that will be updated                                                       |
| **Value**     | The number to apply (e.g., +2 adds two seats).                                                |
| **Run**       | Executes the operation on all selected rows.                                                  |

***

### **2. Departure Table Columns**

#### **General Information**

| Column          | Description                                                   |
| --------------- | ------------------------------------------------------------- |
| **Date**        | Departure date for this transport rule.                       |
| **Day**         | Weekday of the departure (Mon–Sun).                           |
| **Flight Info** | Shows flight code and time window (e.g., FR701, 09:31–11:31). |

Icons:

*   <mark style="color:blue;background-color:blue;">ⓘ</mark> **Blue Icon** – informational note. (Not all seats are allocated)

    <figure><img src="../.gitbook/assets/image (495).png" alt=""><figcaption></figcaption></figure>
*   <mark style="color:purple;">⚠️</mark> **Red Icon** – warning (depending on the column they appear on, they show different warning messages):&#x20;

    * OUTBOUND - Outbound allotment higher than homebound allotment;
    * O/U (Over/Under Allotment) - Sum of homebound allotments lower than sum of outbound allotments;
    * HOMEBOUND - Homebound allotment lower than outbound allotment.

    <figure><img src="../.gitbook/assets/image (494).png" alt=""><figcaption></figcaption></figure>
*   ⚠️ **Yellow Icon -** Homebound allotments higher than outbound allotments.&#x20;

    <figure><img src="../.gitbook/assets/image (493).png" alt=""><figcaption></figcaption></figure>

***

#### **Outbound Section**

| Field          | Description                                            |
| -------------- | ------------------------------------------------------ |
| **7D/14D/21D** | Allocated seats for the 7/14/21-day rotation outbound. |
| **Oneway**     | Allocated seats for one-way outbound passengers.       |
| **O/U**        | Over/Under Allotment                                   |

Values are shown as:\
**Entered value** + **Booked / Capacity** → e.g., _0 / 100_

***

#### **Homebound Section**

| Field          | Description                                                |
| -------------- | ---------------------------------------------------------- |
| **7D/14D/21D** | Seats allocated for the homebound 7/14/21-day return trip. |
| **Oneway**     | Seats allocated for one-way inbound passengers.            |

Same “value + booked / capacity” structure applies.

***

#### **Row Selector**

* Allows selecting one or multiple departures.
* Only selected rows are affected by the Change Values tool.
* Supports:
  * Select single row
  * Select multiple rows
  * Select all

#### Displaying Booked Seats per Stay Day in the Quota View

The quota view on the Transport Rule page shows the **booked/total seats** for each stay-day cell. The _booked_ value reflects the number of seats reserved specifically for that stay day.

<figure><img src="../.gitbook/assets/image (540).png" alt=""><figcaption></figcaption></figure>

Each cell in the quota grid is linked to a **fixed quota** within a Sys-real transport, where the system retrieves the accurate booking information.

To ensure accurate monitoring, the quota view is updated to display the booked seats **per stay day**, based on the data from the corresponding fix-quotas.

***

## **How It Works**

### **1. Select departures**

Use the checkboxes on the left side to choose the dates you want to update.

### **2. Configure the Change Values tool**

* Choose the **column** (e.g., OUT: 7D).
* Choose **operation** (+, –, =).
* Enter the **value**.
* Press **Run**.

The system applies the change ONLY to the selected rows.

***

### **3. Edit values manually**

Every allotment field can also be clicked and edited directly.

Manual changes are reflected immediately.

***

### **4. Save the changes**

A single **Save** button saves all modifications.\
Nothing is applied until Save is pressed.

***

### **5. Cancel**

Reverts all unsaved changes and remains on the page.

***

## **Warnings & System Behavior**

#### **Red Highlighted Values**

Indicate an invalid or negative allotment (e.g., –2).

#### **Red Warning Messsage**

It appears when saving the rule, and there are negative allotment warnings in the rule.

<figure><img src="../.gitbook/assets/image (491).png" alt=""><figcaption></figcaption></figure>

***

## **Examples**

#### **Example 1 – Increase outbound 7D seats by 3**

1. Select desired dates.
2. Column → **OUT: 7D**
3. Operation → **+**
4. Value → **3**
5. Run → **Run**

#### **Example 2 – Set homebound oneway seats to 0**

1. Select rows.
2. Column → HOM&#x45;**: Oneway**
3. Operation → **=**
4. Value → **0**
5. Run

#### **Example 3 – Fix overbooked flight**

A red icon appears showing overbooked state:

* Reduce allotment or
* Increase aircraft capacity if allowed.

***

## **Notes**

* Changes are not saved until **Save** is pressed.
* Negative values are allowed temporarily but cannot be saved.
* Booked seats cannot be overridden.
* Capacity is controlled by the linked **Transport Rule**.
