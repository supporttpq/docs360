# Child pays an adult's price for a double room when it does not occupy an extra bed

### **Overview**

This document describes the behavior of the system when a booking is created with **1 adult and 1 child** sharing a standard **double room**. It verifies that in such cases, the child is charged the **same rate as the adult**, regardless of child pricing configurations, and ensures this is consistently reflected in the **Price List** and **booking total**.

***

### **Prerequisites**

* Administrator access&#x20;
* Feature access enabled for:
  * Child Prices
  * Child Discounts
  * Child Profit Margin
  * Adjustments
* At least one hotel with standard double room availability&#x20;

***

### **Booking Creation and Setup**

#### **1. Login**

* Log in as administrator

#### **2. Start a New Booking**

* Click the **New Booking** button and select a brand.

#### **3. Add Passengers**

* Populate the **Passengers** section with:
  * 1 Adult
  * 1 Child

#### **4. Select Transport**

* **C**lick **Edit** in the transport section and select a transport - Transport is assigned.

#### **5. Select Hotel**

* Click **Edit** in the **Hotel** section - "Select Hotel" pop-up is displayed.

#### **6. Choose Hotel with Standard Double Room**

* Select a hotel that offers a **double room** -  Hotel is successfully selected.

#### **7. Complete the Booking**

* Fill in the **Customer Details**, take allotment, and save the booking. - Booking is successfully created.

#### **8. Note Total Amount**

* Record the **Total Amount** from the booking confirmation&#x20;

#### **9. Verify Price Breakdown per Passenger**

* Open the **Total pr. passenger** section in the booking details. The **child is charged the same price as the adult** (i.e., the standard adult price `P1` is applied to both passengers).

***

### **Price List Verification**

#### **10. Open Price List**

* Go to the **Price List** page - Price List is displayed.

#### **11. Apply Filters**

* Use the booking data from **Step 7** to populate mandatory filters, then click **Display -** Price table is displayed.

#### **12. Customize Column View**

* Click the three-dot menu in the header. Deselect:
  * `I2`, `I3`, `I4`
  * Ensure only `I1` is ticked.

#### **13. Enable Child-Related Columns**

* Tick the following in the same menu:
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

### **Validation of Pricing Behavior**

#### **14. Check Use of CH1P1**

* Confirm whether `CH1P1` (Child Price 1) is considered in the total booking amount.
* `CH1P1` is **not** taken into consideration when calculate the Booking's Price

#### **15. Validate Use of P1 Only**

* Check the booking's price for both passengers (adult & child).&#x20;
* The system uses the **P1 (adult price)** for **both the adult and the child**.
