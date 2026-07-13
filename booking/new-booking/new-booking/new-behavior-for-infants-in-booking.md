# New behavior for infants in booking

## Overview

This new feature makes infant handling consistent with all other passenger types throughout the booking lifecycle.

Previously, infants were treated differently in several areas of Tourpaq. They were excluded from deposit calculations, did not automatically receive cancellation fees, and could not purchase Extras. These differences required manual intervention from sales staff and limited the booking options available for infants.

With this enhancement, infants participate in the same booking logic as other passengers wherever applicable.

***

## Purpose

This feature improves consistency across the booking process by ensuring that infants:

* Are included in deposit calculations.
* Follow the same cancellation rules as other passengers.
* Can purchase Extras when the configured age restrictions allow it.

The result is a more predictable booking flow, fewer manual corrections, and identical behaviour between Back Office and Web Booking.

***

## How it is configured

The feature uses the existing configuration already available in Tourpaq.

#### Deposit rules

Infants are now included in the deposit calculation.

The system uses the same deposit logic for infants as for any other passenger. If the configured deposit rules require a percentage or fixed amount based on the booking value, the infant's price is included in the calculation.

#### Result

* Infant prices contribute to the total booking value.
* Deposit amounts are calculated consistently for all passengers.
* No manual adjustment is required.

#### Cancellation rules

Cancellation fees for infants are calculated using the existing cancellation rules configured for the brand. No separate infant cancellation setup is required.

When a booking or an individual infant is cancelled, the system calculates the cancellation fee according to the cancellation rules configured for the selected brand.

#### Result

* Infant cancellation fees are calculated automatically.
* Brand-specific cancellation policies are respected.
* Manual correction after cancellation is no longer necessary.

#### Extra configuration

Extras become available for infants based on their configured age interval.

To make an Extra available for infants, configure the Extra price with an age range that includes **0 years**.

Infants can now purchase Extras in both **New Booking** and **Web Booking**.

This allows optional services such as:

* Baby stroller
* Baggage
* Infant equipment
* Any other Extra configured for infant ages

### Age validation

An Extra is only available for an infant when its age configuration includes infant ages.

The availability follows the existing age validation used for children.

For example:

| Extra                  | Age range  | Available for infants |
| ---------------------- | ---------- | --------------------- |
| Baby stroller          | 0-2 years  | Yes                   |
| Infant baggage         | 0-1 years  | Yes                   |
| Child activity package | 2-11 years | No                    |
| Adult golf bag         | 18+ years  | No                    |

If the Extra does not include age **0 years**, it is not displayed for infants.

### Where it applies

The new behaviour is available in:

* New Booking
* Web Booking

The same age validation rules are applied in both booking flows.

***

## How it works

### Deposit calculation

Infants are now treated as passengers when the booking deposit is calculated.

If the infant has a price, that amount contributes to the booking value used for the deposit calculation.

#### Example

A booking contains:

| Passenger | Price |
| --------- | ----: |
| Adult     |  €800 |
| Adult     |  €800 |
| Child     |  €500 |
| Infant    |  €100 |

Total booking value: **€2,200**

If the configured deposit is **25%**, Tourpaq calculates the deposit from the full booking value, including the infant.

Required deposit: **€550**

***

### Cancellation handling

Infants now follow the same cancellation process as every other passenger.

When a booking or an individual infant is cancelled, Tourpaq automatically calculates the cancellation fee according to the brand's configured cancellation rules.

This removes the need for manual fee adjustments after cancellation.

#### Example

A booking contains:

* 2 Adults
* 1 Child
* 1 Infant

The booking has been fully paid.

The infant is cancelled before departure.

Tourpaq automatically applies the configured cancellation policy to the infant and calculates the appropriate cancellation fee.

***

### Extras

Infants can now purchase Extras in the same way as other passengers.

An Extra is available only when its configured age interval includes infants.

#### Example

A booking contains one infant aged **8 months**.

The following Extras are configured:

| Extra           | Age range  | Result        |
| --------------- | ---------- | ------------- |
| Baby stroller   | 0-2 years  | Available     |
| Checked baggage | 0-99 years | Available     |
| Kids Club       | 4-12 years | Not available |

Only the Extras matching the infant's age are presented for selection.

***

## Where the feature is available

### Back Office (New Booking)

During booking creation, infants behave like other passengers.

The system:

* Includes infants in the deposit calculation.
* Calculates cancellation fees for infants.
* Displays eligible Extras for infants based on age.

#### Example

A sales agent creates a booking containing two adults and one infant.

When opening the **Extras** step, the infant can be assigned a stroller and checked baggage because both Extras are configured for age **0 years and above**.

***

### Web Booking

Customers creating bookings online experience the same behaviour as in Back Office.

The booking engine automatically:

* Includes infant prices in deposit calculations.
* Displays infant-eligible Extras.
* Applies the same cancellation logic after booking creation.

#### Example

A customer books a holiday with an infant.

During the Extras step, a **Baby Stroller** option appears because its age configuration includes infants, while child-only activities are hidden.

***

### Reporting and financial calculations

Because infants are now included in standard booking calculations, all financial values generated from the booking reflect the infant's participation.

This includes:

* Deposit calculations.
* Cancellation fee calculations.
* Total booking value.
* Revenue generated by infant Extras.

No manual adjustments are required after booking creation or cancellation.

#### Example

A booking includes:

* 2 Adults
* 1 Infant
* Infant baggage (€30)

The booking total, deposit amount, cancellation calculations, and financial reporting all include both the infant fare and the purchased Extra, ensuring that the booking value accurately reflects every passenger.
