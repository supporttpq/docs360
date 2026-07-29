---
description: >-
  Understand how Tourpaq applies board types across the full stay during
  booking, including board changes, availability checks, closeouts, and
  supplement combinations.
---

# Board Behaviour During Booking

## Board behavior during booking

### Overview

This functionality defines how the system handles **board types (pension)** during the booking flow, especially in scenarios where:

* the board must remain consistent throughout the entire stay
* the board changes within the contract period
* availability or closeout restrictions exist on certain days

The goal is to ensure that the customer is offered a valid board option for the **entire stay**, not just partially.

***

### Customer outcome

The customer sees only board options that are valid for the entire booking period.

Example:

* The hotel offers:
  * BB for the first days
  * HB for the remaining days
* The system checks availability across the full stay and proposes:
  * HB for the entire stay (if possible via combination)

If no valid combination exists:

* the system offers no consistent board
* the system displays only individually available supplements

### Board consistency rule

A board can only be selected if:

* it is available for all days in the booking
* there is no closeout on any day

### Board type setup

#### Ordering board types

To support automatic upgrade/downgrade scenarios, board types must be ordered.

**Functionality:**

* Board types can be reordered
* Reordering is done via:
  * drag & drop or
  * arrow buttons

**UI placement:**

* Move arrows are located between **List Name** and the **Trash icon**.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (13).png" alt="Board Type order controls"><figcaption></figcaption></figure></div>

**Tooltip:**

> The order of Board types is used when the system has to downgrade or upgrade a board type automatically.\
> The board type with the highest order is considered the most expensive.

**Rules:**

* Highest order = highest board, for example `ALLINC`.
* Lowest order = lowest board, for example `HB`.

### Extras Category setting

#### All stay days must be available

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="All stay days must be available setting"><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Extras Category settings"><figcaption></figcaption></figure></div>

**Location:**

* **Extras Category** → **Settings**

**Visibility:**

Tourpaq shows this option only when:

* **Category type** = **Pension**
* **Category type** = **Gala dinner**

**Tooltip:**

> If selected, the extra is only eligible if it is available for the full booking period.

**Behavior:**

If enabled:

* the extra is eligible only if:
  * it has pricing for all days
  * it is not closed out on any day

Used for:

* Board supplements → enabled
* Gala dinner → optional

### Boards eligible for booking

A board supplement can only be selected if:

* it is available for all days of the booking
* it complies with the "All stay days must be available" rule

### Board basis changes during booking period

#### Problem

Some hotels have different board basis depending on the period (e.g. BB → HB)

#### System solution

**Step 1: Identify the main board**

* Select the board with the **highest order** within the booking period

**Step 2: Find supplements**

* Search for board supplements for days where the board differs from the main board

**Step 3: Build a combination**

*   Create a combination:

    * main board basis
    * supplements for differences

    <div data-with-frame="true"><figure><img src="../.gitbook/assets/image (803).png" alt="Board basis and supplement combination"><figcaption></figcaption></figure></div>

**Step 4: Validate**

The combination is valid only if:

* it covers all days
* all supplements are available

#### Fallback

If NO valid combination is found:

* the system stops trying to build a consistent board
* the system displays only individually available supplements

#### Ticket display

*   The system displays the main board (highest order)

    <div data-with-frame="true"><figure><img src="../.gitbook/assets/image (11).png" alt="Main board displayed in a ticket"><figcaption></figcaption></figure></div>

#### Pricing

*   The price:

    * includes all supplements
    * is aggregated into the base booking price

    <div data-with-frame="true"><figure><img src="../.gitbook/assets/image (804).png" alt="Booking price including board supplements"><figcaption></figcaption></figure></div>

### Backward compatibility

#### Identify existing board supplements

To preserve existing Board Supplement behavior after this update, all previously configured Board Supplements must be updated to enable **“All stay days must be available.”** at the **Extras Category** level.

This update applies only to extras that meet both of the following conditions:

* The extra uses an Extras Category with type **“Pension”**
* The setting **“Use Stay days in prices”** is enabled

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1).png" alt="Extras Category with all-stay-days setting"><figcaption></figcaption></figure></div>

*   In **Prices**, select **Per day**.

    <div data-with-frame="true"><figure><img src="../.gitbook/assets/image (7) (1) (1) (1) (1).png" alt="Per day checkbox in the Prices tab"><figcaption></figcaption></figure></div>

{% hint style="warning" %}
The option **All stay days must be available** is configured on the **Extras Category**.
{% endhint %}

<div data-with-frame="true"><figure><img src="../.gitbook/assets/All stay days must be available.png" alt="All stay days must be available configuration"><figcaption></figcaption></figure></div>

### Example scenario

#### Input

* Booking: 7 nights

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (805).png" alt="Seven-night booking"><figcaption></figcaption></figure></div>

*   Hotel:

    * days 1–3: BB
    * days 4–7: HB

    <div data-with-frame="true"><figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Hotel board basis by stay date"><figcaption></figcaption></figure></div>
* Board Types order:
  * HB (top)
  * BB

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (9) (1).png" alt="Board Type order"><figcaption></figcaption></figure></div>

#### Output

*   The system:

    * selects HB as the main board
    * adds supplements for days 1–3

    <div data-with-frame="true"><figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1).png" alt="Board supplement configuration for the stay"><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (806).png" alt="Board supplement selection"><figcaption></figcaption></figure></div>

#### Result

* Customer sees:
  *   HB for the entire stay

      <div data-with-frame="true"><figure><img src="../.gitbook/assets/image (11).png" alt="Highest-order board displayed for the full stay"><figcaption></figcaption></figure></div>
* Price:
  * includes upgrade supplements

### Related pages

* [Board Type - Hotel allotment / Ticket](/broken/spaces/ZCqO8EQ5P5Mioq1zbQAc/pages/cmFZtflwPimtmB7ftv4q)
* [Board Type - Extra](/broken/spaces/ZCqO8EQ5P5Mioq1zbQAc/pages/3arRI9CM44AT5Q5CFxzd)
* [How to use a Board Type](board-type-webboking.md)
* [Extra Category Overview](../extras-category/extra-category-overview/)
