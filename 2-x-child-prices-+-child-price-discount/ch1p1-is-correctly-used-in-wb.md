---
description: >-
  Validate that Web Booking uses CH1P1 child pricing from the Tourpaq Office
  Price List and matches the final booking total in Tourpaq.
---

# CH1P1 is correctly used in WB

## Overview

This page documents a test scenario to verify that **Web Booking** correctly uses child pricing from the **Tourpaq Office Price List**.

It focuses on `CH1P1` and related child fields (`CH2P1`, `CH1D1`, `CH2D1`, `CPM1`).

The goal is to ensure the **Web Booking total** matches the final total in Tourpaq.

## Prerequisites

* **Administrator access** to Tourpaq.
* A **Price List entry (PLTA ID)** for a **double room with one extra bed**.
* Child pricing fields populated with valid values:
  * **CH1P1** – Child 1 Price
  * **CH2P1** – Child 2 Price
  * **CH1D1**, **CH2D1** – Child Discounts
  * **CPM1** – Child Profit Margin
  * **CH1PA, CH2PA** – Child price adjustment
* Access to both **Web Booking** and **Tourpaq Office** (to open the booking after completion).

## Price List validation

Access the **Price List** page and search for entries matching a **double room with one extra bed**.\
Confirm that all relevant child pricing fields (**CH1P1**, **CH2P1**, **CH1D1**, **CH2D1**, **CPM1**) contain valid values.\
If **CPM1** is empty, enter the correct value and save.

<figure><img src="../.gitbook/assets/image (656).png" alt=""><figcaption></figcaption></figure>

Once validated, open the **PLTA ID** in the web booking interface to begin the booking process.

## Web Booking flow

Start by adding customer (Rejsebestiller) information.

Add **2 adults and 1 child** in **Rejsedeltagere**.

When the prices are initially displayed:

* Both passengers temporarily reflect the **adult price (P1)**.

<figure><img src="../.gitbook/assets/image (652).png" alt=""><figcaption></figcaption></figure>

The **Rabat** field then applies the corresponding **child discount**, automatically adjusting the total.

The discount label should clearly identify it as a child discount.

Continue by selecting insurance options (**Forsikring**, **Afbestillingsforsikring**).

Proceed to **Summary (Opsummering)**.

<figure><img src="../.gitbook/assets/image (654).png" alt=""><figcaption></figcaption></figure>

After confirming and submitting the booking, decline any optional offers to complete the process and generate the **receipt (Kvittering)** page.

<figure><img src="../.gitbook/assets/image (655).png" alt=""><figcaption></figcaption></figure>

## Validate in Tourpaq Office

Copy the booking number from the **Kvittering** page and open it in the **Tourpaq application**.\
The **Booking Details** page should reflect the same pricing as seen in the web booking.

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (3) (1).png" alt=""><figcaption></figcaption></figure>

This confirms that:

* **CH1P1** and related child pricing fields are correctly sourced from the Price List.
* **Child discounts (Rabat)** are applied accurately during the web booking flow.
* The final total remains **identical** between the web interface and the Tourpaq app.

## Conclusion

The test validates the correct implementation of **child pricing logic** in web bookings.\
It confirms that the **CH1P1**, **CH2P1**, and **CPM1** fields directly influence pricing calculations, ensuring a consistent and transparent experience across both **web** and **back-office** environments.

## FAQ

#### What does this test verify?

It verifies that Web Booking pulls child pricing (`CH1P1`, `CH2P1`, `CPM1`) from the Price List.

It also verifies that the final booking total matches in Tourpaq Office.

#### Why do passengers show the adult price first?

Web Booking can initially render base prices (P1) before applying the child discount logic.

After the calculation, the **Rabat** field should adjust the total.

#### What should I check if the totals do not match?

* The Price List entry is the one used by Web Booking (correct PLTA ID, hotel/room/date).
* `CH1P1` / `CH2P1` and `CPM1` are populated.
* The hotel extra bed cost and discount rules exist for the stay period.
* The booking uses the expected passenger mix (2 adults + 1 child).

#### Which fields matter most for this scenario?

Typically:

* `CH1P1` (child selling price)
* `CH1D1` (child discount price)
* `CPM1` (child profit margin)
* `CH1PA` (child adjustment, if used)
