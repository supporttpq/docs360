# Child Price in Price List

### Overview

Some hotels define special child prices that are valid only up to a certain age. Example: up to 12 years old.

If this age limit is not respected, child prices can be applied to older passengers. Example: passengers aged 16 or 17.\
This leads to incorrect cost calculations and reduced profit.

This page explains how **Child Price (CH)** is determined in the **Price List**, and how pricing is validated during booking.

### Purpose

This behavior ensures that:

* Child prices are applied only when the passenger is within the allowed child age range
* Hotel-specific child age rules are respected
* A brand-level fallback is used when a hotel does not define its own child age limit
* Pricing is recalculated correctly when the passenger age changes
* The **Child Profit Margin** feature continues to work as expected.

### Scope and Applicability

This behavior applies only to companies where **Child Profit Margin** is enabled (set by a super-admin).

It does **not** change or affect:

* Existing child price logic used by other setups, such as other company child pricing
* Non-child-related pricing rules

### Child Age Determination Logic

The age limits defined at the hotel level determine whether the **Child Price** from the price list applies to a booking.\
If no age limits are configured for the hotel, the system uses the **Max Child Age** defined in the brand settings to calculate the child price.

When calculating whether **Child Price (CH)** applies, the system determines the maximum allowed child age using the following order:

1.  **Hotel-level child age limit**

    * Defined in:\
      `Hotel > Basic Setup > Additional Settings`

    <figure><img src="../../../.gitbook/assets/image (565).png" alt=""><figcaption></figcaption></figure>

    * If set, this value always takes priority
2. **Brand-level child age limit (fallback)**&#x20;

*   Defined in `User  > Brands > Other Settings`&#x20;

    <figure><img src="../../../.gitbook/assets/image (601).png" alt=""><figcaption></figcaption></figure>
* Used only if the hotel has no child age configured
* Ensures pricing still works for hotels without a specific rule

### Pricing Rules

Child Price (CH) is applied only when:

* Passenger age is **less than or equal to** the determined child age limit\
  (hotel limit first, brand limit as fallback)

If the passenger age exceeds the limit:

* Adult price is applied
* Child price is not used, even if CH exists in the Price List

### Price List Behavior

#### Child Price (CH)

Child Price entries in the Price List are not applied purely based on passenger type. The child age limit must be respected. This prevents child pricing from being applied to older passengers.

### Booking Validation

#### Office Booking

When an agent changes a passenger’s age and saves the passenger details:

* The system re-evaluates child eligibility
* Pricing is recalculated immediately
* Child Price is applied or removed based on the updated age

#### Web Booking

When a customer changes a passenger’s age and saves the passenger details:

* The same validation logic is applied
* Pricing is recalculated before the booking continues
* The customer always sees the correct price based on age rules

### Result

This ensures accurate pricing and cost calculation.\
It also protects expected profit margins.\
Hotels without a defined child age policy are still supported.

### FAQ

**When is Child Price (CH) applied?**\
Child Price is applied only when the passenger’s age is less than or equal to the allowed child age limit.

**Which child age limit does the system use?**\
Tourpaq first checks the child age limit defined on the hotel.\
If no hotel value exists, the system uses the maximum child age defined on the brand.

**What happens if a passenger is older than the allowed child age?**\
The Child Price is not applied. The passenger is priced as an adult.

**When is pricing recalculated?**\
Pricing is recalculated whenever a passenger’s age is entered or changed and the passenger details are saved, both in Office Booking and Web Booking.

**Does this affect all child pricing setups?**\
No. This behavior applies only to companies using the Child Profit Margin feature. Other child pricing models are not impacted.

**Do agents need to manually update prices after changing an age?**\
No. The system automatically recalculates pricing when passenger details are saved.
