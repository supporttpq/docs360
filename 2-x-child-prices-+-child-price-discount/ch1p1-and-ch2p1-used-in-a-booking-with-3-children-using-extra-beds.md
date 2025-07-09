# CH1P1 & Ch2P1 used in a booking with 3 children using extra beds

### **Overview**

This document describes the end-to-end validation flow for creating a booking with **2 adults and 3 children** where **each child benefits from an extra bed**. It verifies the consistency between the **booking total price** and the **Price List** calculation, using child-specific pricing columns (`CH1P1`, `CH2P1`).

***

### **Prerequisites**

* Administrator login credentials&#x20;
* A hotel offering **extra beds for all children**
* Active and configured pricing fields:
  * `P1` (adult price)
  * `CH1P1`, `CH2P1` (child prices)
  * `CH1D1`, `CH2D1` (child discounts)
  * `CH1%`, `CMP1`, `PA1` (child price %, margin, and adjustments)

***

### **Step-by-Step Test Case**

#### **1. Login**

* Log in as administrator.

#### **2. Start a New Booking**

* Click the **New Booking** button and select a brand.

#### **3. Add Passengers**

* Set the number of passengers to **2 Adults** and **3 Children**.

#### **4. Select Transport**

* Click **Edit** in the transport section and select a transport.

#### **5. Select Hotel**

* Click **Edit** in the hotel section - The "Select Hotel" pop-up appears.

#### **6. Choose Hotel with Extra Beds**

* Choose a hotel that provides **an extra bed for each child**.

#### **7. Complete Booking**

* Fill in customer details, take allotment, and **save the booking**.
* Booking is successfully created.

#### **8. Note the Total Amount**

* Record the **Total Amount** displayed in the booking summary.

***

### **Validate Price List Calculation**

#### **9. Open Price List**

* Go to the **Price List** page.

#### **10. Apply Booking Filters**

* Fill in the required fields using the data from Step 7, then click **Display**.

#### **11. Adjust Column View**

* Click the three-dot menu in the header, deselect `I2`, `I3`, and `I4`. Ensure **only `I1`** is ticked.
* Only `I1` is displayed.

#### **12. Enable Child Pricing Columns**

* Tick the following fields:
  * `CHILD 1 PRICES`
  * `CHILD 2 PRICES`
  * `CHILD 1 DISCOUNTS`
  * `CHILD 2 DISCOUNTS`
  * `CHILD PRICES %`
  * `CHILD PROFIT MARGIN`
  * `ADJUSTMENTS`
* The following columns are added:
  * `CH1P1`, `CH2P1`
  * `CH1D1`, `CH2D1`
  * `CH1%`, `CMP1`, `PA1`

***

### &#x20;**Validate Total Price Calculation**

*   Verify that the **total amount from Step 8** is equal to:

    ```
    Total = (P1 × 2 Adults) + CH1P1 + CH2P1 + CH2P1
    ```
