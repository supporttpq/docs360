# Arbejdernes Bank Payment Integration (Danske & Syd Bank)

### Official Format Reference

The payment file follows the FI format (FI01–FI09), where each line represents a specific record type.

{% hint style="info" %}
Each record type (FI01–FI09) has a fixed-length structure and must follow strict positional formatting.
{% endhint %}

### File Overview

<figure><img src="../../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

### FI01 — File Header

<table data-header-hidden><thead><tr><th width="199.5555419921875"></th><th></th></tr></thead><tbody><tr><td>FI01</td><td>File Header · Trimmed length: 58 characters · Appears once, first line</td></tr></tbody></table>

**Example:**

```
FI0101308881000314947100000000000000000000020260417065901P
```

{% hint style="info" %}
For the testing environment, this line doesn't need to be modified.
{% endhint %}

### FI02 — Batch Header

<table data-header-hidden><thead><tr><th width="134"></th><th></th></tr></thead><tbody><tr><td>FI02</td><td>Batch Header · Trimmed length: 65 characters · Appears once, second line</td></tr></tbody></table>

The FI02 record describes the payment batch. The import code uses this record to verify that the file belongs to the correct creditor — if the creditor number extracted from this line does not match the system's expected value, the import is rejected with an error.

**Example:**

```
FI020861492065301000090278400000000000000000000000020260417065901
```

<table><thead><tr><th width="104.5555419921875">Position</th><th width="95.5555419921875">Length</th><th width="163.1112060546875">Field Name</th><th width="143.1112060546875">Example</th><th>Description</th></tr></thead><tbody><tr><td>[0 : 4]</td><td>4</td><td>RecordType</td><td>FI02</td><td>Literal record identifier. Always 'FI02'.</td></tr><tr><td>[5 : 13]</td><td>8</td><td>CreditorNumber</td><td>82040226</td><td>Creditor/batch identifier used for validation. Compared against the system-stored creditor number by the C# importer.</td></tr></tbody></table>

{% hint style="info" %}
From the **FI02** line, in the test environment, only the **Creditor Number** field can be modified, located at position **\[5,13]**.
{% endhint %}

{% hint style="info" %}
The Creditor number for each agency can be found in **User -> Brands-> Select agency -> General -> Ticket**. &#x20;
{% endhint %}

<figure><img src="../../.gitbook/assets/image (801).png" alt=""><figcaption></figcaption></figure>

***

### FI03 — Payment Record

**Example:**

```
FI03020260416710000000000308466036227620260416569438084220260417000000000118000 CC000000000N
```

{% hint style="info" %}
This record contains the actual payment transaction details and is the most important line for processing.
{% endhint %}

**Decoding:**

| Field           | Position | Length | Value                 | Description              |
| --------------- | -------- | ------ | --------------------- | ------------------------ |
| Record Type     | 0–3      | 4      | FI03                  | Transaction record       |
| Payment Date    | 5–12     | 8      | 20260416              | Format: YYYYMMDD         |
| Form Type       | 13–14    | 2      | 71                    | Transaction type code    |
| Payer ID        | 15–33    | 19     | 0000000000308466036   | Payer identifier         |
| Booking Number  | 15–30    | 16     | 0000000000308466      | Booking reference        |
| Tracking Code   | 34–55    | 22     | 036227620260416569438 | Archive / reference code |
| Accounting Date | 56–63    | 8      | 20260416              | Accounting date          |
| Amount          | 64–78    | 15     | 0000000000118000      | Amount (÷100 → 1180.00)  |
| Fee Type        | 101–102  | 2      | CC                    | Fee type                 |
| Fee Amount      | 103–111  | 9      | 000000000             | Fee value                |

{% hint style="warning" %}
The **Amount** field is stored without decimals. Always divide by 100 to get the actual value.
{% endhint %}

{% hint style="info" %}
The **Booking Number** is extracted as a subset of the **Payer ID** field.
{% endhint %}

### FI08 — Batch Summary

**Example:**

```
FI0808614920600000000007000000007066700000000000000000
```

{% hint style="info" %}
For the testing environment, this line doesn't need to be modified.
{% endhint %}

{% hint style="info" %}
This record contains aggregated totals for validation purposes.
{% endhint %}

***

### FI09 — File Trailer

**Example:**

```
FI09013088810003149471000000000000000000000100000000007
```

{% hint style="info" %}
For the testing environment, this line doesn't need to be modified.
{% endhint %}

The footer typically contains record counts and control totals.

### Notes

{% hint style="info" %}
The file format is identical for:

* Arbejdernes Bank
* Syd Bank
* Danske Bank
{% endhint %}

{% hint style="warning" %}
There are currently no structural or decoding differences between these banks. Any deviation should be treated as an error.
{% endhint %}
