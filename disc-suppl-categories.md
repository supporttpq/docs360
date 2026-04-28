# Disc/Suppl Categories

The **Discount Supplement Categories** section in BookingX allows administrators to manage and classify supplemental charges or discounts applied to bookings. These can include additional services, room preferences, change fees.

<figure><img src=".gitbook/assets/image (9) (2).png" alt=""><figcaption></figcaption></figure>

### Overview Table

The list contains predefined supplement or discount categories with the following attributes:

| Column               | Description                                                                                                                                      |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Code**             | A unique short identifier used in the system for internal reference or automation logic.                                                         |
| **Category Name**    | The descriptive name of the discount or supplement category. Displayed for internal or customer visibility based on settings.                    |
| **Use in Extra Sum** | <p>Indicates whether this supplement should be included in the total calculation of extras. Marked with:<br>✅ = Included<br>❌ = Not included</p> |
| **Behavior on Web**  | Specifies the display behavior of the category in the web booking process.                                                                       |

### Creating a New Category

Click the **Create** button in the top-right to add a new category.

<figure><img src=".gitbook/assets/image (762).png" alt=""><figcaption></figcaption></figure>

#### Required Fields:

* **Code** – Must be unique.
* **Round Rule** - If a round rule is specified, then it is applied to the price before it is used in a booking. If the price is a per-day price, the round rule is applied after the full price for the booking is calculated.
* **Hide as filters on lists** - Hide the disc / suppl category in the lists throughout the system.
* **Status** - Select the category status (Visible / Hidden)
* **Category Name** – Should clearly describe the type of discount or supplement.
* **Use in Extra Sum** – Define whether this category contributes to the extra total.
* **Web Behavior** – Choose visibility logic
* **Description -** When changing a disc/suppl category's description, please test the change on Web Booking using a different browser, since a session cache is in place, or test after 30 minutes of inactivity on Web Booking.

### Rounding on Extras & Discount/Supplements

#### Overview

This functionality introduces rounding rules for **Discount/Supplement categories**, ensuring that sales prices generated during contract import or booking calculations are consistent and commercially correct.

It extends the existing rounding logic already available in **System Settings (Profit margin round rule)** and makes it applicable at the category level.

#### Purpose

When contracts are imported, **Board supplements** and **Single supplements** are automatically created, including both cost and sales prices. However, these prices may not always align with desired commercial rounding standards.

The purpose of this feature is to:

* Ensure consistent price rounding across the system
* Avoid incorrect or non-standard pricing (e.g., 123.47 instead of 125)
* Apply rounding automatically during booking calculations and in the booking engine

#### Where It Applies

Rounding rules are applied in the following areas:

* Extras pricing
* Discount/Supplement pricing
* Booking Engine
* Elastic (search and pricing layer)

#### System Behavior

#### General Rule

If a **Round Rule** is defined on the category,  it is always applied before the price is used in a booking

#### Per-Day Pricing

If the price is defined per da&#x79;**,** the system first calculates the total booking price:

* ```
  total = price_per_day × number_of_days
  ```
* Then applies the rounding rule on the final value

#### Booking Engine & Elastic

* Rounding is always applied when a discount or supplement is calculated
* Ensures consistency between:
  * Back-office calculations
  * Front-end (booking engine) pricing
  * Elastic search results

#### **Configuration**

#### Extras Setup > Disc/Suppl Categories

**Behavior**

* Applies to all discounts and supplements in the category
* Same rounding logic as Extras Categories

**Tooltip (blue info icon)**

```
If a round rule is specified, then it is applied to the price before it is used in a booking. If the price is a per-day price, the round rule is applied after the full price for the booking is calculated.
```

### Related Pages

* [Profit Margin Round Rule (System Settings)](profit-margin-rules.md)
* [Discount and Supplement](discounts-supplements.md)
