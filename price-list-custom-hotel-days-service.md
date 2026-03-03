---
description: >-
  Set up Tourpaq Office Custom Hotel Days price lists for hotel-only stays and
  custom night counts without transport packages. Configure rooms, sales period,
  prices, and tiered profit margin rules.
---

# Price List Custom Hotel days Service

## Overview

**Custom Hotel Days** lets you sell **hotel-only stays** in Tourpaq Office.

It creates price list lines without a transport package, fixed quota, or fixed departure setup. Use it for custom night counts and standalone accommodation sales.

## Purpose

The purpose of this feature is to:

* Enable brands (agencies) to sell **hotel-only stays** or **custom night counts**.
* Offer flexibility to customers who may not require a full transport + hotel package.
* Control availability and pricing independent of transport schedules.

<figure><img src=".gitbook/assets/image (9) (1) (3) (1).png" alt=""><figcaption></figcaption></figure>

## Instructions

1. Navigate to **Price List → Custom Hotel Days**.
2. Click the **Create** button.
3. Fill in the required fields:
   * **Agency** – Select the agency/brand responsible for the setup.
   * **Country / Arrival / Resort / Hotel** – Choose the location and hotel details.
   * **Rooms** – Select room types and configure allotments.
   * **Departure Start / Departure Stop** – Define the sales period for the price list.
4. Enable or disable the price list using the **Enabled** toggle.
5. Click **View Prices** to define or adjust hotel prices for the selected period.
6. Save the configuration.

Manage created entries in the list view. You can review prices, availability, and status.

## Profit margin rules (field explanations)

<figure><img src=".gitbook/assets/image (10) (1) (3) (1).png" alt=""><figcaption></figcaption></figure>

#### **Profit Margin**

Profit added on top of the base room cost.

* If **Is Percent** is enabled, the value is a percentage.
  * Example: `15` means **+15%**.
* If **Is Percent** is disabled, the value is a fixed amount.
  * Example: `15` means **+15 currency units**.

#### **Is Percent (checkbox)**

* Defines how the **Profit Margin** should be applied.
* **Checked:** Applied as a **percentage** of the room cost.
* **Unchecked:** Applied as a **fixed amount**.

#### **Room Cost Start**

Minimum base room cost for the rule.

Example: If set to `1`, the rule applies from `1` and up.

#### **Room Cost End**

Maximum base room cost for the rule.

Example: If set to `2000`, the rule applies up to `2000`.

#### **Add Price (button)**

Adds another profit margin rule row for a different cost range.

Example:

* Rule 1: `15%` for `1–2000`
* Rule 2: `10%` for `2001–5000`

#### **Save (button)**

Saves the rule setup.

#### **Trash/Delete Icon**

Deletes a rule row.

This setup supports **tiered profit margin rules** based on room cost ranges.
