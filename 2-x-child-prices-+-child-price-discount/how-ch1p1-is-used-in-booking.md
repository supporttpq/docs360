# How CH1P1 is used in booking

#### **Overview**

This document explains how the **CH1P1** value (child price) is applied within bookings that include child passengers. It covers the required setup, validation in the **Price List**, and how the total booking amount is derived by combining adult and child prices.

***

#### **Prerequisites**

To perform this validation, ensure the following conditions are met:

* The user has **Administrator** access.
* At least one hotel in the system offers an **extra bed for children**.
* Access is granted to both **Booking Management** and the **Price List** page.
* The following feature flags are enabled:
  * **Child Prices**
  * **Child Discounts**
  * **Child Profit Margin**
  * **Adjustments**

***

#### **Booking Creation and Child Price Application**

A booking is created with one adult and one child, selecting a hotel that provides an extra bed option for children. Once the booking is completed and the allotment is taken, the system generates a **Total Amount** in the booking confirmation, which includes both adult and child pricing components.

<figure><img src="../.gitbook/assets/image (453).png" alt=""><figcaption></figcaption></figure>

The child price component used in this calculation corresponds to the **CH1P1** column in the **Price List**.

***

#### **Verifying CH1P1 in the Price List**

To confirm that the booking values align with the pricing setup:

* Access the **Price List** page.
* Filter results according to the hotel, travel dates, and booking details.
* Enable the following columns for visibility:
  * **CHILD 1 PRICES**
  * **CHILD 2 PRICES**
  * **CHILD 1 DISCOUNTS**
  * **CHILD 2 DISCOUNTS**
  * **CHILD PRICES %**
  * **CHILD PROFIT MARGIN**
  * **ADJUSTMENTS**

<figure><img src="../.gitbook/assets/image (454).png" alt=""><figcaption></figcaption></figure>

The displayed table should now include columns such as **CH1P1**, **CH2P1**, **CH1D1**, **CH2D1**, **CH1%**, **CMP1**, and **PA1**, representing the child price, discounts, percentages, and related adjustments.

<figure><img src="../.gitbook/assets/image (455).png" alt=""><figcaption></figcaption></figure>

***

#### **Calculation Logic**

The **Total Amount** displayed in the booking is calculated as:

Total Amount = P1 × Number of Adults + CH1P1

Ex: Total Amount = (5000 +306 (insurnace) + 100 (Pickup point) ) x 1 (no adults) + 500 (CH1P1) + 306 (insurance) + 100 (Pickup point) = 5406 x 1 + 906 = 6312 DKK&#x20;

<figure><img src="../.gitbook/assets/image (456).png" alt=""><figcaption></figcaption></figure>

Where:

* **P1** represents the base price per adult.
* **CH1P1** represents the price applied for the first child.

This formula ensures that the system accurately reflects the pricing breakdown between adult and child passengers.

***

#### **Conclusion**

The **CH1P1** value directly influences the total price of a booking containing child passengers. Verifying it in the **Price List** ensures consistency between backend pricing logic and the values displayed in bookings.\
This setup guarantees transparency, helping administrators and agents validate that child pricing is applied correctly across all bookings.
