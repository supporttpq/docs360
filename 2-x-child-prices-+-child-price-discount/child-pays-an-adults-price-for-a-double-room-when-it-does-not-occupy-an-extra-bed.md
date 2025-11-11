# Child pays an adult's price for a double room when it does not occupy an extra bed

#### **Overview**

This document explains the system behavior when a booking is made for one adult and one child sharing a **standard double room**. In such cases, the child is charged the same rate as the adult, regardless of any child pricing configurations. This ensures consistency between the **Price List** and the **booking total**.

***

#### **Prerequisites**

To verify this behavior, the following conditions must be met:

* User has **Administrator** access.
* The following features are enabled:
  * **Child Prices**
  * **Child Discounts**
  * **Child Profit Margin**
  * **Adjustments**
* At least one hotel offers **standard double room** availability.

***

#### **Booking Setup and Pricing Behavior**

A booking is created for **1 adult and 1 child**, both assigned to a **standard double room**.\
Since the child does not occupy an extra bed, the system automatically applies the **adult price (P1)** to both passengers.

<figure><img src="../.gitbook/assets/image (457).png" alt=""><figcaption></figcaption></figure>

Once the booking is saved and allotment is confirmed:

* The **Total Amount** in the booking confirmation reflects the same rate for both passengers.
* In the **Total per passenger** section of the booking, both the adult and child show identical pricing.
* The **CH1P1** (child price) column is not used in the total calculation.

<figure><img src="../.gitbook/assets/image (458).png" alt=""><figcaption></figcaption></figure>

This behavior ensures pricing alignment when no child-specific bed or discount applies.

***

#### **Price List Verification**

In the **Price List** page:

* Apply filters corresponding to the booking details.
* Display columns related to child pricing:
  * **CH1P1**, **CH2P1** (child prices)
  * **CH1D1**, **CH2D1** (child discounts)
  * **CH1%**, **CMP1**, **PA1**

The data confirms that **CH1P1** is **not used** in price computation for this type of booking.\
Instead, the system consistently references **P1**, the adult base price, for both passengers.

***

#### **Validation Result**

When a child shares a **double room** without requiring an **extra bed**, the system treats the child as a second adult for pricing purposes.

* **CH1P1 is ignored.**
* **P1** is applied to both passengers.

This logic ensures fair and predictable pricing in scenarios where a child shares standard accommodation space with an adult.
