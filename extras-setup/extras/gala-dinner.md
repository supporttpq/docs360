# Gala Dinner

## **Overview**

Many hotels apply a mandatory **Gala Dinner surcharge** on specific dates such as **25 December** or **31 December**. While hotels often justify this by adding minor enhancements (e.g., sparkling wine or small upgrades), guests may feel disappointed if the surcharge appears explicitly on their travel documents.

To prevent guest dissatisfaction and reduce service cases, Tourpaq now supports **including mandatory extras (such as Gala Dinner) in the basic price** and **hiding them from the e-ticket**.

## **Purpose**

The goal is to:

* Ensure guests **pay for the mandatory Gala Dinner** without it appearing explicitly as a separate extra on the ticket.
* Prevent negative customer expectations that arise when the Gala Dinner appears as a paid add-on but does not match expectations.
* Provide flexible configuration options for hiding extras both:
  * **As individual extras**, or
  * **By hiding an entire category**.

## **Expected Behavior**

#### **Customer Outcome**

* The guest **will still pay for the Gala Dinner**.
* The Gala Dinner **will not appear**:
  * in Web Booking,
  * in Customer Centre, or
  * on the e-ticket (when configured).
* The cost of the Gala Dinner will instead be **merged into the Basic Price** of the booking.
* The booking total remains correct and includes the Gala Dinner cost.

## **Specifications**

### 1. **Extras – New “Include In Basic Price” Option**

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

### 2. **Extras Category – New “Hide on Ticket” Option**

**Location - Extras Setup → Extras Category → Settings box**

**New Field -** **Hide on Ticket** (checkbox), located below “Ticket Category”.

**Behavior**

When checked:

* All extras in this category are **hidden on the e-ticket**.
* Only supported on **E-ticket Version 3**.
* Often used together with **Include In Basic Price** on Extras.

**Tooltip (blue info icon)**

> _If checked, this will hide the extras on the e-ticket. This is supported by e-ticket version 3 only._

### 3. **Booking Engine**&#x20;

#### **Behavior**

When an extra has “Include in Basic Price” enabled:

* Its price is **added automatically to the Basic Price** of the booking.
* The extra **does not appear** as a selectable or visible component for the customer.
* Booking totals and price calculations **must reflect** the increased base price.

## **Summary**

| Feature                    | Location                    | Effect                                                                        |
| -------------------------- | --------------------------- | ----------------------------------------------------------------------------- |
| **Include In Basic Price** | Extras → Behaviour Settings | Extra is hidden in Web Booking & Customer Centre. Price added to Basic Price. |
| **Hide on Ticket**         | Extras Category → Settings  | Extra is hidden from the e-ticket (V3 only).                                  |
| **Booking Engine Support** | System                      | Extra cost merged into Basic Price automatically.                             |

***

## **Typical Use Case: Gala Dinner**

To configure Gala Dinner so the guest pays for it but **does not see it as a separate charge**:

1.  Create an Extra for the Gala Dinner.&#x20;

    <figure><img src="../../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
2.  Check **Include In Basic Price** on the Extra.&#x20;

    <figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>
3.  Assign the Extra to a category dedicated for Gala Dinner.

    <figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
4.  Enable **Hide on Ticket** on the Gala Dinner category.&#x20;

    <figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>
5. The booking engine will merge the Gala Dinner price into the Basic Price.

Result:

✔ Guest pays the correct total\
✔ Gala Dinner is invisible in booking flows\
✔ No confusing extra line on the e-ticket\
✔ Less risk of customer dissatisfaction
