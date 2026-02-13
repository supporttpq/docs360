# Add Base Cost on Real Transports

### Overview

A new field named **Base Cost** is introduced on Real Transport departures.

This field allows separation between:

* The operational seat cost, subject to load factor and contract adjustments.
* A fixed commercial cost used exclusively for price list calculations.

The Base Cost provides pricing stability and ensures margin rules are not impacted by operational seat cost fluctuations.

<figure><img src="../../.gitbook/assets/image (628).png" alt=""><figcaption></figcaption></figure>

### Purpose

The feature enables commercial control over pricing logic by:

* Decoupling operational seat cost from sales margin calculation.
* Ensuring price list calculations remain stable even if contracted seat cost changes.
* Allowing controlled pricing strategies independent of transport cost fluctuations.

#### When Base Cost is defined

* The Base Cost overrides:
  * Guaranteed seat cost
  * Allotment seat cost
  * Pro-rate seat cost
* It is used only for:
  * Price list P prices
  * Price list D prices
* It is not impacted by load factor.

#### When Base Cost is empty

* The system follows existing behaviour.
* The actual seat cost including load factor is used.

## Price List

The price list logic is updated to support Base Cost.

#### P1–P4 and D1–D4

If Base Cost exists:

* Use Base Cost in price calculation.

If Base Cost is empty:

* Use current calculation logic.

#### Profit Prices (PP1–PP4)

Profit Prices continue to use:

* Actual cost
* Including load factor
* Not Base Cost

## Booking Logic

The transport cost used in a booking is always:

Actual seat cost calculated based on load factor and contract rules.

Base Cost does not impact booking cost calculation.

This ensures:

* Commercial pricing stability
* Operational cost accuracy

***

## Outbound / Return Combination

Each leg is evaluated independently.

If:

* Outbound Real Transport has Base Cost
* Return Real Transport does not

Then:

* Outbound uses Base Cost
* Return uses existing cost calculation

Total transport cost = Outbound cost + Return cost
