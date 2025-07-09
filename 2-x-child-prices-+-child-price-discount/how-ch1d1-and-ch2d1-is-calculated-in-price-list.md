# How CH1D1 & CH2D1 is calculated in Price List

### **Overview**

This document describes the steps for displaying child-related pricing and discount columns in the **Price List** page and validating their calculations. It includes detailed configuration and the logic used to compute values like **CH1D1** and **CH2D1**.

***

### **Prerequisites**

* Administrator access&#x20;
* Features enabled for:
  * **Child Prices**
  * **Child Discounts**
  * **Child Profit Margin**
  * **Adjustments**

***

### **Step-by-Step Instructions**

#### **1. Login as Administrator**

* Log in as the  administrator.

#### **2. Access the Price List Page**

* Navigate to the **Price List** section in the platform.

#### **3. Perform a Search**

* Fill in all required fields and click the **Display** button.- Search results are displayed in the price table.

#### **4. Filter Table Columns**

* Click the three-dot menu in the table's header. In the pop-up window:
  * Deselect options: `I2`, `I3`, and `I4`
  * Ensure only `I1` remains selected.
* Only `I1` is ticked in the pop-up column selector.

#### **5. Enable Child Pricing and Discount Columns**

* In the same pop-up window, tick the following options:
  * `CHILD 1 PRICES`
  * `CHILD 2 PRICES`
  * `CHILD 1 DISCOUNTS`
  * `CHILD 2 DISCOUNTS`
  * `CHILD PRICES %`
  * `CHILD PROFIT MARGIN`
  * `ADJUSTMENTS`
* New columns are added to the table:
  * `CH1P1`, `CH2P1` – Child prices
  * `CH1D1`, `CH2D1` – Child discounts
  * `CH1%` – Child price percentage
  * `CMP1` – Child profit margin
  * `PA1` – Price Adjustments

#### **6. Validate CH1D1 Calculation**

*   Check that the `CH1D1` value is computed as:

    ```excel-formula
    (Extra Bed Cost Price from the hotel × Number of nights) - Early Booking Discount + CPM1 + Transport Cost + (-PA1)
    ```

#### **7. Validate CH2D1 Calculation**

*   **Action:** Check that the `CH2D1` value is computed using:

    ```
    (Extra Bed Cost Price 2ND from the hotel × Number of nights) - Early Booking Discount + CPM1 + Transport Cost + (-PA1)
    ```
