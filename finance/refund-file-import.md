# Refund File Import

### Overview

**Refund File Import** lets you import **refund transactions** exported from **Business Central** into Tourpaq.

This is useful when refunds are created in Business Central and you want them registered in Tourpaq without manual entry.

***

### Before you start

* You must have a refund file **exported from Business Central**.
* The **PaymentCode** in the file must match a payment method in Tourpaq that is used for refunds.
  * If you are missing a payment method, see [Method of Payment](method-of-payment.md).

{% hint style="warning" %}
Only files exported from **Business Central** can be processed in this import.
{% endhint %}

***

### File requirements

Your file must follow these rules:

* **No header row** (the first row must be data).
* **Column order** must be exactly:

`PaymentCode ; Date ; BookingNo ; Amount ; Comment`

* Each line is matched to a booking using **BookingNo**.

***

### Import a refund file (Business Central)

<figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1).png" alt="Refund File Import (Business Central)"><figcaption></figcaption></figure>

{% stepper %}
{% step %}
### Open Refund File Import

Go to **Finance → Refund File Import**.
{% endstep %}

{% step %}
### Choose the import source

Select the **Business Central** tab.
{% endstep %}

{% step %}
### Upload the file

Upload the file by:

* Clicking to browse for a local file, or
* Dragging and dropping the file into the upload area.
{% endstep %}

{% step %}
### Process the import

Click **Process** to start the import.
{% endstep %}

{% step %}
### Review the result

If Tourpaq finds formatting issues or cannot match a line (for example BookingNo not found or an unknown PaymentCode), you will see error messages after you click **Process**.

Fix the file/export and try again.
{% endstep %}
{% endstepper %}

***

### Notes

* **BookingNo** is required so Tourpaq can connect the refund to the correct booking.
* **PaymentCode** must already exist in Tourpaq and must be valid for refund usage.

***

### FAQ

#### 1. What files can I import here?

Only refund files **exported from Business Central**.

#### 2. Why can’t I upload a file with a header row?

This import expects the first line to be refund data. If you include a header row, Tourpaq will treat it as a transaction and the import will fail.

#### 3. What does “PaymentCode” mean?

**PaymentCode** is the internal code for the payment method used for the refund. It must match a configured payment method in Tourpaq.

#### 4. What happens if the BookingNo in the file does not exist in Tourpaq?

That line cannot be matched to a booking and will be shown as an error after you click **Process**.

#### 5. I get an error about an unknown PaymentCode—what should I do?

Make sure the payment code exists and is active in [Method of Payment](method-of-payment.md). If needed, ask an Admin/Financial user to create or activate it.

#### 6. Where can I see the imported refunds after processing?

After a successful import, you can typically find the transactions in your payment listings (for example in [Payment Registration](payment-registration.md)), depending on your setup and filters.
