# Golf Course Check-In Module

### Overview

The **Golf Course Check‑In** module allows guests to confirm their arrival for booked **tee times** using a simple on‑site kiosk (tablet). This helps optimize tee-time usage, reduce no‑shows, and provide a smoother experience for both guests and golf‑club staff.

The module has two components:

1. **Customer Check‑In interface** – Touch‑screen kiosk where players register their arrival.
2. **Master Module** – Staff and guide interface used to manage check‑ins, verify tee times, and adjust registrations.

The module integrates with the Tourpaq booking database and retrieves relevant tee‑time, player, and booking information.

{% hint style="warning" %}
The system is designed to work with **parent products**, **child products**, and **standalone products**.

The only requirement is that the product uses the **Tee Time** category.
{% endhint %}

***

### Purpose

The purpose of the check‑in module is to:

* Capture guest arrivals for tee times directly at the golf course.
* Reduce no‑shows by making check‑in easy and structured.
* Provide up‑to‑date tee‑time status for staff.
* Improve guest experience through a simple, language‑aware self‑service kiosk.
* Support GDPR principles by only showing data relevant for **today’s** tee times.
* Allow staff to handle check‑ins across multiple tee times efficiently through the Master Module.

***

### 1. Customer Check‑In Flow (Kiosk)

<figure><img src="../../../.gitbook/assets/image (474).png" alt=""><figcaption></figcaption></figure>

#### Screen 1 – Booking number entry

**Purpose:** Identify the booking for today’s tee time(s).

<figure><img src="../../../.gitbook/assets/image (475).png" alt=""><figcaption></figcaption></figure>

**Elements**

* Numeric input field with an on‑screen keypad.
* **Next** button.

**Validation**

* Format check: must be **5–6 digits**.
* Booking must have tee times **on the current day**.

**Error messages**

*   Invalid format → “The entered booking number is not valid. Please check your ticket (5–6 digits).”

    <figure><img src="../../../.gitbook/assets/image (476).png" alt=""><figcaption></figcaption></figure>
*   No tee times today → “This booking number has no registered tee times on this day.”

    <figure><img src="../../../.gitbook/assets/image (477).png" alt=""><figcaption></figcaption></figure>

***

#### Screen 2 – Player selection

**Purpose:** Select which players from the booking are checking in.

<figure><img src="../../../.gitbook/assets/image (478).png" alt=""><figcaption></figcaption></figure>

**Language**

The kiosk automatically switches to the language of the booking’s Brand.

**Displayed**

* Player names and tee times relevant for today.
* A checkbox for each player for quick selection.

{% hint style="warning" %}
- Only players from the **same tee time** can be checked in together.
-   If a user attempts to mix tee times, the following message appears:

    “Only possible to register players with the same tee-time at the same time.”
{% endhint %}

**Buttons**

*   **Next** – continues if at least one player is selected.

    <figure><img src="../../../.gitbook/assets/image (479).png" alt=""><figcaption></figcaption></figure>
* **Go Back / Start Over** – returns to Screen 1 and resets the session.

**Timeout**

*   After **30 seconds** of inactivity, a warning popup appears and the kiosk auto‑resets after 5 seconds.

    <figure><img src="../../../.gitbook/assets/image (481).png" alt=""><figcaption></figcaption></figure>

#### Screen 3 – Confirmation

**Purpose:** Confirm the selected players before finalizing.

Shows:

* Tee time (including weekday and date).
* List of all players on the tee time:
  * Checked → “Confirmed check‑in”
  * Not checked → “Not confirmed”
* Empty slots displayed as “Player X”.

Buttons:

* **Next** – saves the check‑in.
* **Go back** – returns to Screen 2 (and resets input).

#### Screen 4 – Completion

Displays:

* “Thank you and have a good round!”
* 5‑second countdown.
* Auto return to Screen 1 (full reset).

***

### 2. Master Module (Staff interface)

<figure><img src="../../../.gitbook/assets/image (482).png" alt=""><figcaption></figcaption></figure>

#### Login

* **Username:** Extra ProductID (for example, `3692`)
* **Password:** A 4‑digit PIN displayed in the extra configuration

<figure><img src="../../../.gitbook/assets/image (483).png" alt=""><figcaption></figcaption></figure>

***

#### Master Module – Main screen

This is Screen 1 for staff (default view).

<figure><img src="../../../.gitbook/assets/image (484).png" alt=""><figcaption></figcaption></figure>

**Search options**

* Dropdown: today’s tee times
* Dropdown: today’s booking numbers
* Input: numeric booking number
* Input: name
* **Find** button

Results show all players across all tee times matching the search.

<figure><img src="../../../.gitbook/assets/image (485).png" alt=""><figcaption></figcaption></figure>

**Columns**

* Check‑in status
* Tee time
* Booking number
* Name
* Handicap

***

#### Master Module – “Today” screen

A live operational overview similar to the Tee Time Extras PDF.

<figure><img src="../../../.gitbook/assets/image (486).png" alt=""><figcaption></figcaption></figure>

Displays all tee times for today:

<figure><img src="../../../.gitbook/assets/image (487).png" alt=""><figcaption></figcaption></figure>

* Status: Available / Blocked / Occupied
* Player names
* Handicap

***

### Related documentation

* [**Tee Times**](./) – How agents assign tee times to passengers in a booking.
* [**Teetime**](../../../extras-setup/extras/teetime.md) – How tee-time products and time-slot availability are configured.
* [**Tee Time extras list**](../../../tee-time-extras-list/) – Export/reporting for tee time bookings.

***

### FAQ

#### What booking number format is accepted in the kiosk?

The kiosk validates that the booking number is **5–6 digits** and that the booking has tee times **today**.

***

#### Why can’t I check in players from different tee times together?

The kiosk only allows check‑in for players who belong to the **same tee time**. This prevents mixing groups across different time slots.

***

#### What should staff do if a guest cannot check in at the kiosk?

Use the **Master Module** to search by booking number or name and register the check‑in manually, following your internal procedures.

***

#### What does “Blocked” mean on the Today screen?

“Blocked” indicates a tee time that is not available for check‑in/usage as shown in the operational overview. The exact reason (for example, maintenance or a manually blocked slot) depends on your tee‑time configuration and daily operations.
