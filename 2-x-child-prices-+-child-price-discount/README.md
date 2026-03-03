---
description: >-
  Enable two child prices (CH1/CH2) and child price discounts in the Tourpaq
  Office Price List using the Child Profit Margin feature.
---

# 2 x Child prices + Child price discount

## Overview

Tourpaq Office can maintain **two child prices** in the **Price List**:

* **CH1…** for child 1 (for example `CH1P1`, `CH1D1`)
* **CH2…** for child 2 (for example `CH2P1`, `CH2D1`)

This is enabled by the **Child Profit Margin** feature.

Only a **Super Administrator** can enable the feature at company level.

### Key behavior

* The **child profit margin** setup applies to both child price sets (CH1 and CH2).
* You can still adjust CH1 and CH2 separately using child adjustments.

## Child prices in the Price List

### What you get

When enabled, Price List users can:

* Maintain two child price columns (CH1 and CH2).
* See how child adjustments, discounts, and margins affect the child prices.
* Improve yield management for families and multi-child bookings.

### Enable the feature (Super Administrator)

1. Open **Companies**.
2. Open the company configuration.
3. Go to **Feature Access**.
4. Under **Yield Management**, enable **Child Profit Margin**.
5. Save.

After enabling, the Price List can show extra child-related columns.

### Show the child columns in Price List

In **Price List**, open the column visibility menu (three-dot menu in the table header).

Enable the relevant column groups:

* **CHILD PRICES**
* **CHILD PROFIT PRICES**
* **CHILD PROFIT MARGIN**
* **CHILD ADJUSTMENTS**
* **CHILD DISCOUNTS**
* **CHILD PROFIT DISCOUNT PRICES**

<figure><img src="../.gitbook/assets/image (635).png" alt=""><figcaption></figcaption></figure>

### Child price fields (most common)

Once enabled, you will see new child pricing fields. The most used ones are:

* **Child prices**: `CH1P1`, `CH2P1` (and other intervals where shown).
* **Child adjustments**: `CH1PA`, `CH2PA`.
* **Child profit margin**: `CPM1` (and other intervals where shown).
* **Child discount prices**: `CH1D1`, `CH2D1`.
* **Child profit discount prices**: `CH1PD1`, `CH2PD1`.

<figure><img src="../.gitbook/assets/image (637).png" alt=""><figcaption></figcaption></figure>

These columns help you validate child price logic and troubleshoot booking price results.

## Purpose and benefits

* Separate handling for child pricing improves pricing accuracy for family bookings.
* Better transparency for how child discounts affect margin.
* Easier troubleshooting of CH1/CH2 pricing differences.

## FAQ

### What is the “Child Profit Margin” feature?

It enables additional child pricing fields in the Price List.

It also enables two child price sets (CH1 and CH2) with child discount prices.

### Why do I have CH1 and CH2 prices?

They let you price two children separately in the same room.

This is useful when children have different discount logic or adjustments.

### Is the child profit margin different for CH1 and CH2?

No. The configured child profit margin applies to both.

You can still adjust CH1 and CH2 using `CH1PA` and `CH2PA`.

### Where do I enable the child columns in the Price List?

Open the column visibility menu (three dots in the grid header).

Enable the **CHILD …** column groups.

### Why can I see the offer, but not book it?

If the selling price is `0` (or missing), the offer can be visible.

It cannot be booked in Web Booking or Tourpaq Office.

### I enabled the feature, but I still cannot see CH1/CH2 columns. What should I check?

* The feature is enabled for the correct company.
* Your user role has access to Price List.
* The column groups are enabled in the column visibility menu.

### Does this page explain how CH1P1/CH2P1 are calculated?

It explains how to enable and display the fields.

For calculation details, see:

* [Child Price](../booking/new-booking/child-price/)
* [Child Price in Price List](../booking/new-booking/child-price/child-price-in-price-list.md)
