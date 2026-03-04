---
description: >-
  Learn how Tourpaq Office applies CH1P1 child price from the Price List in
  bookings and how it affects the booking total for adults and children.
---

# How CH1P1 is used in booking

## Overview

This page explains how **CH1P1** (child price for child 1, interval P1) is applied in **Tourpaq Office bookings**.

It covers the required setup, how to validate the value in **Price List**, and how the booking total is calculated for adults and children.

## Prerequisites

To perform this validation, ensure the following conditions are met:

* The user has **Administrator** access.
* At least one hotel in the system offers an **extra bed for children**.
* Access is granted to both **Booking Management** and the **Price List** page.
* The company feature **Child Profit Margin** is enabled (Super Administrator action).

## Booking creation and child price application

A booking is created with one adult and one child, selecting a hotel that provides an extra bed option for children. Once the booking is completed and the allotment is taken, the system generates a **Total Amount** in the booking confirmation, which includes both adult and child pricing components.

<figure><img src="../.gitbook/assets/image (453).png" alt=""><figcaption></figcaption></figure>

The child price component used in this calculation corresponds to the **CH1P1** column in the **Price List**.

## Verify CH1P1 in the Price List

To confirm that the booking values align with the pricing setup:

* Access the **Price List** page.
* Filter results according to the hotel, travel dates, and booking details.
* Enable the following columns for visibility:
  * **CHILD 1 PRICES**
  * **CHILD 2+ PRICES**
  * **CHILD 1 DISCOUNTS**
  * **CHILD 2 DISCOUNTS**
  * **CHILD PROFIT MARGIN**
  * **ADJUSTMENTS**

<figure><img src="../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

The displayed table should now include columns such as:

* `CH1P1`, `CH2P1`
* `CH1D1`, `CH2D1`
* `CPM1`
* `CH1PA`, `CH2PA`

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Calculation logic

The booking total depends on multiple components (adult price, child price, extras, insurance, fees).

For the child price part, the key rule is:

`Child total = CH1P1` (for one child using child-1 pricing)

For an adult + child booking, a simplified view is:

`Total = (P1 × number of adults) + CH1P1 + extras/fees`

Example (illustrative):

* Adult price (`P1`) = 5000
* Insurance = 306
* Pickup point = 100
* Child price (`CH1P1`) = 500

`Total = (5000 × 1) + 500 + 306 + 100 = 5906`

<figure><img src="../.gitbook/assets/image (456).png" alt=""><figcaption></figcaption></figure>

Where:

* **P1** represents the base price per adult.
* **CH1P1** represents the price applied for the first child on interval 1.

This formula ensures that the system accurately reflects the pricing breakdown between adult and child passengers.

## Conclusion

The **CH1P1** value directly influences the total price of a booking containing child passengers. Verifying it in the **Price List** ensures consistency between backend pricing logic and the values displayed in bookings.\
This setup guarantees transparency, helping administrators and agents validate that child pricing is applied correctly across all bookings.

## FAQ

#### What is CH1P1?

`CH1P1` is the child selling price for **child 1** on interval **P1** in the Price List.

#### When is CH1P1 used in a booking?

When a booking includes a child passenger and the pricing setup uses child-1 pricing.

#### Why does my booking not use CH1P1?

Common causes:

* The booking has no child passenger assigned to a child price type.
* Child pricing features are not enabled for the company.
* The hotel/room setup does not allow extra bed for children for the dates.
* The relevant price list entry is missing for the departure/stay dates.

#### How do I validate which child price was used?

Open the matching Price List entry for the booking’s hotel/room/departure date.

Compare the booking total breakdown with the `CH1P1` value (and related fields like `CH1PA`).

#### What is the difference between CH1P1 and CH1D1?

`CH1P1` is the child's selling price (P1).

`CH1D1` is the child discount price (D1) and follows the discount calculation logic.
