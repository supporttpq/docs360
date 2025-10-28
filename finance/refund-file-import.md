# Refund File Import

This section allows users to import **refund transactions** exported from **Business Central** directly into the system.

#### File Requirements

* Only files **exported from Business Central** are accepted.
* **No header row** should be present in the file.
* Required **column order**:\
  `PaymentCode ; Date ; BookingNo ; Amount ; Comment`

***

#### Import Steps

1. Navigate to the **Refund File Import** page.
2. Select the **Business Central** tab.
3. **Upload** the file by:
   * Clicking to browse for a local file, or
   * Dragging and dropping the file into the upload zone.
4. Click the **Process** button to begin import.

<figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Related Notes

* Each line is automatically matched to a booking based on the **Booking Number**.
* **Payment Code** must correspond to a refund-capable payment method already defined in the system.
* Errors due to format mismatches or unmatched records will be shown after clicking **Process**.

{% hint style="warning" %}
Note: Only documents from exported from "Business Central" can be processed. Columns order should be: "PaymentCode; Date; BookingNo; Amount;Comment" - without header
{% endhint %}
