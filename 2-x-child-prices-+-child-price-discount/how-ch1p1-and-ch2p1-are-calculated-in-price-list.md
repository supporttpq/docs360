# How CH1P1 & CH2P1 are calculated in Price List

### **Overview**

This document explains how the child pricing columns **CH1P1** and **CH2P1** are displayed and calculated in the **Price List** section.\
The feature allows administrators to view detailed child pricing information and understand how child prices are derived based on hotel room costs, profit margins, and transport costs.

***

### **Accessing Child Price Columns**

Within the **Price List**, administrators can customize the displayed columns to include child-related pricing data.\
From the column selection menu (three-dot icon in the table header), users can enable the following columns:

* **CHILD 1 PRICES** and **CHILD 2+ PRICES**
* **CHILD PROFIT PRICES**&#x20;
* **CHILD 1 DISCOUNTS** and **CHILD 2 DISCOUNTS**
* **CHILD PROFIT MARGIN**
* **CHILD ADJUSTMENTS**

<figure><img src="../.gitbook/assets/image (640).png" alt=""><figcaption></figcaption></figure>

When activated, the table will display a series of child pricing columns, including:\
**CH1P1**, **CH2P1**, **CH1D1**, **CH2D1**, , **CPM1, PCH1P1, PCH2P1, CH1PD1, CH2PD1, CH1PA, CH2PA.**

<figure><img src="../.gitbook/assets/image (641).png" alt=""><figcaption></figcaption></figure>

\
These columns represent price values, applied discounts, profit margins, and adjustments relevant to the selected room type and travel package.

***

### **Calculation Logic**

**CH1P1 Calculation**

The column **CH1P1** represents the calculated price for the first child and follows this formula:

**CH1P1 = (Room Cost from the hotel × Number of nights) + CMP1 + Transport Cost**

This ensures the child's price reflects the total room cost across the stay period, combined with the applied profit margin and any associated transport cost.

Example:

Room cost = 50 Euro /pax/night = 373.5 DKK /pax/night&#x20;

<figure><img src="../.gitbook/assets/image (642).png" alt=""><figcaption></figcaption></figure>

Number of nights  = 7

CPM1 = 100 DKK&#x20;

<figure><img src="../.gitbook/assets/image (643).png" alt=""><figcaption></figcaption></figure>

Transport cost = 13094 DKK&#x20;

<figure><img src="../.gitbook/assets/image (644).png" alt=""><figcaption></figcaption></figure>

**CH1P1 = (Room Cost from the hotel × Number of nights) + CMP1 + Transport Cost = (373.5 \* 7) + 100 + 13094 = 15849 DKK**

If child adjusment it is used (CH1PA),  the CH1P1 it will be calculate with the same formula, but it will be added the child adjusment. This field accept both positive and negative value:

* Positive Adjustment for CH1PA

**CH1P1 = (Room Cost from the hotel × Number of nights) + CMP1 + Transport Cost + CH1PA**&#x20;

<figure><img src="../.gitbook/assets/image (645).png" alt=""><figcaption></figcaption></figure>

Child prices (CH1P1,CH1P2,CH1P1, CH2P2) are increased with CPA values. CPA triggers costs so will change the prices considering the cost. If there is no cost, then PA have no effect. PM is not mandatory to be set, if PA is set will trigger PMS and will calculate considering PM=0

**Adjustment set to 0** (CPA=0), if the PLTA has no PM set, will be ignored, so the prices will remain the same. Otherwise main price (CH1/2P1) is modified according to cost and PM.

* Negative Adjustment

**CH1P1 = (Room Cost from the hotel × Number of nights) + CMP1 + Transport Cost**&#x20;

**CH1D1 = CH1P1 - CH1PA**

<figure><img src="../.gitbook/assets/image (646).png" alt=""><figcaption></figcaption></figure>

**CH2P1 Calculation**

The column **CH2P1** follows the same calculation logic as CH1P1:

**CH2P1 = (Room Cost from the hotel × Number of nights) + CMP1 + Transport Cost**

Since both child prices share the same profit margin (CMP1), the resulting calculation ensures consistency and transparency across child pricing configurations.

***

### **Purpose and Usage**

Displaying the **CH1P1** and **CH2P1** columns allows administrators to verify that child pricing aligns with the configured profit margins and cost rules.\
This setup ensures accurate pricing representation for child passengers and supports better monitoring of profit structures within the **Price List** interface.
