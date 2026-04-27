---
description: >-
  Import a bank payment file to automatically register booking payments in
  Tourpaq Office, validate matching, and reconcile in Payment Registration.
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
---

# Payment File Import

### Overview

**Payment File Import** lets you import a **bank payment file** so Tourpaq Office can **register booking payments automatically**.

This is a function that allows importing in the system the payments that have been made to the bank by the customers.

{% hint style="info" %}
Each company in the system can choose a certain bank where its payments will be made.
{% endhint %}

The bank will provide a file with payments together with the specification for importing them in the system.

This helps with **bank reconciliation** and reduces manual payment entry.

After the import, the payments are visible in [Payment Registration](../payment-registration.md).

***

### Purpose

Use Payment File Import when you receive payments through the bank and want to avoid registering each payment manually.

Although the file format depends on your bank, each payment line normally needs:

* A **booking identifier** (for example booking number/reference)
* A **payment date**
* An **amount**

***

### Before you start

* Make sure you have the **payment file** from your bank.
* Make sure the file contains the **booking reference/identifier** Tourpaq expects.
* Each payment from the system has a certain “method of payment” associated. For the payments that come from the bank, a special method of payment will be needed.
  * If you do not see a suitable method, ask an Admin/Financial user to configure it in [Method of Payment](../method-of-payment.md).
* You must have the required permissions (typically **Financial** or **Administrator**).

{% hint style="info" %}
Your bank (or your finance setup) should provide the **specification** that explains which file format to export and which booking identifier Tourpaq expects.
{% endhint %}

***

### Dependency on System Configuration

The supported file format is directly linked to the system configuration.

{% hint style="warning" %}
Before importing any payment file, ensure that the correct input type is configured.
{% endhint %}

#### Related Setting

**System Setup → General Settings → Input Payments Type**

<figure><img src="../../.gitbook/assets/image (797).png" alt=""><figcaption></figcaption></figure>

* This setting defines which file formats are supported
* Different banks/providers may require different formats
* The system parses the file based on this configuration

{% hint style="info" %}
Selecting an incorrect **Input Payments Type** may result in:

* Failed imports
* Incorrect parsing of payment lines
* Missing or misinterpreted transactions
{% endhint %}

### Workflow Summary

To ensure a successful payment import, follow this sequence:

1. Configure **Input Payments Type** in:
   * System Setup → General Settings
2. Verify that the file matches the expected provider format\
   (e.g. FI 128-character format)
3. Import the file via:
   * **Finance → Payment File Import**
4. The system processes the file based on the selected configuration

### Notes

{% hint style="warning" %}
If you are unsure which format to use, contact your bank or payment provider before attempting the import.
{% endhint %}

{% hint style="info" %}
The format described in this section should be used as a reference guide, not as a substitute for the official provider specification.
{% endhint %}

### Import a payment file

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (9).png" alt="Payment File Import screen"><figcaption><p>Upload a bank payment file to import booking payments and validate matching.</p></figcaption></figure>

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

<figure><img src="../../.gitbook/assets/image (798).png" alt=""><figcaption></figcaption></figure>

Tourpaq validates the file during the upload/import.
{% endstep %}

{% step %}
### Process the file

<figure><img src="../../.gitbook/assets/image (799).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Review validation results

If Tourpaq flags errors (for example missing booking reference or invalid amount), correct the file and upload again.

When the file is accepted, the payments are created in Tourpaq.
{% endstep %}

{% step %}
### Verify the imported payments

Open [Payment Registration](../payment-registration.md) and search by payment date range and payment method (for example **BANKIN**) to confirm the payments are listed.
{% endstep %}
{% endstepper %}

***

### Notes

* Imported payments are validated during import. Any unmatched or erroneous lines are flagged for review.
* The payment date used can depend on your bank file and setup. If your import source uses an **accounting date**, Tourpaq may use that date instead of today.

***

### FAQ

#### 1. Where do imported payments show up?

All the imported payments appear in [Payment Registration](../payment-registration.md).

#### 2. What information must the bank file contain?

At a minimum, Tourpaq needs a **booking identifier**, a **payment date**, and an **amount** for each payment line.

#### 3. Why does the import fail with “booking not found” (or similar)?

Usually, the booking identifier in the file does not match what Tourpaq expects (e.g., the wrong booking number, a missing reference, extra characters, etc.). Confirm the correct identifier format with your bank export specification or your finance administrator.

Ex: If the booking number is not correct in the import file, in this case, when processing the file from the bank, the message "Payments with no correspondent bookings found" will appear, and it will also appear in Balance Administration, where the correct booking number can be added and after saving it will disappear from here.&#x20;

<figure><img src="../../.gitbook/assets/image (800).png" alt=""><figcaption></figcaption></figure>

#### 4. Which payment method is used for imported payments?

Imported payments should use a dedicated payment method. If it is missing, it must be configured in [Method of Payment](../method-of-payment.md).

#### 5. Can I use Payment File Import for refunds?

Not usually. Refunds are typically handled through a separate refund process/file (depending on your setup). If you have a refund import feature available, use that instead.

If your company uses refund imports, see [Refund File Import](../refund-file-import.md).
