---
description: >-
  Set up Tourpaq Office price lists. Create/copy by brand, transport, fix quota,
  hotel, and room. Manage PLTA lines, P1–P4, discounts, and allotment filters.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# Pricelist Setup

Only administrators can access **Pricelist Setup**.

See also: [Pricelist](pricelist.md).

## Overview

Use **Pricelist Setup** to:

* Create new **Tourpaq Office price lists** for a transport + hotel + room combination.
* Copy prices and discounts across departures and related price lists.
* Maintain price list lines (PLTA) with prices, discounts, child prices, and one-way prices.
* Filter by **allotment type** (Allotment vs Guarantee/Secured) and selling logic.

## Create or copy a price list

### Create price lists

Create price lists in the **Price List** tab. Click **Create/Copy Price List**.

1. **Select Brand** – Choose the brand for which the price list will be available.
2. **Select Transport** – Choose the transport option for the price list.
3. **Set Fix Quota** – Select the transport’s fixed quota.
4. **Select Hotel** – Choose the hotel that will use the price list.
5. **Select Rooms** – Specify the rooms to include in the price list.

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Not created prices (missing price lists)

Use **Not created prices** to identify **missing price lists** for selected criteria.

Common reasons:

1. The **fix quota** does not cover the hotel allotment period.
2. Required **transport or hotel setup** is missing (for example, allotments).

<figure><img src="../.gitbook/assets/image (36) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Copy a price list

The **Copy Price List** feature allows users to duplicate price lists **within the same brand**.

### Steps to Copy a Price List

1. **Select Source** – Choose the **Transport**, **Hotel**, **Room**, and **Date** from which the price list will be copied.
2. **Select Destination** – Choose the **Transport**, **Hotel**, **Room**, and **Date** to which the prices will be copied.
3. **Different Days** – Set the day offset between source and destination. Use this if:
   * The transport’s fixed quota does not match, or
   * You want to extend the price list by a specific number of days.
4. **Adjust Prices and Discounts** – Use the **Change Discounts for Original Prices** and **PRICE DIFFERENCE** sections to modify values as needed.
5. **Copy Options** – Checkboxes allow copying prices from:
   * A transport to all transports of the brand.
   * A hotel to all hotels assigned to the transport.
   * A room to all rooms of a hotel.
6. **Important:** Select all checkboxes in **PRICE DIFFERENCE**, even when values are `0`.
7. **Execute Copy** – Click **Copy Prices**.
8. **Save Discounts** – Click **Save Changed Discounts** to finalize.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Field-by-Field Explanation

#### Filters (top section)

* **Departure date**: Travel date range to display. Example: `03-03-2025` to `03-03-2025`.
* **Resorts**: Filter by resort.
* **Transports**: Filter by transport (flight, bus, etc.).
* **Transport type**: Filter by transport/seat type.
* **Hotels**: Filter by hotel.
* **Allotment type**: All rooms, Allotment, or Guarantee/Secured.
* **Room**: Filter by room type.
* **Fix quotas**: Limit results to a fixed quota contract.
* **Display names**: Show hotel names in the grid.
* **Stay Length**: Nights/stay length filter.

A price list is blank when first created.

<figure><img src="../.gitbook/assets/image (41) (1).png" alt=""><figcaption></figcaption></figure>

You must then enter the required values. Some fields auto-fill based on formulas and existing values. A filled price list looks like this:

<figure><img src="../.gitbook/assets/image (632).png" alt=""><figcaption></figcaption></figure>

#### Price list grid fields (PLTA lines)

* **Tools (row icons)**:
  * **Show/Hide History**: See changes for the price list line.
  * **Reset price list in API v4.1**: Clears cached price list data.
  * **Recalculate FHA**: Recalculates Free Hotel Allotment (FHA) on demand.
* **PLTA ID**: Unique identifier for the price list line.
* **Hotel / Room / Dep. date / Stays**: Context fields. Mostly auto-filled.
* **FHA / FTA**: Free Hotel Allotment and Free Transport Allotment. Auto-filled.
* **P1–P4**: Selling prices per interval. Entered manually unless rules fill them.
* **PP1–PP4**: Profit forecast for P1–P4. Auto-calculated.
* **D1–D4**: Discount prices (used in web booking when configured). Entered manually.
* **PD1–PD4**: Profit forecast for D1–D4. Auto-calculated.
* **G1–G4 / PG1–PG4**: Group prices and profit forecast.
* **CH1P1–CH1P4**: Child prices per interval.
* **CH%**: Calculates child prices as a percentage of P prices.
* **POWO / POWH**: One-way outbound / homebound prices.
* **GPOWO / GPOWH / CPOWO / CPOWH / DPOWO / DPOWH**: One-way group/child/discount fields.
* **DEBD / DEBDPD**: Disable extra bed discount (all price types, or discount only).
* **CPM1–CPM4**: Child profit margin per interval.
* **M1–M4**: Max rooms per transport per interval.
* **PM1–PM4 / PM%**: Profit margin values and percentage.
* **PA1–PA4 / C1PA / C2PA**: Price adjustments (adult/child).
* **WL / HD / FB / NFIS**: Waitlist, hot deal, Facebook, not for internet sale.
* **1W / 2W**: Booked one week / two weeks before.
* **PL. REG. RULE. / TR R Rule / LOWP1–LOWP4**: Price regulation and transport regulation rule fields.
* **GR / GS**: Guarantee room / guarantee seats flags.
* **TP (Transport Price)**: Used by percent-based extra bed discount rules. It affects the base used for discount calculations.
* **TAG / TAG CH / STATUS / HNI1–HNI4**: Operational tagging and hotel name interval fields.

