# CH1P1 is correctly used in WB

### **Overview**

This document describes the test scenario for validating that child pricing data (`CH1P1`, `CH2P1`, `CH1D1`, `CH2D1`, `CPM1`) populated in the **Price List** is correctly applied when making a **web booking**. The process also ensures consistency between the **web booking price** and the final price in the **Tourpaq app**.

***

### **Prerequisites**

* Administrator access&#x20;
* Price list entry (PLTA ID) for a **double room with 1 extra bed**
* Values for child pricing fields populated: `CH1P1`, `CH2P1`, `CH1D1`, `CH2D1`, `CPM1`
* Access to the **web booking page**
* Access to the **Tourpaq app**

***

### **Step-by-Step Guide**

#### **1. Login**

* Login as administrator.

#### **2. Open Price List**

* Navigate to the **Price List** page.

#### **3. Perform a Search**

* Populate all mandatory fields and click **Display -** Price list is generated with valid entries.

#### **4. Open PLTA Web Booking**

* Click on a **PLTA ID** for a **double room with 1 extra bed** that has values for:
  * `CH1P1`, `CH2P1`, `CH1D1`, `CH2D1`, and `CPM1`
  * If `CPM1` is empty, populate it and click **Save**
* Web Booking page is opened for the selected offer.

***

### **Web Booking Flow**

#### **5. Populate Rejsebestiller**

* Enter valid customer (Rejsebestiller) information.

#### **6. Add One Child**

* Select **1 Barn** and set the age - Child is added to booking.

#### **7. Populate Rejsedeltagere**

* Add valid participant data (for adult and child).

#### **8. Validate Passenger Prices**

* Ensure all persons (adult and child) are initially shown the same price as `P1` from Step 4.

#### **9. Check Discount (Rabat)**

* Confirm that the **Rabat** field correctly reflects the **child discount -** Discount is applied and labeled as a child discount.

***

### **Continue Booking**

#### **10. Click “Fortsaet”**

* Click **Fortsaet** to proceed - “Ekstra tilkob” page is displayed.

#### **11. Select Insurance Options**

* Populate `Forsikring` and `Afbestillingsforsikring` fields.

#### **12. Click “Fortsaet” Again**

* Proceed to the next step - “Opsummering” (Summary) page is displayed.

#### **13. Confirm and Submit**

* Tick mandatory checkboxes and click **Bestil Rejse -** A confirmation pop-up is displayed.

#### **14. Decline Extra Offer**

* Click **Nej Tak** in the pop-up - “Kvittering” (Receipt) page is displayed and booking is successfully created.

***

### **Validate Booking in Tourpaq**

#### **15. Copy Booking Number**

* Copy the booking number from the Kvittering page and open the booking in the **Tourpaq app**.
* **Expected Result:** Booking details page is displayed.

#### **16. Compare Prices**

* **Action:** Verify that the **price shown in the web booking** matches the **price in the Tourpaq app -** Prices are identical.

***

### **Conclusion**

This test validates:

* Accurate use of child pricing and profit margin values from the **Price List**
* Correct application of child discounts (Rabat) in **web booking**
