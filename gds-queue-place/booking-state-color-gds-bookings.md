# Booking State Color – GDS Bookings

### Introduction

The **Booking State Color** feature introduces a visual indicator for GDS booking statuses across multiple areas in Tourpaq.

It enhances visibility by displaying a **colored dot** that reflects the current status of a booking, making it easier to identify and manage GDS bookings in lists and search results.

This functionality is used in combination with:

* **All Bookings overview**
* **Search flows (New Booking, New Offer)**
* **Customer History**
* **Tickets → E-tickets Overview**

***

### Overview

GDS bookings are marked with a **colored dot** corresponding to their booking status.\
The color is consistent across all supported pages and reflects the real-time status of the booking.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>All Bookings State Color</p></figcaption></figure>

***

### Purpose

* Improve visibility of booking status
* Reduce the time needed to identify GDS booking states
* Provide consistent UI behavior across modules
* Support faster operational decision-making

***

### Requirements

* Booking must be a **GDS booking**
* Booking must have a valid **status (PENDING, HK, TKOK)**
* User must have access to booking-related pages

***

### Navigation

The colored indicator is visible in the following areas:

* **All Bookings**
* **Search results** (New Booking, New Offer)
* **Customer History**
* **Tickets → E-tickets Overview**

No additional navigation or setup is required.

***

### Interface Overview

A **colored dot** is displayed next to or within booking-related rows in tables.

* The dot is aligned with booking entries
* It visually represents the booking status
* It is non-clickable and informational only

***

### Color Mapping

The following color scheme is applied:

<table><thead><tr><th width="161.22222900390625">Status</th><th width="120.333251953125">Color</th><th></th><th>Meaning</th></tr></thead><tbody><tr><td><strong>PENDING</strong></td><td>Brown</td><td><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td>Booking is not yet confirmed</td></tr><tr><td><strong>HK</strong></td><td>Pink</td><td><img src="../.gitbook/assets/image (5) (1) (1) (1) (1).png" alt="" data-size="original"></td><td>Booking is confirmed (holding confirmed status)</td></tr><tr><td><strong>TKOK</strong></td><td>Light green</td><td><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td>Ticketing is confirmed and completed</td></tr><tr><td><strong>OK</strong></td><td>Green</td><td><img src="../.gitbook/assets/image (6) (1) (1).png" alt="" data-size="original"></td><td>Booking OK</td></tr><tr><td><strong>ERR</strong></td><td>Yellow</td><td><img src="../.gitbook/assets/image (7) (1) (1).png" alt="" data-size="original"></td><td>Error</td></tr><tr><td><strong>CXL</strong></td><td>Red</td><td><img src="../.gitbook/assets/image (8) (1) (1).png" alt="" data-size="original"></td><td>Cancelled</td></tr><tr><td><strong>TKQ</strong></td><td>Light pink</td><td><img src="../.gitbook/assets/image (9) (1).png" alt="" data-size="original"></td><td></td></tr></tbody></table>

***

### Field Description

#### Booking Status Indicator (Colored Dot)

* Visual representation of booking status
* Automatically derived from GDS status
* Not editable
* Updates dynamically when booking status changes

**Behavior:**

* Appears only for GDS bookings
* Hidden for non-GDS bookings
* Consistent across all supported modules

***

### Configuration Steps

No configuration is required.

The feature is automatically enabled and applied across all relevant pages.

***

### System Behavior

* System reads booking status from GDS data
* Matches the status to a predefined color
* Displays a colored dot in all supported views
* Updates automatically when booking status changes

***

### Export Behavior

#### All Bookings Export

* All columns visible in **All Bookings** are now included in the export
* The color indicator itself is not exported as a visual element
* Booking status remains available as a standard field in export data

***

### Examples

#### Example 1 – Pending Booking

* Status: PENDING
* Display: Brown dot
* Interpretation: Booking is not confirmed yet

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

#### Example 2 – Confirmed Booking

* Status: HK
* Display: Pink dot
* Interpretation: Booking is confirmed

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

#### Example 3 – Ticketed Booking

* Status: TKOK
* Display: Light green dot
* Interpretation: Ticketing is completed

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### System Behavior

* System reads booking status from GDS
* Matches it to a predefined color
* Displays consistently across all modules
* Updates automatically when status changes

***

### Related Pages

* [**All Bookings**](../booking/all-bookings/)
* [**New Booking**](../booking/new-booking/)
* [**Tickets → E-tickets Overview**](../e-tickets-overview.md)
