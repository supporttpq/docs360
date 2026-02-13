# Add Base Cost on Real Transports

### Overview

A new field named **Base Cost** is introduced on Real Transport departures.

The Base Cost field allows a fixed transport cost to be defined on a Real Transport departure. When specified, this cost is used in the Price List calculation instead of the calculated seat cost.

Base Cost affects pricing only. It does not change the actual operational seat cost used in bookings.

The Base Cost provides pricing stability and ensures margin rules are not impacted by operational seat cost fluctuations.

<figure><img src="../../.gitbook/assets/image (628).png" alt=""><figcaption></figcaption></figure>

### Purpose

This feature allows price calculation to use a fixed transport cost in the price list, independent of:

* Load factor
* Guaranteed seat cost
* Allotment seat cost
* Pro-rate seat cost

It provides pricing stability while preserving operational seat cost logic in bookings.

### Field Description

#### BASE COST

Defines a fixed transport cost used when calculating Price List P and D prices.

If Base Cost is specified:

* It overrides Guaranteed, Allotment and Pro-rate seat costs in the Price List
* The Load Factor does not affect this value

If Base Cost is empty:

* The system uses the current transport cost calculation logic

{% hint style="info" %}
If a base cost is specified, it will be used as the transport cost when calculating the price in the price list. The load factor will not impact the base cost.

The transport cost used in a booking is the actual cost of a seat (calculated based on the load factor, etc.).
{% endhint %}

### Price List Behavior

#### P and D Prices

When calculating P1–P4 and D1–D4 prices:

* If Base Cost is defined, it is used as the transport cost
* If Base Cost is empty, the system uses the calculated seat cost

#### Mixed Leg Scenario

If:

* Outbound real transport has Base Cost defined
* Return real transport does not

Then:

* Outbound leg uses Base Cost
* Return leg uses the calculated seat cost

Total transport cost in the Price List equals: Outbound Base Cost + Return Calculated Cost

Each leg is evaluated independently.

#### Profit Prices

Profit Prices (PP1–PP4) and Profit Discount Prices (PD1–PD4) continue to use the Actual Cost including Load Factor.

Base Cost is not used for profit calculations.

### Booking Behavior

Base Cost does not affect bookings.

The transport cost used in a booking is always the actual seat cost calculated based on load factor and cost structure.

Base Cost does not impact booking cost calculation.

This ensures:

* Commercial pricing stability
* Operational cost accuracy