{% hint style="info" %}
#### Room type display logic for the Allotment filter

**Principle**

The type shown in filters must reflect the **effective allotment that will be consumed next**, not only the technical configuration.

This ensures that the filter behavior matches operational reality and user expectations.

**Functional rule**

**1) Guarantee/Secured allotment has priority**

If both **Guarantee/Secured allotment** and **Allotment** exist for the same room type, the system consumes:

1. Guarantee/Secured allotment first
2. Allotment after guarantee is exhausted

**2) Display rule in filters**

**Case A: Guarantee Allotment Still Available**

If Guarantee/Secured allotment > 0:

* The room type is treated as **Guarantee**
* It shall NOT appear when filtering by **Allotment**
* It shall appear when filtering by **Guarantee**

Reason: The next booking will consume guarantee allotment.

**Case B: Guarantee Allotment Fully Consumed**

If Guarantee/Secured allotment = 0 and Allotment > 0:

* The room type is treated as **Allotment**
* It shall appear when filtering by **Allotment**
* It shall no longer be considered Guarantee

Reason: The next booking will consume allotment.

**Rationale**

The filter must reflect the **current effective selling logic**, not just the configured allotment types.

This ensures that users selecting the Allotment filter only see rooms that will actually consume allotment.
{% endhint %}

### Tabs

Below the filters are the following tabs:

**Prices** – Contains the price list grid (PLTA lines).

**Discounts** – Contains discounts inherited from the hotel.

<figure><img src="../.gitbook/assets/image (42) (1).png" alt=""><figcaption></figcaption></figure>

**Column filters** – Controls which columns show in **Prices**. Unchecked fields are hidden.

<figure><img src="../.gitbook/assets/image (633).png" alt=""><figcaption></figcaption></figure>

Filter categories:

* Price - display prices per intervals, as well as PLTA ID (price list transport allotment ID)
* Profit Price - display profit forecasts for prices per intervals
* Disc price - display discount prices per intervals
* Profit disc. price - display profit forecasts for discount prices per intervals
* Gr. prices - display group prices per intervals
* Profit gr. prices - display profit forecasts for group prices per intervals
* Ch. prices - display child prices per intervals
* Max rooms - display max number of rooms per intervals
* Low. reg. prices - lowest value of price regulation rules
*   Generic filters

    * P. Ch. - increase/decrease prices per interval
    * Hide average profit - hides average real profit per pax
    * TP - transport price

    ⚠️ **Warning:** Some extra bed discount setups use **TP (Transport Price)** as input. Validate your results after edits.

    * GR - guarantee rooms
    * GS - guarantee seats
* Regulation rules - display price regulation rule filters
* Other tools
  * Waitlist
  * Hot Deal
  * Facebook
* OW Prices - display one way price filters

### Alternative hotel name

You can set an **alternative hotel name** for specific departures.

<figure><img src="../.gitbook/assets/image (634).png" alt=""><figcaption></figcaption></figure>

The alternative name also appears on the ticket.

In Tourpaq Office, it replaces the standard hotel name.

## P. Ch. (Price Change)

The **P. Ch.** column adjusts values relative to the current price in a column.

<figure><img src="../.gitbook/assets/image (46) (1).png" alt=""><figcaption></figcaption></figure>

When you select a row in **P. Ch.**, more options appear at the top.

* **Pr. Change**: Column to modify.
* **Value**: Value to add to the current value.
  * Example: If `P1 = 1000` and `Value = 200`, then `P1` becomes `1200`.
* **Run**: Applies the change in the grid. Running again applies the change again.

**Difference from Price** is only available for discount columns. It makes discount values relative to the matching P column (D1→P1, D2→P2, etc.).

<figure><img src="../.gitbook/assets/image (47) (1).png" alt=""><figcaption></figcaption></figure>

When **Difference from Price** is checked, **Run** calculates discount values by subtracting the configured value from the matching P price.

Example: If `P1 = 2000` and `Value = 200`, then `D1 = 1800` after **Run**. Click **Save** to persist changes.

### FAQ

#### How do I create a new price list?

Use **Create/Copy Price List**, then select brand, transport, fix quota, hotel, and rooms.

#### Why is a price list not created?

This usually happens when fix quotas do not cover the hotel allotment period or required data is missing.

#### Can I copy an existing price list?

Yes. You can copy prices from an existing price list within the same brand.

#### What copy scopes are available?

You can copy prices from one transport to all brand transports, from one hotel to all hotels on a transport, or from one room to all rooms of a hotel.

#### What must be selected before copying prices?

All checkboxes in **Price Difference** should be selected, even if the values are zero.

#### What filters are available in Pricelist Setup?

You can filter by departure date, resort, transport, transport type, hotel, allotment type, room, fix quota, hotel name, and stay length.

#### Why do no rows appear after filtering?

Common causes are missing brand context, incorrect date range, or no price lists created for the selected criteria.

#### What information is shown in the price list grid?

The grid shows hotel, room, departure date, free hotel and transport allotments, selling prices (P1–P4), child prices, group prices, discounts, and profit-related fields.

#### How are child prices calculated?

Child prices can be entered directly. They can also be calculated as a percentage of adult prices using **CH%** columns.
