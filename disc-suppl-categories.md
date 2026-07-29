# Disc/Suppl Categories

## Disc/Suppl Categories

The **Discount Supplement Categories** section in BookingX allows administrators to manage and classify supplemental charges or discounts applied to bookings. These can include additional services, room preferences, and change fees.

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (9) (2).png" alt="Disc/Suppl Categories overview table"><figcaption></figcaption></figure></div>

### Overview table

The list contains predefined supplement or discount categories with the following attributes:

| Column               | Description                                                                                                                                      |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Code**             | A unique short identifier used in the system for internal reference or automation logic.                                                         |
| **Category Name**    | The descriptive name of the discount or supplement category. Displayed for internal or customer visibility based on settings.                    |
| **Use in Extra Sum** | <p>Indicates whether this supplement should be included in the total calculation of extras. Marked with:<br>✅ = Included<br>❌ = Not included</p> |
| **Behavior on Web**  | Specifies the display behavior of the category in the web booking process.                                                                       |

### Create a new category

In **Disc/Suppl Categories**, click **Create** to add a category.

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (762).png" alt="Create Disc/Suppl Category page"><figcaption></figcaption></figure></div>

#### Required fields

* **Code** – Must be unique.
* **Round Rule** - Applies to the price before a booking uses it. For per-day prices, it applies after calculating the full booking price.
* **Hide as filters on lists** - Hides the Disc/Suppl Category in lists throughout the system.
* **Status** - Selects the category status: **Visible** or **Hidden**.
* **Category Name** – Should clearly describe the type of discount or supplement.
* **Use in Extra Sum** – Defines whether the category contributes to the extra total.
* **Web Behavior** – Chooses the visibility logic.
* **Description** - Test description changes in Web Booking using a different browser. Alternatively, wait 30 minutes without Web Booking activity.

### Rounding on Extras and Discount/Supplements

#### Overview

This functionality introduces rounding rules for **Discount/Supplement categories**, ensuring that sales prices generated during contract import or booking calculations are consistent and commercially correct.

It extends the existing rounding logic already available in **System Settings (Profit margin round rule)** and makes it applicable at the category level.

#### Purpose

When contracts are imported, **Board supplements** and **Single supplements** are automatically created, including both cost and sales prices. However, these prices may not always align with desired commercial rounding standards.

The purpose of this feature is to:

* Ensure consistent price rounding across the system
* Avoid incorrect or non-standard pricing (e.g., 123.47 instead of 125)
* Apply rounding automatically during booking calculations and in the booking engine

#### Where it applies

Rounding rules are applied in the following areas:

* Extras pricing
* Discount/Supplement pricing
* Booking Engine
* Elastic (search and pricing layer)

#### System behavior

**General rule**

If a **Round Rule** is defined on the category, it is always applied before the price is used in a booking.

**Per-day pricing**

If the price is defined per day, the system first calculates the total booking price:

*   The calculation is:

    ```
    total = price_per_day × number_of_days
    ```
* Then applies the rounding rule on the final value

**Booking Engine and Elastic**

* Rounding is always applied when a discount or supplement is calculated
* Ensures consistency between:
  * Back-office calculations
  * Front-end (booking engine) pricing
  * Elastic search results

#### Configuration

**Extras Setup → Disc/Suppl Categories**

**Behavior**

* Applies to all discounts and supplements in the category
* Same rounding logic as Extras Categories

**Tooltip**

```
If a round rule is specified, then it is applied to the price before it is used in a booking. If the price is a per-day price, the round rule is applied after the full price for the booking is calculated.
```

### Related pages

* [Profit Margin Round Rule (System Settings)](profit-margin-rules.md)
* [Discounts/Supplements combinations in Tourpaq](discounts-supplements/discounts-supplements.md)
