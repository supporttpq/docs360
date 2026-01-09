# Child Price in Price List

### Overview

Some hotels define special child prices that are valid only up to a certain age, for example up to 12 years.\
If this age limit is not respected, child prices may be incorrectly applied to older passengers, such as youths aged 16 or 17. This results in incorrect cost calculation and reduced profit.

This documentation describes how **Child Price (CH)** is determined in the **Price List** and how pricing is validated during booking.

***

### Purpose

The purpose of this behavior is to ensure that:

* Child prices are applied only when the passenger is within the allowed child age range
* Hotel-specific child age rules are respected
* A brand-level fallback is used when a hotel does not define its own child age limit
* Pricing is recalculated correctly when passenger age changes
* The existing **Child Profit Margin** company feature continues to work as expected

***

### Scope and Applicability

This behavior applies only to companies where **Child Profit Margin** is enabled (set by Super Administrator).

It does **not** change or affect:

* Existing child price logic used by other setups, such as other company child pricing
* Non-child-related pricing rules

***

### Child Age Determination Logic

When calculating whether **Child Price (CH)** applies, the system determines the maximum allowed child age using the following order:

1.  **Hotel-level child age limit**

    * Defined in:\
      `Hotel > Basic Setup > Additional Settings`

    <figure><img src="../../../.gitbook/assets/image (565).png" alt=""><figcaption></figcaption></figure>

    * If set, this value always takes priority
2. **Brand-level child age limit (fallback)**

<figure><img src="../../../.gitbook/assets/image (566).png" alt=""><figcaption></figcaption></figure>

* Used only if the hotel has no child age configured
* Ensures pricing still works for hotels without a specific rule

***

### Pricing Rules

Child Price (CH) is applied only when:

* Passenger age is **less than or equal to** the determined child age limit\
  (hotel limit first, brand limit as fallback)

If the passenger age exceeds the limit:

* Adult price is applied
* Child price is not used, even if CH exists in the Price List

***

### Price List Behavior

#### Child Price (CH)

* Child Price entries in the Price List are no longer applied purely based on passenger type
* The child age limit must be respected
* This prevents child pricing from being applied to older passengers incorrectly

***

### Booking Validation

#### Office Booking

When a booking agent changes a passenger’s age and saves the passengers:

* The system re-evaluates child eligibility
* Pricing is recalculated immediately
* Child Price is applied or removed based on the updated age

***

#### Web Booking

When a customer changes a passenger’s age and saves the passengers:

* The same validation logic is applied
* Pricing is recalculated before the booking continues
* The customer always sees the correct price based on age rules

***

### Acceptance Criteria

The solution is considered complete when:

* The system first checks for a hotel-specific child age limit
* If none exists, the brand-level child age limit is used
* Child Price (CH) is applied only when the passenger age is within the allowed range
* Pricing is recalculated whenever passenger age is entered or modified
* The Child Profit Margin company feature continues to function without regression

***

### Result

This ensures accurate pricing, correct cost calculation, and protects expected profit margins while still supporting hotels that do not define their own child age policy.

### FAQ&#x20;

**When is Child Price (CH) applied?**\
Child Price is applied only when the passenger’s age is less than or equal to the allowed child age limit.

**Which child age limit does the system use?**\
Tourpaq first checks the child age limit defined on the hotel. If no hotel value exists, the system uses the maximum child age defined on the Brand.

**What happens if a passenger is older than the allowed child age?**\
The Child Price is not applied. The passenger is priced as an adult.

**When is pricing recalculated?**\
Pricing is recalculated whenever a passenger’s age is entered or changed and the passenger details are saved, both in Office Booking and Web Booking.

**Does this affect all child pricing setups?**\
No. This behavior applies only to companies using the Child Profit Margin feature. Other child pricing models are not impacted.

**Do agents need to manually update prices after changing an age?**\
No. The system automatically recalculates pricing when passenger details are saved.

