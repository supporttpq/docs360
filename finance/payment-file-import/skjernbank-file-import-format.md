# SkjernBank File Import Format

## Official Format Reference

The structure presented in this documentation is based on the FI payment format (128-character format).

{% hint style="info" %}
The official reference specification is: **"Systemvejledning for FI-advisering (128-karakter format)"**&#x20;

This document can be obtained from your payment provider (e.g., Mastercard Payment Services), depending on your agreement with them.
{% endhint %}

{% hint style="warning" %}
Availability and exact specifications may vary depending on the provider implementation.
{% endhint %}

## File Overview

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

This specific file — FI\_payments\_17\_03\_2026.PBS — contains 136 lines total and represents payments collected on behalf of creditor 45801012 and processed on 17 March 2026.

This section describes the expected structure of supported payment import files.\
The exact format depends on the selected **Input Payments Type** and the bank or payment provider configuration.

{% hint style="info" %}
The file format described below is provided for informational purposes only.
{% endhint %}

### Record Type Summary

<table><thead><tr><th width="133.6666259765625" align="center">Record Type</th><th width="106.2222900390625" align="center">Length</th><th width="171.77783203125" align="center">Name</th><th valign="middle">Purpose</th></tr></thead><tbody><tr><td align="center">FI01</td><td align="center">58</td><td align="center"><strong>File Header</strong></td><td valign="middle">Identifies the creditor and file creation timestamp. Validated once per file.</td></tr><tr><td align="center">FI02</td><td align="center">65</td><td align="center"><strong>Batch Header</strong></td><td valign="middle">Batch-level metadata. The C# import code validates the creditor number from this line.</td></tr><tr><td align="center">FI03</td><td align="center">113</td><td align="center"><strong>Payment Record</strong></td><td valign="middle">One line per individual payment. Contains all fields extracted by the importer.</td></tr><tr><td align="center">FI08</td><td align="center">53</td><td align="center"><strong>Batch Summary</strong></td><td valign="middle">Closing totals for the batch: record count and grand total amount.</td></tr><tr><td align="center">FI09</td><td align="center">53</td><td align="center"><strong>File Trailer</strong></td><td valign="middle">File-level footer confirming creditor identity and total record count.</td></tr></tbody></table>

### FI01 — File Header

<table data-header-hidden><thead><tr><th width="199.5555419921875"></th><th></th></tr></thead><tbody><tr><td>FI01</td><td>File Header · Trimmed length: 58 characters · Appears once, first line</td></tr></tbody></table>

**Example line:**

```
FI010458010120032479081 000000000020260324112701P
```

{% hint style="info" %}
For the testing environment, this line doesn't need to be modified.
{% endhint %}

### FI02 — Batch Header

<table data-header-hidden><thead><tr><th width="134"></th><th></th></tr></thead><tbody><tr><td>FI02</td><td>Batch Header · Trimmed length: 65 characters · Appears once, second line</td></tr></tbody></table>

The FI02 record describes the payment batch. The import code uses this record to verify that the file belongs to the correct creditor — if the creditor number extracted from this line does not match the system's expected value, the import is rejected with an error.

{% hint style="info" %}
From the **FI02** line, in the test environment, only the **Creditor Number** field can be modified, located at position **\[5,13]**.
{% endhint %}

**Example line:**

```
FI020820402267780000207443300000000000000000000000020260324112701
```

<table><thead><tr><th width="104.5555419921875">Position</th><th width="95.5555419921875">Length</th><th width="163.1112060546875">Field Name</th><th width="143.1112060546875">Example</th><th>Description</th></tr></thead><tbody><tr><td>[0 : 4]</td><td>4</td><td>RecordType</td><td>FI02</td><td>Literal record identifier. Always 'FI02'.</td></tr><tr><td>[5 : 13]</td><td>8</td><td>CreditorNumber</td><td>82040226</td><td>Creditor/batch identifier used for validation. Compared against the system-stored creditor number by the C# importer.</td></tr></tbody></table>

### FI03 — Payment Record

<table data-header-hidden><thead><tr><th width="112.8887939453125"></th><th></th></tr></thead><tbody><tr><td>FI03</td><td>Payment Record · Trimmed length: 113 characters · Repeats once per payment (132 records)</td></tr></tbody></table>

