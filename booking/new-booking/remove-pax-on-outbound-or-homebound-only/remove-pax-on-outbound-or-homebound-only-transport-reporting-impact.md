# Remove pax on outbound or homebound only, Transport Reporting Impact

### Overview

This documentation outlines how the system handles bookings marked with **"No-show"** in various transport reporting types. It details the steps to generate the reports and describes the expected results depending on the scheduler type used.

***

### **Purpose**

To ensure accurate reporting of transport bookings while excluding or treating differently those marked as **"No-show"** on outbound or homebound journeys.

***

### **Steps and Behavior Overview**

#### **1. Navigate to the Transport Page**

* **Step:** Go to **“Transport” → “Transports”**
* **Expected Result:** Transport list page is displayed.

***

#### **2. Select Specific Transport**

* **Step:** Search for a transport with bookings marked as **"No-show"** and click its code.
* **Expected Result:** Transport edit page is displayed.

***

#### **3. Access Communication Tab**

* **Step:** Go to the **"Communication"** tab.
* **Expected Result:** All schedulers set for the transport are listed.

***

### **Report Generation by Scheduler Type**

#### **4. Both Ways Scheduler**

* **Steps:**
  * Set the **“No start”** so that a report is generated.
  * Select a **departure date** that includes **"No-show"** bookings.
  * Generate and check the report.
* **Expected Results:**
  * Passengers with **"No-show"** on **outbound** are listed as **one-way homebound**.
  * Passengers with **"No-show"** on **homebound** are listed as **one-way outbound**.
  * Passengers with **"No-show"** on **both directions** are **not listed at all**.
  * Passengers from **one-way bookings** (either outbound or homebound) with **"No-show"** will **not be listed**.

***

#### **5. Outbound Scheduler**

* **Steps:** Same as above.
* **Expected Results:**
  * Passengers with **"No-show"** on **outbound** will **not be listed**.
  * Passengers with **"No-show"** on **homebound** are not included by default.
  * Passengers with **"No-show"** on **both directions** will **not be listed**.
  * One-way bookings with **"No-show"** are excluded.

***

#### **6. Homebound Scheduler**

* **Steps:** Same as above.
* **Expected Results:**
  * Passengers with **"No-show"** on **homebound** will **not be listed**.
  * Passengers with **"No-show"** on **outbound** are not included by default.
  * Passengers with **"No-show"** on **both** directions are **not listed**.
  * One-way bookings with **"No-show"** are excluded.

***

#### **7. OutHome Scheduler**

* **Steps:** Same as above.
* **Expected Results:**
  * Passengers with **"No-show"** on **outbound** will be listed as **one-way out**.
  * Passengers with **"No-show"** on **homebound** will be listed as **one-way home**.
  * Passengers with **"No-show"** on **both directions** are **not listed**.
  * One-way bookings with **"No-show"** are not listed.

***

#### **8. Summary for All Scheduler Types**

* **Step:** Review results from Steps 4 to 7.
* **Expected Result:** Reporting behavior for **"No-show"** bookings is consistently handled across different scheduler types as outlined above.

***

### **Notes**

* Ensure that the **departure date** selected includes the time frame where **"No-show"** bookings exist.
* “No-show” passengers are excluded from reporting where appropriate to maintain accuracy in passenger manifests.
