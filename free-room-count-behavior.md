# Free room count behavior

### Overview

This feature manages the **recalculation of the free hotel allotment** for price list rules. It ensures that the number of available rooms is updated correctly after changes such as allotment updates, bookings, cancellations, or manual triggers.

### Purpose

The recalculation is necessary to:

* Keep the free room count accurate across the system.
* Ensure agencies and web booking tools display the correct availability.
* Prevent booking errors caused by outdated allotment values.

### Preconditions

* The price list rule must have a **sale value** set (e.g., P1, P2, D1).
* If the price list value is not greater than 0:
  * The offer will appear on the **agency presentation site**, but
  * It **cannot be booked** via Web Booking or Office.

### Process

#### Automatic Recalculation via Queue

* Tourpaq uses a **queue system** to handle free room recalculation.
* When hotel allotments are updated, the affected price lists are placed in the queue.
* The system processes them one by one, updating the free room values.
* Processing time depends on the number of rules, agencies, and transports, typically taking **2–15 minutes**.
* If recalculation takes **longer than 15 minutes**, it is considered suspicious and requires investigation.

#### Instant Recalculation on Bookings

* When a booking is placed, canceled, or modified (e.g., replacing a room), the free/occupied allotment is updated **immediately** in the _Hotel Allotment per Day_ tab.
* The corresponding price list rule is recalculated **instantly** (no queue).
* This allows the same price list rule to be booked again within seconds.
* ⚠️ Note: Other price list rules selling the same room (but with different transports) are **not** updated instantly. They still follow the queued process.

### Manual Recalculation

* Users can trigger a **manual recalculation** of a price list rule.
* To do this, click on the **Magic Wand icon** (highlighted in the interface).
* This recalculation is **instant**.

<figure><img src=".gitbook/assets/image (64) (1).png" alt=""><figcaption></figcaption></figure>