FI03 is the core data record. Each line represents a single payment collected from a payer (subscriber) and credited to the agency. The importer reads every FI03 line and constructs an `ImportedPayment` object from six fields within it.

**Example line:**

```
FI030202603167100000000007745180132225202603163573674200202603170000000000996000000000000000000099600CC000000000N
```

In the test environment, for any **FI03** line, modifications can be made to the following positions:

<table><thead><tr><th width="105.6666259765625">Position</th><th width="98.888916015625">Length</th><th width="168.77783203125">Field Name</th><th width="164.7777099609375">Example</th><th>Description</th></tr></thead><tbody><tr><td>[0 : 4]</td><td>4</td><td>RecordType</td><td>FI03</td><td>Literal record identifier. Always 'FI03'.</td></tr><tr><td>[5 : 13]</td><td>8</td><td>DateCustomerPaid</td><td>20260316</td><td>Date the payer's bank debited the payment, in YYYYMMDD format (DateCustomerPaid in C#). This is the customer-facing payment date.</td></tr><tr><td>[19 : 31]</td><td>12</td><td>BookingNo</td><td>000007745180</td><td>12-digit payer subscription/booking number, zero-padded. Parsed as Int64 (bookingNo). This is the primary subscriber identifier.</td></tr><tr><td>[19 : 34]</td><td>15</td><td>PayerID</td><td>000007745180132</td><td>15-character payer identifier = BookingNo (12) + 3-digit sequence suffix. This is the full PayerID stored on ImportedPayment.</td></tr><tr><td>[46 : 56]</td><td>10</td><td>TrackingCode</td><td>3573674200</td><td>Unique 10-digit transaction reference assigned by the clearing system (TrackingCode in C#). Can be used to identify or reconcile a specific payment.</td></tr><tr><td>[56 : 64]</td><td>8</td><td>AccountingDate</td><td>20260317</td><td>Date the payment is posted to the creditor's account, in YYYYMMDD format (AccountingDate in C#). Typically one business day after DateCustomerPaid.</td></tr><tr><td>[64 : 79]</td><td>15</td><td>Amount</td><td>000000000099600</td><td>Payment amount in øre (1/100 of DKK) or eurocents, zero-padded to 15 digits. Divided by 100 by the importer to get the decimal value (996.00 in this example).</td></tr></tbody></table>

{% hint style="info" %}
Note on overlapping fields: PayerID (positions 19–34, 15 chars) and BookingNo (positions 19–31, 12 chars) share the same starting position. BookingNo is simply the first 12 characters of PayerID. The C# code reads both independently using different `Substring()` lengths.
{% endhint %}

{% hint style="info" %}
Note on amount encoding: amounts are stored as integers in the smallest currency unit (øre for DKK, eurocents for EUR). The value 000000000099600 = 99,600 øre = 996.00 DKK. Always divide the raw field by 100 to obtain the decimal amount.
{% endhint %}

### FI08 — Batch Summary

<table data-header-hidden><thead><tr><th width="109.5555419921875"></th><th></th></tr></thead><tbody><tr><td>FI08</td><td>Batch Summary · Trimmed length: 53 characters · Appears once after last FI03</td></tr></tbody></table>

The FI08 record closes the payment batch. It provides control totals that can be used to verify the integrity of all FI03 records: the total record count and the total of all amounts.

{% hint style="info" %}
The importer does not currently read this record, but it should be used for reconciliation.
{% endhint %}

**Example line:**

```
FI0808204022600000000132000000068752200000000000000000
```

### FI09 — File Trailer

<table data-header-hidden><thead><tr><th width="112.888916015625"></th><th></th></tr></thead><tbody><tr><td>FI09</td><td>File Trailer · Trimmed length: 53 characters · Appears once, last line</td></tr></tbody></table>

The FI09 record is the file-level footer. It repeats the creditor identification from FI01 and provides a final record count covering the entire file.

{% hint style="info" %}
Can be used as a second-level integrity check, independent of the batch summary in FI08.
{% endhint %}

**Example line:**

```
FI090458010120032479081 0000000000100000000132
```

## Annotated File Sample

The table below shows the first six lines of FI\_payments\_17\_03\_2026.PBS with key fields annotated.

```
// FI01 — File Header (creditor: 45801012, created: 2026-03-24 11:27:01, type: Production)
FI01 04580101 2003247908 1 000000000020260324112701P

// FI02 — Batch Header (creditorNo check at [5:13] = '82040226', date: 2026-03-24)
FI02 08204022 6778000020 7443300000000000000000000000020260324112701

// FI03 — Payment #1 | BookingNo: 7745180 | Payer ID: 000007745180132 | Traking code: 3573674200 |Amount: 996.00 | Paid: 2026-03-16 | Accounted: 2026-03-17
FI03 0 20260316 710000 000007745180 132 2225 20260316 3573674200 20260317 000000000099600 00000000000000 00099600 CC 000000000 N

// FI03 — Payment #2 | BookingNo: 7746160 | Payer ID: 000007746160152 | Traking code: 3573852000 |Amount: 498.00 | Paid: 2026-03-16 | Accounted: 2026-03-17 | Cumulative: 1,494.00
FI03 0 20260316 710000 000007746160 152 2225 20260316 3573852000 20260317 000000000049800 00000000000000 00149400 CC 000000000 N

// FI08 — Batch Summary | Records: 132 | Grand Total: 687,522.00
FI08 0820 4022600000 000000 132 68752200 000000000000000000

// FI09 — File Trailer | Creditor: 45801012 | Total records: 132
FI09 0 45801012 0032479081 0000000000 1 0000000132
```

Spaces have been inserted between fields in the annotated sample above for readability only. The actual file contains no spaces between fields — every field is contiguous.

## FAQ

#### Which lines matter for the Tourpaq import?

The import logic mainly depends on:

* **FI02** for creditor validation
* **FI03** for individual payment data

**FI08** and **FI09** are useful for reconciliation and integrity checks, but the importer does not currently use them to create payments.

#### Which FI03 fields must be correct for a payment to import properly?

The most important fields are:

* **BookingNo**
* **PayerID**
* **TrackingCode**
* **AccountingDate**
* **Amount**
* **DateCustomerPaid**

If one of these values is malformed, the payment may fail validation, import incorrectly, or be hard to reconcile afterward.

#### Which date is used as the payment date in Tourpaq?

That depends on the import setup.

This file contains both:

* **DateCustomerPaid**
* **AccountingDate**

In many finance flows, **AccountingDate** is the value used for posting and reconciliation. Validation should still include both dates because they describe different stages of the transaction.

#### Can BookingNo and PayerID contain different values?

Partly.

**BookingNo** is the first 12 characters of **PayerID**. The last 3 characters in **PayerID** are a suffix sequence. If the first 12 characters do not match the intended booking reference, the payment may be linked incorrectly or rejected by downstream validation.

#### Why is the Amount field 15 characters long?

The file stores the amount as a zero-padded integer in the smallest currency unit.

Example:

* `000000000099600` = `99600` øre = **996.00**

The importer divides the raw value by **100** before storing the final payment amount.

#### Can FI08 and FI09 be ignored?

They should not be ignored during file validation. In the test environment, these can be ignored in generating the payment file.

Even though the importer does not currently parse them into payments, they help confirm:

* the expected number of payment records
* the expected grand total
* the file-level consistency of the import source

These checks are useful when investigating missing or duplicated payments.

#### What is the safest way to test a modified PBS file?

Validate the file in this order:

1. Confirm the **FI02 CreditorNumber** matches the expected test setup.
2. Confirm each edited **FI03** line keeps its fixed-width length.
3. Confirm **BookingNo**, **PayerID**, **Dates**, and **Amount** still sit at the correct positions.
4. Import the file and verify the result in payment registration.

## Related pages

* [Payment File Import](./) — import the bank file and validate payment lines.
* [Payment Registration](../payment-registration.md) — review imported payments after processing.
* [Refund File Import](../refund-file-import.md) — handle imported refund transactions instead of incoming payments.
* [Method of Payment](../method-of-payment.md) — configure the payment method used for bank imports.
* [Balance Administration](../../balance-administration.md) — reconcile balances after payment import.
