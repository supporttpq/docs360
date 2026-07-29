---
description: >-
  When there are more eligible rules, the system will choose the lowest rule
  from the table
---

# Generic Product Price Rules

## Generic Product Price Rules

### Overview

The **Generic Product Price Rules** page configures pricing for generic products (extras). These rules vary product prices by booking periods, allotments, agencies, and other conditions.

When multiple price rules overlap, the system automatically applies the most specific one. For example:

* A rule defined for a **specific brand** takes priority over one defined for **all brands** within the same period.

### Purpose

This functionality ensures accurate and flexible pricing for generic products by allowing companies to:

* Adjust prices dynamically according to booking conditions.
* Manage exceptions or brand-specific pricing.
* Maintain consistent and automated pricing behavior across all extras.

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (278).png" alt="Generic Product Price Rules table"><figcaption></figcaption></figure></div>

### Interface fields explained

| Field                     | Description                                                                                                                                                             |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**                  | A label or description of the pricing rule                                                                                                                              |
| **Product**               | The product or extra that this rule is applied to. Dropdown to select from available extras.                                                                            |
| **Booking Start / End**   | Time range when the rule becomes valid for bookings. Useful for seasonal pricing or campaign periods.                                                                   |
| **Allotment Start / End** | Defines a valid travel or stay window for the product rule to apply.                                                                                                    |
| **All. Time Start / End** | Restricts the time of day when the rule is active                                                                                                                       |
| **Agency**                | Restricts the rule to a specific agency or all agencies. Selecting "All brands" supports products sold across several brands. It also reduces duplicate product setups. |
| **Price**                 | Base price charged to the customer.                                                                                                                                     |
| **Child Price**           | Special pricing for children (can be set to `0` if not applicable).                                                                                                     |
| **Cost**                  | Cost associated with the product.                                                                                                                                       |
| **Enabled**               | Checkbox to toggle the rule's activity (green = enabled).                                                                                                               |
| **Order**                 | Use the arrows to prioritize or reorder rules (useful when multiple rules overlap).                                                                                     |

#### Actions

The page provides these actions:

* **Show Disabled**: Shows or hides inactive or paused rules.
* **Create**: Opens a form to add a generic product price rule.

### Additional notes

Use these practices to maintain predictable pricing:

* Verify overlapping date ranges before saving a rule.
* Use specific filters, such as brand or agency, for precise pricing control.
