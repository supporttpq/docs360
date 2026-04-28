---
description: >-
  Understand how Tourpaq Office calculates child prices CH1P1 and CH2P1 in the
  Price List, including room cost per night, number of nights, transport cost,
  and child profit margin (CPM).
---

# How CH1P1 & CH2P1 are calculated in Price List

## Overview

This page explains how **CH1P1** and **CH2P1** are displayed and calculated in **Tourpaq Office → Price List**.

These fields show **child selling prices** per interval (for example P1).

The calculation uses:

* **Hotel room cost** (per pax, per night)
* **Number of nights** (stay length)
* **Transport cost**
* **Child profit margin** (`CPM1`)

## Show child price columns in Price List

In **Price List**, open the column visibility menu (three-dot icon in the table header).

Enable the relevant child column groups, for example:

* **CHILD 1 PRICES** and **CHILD 2+ PRICES**
* **CHILD PROFIT PRICES**
* **CHILD 1 DISCOUNTS** and **CHILD 2 DISCOUNTS**
* **CHILD PROFIT MARGIN**
* **CHILD ADJUSTMENTS**

<figure><img src="../.gitbook/assets/image (640).png" alt=""><figcaption></figcaption></figure>

Common child fields you will see after enabling the column groups:

* **Child prices**: `CH1P1`, `CH2P1`
* **Child profit margin**: `CPM1`
* **Child adjustments**: `CH1PA`, `CH2PA`
* **Child discount prices**: `CH1D1`, `CH2D1`
* **Child profit discount prices**: `CH1PD1`, `CH2PD1`

<figure><img src="../.gitbook/assets/image (637).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
You only need `CH1P1`, `CH2P1`, and `CPM1` to validate the base child price calculation.

Discount fields (`CH…D…`) are covered separately.
{% endhint %}

## Calculation logic (CH1P1 and CH2P1)

### Base formula

Both child price fields follow the same structure:

`CHxP1 = (Hotel room cost per pax per night × nights) + CPM1 + transport cost`

Where:

* `CHxP1` is either `CH1P1` or `CH2P1`
* `CPM1` is the **child profit margin** for interval 1

This ensures the child price reflects the stay cost plus margin and transport.

### Example

Room cost = 50 EUR per pax per night = 373.5 DKK per pax per night

<figure><img src="../.gitbook/assets/image (642).png" alt=""><figcaption></figcaption></figure>

Nights = 7

CPM1 = 100 DKK

<figure><img src="../.gitbook/assets/image (643).png" alt=""><figcaption></figcaption></figure>

Transport cost = 13094 DKK

<figure><img src="../.gitbook/assets/image (644).png" alt=""><figcaption></figcaption></figure>

`CH1P1 = (373.5 × 7) + 100 + 13094 = 15849 DKK`

### Child adjustments (CH1PA / CH2PA)

If you use child adjustments, they are added to the same base formula.

`CH1P1 = (room cost × nights) + CPM1 + transport cost + CH1PA`

`CH2P1 = (room cost × nights) + CPM1 + transport cost + CH2PA`

`CH1PA` and `CH2PA` accept **positive or negative** values.

<figure><img src="../.gitbook/assets/image (645).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Adjustments can trigger price recalculation logic that depends on underlying cost data.

If required costs are missing, adjustments may not behave as expected.
{% endhint %}

## Purpose and usage

Use `CH1P1` and `CH2P1` to validate that:

* Child prices follow the configured **child profit margin** (`CPM1`).
* Room cost and stay length are applied correctly.
* Transport cost is included as expected.

## FAQ

#### What are CH1P1 and CH2P1?

They are child selling prices in the Price List for interval 1 (P1).

CH1 typically represents child 1. CH2 represents child 2+.

#### Do CH1P1 and CH2P1 use different profit margins?

No. Both use the same child profit margin field for the interval (for example `CPM1`).

#### Where do I enable the CH1/CH2 columns?

Open the Price List grid’s column visibility menu (three dots).

Enable the **CHILD …** column groups.

#### Why are CH1P1 / CH2P1 blank or 0?

Common causes:

* Missing hotel cost data for the period.
* Missing transport cost data.
* The company feature for child profit margin is not enabled.
* The price list entry is not fully created for the date range.

#### Do child adjustments (CH1PA/CH2PA) affect CH1P1/CH2P1?

Yes. They are added to the base formula and can be positive or negative.
