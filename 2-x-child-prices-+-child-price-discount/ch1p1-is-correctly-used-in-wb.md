# CH1P1 is correctly used in WB

#### **Overview**

This document describes the test scenario for validating that **child pricing data** — including **CH1P1**, **CH2P1**, **CH1D1**, **CH2D1**, and **CPM1** — from the **Price List** is correctly applied during the **web booking process**.\
It ensures consistency between the **web booking price** and the **final price displayed in the Tourpaq application**.

***

#### **Prerequisites**

* **Administrator access** to Tourpaq.
* A **Price List entry (PLTA ID)** for a **double room with one extra bed**.
* Child pricing fields populated with valid values:
  * **CH1P1** – Child 1 Price
  * **CH2P1** – Child 2 Price
  * **CH1D1**, **CH2D1** – Child Discounts
  * **CPM1** – Child Profit Margin
* Access to both the **Web Booking** page and the **Tourpaq App**.

***

#### **Price List Validation**

Access the **Price List** page and search for entries matching a **double room with one extra bed**.\
Confirm that all relevant child pricing fields (**CH1P1**, **CH2P1**, **CH1D1**, **CH2D1**, **CPM1**) contain valid values.\
If **CPM1** is empty, enter the correct value and save.

<figure><img src="../.gitbook/assets/image (459).png" alt=""><figcaption></figcaption></figure>

Once validated, open the **PLTA ID** in the web booking interface to begin the booking process.

***

#### **Web Booking Flow**

Start by adding customer (Rejsebestiller) information, followed by **2 adults and one child** in the **Rejsedeltagere** section.\
When the prices are initially displayed:

*   Both passengers temporarily reflect the **adult price (P1)**.&#x20;

    <figure><img src="../.gitbook/assets/image (460).png" alt=""><figcaption></figcaption></figure>
* The **Rabat** field then applies the corresponding **child discount**, automatically adjusting the total.\
  The discount label clearly identifies it as a **child discount**.

Continue through the booking by selecting **insurance options** (Forsikring, Afbestillingsforsikring) and proceeding to the **Summary (Opsummering)** page.&#x20;

<figure><img src="../.gitbook/assets/image (461).png" alt=""><figcaption></figcaption></figure>

\
After confirming and submitting the booking, decline any optional offers to complete the process and generate the **receipt (Kvittering)** page.

<figure><img src="../.gitbook/assets/image (462).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (463).png" alt=""><figcaption></figcaption></figure>

***

#### **Validation in Tourpaq**

Copy the booking number from the **Kvittering** page and open it in the **Tourpaq application**.\
The **Booking Details** page should reflect the same pricing as seen in the web booking.

<figure><img src="../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

This confirms that:

* **CH1P1** and related child pricing fields are correctly sourced from the Price List.
* **Child discounts (Rabat)** are applied accurately during the web booking flow.
* The final total remains **identical** between the web interface and the Tourpaq app.

***

#### **Conclusion**

The test validates the correct implementation of **child pricing logic** in web bookings.\
It confirms that the **CH1P1**, **CH2P1**, and **CPM1** fields directly influence pricing calculations, ensuring a consistent and transparent experience across both **web** and **back-office** environments.
