---
description: >-
  Add scannable QR codes to vouchers in Tourpaq Office. Enable the setting,
  generate vouchers, and scan QR codes for voucher lookup and on-site
  validation.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# QR code for vouchers

#### Overview

**QR code for vouchers** adds a scannable QR code to generated vouchers in **Tourpaq Office**. It supports voucher lookup and on-site handling without manual voucher-reference entry.

Tourpaq adds the QR code when it generates the voucher. Customers receive it by email or download. Staff or suppliers can scan the QR code from a printout or mobile device. Scanning can support redemption, validation, audit, and tracking workflows.

<figure><img src="../../.gitbook/assets/28.08.2026_13.50.12_REC.png" alt="Generated voucher document showing a QR code."><figcaption><p>A generated voucher includes a QR code.</p></figcaption></figure>

{% hint style="info" %}
QR codes appear only on generated vouchers. Voucher generation follows the rules and timing in [vouchers.md](../../setup/vouchers.md "mention").
{% endhint %}

{% hint style="warning" %}
This page documents the voucher-side QR code feature only.
{% endhint %}

#### Purpose

* Make vouchers easier to use on-site by enabling quick scanning.
* Reduce manual entry errors when looking up voucher information.
* Improve operational handling for suppliers and passengers.

#### Preconditions

* The setting **Show QR Code in Vouchers** must be enabled.
* Vouchers must be generated for the booking (typically requires):
  * Booking status **OK**
  * Booking is **fully paid**
  * The relevant entity has **Issue Voucher** enabled and a **Supplier** assigned
  * Voucher generation timing is reached

For the detailed rules, see [vouchers.md](../../setup/vouchers.md "mention").

#### How-to

{% stepper %}
{% step %}
**1. Enable QR codes on vouchers**

1. Go to **System Setup**.
2. Enable **Show QR Code in Vouchers**.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="System Setup showing the Show QR Code in Vouchers and QR Code in Vouchers - hide passenger name settings."><figcaption><p>Enable Show QR Code in Vouchers in System Setup.</p></figcaption></figure>

3. Click **Save**.
{% endstep %}

{% step %}
**2. Ensure vouchers will be generated**

Confirm that the booking and product setup meet the voucher generation rules (status OK, fully paid, Issue Voucher + Supplier, and correct timing).

See [vouchers.md](../../setup/vouchers.md "mention").
{% endstep %}

{% step %}
**3. Verify on a voucher**

Once vouchers are generated, open or download a voucher and confirm the QR code is visible.

<figure><img src="../../.gitbook/assets/28.08.2026_13.53.12_REC.png" alt="Generated voucher showing a QR code and the guest name TBA2 TBA2. The guest name is an illustrative placeholder, not real guest data."><figcaption><p>Example voucher with a QR code. TBA2 TBA2 is an illustrative placeholder name.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/28.08.2026_13.54.13_REC.png" alt="Generated voucher showing a QR code and the guest name Adriana Spataru-TESTER. The guest name is an illustrative placeholder, not real guest data."><figcaption><p>Example voucher with a QR code. Adriana Spataru-TESTER is an illustrative placeholder name.</p></figcaption></figure>
{% endstep %}
{% endstepper %}

#### Field reference

Configure QR codes in **System Setup**.

| Field                                         | Description                                                           | Notes                                                                                                                                                                                                                         |
| --------------------------------------------- | --------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Show QR Code in Vouchers**                  | Enables QR codes on generated vouchers.                               | QR codes appear on the **voucher PDF**. QR codes require a generated voucher. Vouchers can be generated per passenger or product, depending on the setup. In many setups, Tourpaq generates one QR code per voucher document. |
| **QR Code in Vouchers - hide passenger name** | Passenger names are hidden **on vouchers when QR codes are enabled**. | **TO VERIFY:** Confirm this setting's exact effect.                                                                                                                                                                           |

#### Related pages

* [vouchers.md](../../setup/vouchers.md "mention") — Configure voucher generation timing and resolve missing vouchers.
* [economics.md](economics.md "mention") — Register payments and verify the booking payment status.
* [e-mails.md](e-mails.md "mention") — Review voucher emails sent from a booking.
