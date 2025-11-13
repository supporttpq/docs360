# Price List Custom Hotel days Service

### Overview

The **Price List Custom Hotel Days** feature allows the setup of hotel stays that are independent of a predefined transport package. Unlike standard price lists, this functionality provides flexibility for creating hotel-only stays or combinations that can be sold outside of fixed departure packages.

### Purpose

The purpose of this feature is to:

* Enable agencies to sell **hotel-only stays** or **custom-configured nights**.
* Offer flexibility to customers who may not require a full transport + hotel package.
* Allow for tailored availability and pricing, independent of transport schedules.

<figure><img src=".gitbook/assets/image (9) (1) (3) (1).png" alt=""><figcaption></figcaption></figure>

### Instructions

1. Navigate to **Price List → Custom Hotel Days**.
2. Click the **Create** button.
3. Fill in the required fields:
   * **Agency** – Select the agency responsible for the custom hotel day.
   * **Country / Arrival / Resort / Hotel** – Choose the location and hotel details.
   * **Rooms** – Assign the rooms and their allotments.
   * **Departure Start / Departure Stop** – Define the sales interval.
4. Enable or disable the price list using the **Enabled** toggle.
5. Click **View Prices** to define or adjust the hotel prices for the selected period.
6. Save the configuration.

Once created, the custom hotel days can be managed in the list view, where prices, availability, and statuses are displayed.



## **Define Rules for Price List – Field Explanations**

<figure><img src=".gitbook/assets/image (10) (1) (3) (1).png" alt=""><figcaption></figcaption></figure>

#### **Profit Margin**

* The markup or profit value to be applied on top of the base room cost.
* **How it works:**
  * If **“Is Percent”** is checked → the number entered here is treated as a percentage (%).
    * Example: 15 means a **15% profit margin** will be added.
  * If **“Is Percent”** is not checked → the number is treated as a fixed amount.
    * Example: 15 means **15 units of currency** (e.g., 15 EUR) will be added.

***

#### **Is Percent (checkbox)**

* Defines how the **Profit Margin** should be applied.
* **Checked:** Profit margin is applied as a **percentage** of the room cost.
* **Unchecked:** Profit margin is applied as a **fixed amount**.

***

#### **Room Cost Start**

* The **minimum base room cost** for which this rule applies.
* **Example:** If set to 1, the rule applies to all room costs starting from 1 currency unit.

***

#### **Room Cost End**

* The **maximum base room cost** for which this rule applies.
* **Example:** If set to 2000, the rule applies to all room costs up to 2000 currency units.

***

#### **Add Price (button)**

* Allows you to define **additional profit margin rules** for different cost ranges.
* **Example:**
  * Rule 1: 15% margin for room costs 1 – 2000
  * Rule 2: 10% margin for room costs 2001 – 5000

***

#### **Save (button)**

* Confirms and saves the defined rules into the price list.

***

#### **Trash/Delete Icon**

* Removes the current rule row from the configuration.

***

✅ This setup lets you define **tiered profit margin rules** depending on the room cost range.
