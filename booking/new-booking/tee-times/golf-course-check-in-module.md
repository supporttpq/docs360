# Golf Course Check-In Module

### Overview

The Golf Course Check-In module allows guests to verify their arrival for booked tee-times using a simple on-site kiosk (tablet).\
It optimizes tee-time usage, reduces no-shows, and provides a smooth experience both for guests and golf-club staff.

The module consists of two components:

1. Customer Check-In Interface – Touch-screen for players to register their arrival.
2. Master Module – For staff and guides to manage check-ins, verify all tee-times, and adjust registrations.

The system integrates with the Tourpaq booking database and pulls relevant tee-time, player, and booking information.

{% hint style="warning" %}
The system is designed to work with parent products, child products, as well as standalone products.\
The only requirement is that the product has the **Tee Time** category.
{% endhint %}

***

### Purpose

The purpose of the check-in module is to:

* Capture guest arrivals for tee-times directly at the golf course.
* Reduce no-show rates by making check-in mandatory.
* Provide up-to-date tee-time status for staff.
* Improve guest experience through an easy, language-aware self-service kiosk.
* Ensure GDPR compliance by only showing data relevant for today’s tee-times.
* Allow staff to modify check-ins across multiple tee-times efficiently through the Master Module.

***

### 1. Customer Check-In Flow (Kiosk)

<figure><img src="../../../.gitbook/assets/image (474).png" alt=""><figcaption></figcaption></figure>

#### Screen 1 – Booking Number Entry

Purpose: Identify the booking for today’s tee-time(s).

<figure><img src="../../../.gitbook/assets/image (475).png" alt=""><figcaption></figcaption></figure>

Elements:

* Numeric input field with on-screen number keyboard.
* “Next” button.
* Validation:
  * Format check: must be 5–6 digits.
  * Must have tee-times on the current day.

Error messages:

*   Invalid format → “The entered booking number is not valid. Please check your ticket (5–6 digits).” &#x20;

    <figure><img src="../../../.gitbook/assets/image (476).png" alt=""><figcaption></figcaption></figure>
*   No tee-times today → “This booking number has no registered tee times on this day.” &#x20;

    <figure><img src="../../../.gitbook/assets/image (477).png" alt=""><figcaption></figcaption></figure>

***

#### Screen 2 – Player Selection

Purpose: Select which players from the booking are checking in.&#x20;

<figure><img src="../../../.gitbook/assets/image (478).png" alt=""><figcaption></figcaption></figure>

Language automatically switches to the language of the booking’s brand.

Displayed:

* names & tee-times relevant for today.
* checkbox for each name for quick selection.

{% hint style="warning" %}
- Only players from the _same tee-time_ can be checked in together.
- If a user attempts to mix tee-times →\
  “Only possible to register players with the same tee-time at the same time.”
{% endhint %}



Buttons:

*   “Next” → continues if at least one name selected.&#x20;

    <figure><img src="../../../.gitbook/assets/image (479).png" alt=""><figcaption></figcaption></figure>
* “Go Back / Start Over” → returns to screen 1 with all state reset.

Timeout:

*   30 seconds inactivity → popup warning + auto-reset after 5 seconds.

    <figure><img src="../../../.gitbook/assets/image (481).png" alt=""><figcaption></figcaption></figure>

#### **Screen 3 – Confirmation**

**Purpose:** Confirm selected names before finalizing.

Shows:

* Tee-time (incl. weekday & date).
* List of all players on the tee-time:
  * Checked → “Confirmed check-in”
  * Not checked → “Not confirmed”
* Empty slots displayed as “Player X”.

Buttons:

* “Next” → saves the check-in.
* “Go back” → returns to screen 2 but resets input.

#### Screen 4 – Completion

Displays:

* “Thank you and have a good round!”
* 5-second countdown.
* Auto return to Screen 1 (full reset).

***

### 2. Master Module (Staff Interface)

<figure><img src="../../../.gitbook/assets/image (482).png" alt=""><figcaption></figcaption></figure>

Login

* Username: Extra ProductID (e.g., 3692)
* Password: A 4-digit PIN displayed in the extra configuration

<figure><img src="../../../.gitbook/assets/image (483).png" alt=""><figcaption></figcaption></figure>

***

#### Master Module – Main Screen

This is Screen 1 for staff (default view).

<figure><img src="../../../.gitbook/assets/image (484).png" alt=""><figcaption></figcaption></figure>

Search options:

* Dropdown: today's tee-times
* Dropdown: today's booking numbers
* Input: numeric booking number
* Input name
* “Find” button

Results show all players across all tee-times matching the search.

<figure><img src="../../../.gitbook/assets/image (485).png" alt=""><figcaption></figcaption></figure>

Columns:

* Check-in status
* Tee-time
* Booking number
* Name
* Handicap

***

#### &#x20;Master Module – “Today” Screen

A live operational overview similar to the Tee-Time Extras PDF.

<figure><img src="../../../.gitbook/assets/image (486).png" alt=""><figcaption></figcaption></figure>

Displays:

<figure><img src="../../../.gitbook/assets/image (487).png" alt=""><figcaption></figcaption></figure>

All tee-times for today

* Status: Available / Blocked / Occupied
* Player names
* Handicap
