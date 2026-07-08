---
description: >-
  How Tourpaq Office calculates CH1D1/CH2D1 child discount prices in Price List
  using extra bed cost, nights, early booking discount, CPM1, transport cost,
  and adjustments.
---

# How CH1D1 & CH2D1 is calculated in Price List

## Overview

This page explains how **CH1D1** and **CH2D1** are displayed and calculated in **Tourpaq Office → Price List**.

These fields are the **child discount prices** for interval 1 (D1).

The calculation depends on:

* **Extra bed cost** from the hotel (child cost price)
* **Number of nights** (stay length)
* **Early booking discount** (if configured)
* **Child profit margin** (`CPM1`)
* **Transport cost**
* **Child adjustments** (`CH1PA`, `CH2PA`)

## Prerequisites

To view and validate the child discount calculations, you need:

* Have **Administrator** access.
* Have the company feature **Child Profit Margin** enabled (Super Administrator action).
* Enable the relevant child columns in the Price List grid.

## Show child discount columns in Price List

In **Price List**, open the column visibility menu (three-dot icon in the table header).

Enable these column groups:

* **CHILD 1 PRICES**
* **CHILD 2+ PRICES**
* **CHILD 1 DISCOUNTS**
* **CHILD 2 DISCOUNTS**
* **CHILD PROFIT MARGIN**
* **ADJUSTMENTS**

<figure><img src="../.gitbook/assets/image (635).png" alt=""><figcaption></figcaption></figure>

Common fields used when validating the discount calculation:

* **Child prices**: `CH1P1`, `CH2P1`
* **Child discount prices**: `CH1D1`, `CH2D1`
* **Child profit margin**: `CPM1`
* **Child adjustments**: `CH1PA`, `CH2PA`

<figure><img src="../.gitbook/assets/image (637).png" alt=""><figcaption></figcaption></figure>

## Calculation logic

### CH1D1 (child 1 discount price)

The **CH1D1** column represents the discount-adjusted value for the first child and is calculated as:

`CH1D1 = (extra bed cost × nights) - early booking discount + CPM1 + transport cost - CH1PA`

<figure><img src="../.gitbook/assets/image (647).png" alt=""><figcaption></figcaption></figure>

This formula uses the hotel’s extra bed cost for the full stay.

It then applies early booking discount logic and adds margin and transport cost.

`CH1PA` is included as an adjustment input and can be positive or negative.

### CH2D1 (child 2+ discount price)

The **CH2D1** column follows a similar structure but applies the second child’s extra bed cost:

`CH2D1 = (extra bed cost (2nd) × nights) - early booking discount + CPM1 + transport cost - CH2PA`

<figure><img src="../.gitbook/assets/image (648).png" alt=""><figcaption></figcaption></figure>

This ensures both discount prices follow the same logic, but can use different extra bed cost inputs.

## Purpose and usage

Use `CH1D1` and `CH2D1` to validate that child discount prices:

* Use the correct extra bed cost and stay length.
* Apply early booking discount as expected.
* Include the configured margin (`CPM1`) and transport cost.

{% hint style="info" %}
`CH1D1` / `CH2D1` are discount prices (D1).

They are not the same as `CH1P1` / `CH2P1` (P1).
{% endhint %}
