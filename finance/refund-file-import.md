---
description: >-
  Import refund transactions from Business Central into Tourpaq Office Finance.
  Validate PaymentCode and BookingNo, then process refunds without manual entry.
---

# Refund File Import

### Overview

**Refund File Import** lets you import **refund transactions** exported from **Business Central** into **Tourpaq Office Finance**.

Use it when refunds are created in Business Central and you want them registered in Tourpaq without manual entry.

***

### Before you start

* You must have a refund file **exported from Business Central**.
* You must have the required permissions (typically **Financial** or **Administrator**).
* The **PaymentCode** in the file must match a payment method in Tourpaq that is used for refunds.
  * If you are missing a payment method, see [Method of Payment](method-of-payment.md).

{% hint style="warning" %}
Only files exported from **Business Central** can be processed in this import.
{% endhint %}

***

### File requirements

Your file must follow these rules:

* **No header row** (the first row must be data).
* **Semicolon-separated values** with this exact delimiter: `;`
* **Column order** must be exactly:

`PaymentCode ; Date ; BookingNo ; Amount ; Comment`

* Each line is matched to a booking using **BookingNo**.

***

### Import a refund file (Business Central)

<figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Refund File Import (Business Central)"><figcaption><p>Import Business Central refund transactions into Tourpaq using the required PaymentCode and BookingNo file format.</p></figcaption></figure>

{% stepper %}
{% step %}
**Open Refund File Import**

Go to **Finance → Refund File Import**.
{% endstep %}

{% step %}
**Choose the import source**

Select the **Business Central** tab.
{% endstep %}

{% step %}
**Upload the file**

Upload the file by:

* Clicking to browse for a local file, or
* Dragging and dropping the file into the upload area.
{% endstep %}

{% step %}
**Process the import**

Click **Process** to start the import.
{% endstep %}

{% step %}
**Review the result**

If Tourpaq finds formatting issues or cannot match a line (for example BookingNo not found or an unknown PaymentCode), you will see error messages after you click **Process**.

Fix the file/export and try again.
{% endstep %}
{% endstepper %}

***

### Notes

* **BookingNo** is required so Tourpaq can connect the refund to the correct booking.
* **PaymentCode** must already exist in Tourpaq and must be valid for refund usage.
