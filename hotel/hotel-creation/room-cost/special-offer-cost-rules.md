---
description: >-
  Configure promotional hotel cost rules that can override standard room cost
  rules.
---

# Special Offer Cost Rules

### **Overview**

Special Offer Costs are advanced rules defined by hotel owners that can override any other cost rules configured for a hotel. These rules are designed to manage promotional pricing strategies such as discounts, free nights, or early booking benefits.

**Purpose**\
The purpose of Special Offer rules is to provide flexibility for hotels to apply promotional pricing conditions that take precedence over standard cost rules. This ensures accurate cost handling while allowing hotels to incentivize bookings through discounts or stay-based offers.

<figure><img src="../../../.gitbook/assets/image (318).png" alt=""><figcaption></figcaption></figure>

#### Types of Special Offer Rules

There are four types of rules available:

1. **Room Cost** – Adjusts the base room cost.
2. **Extra Bed Cost** – Applies a discount or adjustment to extra beds.
3. **Early Booking (EB)** – Provides discounts for bookings made in advance.
4. **Stay and Pay (S\&P)** – Offers free nights or reduced costs based on length of stay (e.g., _Stay 7 nights, Pay 5_).

#### Rule Configuration and Filters

* **Approved** – The rule must be approved before it can be applied.
* **Rule Type** – Select the rule type (_Room Cost, Extra Bed Cost, Stay & Pay, Early Booking_).
  * If set to **Early Booking**, the **Board** field becomes available, displaying all board types defined in the company. For other rule types, the field is disabled.
* **Board Types**:
  * Assigned under **Basic Setup > Board Supplements**.
  * Passengers must select a product with the desired board type.
  * If a rule includes a board filter, it only applies when **all passengers in the same room** share the same board type.
  * If different board types exist in one room, the rule is not applied.
  * If no board type filter exists, the rule applies only to passengers with **no board type** selected.

**Date and Time Filters:**

* **Stay Start / Stay End Dates** – Define the stay period when the offer applies.
* **Booking Start / Booking End Dates** – Specify when the booking must be created.
* **Days Before Arrival** – Apply the offer only if the booking is made a certain number of days in advance.
* **Days of the Week** – Restrict validity to selected weekdays (_only for Stay & Pay or Early Booking rules_).

**Room and Price Filters:**

* **Room** – Apply to one or multiple room types.
* **Price per Interval** – Define a cost or discount for each time interval.
* **Per Day** (checkbox) – If enabled, the price is applied per day instead of per interval.
* **Normal Price** (checkbox) – If enabled, the rule behaves as a fixed price rather than a discount.
* **Per Pax** (checkbox) – If enabled, the rule applies per passenger.
* **Percent** (checkbox) – If enabled, the value is treated as a percentage rather than a fixed amount.

**Special Options:**

* **Add to Default Rule (Early Booking only)** – If enabled, the Special Offer EB rule is added on top of the contract EB rule instead of replacing it:
  1. The contract EB rule is applied first.
  2. The Special Offer EB rule is then applied to the resulting value.
* **Stay / Pay Duration** – Define the length of the stay and the payable duration (e.g., _Stay 7, Pay 5_).
* **Combine with Early Booking** – Defines whether an EB rule can be combined with an S\&P rule. If disabled, EB overrides S\&P.
* **Combine with Stay & Pay** – Defines whether an S\&P rule can be combined with an EB rule. If disabled, S\&P overrides EB.
* **From Age / To Age** – Apply the rule only to passengers within the defined age range. Leave empty to allow all ages.

### Related pages

* [Room cost](./)
* [Early Booking Cost Discount Rules](early-booking-cost-discount-rules/)
* [Stay and Pay Cost Rules](stay-and-pay-cost-rules.md)
