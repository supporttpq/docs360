---
description: >-
  Validate how Tourpaq Office applies CH1P1 and CH2P1 child prices in a booking
  with 2 adults and 3 children using extra beds, including totals with insurance
  and pickup.
---

# CH1P1 & CH2P1 used in a booking with 3 children using extra beds

## Overview

This page explains how **Tourpaq Office** applies child pricing when a booking includes **2 adults and 3 children**, and **each child uses an extra bed**.

It validates that booking totals match the **Price List** values:

* Adult price: `P1`
* Child prices: `CH1P1` and `CH2P1`

In this scenario, `CH2P1` can be used more than once (child 2+ pricing).

## Purpose

Confirm that child pricing logic is applied consistently across:

* **Booking**
* **Price List**
* Web views (if applicable in your setup)

When the booking is created, Tourpaq references the matching **Price List entry (PLTA ID)** and uses:

* **P1** – Price per adult
* **CH1P1**, **CH2P1** – Child prices for the first and second extra beds
* **CH1D1**, **CH2D1** – Associated discounts
* **CPM1**, **CH1PA / CH2PA** – Child profit margin and child adjustments (if used)

## Validation result

When the booking is completed for **2 adults and 3 children**, each with an extra bed:

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

The system calculates the base accommodation + transport total as:

`Total (base) = (P1 × 2 adults) + CH1P1 + CH2P1 + CH2P1`

Example (illustrative):

* `P1 = 1249`
* `CH1P1 = 500`
* `CH2P1 = 250`

`Total (base) = (1249 × 2) + 500 + 250 + 250 = 3498 DKK`

If you also add per-passenger products (for example insurance and pickup point), they are added on top:

* Insurance = `306 × 5` pax
* Pickup point = `100 × 5` pax

`Total (with add-ons) = 3498 + (306 × 5) + (100 × 5) = 5528 DKK`

* Each child occupying an extra bed is charged based on the corresponding child pricing logic:
  * The **first child** uses **CH1P1**
  * The **second and third children** use **CH2P1**
*   The final **Total Amount** displayed in the booking matches the calculated total from the Price List.

    <figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
* Any configured discount and margin logic (for example `CH1D1`, `CH2D1`, `CPM1`, `CH1PA`, `CH2PA`) is included in the underlying computation.

This confirms that:

* The **Price List and booking modules** share identical calculation logic.
* Multiple child passengers can correctly use repeated **CH2P1** pricing when applicable.
* The displayed booking total remains consistent across all system views, ensuring pricing accuracy for both administrators and agents.

## FAQ

#### Why is CH2P1 used twice for 3 children?

Because `CH1P1` is for the first child.

`CH2P1` is the “child 2+” price and can be applied to additional children.

#### Does this total include discounts (CH1D1/CH2D1)?

The booking total reflects the active pricing logic for the selected setup.

Use the Price List entry to verify whether the booking uses `CH…P…` or `CH…D…` values for the period.

#### Where do I verify the values used in the calculation?

Open **Price List** for the same hotel, room, departure date, and stay length.

Enable the child column groups and compare `P1`, `CH1P1`, and `CH2P1`.

#### What if the totals do not match between booking and Price List?

Common causes:

* The booking is using a different PLTA entry (different date, room, or stay).
* Some add-ons are per pax and were not included in the comparison.
* Child adjustments (`CH1PA` / `CH2PA`) or discounts are active for the period.
* The Price List values were edited after the booking was created.

#### What if the hotel does not have extra bed capacity for children?

Then this scenario cannot be reproduced.

The room type must allow extra beds for children for the stay period.
