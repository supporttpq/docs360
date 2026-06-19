# Discount Extra Beds

### Overview

The **Extra Bed Discounts** feature lets administrators define discounts for passengers using **extra beds**.

You can target both children and adults using age rules. You can also define different discounts per extra bed (up to four).

### Purpose

Use this to:

* Discount passengers who occupy extra beds.
* Automate price reductions based on rules.
* Vary discounts by age, stay dates, booking dates, room type, transport, and period.
* Keep pricing consistent across seasons and configurations.

This reduces manual corrections and keeps booking totals consistent.

{% hint style="info" %}
Extra-bed discounts are only applied when a passenger is actually assigned to an extra bed in the room allocation.
{% endhint %}

<figure><img src="../../.gitbook/assets/disc extra bed.png" alt=""><figcaption></figcaption></figure>

### Field Explanations

* **Age** – The passenger's age to which the rule applies to.
* **Start Date / End Date** – Stay dates where the discount is valid.
* &#x20;B**ooking Start/End -** Booking interval (interval dates when the bookings are made and the discount is valid)
* **Discount columns** – Discount values per extra bed:
  * **1st** – First extra bed
  * **2nd** – Second extra bed (optional)
  * **3rd** – Third extra bed (optional)
  * **4th** – Fourth extra bed (optional)
* **% (Percent)** – Apply the values as percentages (example: `10` = 10%).
* **Discount type**
  * **FHC** – Calculated from profit (works with Price Margin Service).
  * **H (Hidden)** – Distributes the average discount per passenger in the room.
  * **HP (Hotel Price)** – Percentage calculated from the hotel price.
  * **PD (Per Day)** – Apply the discount per day instead of per interval.
* **Room Type** – Room types the rule applies to.
* **Transports** – Transports the rule applies to.
* **Period** – The period the rule applies to.
* **Delete** – Removes the discount row.
* **Create** – Adds a new discount row.
* **Removed Discounts** – Shows removed rules for audit or restoration.

<figure><img src="../../.gitbook/assets/image (509).png" alt=""><figcaption></figcaption></figure>

* **Show All** – Displays all discount rows, regardless of filtering.

***

### Instructions for Use

1. Navigate to the **Extra Bed Discounts** section in the Hotel Menu.
2. Click **Create**.
3. Set the **Age** rule (example: 2–11 years).
4. Set **Start Date / End Date** for the stay.
5. Set **Booking Start / End Date** (optional).
6. Enter discount values for the relevant extra beds (1st–4th).
7. Choose **%**, **PD**, and **Discount type** as needed.
8. Select the **Room Type**, **Transports**, and **Period** filters.
9. Save.

Once configured, the system automatically calculates and applies the appropriate discount when a booking meets all criteria.

### Example use case

A hotel gives the following discounts for children:

* Ages **2–11**
* Valid for stays from **01-01-2025 to 31-12-2025**
* Booking period between **01-07-2024 and 01-12-2025**
* First child: **2000 DKK discount**
* Only applies to **CPHKGS70** transport
* Valid for all room types
* Assigned to **Period 1**

***
