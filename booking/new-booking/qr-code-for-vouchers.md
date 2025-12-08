# QR code for vouchers

### Overview

The **QR Code for Vouchers** feature enables the inclusion of a QR-code in the voucher/ticket that is issued to customers after booking. Scanning the QR code allows quick access to voucher details, verification at check-in, or partner / supplier validation, improving ease of use and reducing manual entry errors.

***

### Purpose

This functionality aims to:

* Provide customers with a fast and secure way to present their voucher via a mobile device or printed copy.
* Enable partners, guides, suppliers or reception staff to scan and validate a booking without manual keying of voucher numbers.
* Improve operational efficiency, reduce errors in check-in or voucher redemption, and enhance user experience.
* Strengthen security and traceability of voucher usage through unique QR codes linked to the booking.

### How It Works

1. **Voucher Generation**\
   After a booking is confirmed and voucher(s) are generated, the system embeds a unique QR-code onto the voucher. That QR-code encodes the voucher reference or URL, which points to the booking and voucher details.
2. **Customer Receipt**\
   The customer receives the voucher (via email or download) with the QR-code visible. They may either print it or show on their mobile device.
3. **Redemption / Validation**\
   At check-in or on-site, staff or suppliers scan the QR-code with a scanner or mobile device. The system locates the corresponding booking, verifies voucher validity (unused, correct date, correct service) and marks it as redeemed.
4. **Audit & Tracking**\
   Each scan and redemption event is logged, allowing for reporting on voucher scans, redemptions, no-shows, and discrepancies.

***

### Instructions for Use

#### Setup

1.  In the system setup configuration section, **enable Show QR-code in** vouchers.&#x20;

    <figure><img src="../../.gitbook/assets/image (3) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
2. Assign which voucher types or services should include QR-codes (e.g., extras, transfers, tours).
3. Confirm that your voucher printing or emailing process supports QR-code graphics (ensure PDF generation, mobile friendly, etc).

#### Booking&#x20;

1. Create a new booking as usual: Booking → New Booking.
2. Once booking is confirmed and fully paid,  the voucher is created and includes the QR-code.
3.  The customer receives the voucher via email or download. Vouchers have the QR code generated for each person separately

    <figure><img src="../../.gitbook/assets/image (4) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
