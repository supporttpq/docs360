# How CH1P1 & CH2P1 are calculated in Price List

#### **Overview**

This document explains how the child pricing columns **CH1P1** and **CH2P1** are displayed and calculated in the **Price List** section.\
The feature allows administrators to view detailed child pricing information and understand how child prices are derived based on hotel room costs, profit margins, and transport costs.

***

#### **Accessing Child Price Columns**

Within the **Price List**, administrators can customize the displayed columns to include child-related pricing data.\
From the column selection menu (three-dot icon in the table header), users can enable the following columns:

* **CHILD 1 PRICES** and **CHILD 2 PRICES**
* **CHILD 1 DISCOUNTS** and **CHILD 2 DISCOUNTS**
* **CHILD PRICES %**
* **CHILD PROFIT MARGIN**
* **ADJUSTMENTS**

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (447).png" alt=""><figcaption></figcaption></figure></div>

When activated, the table will display a series of child pricing columns, including:\
**CH1P1**, **CH2P1**, **CH1D1**, **CH2D1**, **CH1%**, **CMP1**, and **PA1**.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (448).png" alt=""><figcaption></figcaption></figure></div>

\
These columns represent price values, applied discounts, percentage-based values, profit margins, and adjustments relevant to the selected room type and travel package.

***

#### **Calculation Logic**

**CH1P1 Calculation**

The column **CH1P1** represents the calculated price for the first child and follows this formula:

**CH1P1 = (Room Cost from the hotel × Number of nights) + CMP1 + Transport Cost**

This ensures the child price reflects the total room cost across the stay period, combined with the applied profit margin and any associated transport cost.

**CH2P1 Calculation**

The column **CH2P1** follows the same calculation logic as CH1P1:

**CH2P1 = (Room Cost from the hotel × Number of nights) + CMP1 + Transport Cost**

Since both child prices share the same profit margin (CMP1), the resulting calculation ensures consistency and transparency across child pricing configurations.

***

#### **Purpose and Usage**

Displaying the **CH1P1** and **CH2P1** columns allows administrators to verify that child pricing aligns with the configured profit margins and cost rules.\
This setup ensures accurate pricing representation for child passengers and supports better monitoring of profit structures within the **Price List** interface.
