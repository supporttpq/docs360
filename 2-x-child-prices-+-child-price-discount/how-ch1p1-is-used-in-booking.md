# How CH1P1 is used in booking

### **Overview**

This document outlines the steps required to create a booking with child passengers, enable child-related price columns in the **Price List**, and validate the final **Total Amount** by comparing booking values with pricing breakdowns.

***

### **Prerequisites**

* Administrator access
* At least one hotel offering **extra bed** for children
* Proper access to:
  * Booking management
  * Price List page
  * Feature flags such as **Child Prices**, **Child Discounts**, **Child Profit Margin**, and **Adjustments**

***

### **Step-by-Step Instructions**

#### **1. Login**

* Log in using the administrator account.

#### **2. Start New Booking**

* Click the **New Booking** button and select a brand. - The brand is selected, and the new booking page is displayed.

#### **3. Add Passengers**

* In the **Passengers** section, select `2 Adults` and `1 Child`.

#### **4. Select Transport**

* Click the **Edit** button in the transport section and choose a transport.

#### **5. Select Hotel**

* Click the **Edit** button in the **Hotel** section.

#### **6. Choose Hotel with Extra Bed**

* Select a hotel that provides an **extra bed for a child**.

#### **7. Complete Booking**

* Fill in the **Customer Details**, take the allotment, and save the booking.

#### **8. Note Total Amount**

* Record the **Total Amount** shown in the booking confirmation.

***

### **Verify Price List Data**

#### **9. Open Price List**

* Go to the **Price List** page.

#### **10. Populate Filters**

* Fill in all required filters using the booking data from **Step 7**, then click **Display -** Search is performed.

#### **11. Adjust Column Display**

* Click the three-dot menu on the table header. Deselect `I2`, `I3`, and `I4`, and ensure only `I1` is ticked. - Column selector is updated to display only `I1`.

#### **12. Enable Child Pricing Fields**

* In the same pop-up, tick the following:
  * `CHILD 1 PRICES`
  * `CHILD 2 PRICES`
  * `CHILD 1 DISCOUNTS`
  * `CHILD 2 DISCOUNTS`
  * `CHILD PRICES %`
  * `CHILD PROFIT MARGIN`
  * `ADJUSTMENTS`
* The following columns are added to the table:
  * `CH1P1`, `CH2P1` – child prices
  * `CH1D1`, `CH2D1` – child discounts
  * `CH1%` – child price percentage
  * `CMP1` – child profit margin
  * `PA1` – adjustments

***

### **Validate Calculation**

#### **13. Compare Total Amount**

*   Validate that the Total Amount from **Step 8** matches the following calculation:

    ```
    Total Amount = P1 × Number of Adults + CH1P1
    ```

    Where:

    * `P1` = Price per adult
    * `CH1P1` = Price for child 1
* The total amount from the booking is consistent with the formula.

***

### **Conclusion**

This scenario ensures the correct linkage between **booking totals** and **price list breakdowns**, especially regarding child pricing. It validates both **data display** and **price calculation logic**, supporting reliable pricing transparency for agents and admins.
