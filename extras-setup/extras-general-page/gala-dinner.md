# Gala Dinner

## Gala Dinner

### Overview

Many hotels apply a mandatory **Gala Dinner surcharge** on specific dates such as **25 December** or **31 December**. While hotels often justify this by adding minor enhancements (e.g., sparkling wine or small upgrades), guests may feel disappointed if the surcharge appears explicitly on their travel documents.

To prevent guest dissatisfaction and reduce service cases, Tourpaq now supports **including mandatory extras (such as Gala Dinner) in the basic price** and **hiding them from the e-ticket**.

### Purpose

The goal is to:

* Ensure guests **pay for the mandatory Gala Dinner** without it appearing explicitly as a separate extra on the ticket.
* Prevent negative customer expectations that arise when the Gala Dinner appears as a paid add-on but does not match expectations.
* Provide flexible configuration options for hiding extras both:
  * **As individual extras**, or
  * **By hiding an entire category**.

### Expected behavior

#### Customer outcome

* The guest **still pays for the Gala Dinner**.
* The Gala Dinner **does not appear**:
  * in Web Booking,
  * in Customer Centre, or
  * on the e-ticket (when configured).
* The cost of the Gala Dinner instead **merges into the Basic Price** of the booking.
* The booking total remains correct and includes the Gala Dinner cost.

### Specifications

#### Extras: Include in Basic Price option

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Include in Basic Price option"><figcaption></figcaption></figure></div>

**Location - Extras Setup → Extras → Behaviour Settings**

**New Field -** **Include in Basic Price** (checkbox)

**Behavior:**

When checked:

* The extra **does not appear** to the customer in:
  * Web Booking
  * Customer Centre
* The price of the extra is **added to the Basic Price** of the booking.
* The booking’s **Total Amount** increases accordingly.
* The extra still counts financially, but remains **invisible** to the customer.

**Tooltip (blue info icon)**

> _If checked, this will hide the extras from the view of the customer in Web Booking and Customer Centre. It will, however, increase the base price and affect the booking total._

#### Extras Category: Hide for Customers option

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Hide for Customers option"><figcaption></figcaption></figure></div>

**Location - Extras Setup → Extras Category → Settings box**

**New Field -** **Hide for Customers** (checkbox), located below “Ticket Category”.

**Behavior**

When checked:

* All extras in this category are **hidden on the e-ticket**.
* Only supported on **E-ticket Version 3**.
* Often used together with **Include In Basic Price** on Extras.

**Tooltip (blue info icon)**

> _If checked, this will hide the extras on the e-ticket. This is supported by e-ticket version 3 only._

#### Booking Engine

**Behavior**

When an extra has “Include in Basic Price” enabled:

* Its price is **added automatically to the Basic Price** of the booking.
* The extra **does not appear** as a selectable or visible component for the customer.
* Booking totals and price calculations **must reflect** the increased base price.

#### Use Stay dates in prices

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Use Stay dates in prices option"><figcaption></figcaption></figure></div>

The **Use Stay dates in prices** option is available in the **Basic setup** tab when configuring an **Extra** such as a **Gala Dinner**. This option controls how the system interprets the date periods defined in the **Prices** tab.

When this option is enabled, the system evaluates the **stay dates of the booking** when determining which price rule should apply. This is typically required for extras that occur during a **specific date of the guest’s stay.**

**Use Stay dates in prices**

Checkbox located in: **Extras ->** **Basic setup → Other settings**

When enabled, the system evaluates the **stay dates of the booking** against the price periods defined in the **Prices** tab.

**Behavior when enabled**

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (4) (1) (1) (3).png" alt="Stay date price rule"><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Stay date price configuration"><figcaption></figcaption></figure></div>

* The correct price is selected based on the **stay period**, not the departure date.
* The extra applies only when the guest is **present at the hotel during the event date**.

**Behavior when disabled**

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Departure date price rule"><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1).png" alt="Departure date price configuration"><figcaption></figcaption></figure></div>

* The price rules are evaluated using **departure dates rather than stay dates**.
* This configuration is usually used for extras that are **not tied to a specific stay date**.

### Summary

| Feature                     | Location                    | Effect                                                                        |
| --------------------------- | --------------------------- | ----------------------------------------------------------------------------- |
| **Include In Basic Price**  | Extras → Behaviour Settings | Extra is hidden in Web Booking & Customer Centre. Price added to Basic Price. |
| **Hide on Ticket**          | Extras Category → Settings  | Extra is hidden from the e-ticket (V3 only).                                  |
| **Booking Engine Support**  | System                      | Extra cost merged into Basic Price automatically.                             |
| **Use Stay dates in price** | Extras -> Other settings    | The price is selected based on the **stay period**, not the departure date.   |

***

### Typical use case: Gala Dinner

To configure Gala Dinner so the guest pays for it but **does not see it as a separate charge**:

1.  Create an Extra for the Gala Dinner.

    <div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2).png" alt="Gala Dinner Extra"><figcaption></figcaption></figure></div>
2.  Check **Include In Basic Price** on the Extra.

    <div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Include In Basic Price checkbox"><figcaption></figcaption></figure></div>
3.  Assign the Extra to a category dedicated for Gala Dinner.

    <div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)   (5).png" alt="Gala Dinner category"><figcaption></figcaption></figure></div>
4.  Enable **Hide on Ticket** on the Gala Dinner category.

    <div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Hide on Ticket checkbox"><figcaption></figcaption></figure></div>
5. The booking engine merges the Gala Dinner price into the Basic Price.

Result:

✔ Guest pays the correct total\
✔ Gala Dinner is invisible in booking flows\
✔ No confusing extra line on the e-ticket\
✔ Less risk of customer dissatisfaction
