---
description: >-
  Understand how Tourpaq applies board types across the full stay during
  booking, including board changes, availability checks, closeouts, and
  supplement combinations.
---

# Board Behaviour During Booking

## Board behavior during booking

### Availability across the stay

Configure **All stay days must be available** in the **Extras Category**. The hotel must offer the Board Basis and Board Supplement for every day of the stay. Tourpaq offers an option only when it covers the full stay.

<figure><img src="../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>

### Board basis changes

When the Board Basis changes, Tourpaq combines a Board Basis with a Board Supplement. The **Board Type** order determines the board offered. Tourpaq selects the highest ordered Board Type and adds a supplement for days with a lower Board Basis.

Examples:

* BB for days one through three and HB for days four through seven: Tourpaq offers HB with an HB supplement for days one through three.
* HB for days one through two and All Inclusive for days three through five: Tourpaq offers All Inclusive with an All Inclusive supplement for days one through two.

### Booking and ticket display

During booking, Tourpaq shows the selected Board Basis and the related Board Supplement. For a BB-to-HB stay, the booking shows HB and an HB supplement for the BB days. The ticket's hotel section shows HB with the supplement details for those days.

**Ticket display**

* The system displays the main board (highest order)

<figure><img src="../.gitbook/assets/image (205).png" alt=""><figcaption></figcaption></figure>

**Pricing**

* The price:
  * includes all supplements
  * is aggregated into the base booking price

<figure><img src="../.gitbook/assets/image (214).png" alt=""><figcaption></figcaption></figure>

#### Example

If there is a booking made with stay period by 7 nights and the following board configuration:

<figure><img src="../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure>

| Stay days | Board Type |
| --------- | ---------- |
| Days 1–3  | BB         |
| Days 4–7  | HB         |

<figure><img src="../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>

The Board Types are configured in the following order:

1. **HB**
2. **BB**

<figure><img src="../.gitbook/assets/image (264).png" alt=""><figcaption></figcaption></figure>

#### Step 1: Determine the board type for each stay date

The system evaluates the board type configured for each day of the stay:

* Days 1–3: **BB**
* Days 4–7: **HB**

#### Step 2: Select the main board type

Because **HB** has a higher priority than **BB** in the Board Type order, the system selects **HB** as the main board type for the booking.

#### Step 3: Add supplements for the lower board type

The system identifies that **BB** applies to days 1–3, while **HB** is the selected main board type.

As a result, the system adds the configured **board supplements** for days 1–3 to represent the upgrade from BB to HB.

#### Step 4: Display the board type to the customer

The customer sees **HB for the entire stay**, even though the original hotel configuration contains BB for days 1–3.

The displayed board type is therefore based on the highest-priority board type configured for the stay.

#### Step 5: Calculate the price

The booking price includes the applicable **upgrade supplements** for days 1–3.

The final price therefore consists of:

* The hotel price based on the selected board configuration.
* The board upgrade supplements for days 1–3.

#### Result

The booking is displayed to the customer as: **Board Type: HB**

<figure><img src="../.gitbook/assets/image (286).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (293).png" alt=""><figcaption></figcaption></figure>
