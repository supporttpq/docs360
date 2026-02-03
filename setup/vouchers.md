# Vouchers

### Overview

Tourpaq creates voucher documents automatically.

It runs several times per day.

Vouchers can be created for hotels, extras, transfers, and discounts.

### Purpose

Vouchers make sure customers and suppliers have the right documents before departure.

The automatic process saves time and helps avoid mistakes.

It also makes sure bookings meet the required conditions before a voucher is created.

### Types of vouchers

* **Hotel vouchers**
* **Extra category vouchers**
* **Transfer vouchers**
* **Discount and supplement vouchers**

### When vouchers are created

Vouchers are created only when all rules below are met.

1. **Timing**
   * Vouchers are created **X days before departure**.
   * Set **X** in **System Setup → Vouchers Generation**.
2. **Booking Conditions**
   * Booking status must be **OK**.
   * The booking must be **fully paid**.
   * A voucher of the same type must not already exist.
3. **Extras Categories**
   * If an extra needs additional details (attributes), you must fill them in first.
4. **System Setup Constraints**
   * Vouchers are not created for bookings with departure dates in the past.
5. **Entity Requirements**
   * The hotel/extra/transfer/discount must have:
     * **Issue Voucher** enabled.
     * A **Supplier** selected.

{% hint style="info" %}
If a voucher is missing, start by checking the booking status and payment.

Then check that **Issue Voucher** and **Supplier** are set on the hotel/extra/transfer/discount.
{% endhint %}

### Troubleshooting

If you expected a voucher but did not get one, check these common reasons:

* The booking is not **OK**.
* The booking is not **fully paid**.
* It is not yet **X days before departure**.
* A voucher of the same type already exists.
* The hotel/extra category/transfer/discount does not have **Issue Voucher** enabled.
* The hotel/extra category/transfer/discount is missing a **Supplier**.
* Required extra attributes are not filled in.

### Related pages

* [QR code for vouchers](../booking/new-booking/qr-code-for-vouchers.md)

### FAQ

<details>

<summary><strong>When will vouchers be created?</strong></summary>

They are created automatically when you are **X days before departure**.

You set **X** in **System Setup → Vouchers Generation**.

</details>

<details>

<summary><strong>Why wasn’t a voucher created for a booking?</strong></summary>

Most common reasons:

* The booking status is not **OK**.
* The booking is not **fully paid**.
* The hotel/extra/transfer/discount is missing **Issue Voucher** or **Supplier**.
* It is not yet time to generate vouchers.

</details>

<details>

<summary><strong>Will Tourpaq create vouchers for past departures?</strong></summary>

No.

Vouchers are not created for bookings with departure dates in the past.

</details>

<details>

<summary><strong>Can vouchers be created for extras?</strong></summary>

Yes, if the extra category is set to issue vouchers.

If the extra requires extra details (attributes), those must be filled in first.

</details>

<details>

<summary><strong>What does “Issue Voucher” mean?</strong></summary>

It is a setting that tells Tourpaq that this hotel/extra/transfer/discount should produce a voucher.

If it is not enabled, no voucher will be created for it.

</details>

<details>

<summary><strong>Do I need a supplier to create vouchers?</strong></summary>

Yes.

The hotel/extra/transfer/discount must have a **Supplier** selected.

</details>

<details>

<summary><strong>Is a voucher the same as a ticket?</strong></summary>

No.

A **voucher** is usually for services like hotels, transfers, or extras.

A **ticket** is usually for travel documents and check-in information.

See [Print Tickets](../tickets/print-tickets.md).

</details>
