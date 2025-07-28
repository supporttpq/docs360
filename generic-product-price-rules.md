---
description: >-
  When there are more eligible rules, the system will choose the lowest rule
  from the table
---

# Generic Product Price Rules

This page allows administrators to define **pricing rules** for generic products based on **booking periods, allotments, agencies**, and other time-based or cost-based filters. These rules determine how and when a specific extra (product) is priced differently.

If there are two price rules with overlapping periods, then the most precise price rule wins. A price rule that selects only one brand wins over a price rule that selects more than one brand.(e.g.: if there are 2 price rules: one defined as "all brands" and the other one defined as "specific brand", and the intervals are overlapping, it will take the most specific one (the one set up on the brand))

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

### Other Features

* **Show Disabled** – Toggle to reveal rules that have been disabled or paused.
* **Create** – Button to add a new rule manually.
