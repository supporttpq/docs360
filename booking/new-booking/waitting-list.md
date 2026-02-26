---
description: >-
  Create and manage waitlist bookings in Tourpaq Office when seats or beds are
  sold out. Learn how WL and WLOK statuses work and how waitlist bookings become
  confirmed (OK) when allotment is available.
---

# Waiting list (WL)

## Waiting list (WL) / waitlist bookings

### Overview

Use **Waiting list (WL)** when a customer wants to book, but availability is sold out. This usually means there are not enough **transport seats** and/or **hotel beds** in allotment.

Instead of losing the sale, Tourpaq Office can create a **waitlist booking** that:

* records the customer’s interest
* does **not** reserve allotment immediately (no seats/beds are taken)
* can be converted automatically when allotment becomes available later

### Key terms (common searches)

* **WL**: waitlist booking created. Not confirmed.
* **WLOK**: allotment reserved. Agent must finalize.
* **OK**: booking confirmed. Normal emails and payments apply.
* **Allotment**: the available **seats** (transport) and **beds** (hotel) used for availability.

### When to use this

Use waiting list to accept interest for fully booked departures. Tourpaq processes waitlist bookings fairly (first created → first processed).

{% hint style="warning" %}
A waitlist booking is **not a confirmed contract** until it becomes fully confirmed (see [Status lifecycle](waitting-list.md#status-lifecycle)).
{% endhint %}

### Preconditions

Before you can create waitlist bookings, you need the normal setup for the departure:

* Transport allotment and/or hotel allotment configured
* A valid price list for the departure

### Configure a price as “Waitlist (WL)”

To enable waiting list behavior, mark the relevant price as a waitlist price.

{% stepper %}
{% step %}
### 1. Open the relevant price list entry

Navigate to the price list entry for the departure where you want to allow waitlist bookings.
{% endstep %}

{% step %}
### 2. Enable the **Waitlist (WL)** flag

Check the **Waitlist (WL)** checkbox under **FLAGS**.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Price list entry flags showing the Waitlist (WL) checkbox"><figcaption><p>Enable Waitlist (WL) in the price list flags.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Waitlist (WL) flag selected in a Tourpaq price list"><figcaption><p>Waitlist (WL) flag selected.</p></figcaption></figure>
{% endstep %}
{% endstepper %}

### How it works

#### Standard behavior (while allotment exists)

If there is enough allotment, Tourpaq behaves as usual. It creates a normal booking.

#### Waitlist behavior (when allotment is missing)

When allotment is **not** available and the price is marked as **Waitlist (WL)**, Tourpaq can still create the booking but will treat it as a waitlist booking:

* No allotment is reserved at creation time
* No payment steps are available yet
* No “thank you for booking” email is sent yet
* The booking clearly indicates it is a waitlist and not a confirmed contract

### Status lifecycle

Waitlist bookings move through the following statuses:

* **WL** – Waitlist booking created (not confirmed)
* **WLOK** – Allotment has become available and was reserved automatically; booking is now ready for an agent to finalize
* **OK** – Booking finalized by an agent (normal booking behavior applies)

{% hint style="info" %}
Tourpaq periodically checks for new allotment and will process waitlist bookings in the **order they were created**.
{% endhint %}

#### What happens when the status becomes **WLOK**

When a waitlist booking can be fulfilled, Tourpaq reserves the needed allotments. The booking status changes to **WLOK**.

At this point:

* the booking appears on the Office Dashboard for action
* an admin/sales agent must open the booking and **save it again** to finalize it

Only after the booking is saved and becomes **OK**:

* customer emails/tickets are sent (normal flow)
* payment rates and payment options become active

### In Tourpaq Office (Back Office)

<figure><img src="../../.gitbook/assets/image (247).png" alt="Tourpaq Office booking view showing waitlist indicators (WL/WLOK)"><figcaption><p>Waitlist indicators in Tourpaq Office.</p></figcaption></figure>

When placing a waitlist booking in the Office:

* Transport/hotel popups show additional warnings that you are selecting a waitlist scenario.
* A transport may require using a button such as **Search Waitlist also** to display waitlist options.
* When clicking **Take allotment**, a confirmation checkbox appears and you must acknowledge the waitlist scenario before continuing.

### In Tourpaq WebBooking / Customer Center

<figure><img src="../../.gitbook/assets/image (248).png" alt="WebBooking and Customer Center messaging for waitlist bookings"><figcaption><p>Waitlist messaging in WebBooking / Customer Center.</p></figcaption></figure>

For WebBooking, clear customer communication is critical because the customer is self‑serving.

Typical behavior:

* A visible message/banner is shown on key pages (landing, confirmation, and Customer Center login).
* The message can have a default version and a brand-specific version.
* Payment steps are typically hidden because the booking is not confirmed yet.

{% hint style="info" %}
Brand-specific WebBooking texts may require assistance from **Tourpaq Support**, depending on your setup.
{% endhint %}

### Tips and troubleshooting

#### WebBooking rejects a booking attempt

If a price has **no allotment** and is **not** marked as **Waitlist (WL)**, WebBooking will reject the booking attempt.

#### “Customer asks why they can’t pay yet”

If the booking is still **WL** (waitlist):

* payment is not available yet because the booking is not confirmed
* the booking becomes payable only after it reaches **OK**

#### “The booking is WLOK but nothing is sent to the customer”

This is expected. An agent must open the booking and **save/finalize** it so it becomes **OK** and triggers the normal email/payment flow.
