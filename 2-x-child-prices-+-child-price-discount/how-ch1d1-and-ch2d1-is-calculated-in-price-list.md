# How CH1D1 & CH2D1 is calculated in Price List

### **Overview**

This document explains how the child discount columns **CH1D1** and **CH2D1** are displayed and calculated in the **Price List** section.\
It details the required configuration and the formulas used to compute the discount values for child passengers when child pricing and profit margin features are active.

***

### **Prerequisites**

To view and validate the child discount calculations, the user must:

* Have **Administrator** access.
* Have the following features enabled:
  * **Child Prices**
  * **Child Discounts**
  * **Child Profit Margin**
  * **Adjustments**

***

### **Accessing Child Discount Columns**

Within the **Price List**, the user can customize the displayed table columns to include child-related pricing and discount data.\
From the column selection menu, the following options should be enabled:

* **CHILD 1 PRICES**
* **CHILD 2 PRICES**
* **CHILD 1 DISCOUNTS**
* **CHILD 2 DISCOUNTS**
* **CHILD PRICES %**
* **CHILD PROFIT MARGIN**
* **ADJUSTMENTS**

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (451).png" alt=""><figcaption></figcaption></figure></div>

Once enabled, the table displays additional columns such as:\
**CH1P1**, **CH2P1**, **CH1D1**, **CH2D1**, **CH1%**, **CMP1**, and **PA1**.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (452).png" alt=""><figcaption></figcaption></figure></div>

\
These represent the respective prices, discounts, percentages, profit margins, and applied adjustments for child passengers.

***

### **Calculation Logic**

**CH1D1 Calculation**

The **CH1D1** column represents the discount-adjusted value for the first child and is calculated as:

**CH1D1 = (Extra Bed Cost Price from the hotel × Number of nights) - Early Booking Discount + CMP1 + Transport Cost + (-PA1)**

This formula takes into account the total extra bed cost over the entire stay, applies the early booking discount, and factors in the profit margin, transport cost, and any negative or positive price adjustments.

***

**CH2D1 Calculation**

The **CH2D1** column follows a similar structure but applies the second child’s extra bed cost:

**CH2D1 = (Extra Bed Cost Price 2ND from the hotel × Number of nights) - Early Booking Discount + CMP1 + Transport Cost + (-PA1)**

This ensures that both child discounts are calculated consistently, reflecting their respective extra bed costs and applied pricing rules.

***

### **Purpose and Usage**

The **CH1D1** and **CH2D1** columns allow administrators to validate how discounts for child passengers are derived from base hotel costs, early booking discounts, and profit margins.\
This level of detail provides full transparency in the **Price List** and ensures pricing accuracy for family bookings involving children.
