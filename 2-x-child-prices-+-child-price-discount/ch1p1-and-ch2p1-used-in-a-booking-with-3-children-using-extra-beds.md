# CH1P1 & Ch2P1 used in a booking with 3 children using extra beds

### **Overview**

This document describes how the system applies child pricing for bookings that include two adults and three children, where each child occupies an extra bed.\
The scenario validates that the total booking amount correctly reflects the combined use of adult and child-specific pricing values from the Price List.\
The calculation involves the standard adult price (P1) together with the configured child pricing values (**CH1P1** and **CH2P1**), ensuring that all cost components — including child discounts, profit margins, and adjustments — are accurately represented.

***

### **Purpose**

The purpose of this validation is to confirm that the **Price List child pricing logic** is correctly applied when multiple children with extra beds are included in the same booking.\
When the booking is created, the system automatically references the active price list entry (PLTA ID) and retrieves:

* **P1** – Price per adult
* **CH1P1**, **CH2P1** – Child prices for the first and second extra beds
* **CH1D1**, **CH2D1** – Associated discounts
* **CH1%**, **CMP1**, **PA1** – Child price percentage, profit margin, and adjustment values

The platform ensures that these pricing components are used consistently in both the booking calculation and the price list view, maintaining transparent pricing alignment.

***

### **Validation Result**

When the booking is completed for **2 adults and 3 children**, each with an extra bed:

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (3).png" alt=""><figcaption></figcaption></figure>

* The system calculates the total amount using the following formula without extras and insurance:\
  **Total = (P1 × 2 Adults) + CH1P1 + CH2P1 + CH2P1**

**In our example, the total amount without extras and insurance = (1249 x 2) + 500 + 250 + 250 = 2498 + 1000 = 3498DKK.**&#x20;

**When we add the insurance and pickup point, the total amount = 2498 + (306 x 5) + (100 x 5) = 2498 + 1530 + 1000 = 5528 DKK**

* Each child occupying an extra bed is charged based on the corresponding child pricing logic:
  * The **first child** uses **CH1P1**
  * The **second and third children** use **CH2P1**
*   The final **Total Amount** displayed in the booking matches the calculated total from the Price List.&#x20;

    <figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>
* Any configured **discounts (CH1D1, CH2D1)** or **profit margins (CMP1)** are automatically included in the underlying price computation.

This confirms that:

* The **Price List and booking modules** share identical calculation logic.
* Multiple child passengers can correctly use repeated **CH2P1** pricing when applicable.
* The displayed booking total remains consistent across all system views, ensuring pricing accuracy for both administrators and agents.
