# Payment File Import

### Overview

**Payment File Import** lets you import a payment file from your bank so Tourpaq can register payments on the correct bookings automatically.

After the import, the payments are visible in [Payment Registration](payment-registration.md).

***

### Purpose

Use Payment File Import when you receive payments through the bank and want to avoid registering each payment manually.

Although the file format depends on your bank, the import normally needs these values for each payment line:

* A **booking identifier** (for example booking number/reference)
* A **payment date**
* An **amount**

***

### Before you start

* Make sure you have the **payment file** from your bank.
* Confirm that a payment method exists for bank imports (for example **BANKIN**).
  * If you do not see a suitable method, ask an Admin/Financial user to configure it in [Method of Payment](method-of-payment.md).
* You must have the required permissions (typically **Financial** or **Administrator**).

{% hint style="info" %}
Your bank (or your finance setup) should provide the **specification** that explains which file format to export and which booking identifier Tourpaq expects.
{% endhint %}

***

### Import a payment file

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Payment File Import screen"><figcaption></figcaption></figure>

{% stepper %}
{% step %}
### Get the payment file from your bank

Download/export the payment file in the format your company uses.

If you are unsure which format to use, check the bank’s export options or ask your finance administrator.
{% endstep %}

{% step %}
### Open Payment File Import

Go to **Finance → Payment File Import**.
{% endstep %}

{% step %}
### Upload the file

1. Select the file.
2. Upload/import it.

Tourpaq validates the file during the upload/import.
{% endstep %}

{% step %}
### Review validation results

If Tourpaq flags errors (for example missing booking reference or invalid amount), correct the file and upload again.

When the file is accepted, the payments are created in Tourpaq.
{% endstep %}

{% step %}
### Verify the imported payments

Open [Payment Registration](payment-registration.md) and search by payment date range and payment method (for example **BANKIN**) to confirm the payments are listed.
{% endstep %}
{% endstepper %}

***

### Notes

* Imported payments are validated on import. Any unmatched or erroneous records are flagged for review.
* The payment date used can depend on your bank file and setup. If your import source uses an **accounting date**, Tourpaq may use that date instead of today.

***

### FAQ

#### 1. Where do imported payments show up?

Imported payments appear in [Payment Registration](payment-registration.md).

#### 2. What information must the bank file contain?

At minimum, Tourpaq needs a **booking identifier**, a **payment date**, and an **amount** for each payment line.

#### 3. Why does the import fail with “booking not found” (or similar)?

Usually the booking identifier in the file does not match what Tourpaq expects (wrong booking number, missing reference, extra characters, etc.). Confirm the correct identifier format with your bank export specification or your finance administrator.

#### 4. Which payment method is used for imported payments?

Imported payments should use a dedicated payment method (commonly something like **BANKIN**). If it is missing, it must be configured in [Method of Payment](method-of-payment.md).

#### 5. I imported the file, but I can’t see the payments—what should I check?

* Expand your **payment date** range in Payment Registration.
* Filter by the expected **payment method** (for example **BANKIN**).
* Confirm that the import did not flag validation errors.

#### 6. Can I use Payment File Import for refunds?

Not usually. Refunds are typically handled through a separate refund process/file (depending on your setup). If you have a refund import feature available, use that instead.
