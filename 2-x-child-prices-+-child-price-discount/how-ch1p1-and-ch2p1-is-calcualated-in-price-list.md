# How CH1P1 & CH2P1 is calcualated in Price List

### **Overview**

This document describes the process of enabling and validating child pricing columns in the **Price List** page when logged in as an administrator. It includes enabling specific child-related options, verifying new columns, and confirming their calculation logic.

***

### **Step-by-Step Guide**

#### **1. Login as Administrator**

* **Action:** Log in using the administrator account.

#### **2. Access the Price List**

* **Action:** Navigate to the **Price List** page.

#### **3. Search for Prices**

* Fill in all required fields and click the **Display** button -  The table is populated with available pricing data.

#### **4. Filter Columns**

* Click the three-dot menu on the table header. In the popup window, deselect `I2`, `I3`, and `I4`, ensuring only `I1` remains selected. - The pop-up is displayed, and only `I1` remains ticked.

#### **5. Enable Child Pricing and Related Columns**

* In the same popup, tick the following options:
  * `CHILD 1 PRICES`
  * `CHILD 2 PRICES`
  * `CHILD 1 DISCOUNTS`
  * `CHILD 2 DISCOUNTS`
  * `CHILD PRICES %`
  * `CHILD PROFIT MARGIN`
  * `ADJUSTMENTS`
* Corresponding columns are added in the table:
  * `CH1P1`, `CH2P1`
  * `CH1D1`, `CH2D1`
  * `CH1%`
  * `CMP1`
  * `PA1`

#### **6. Validate Calculation for CH1P1**

*   Verify that `CH1P1` is calculated using the following formula:

    ```
    Room Cost from the hotel × Number of nights) + CPM1 + Transport Cost
    ```

#### **7. Validate Calculation for CH2P1**

*   Verify that `CH2P1` is calculated using the same formula:

    ```
    Room Cost from the hotel × Number of nights) + CPM1 + Transport Cost
    ```
