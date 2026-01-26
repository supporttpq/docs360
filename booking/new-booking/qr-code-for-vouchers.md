# QR code for vouchers

### Overview

The **QR code for vouchers** feature adds a scannable QR code to vouchers. This makes it easier for staff, guides, and suppliers to identify a voucher quickly (for example from a printed voucher or a guest’s phone), without manually typing voucher references.

{% hint style="info" %}
QR codes appear **only on vouchers that have been generated**. Voucher generation is controlled by your voucher rules and timing (see [Vouchers](../../setup/vouchers.md)).
{% endhint %}

***

### Purpose

* Make vouchers easier to use on-site by enabling quick scanning.
* Reduce manual entry errors when looking up voucher information.
* Improve operational handling at suppliers/reception/partners.

***

### Preconditions

* The setting **Show QR-code in vouchers** must be enabled.
* Vouchers must be generated for the booking (typically requires:
  * Booking status **OK**
  * Booking is **fully paid**
  * The relevant entity has **Issue Voucher** enabled and a **Supplier** assigned
  * Voucher generation timing is reached)

For the detailed rules, see: [Vouchers](../../setup/vouchers.md).

***

### How it works

1. **Voucher Generation** After a booking is confirmed and voucher(s) are generated, the system embeds a unique QR-code onto the voucher. That QR-code encodes the voucher reference or URL, which points to the booking and voucher details.
2. **Customer Receipt** The customer receives the voucher (via email or download) with the QR-code visible. They may either print it or show on their mobile device.
3. **Redemption / Validation** At check-in or on-site, staff or suppliers scan the QR-code with a scanner or mobile device. The system locates the corresponding booking, verifies voucher validity (unused, correct date, correct service) and marks it as redeemed.
4. **Audit & Tracking** Each scan and redemption event is logged, allowing for reporting on voucher scans, redemptions, no-shows, and discrepancies.

{% hint style="warning" %}
What happens after scanning (for example, whether it opens a page, validates, or marks a voucher as used) depends on your organization’s scanner/app/workflow. This page documents the voucher-side QR code feature only.
{% endhint %}

***

### Setup

{% stepper %}
{% step %}
### 1. Enable QR codes on vouchers

1. Go to **System Setup**.
2. Enable **Show QR-code in vouchers**.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. Click **Save**.
{% endstep %}

{% step %}
### 2. Ensure vouchers will be generated

Confirm that the booking and product setup meet the voucher generation rules (status OK, fully paid, Issue Voucher + Supplier, and correct timing).

See: [Vouchers](../../setup/vouchers.md)
{% endstep %}

{% step %}
### 3. Verify on a voucher

Once vouchers are generated, open/download a voucher and confirm the QR code is visible.

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

***

### Notes

* QR codes are shown on the **voucher PDF**.
* Vouchers can be generated per passenger/product depending on your setup. In many setups, the QR code is generated **per voucher document**.

***

### Troubleshooting

#### QR code does not show on the voucher

Check the most common causes:

* The global setting **Show QR-code in vouchers** is not enabled.
* The voucher has not been generated yet (voucher generation is often scheduled **X days before departure**).
* The booking is not **fully paid**.
* Booking status is not **OK**.
* The hotel/extra category/transfer/discount is missing:
  * **Issue Voucher** setting, or
  * a valid **Supplier**.

***

### FAQ

#### 1. Where do I enable QR codes for vouchers?

Enable **Show QR-code in vouchers** in **System Setup**, then save.

***

#### 2. I enabled the setting but still don’t see QR codes — why?

QR codes are printed only on vouchers that are **generated**. If vouchers are not generated yet (for example due to timing, payment status, or missing Issue Voucher/Supplier), there will be no QR code to show.

See: [Vouchers](../../setup/vouchers.md)

***

#### 3. Are QR codes created per booking or per passenger?

They are created per passenger. Vouchers have the QR code generated for each person separately

***

#### 6. Do QR codes also appear on tickets?

Yes. The QR codes appear on tickts.
