---
description: >-
  Transport reporting impact of No-show (pax removed outbound/homebound). Covers
  scheduler types (Both Ways, Outbound, Homebound, OutHome) and expected report
  output.
---

# Remove pax on outbound or homebound only, Transport Reporting Impact

### Overview

This page explains how **No-show** affects **transport reporting**.

Reporting behavior depends on the transport **scheduler type** (Both Ways / Outbound / Homebound / OutHome).

### Key terms (search keywords)

* **No-show**
* **remove pax outbound only**
* **remove pax homebound only**
* **transport reporting**
* **Transport → Communication** (schedulers)
* **Both Ways scheduler**
* **Outbound scheduler**
* **Homebound scheduler**
* **OutHome scheduler**
* **one-way out / one-way home**

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

### FAQ

<details>

<summary><strong>Why does a No-show passenger show as a one-way passenger in the report?</strong></summary>

Some scheduler types treat “No-show on one direction” as the passenger still travelling on the other direction.

Example: With **Both Ways**, a pax marked No-show on outbound can appear as **one-way homebound**.

</details>

<details>

<summary><strong>Why is a passenger not listed at all?</strong></summary>

Most common reasons:

* Pax is **No-show on both directions**.
* The report is generated for a departure date that does not match the pax travel line.
* The scheduler type excludes No-show cases (common for Outbound/Homebound schedulers).
* It is a **one-way booking** where the pax is No-show (excluded by the rules above).

</details>

<details>

<summary><strong>Which scheduler types can turn No-show into one-way in reporting?</strong></summary>

* **Both Ways scheduler** can convert No-show on one direction into the opposite one-way.
* **OutHome scheduler** lists No-show outbound as **one-way out** and No-show homebound as **one-way home**.

**Outbound** and **Homebound** schedulers typically exclude No-show passengers for their direction.

</details>

<details>

<summary><strong>Where do I check which scheduler type a transport uses?</strong></summary>

Open the transport, then go to **Communication**.

All schedulers configured for that transport are listed there.

</details>

<details>

<summary><strong>How can I reproduce and verify the behavior?</strong></summary>

1. Pick a transport with known No-show cases.
2. In **Communication**, select the scheduler you want to test.
3. Set **No start** so the report generates.
4. Generate using a departure date where the No-show travel lines exist.
5. Compare the output against the rules for that scheduler type.

</details>
