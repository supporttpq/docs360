---
description: >-
  When there are more eligible rules, the system will choose the lowest rule
  from the table
---

# Generic Product Price Rules

#### Overview

The **Generic Product Price Rules** page allows administrators to configure pricing logic for generic products (extras). These rules determine how product prices vary based on factors such as booking periods, allotments, agencies, and other time- or cost-based conditions.

When multiple price rules overlap, the system automatically applies the most specific one. For example:

* A rule defined for a **specific brand** takes priority over one defined for **all brands** within the same period.

#### Purpose

This functionality ensures accurate and flexible pricing for generic products by allowing companies to:

* Adjust prices dynamically according to booking conditions.
* Manage exceptions or brand-specific pricing.
* Maintain consistent and automated pricing behavior across all extras.

<figure><img src=".gitbook/assets/image (278).png" alt=""><figcaption></figcaption></figure>

### Interface Fields Explained

| Field                     | Description                                                                                                                                                                                                                                                                                                                    |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Name**                  | A label or description of the pricing rule                                                                                                                                                                                                                                                                                     |
| **Product**               | The product or extra that this rule is applied to. Dropdown to select from available extras.                                                                                                                                                                                                                                   |
| **Booking Start / End**   | Time range when the rule becomes valid for bookings. Useful for seasonal pricing or campaign periods.                                                                                                                                                                                                                          |
| **Allotment Start / End** | Defines a valid travel or stay window for the product rule to apply.                                                                                                                                                                                                                                                           |
| **All. Time Start / End** | Restricts the time of day when the rule is active                                                                                                                                                                                                                                                                              |
| **Agency**                | Restricts the rule to a specific agency or for all agencies. When a guide selects "All brands" it will help him to save time when creating Excursions that are for sale in more or all brands in their company, also minimize  the risk of errors that may occur when the same excursion is created separately for each brand. |
| **Price**                 | Base price charged to the customer.                                                                                                                                                                                                                                                                                            |
| **Child Price**           | Special pricing for children (can be set to `0` if not applicable).                                                                                                                                                                                                                                                            |
| **Cost**                  | Cost associated with the product.                                                                                                                                                                                                                                                                                              |
| **Enabled**               | Checkbox to toggle the rule's activity (green = enabled).                                                                                                                                                                                                                                                                      |
| **Order**                 | Use the arrows to prioritize or reorder rules (useful when multiple rules overlap).                                                                                                                                                                                                                                            |

**Interface Fields Explained**

* **Show Disabled:** Enables or disables the display of inactive or paused rules.
* **Create:** Opens a new form to manually add a price rule for a generic product.

**Additional Notes**

* Always verify overlapping date ranges to ensure the correct rule is applied.
* Use specific filters (e.g., brand or agency) whenever possible to achieve precise control over pricing behavior.
