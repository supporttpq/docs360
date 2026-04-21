# Arbejdernes Bank Payment Integration (Danske & Syd Bank)

### Official Format Reference

The payment file follows the FI format (FI01–FI09), where each line represents a specific record type.

{% hint style="info" %}
Each record type (FI01–FI09) has a fixed-length structure and must follow strict positional formatting.
{% endhint %}

### File Overview

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

### Header – FI01

**Example:**

```
FI0101308881000314947100000000000000000000020260417065901P
```

{% hint style="warning" %}
The **Creditor Number** must be replaced with a unique number from your test agency when testing File Import.
{% endhint %}

**Decoding:**

| Position | Length | Description     | Value    |
| -------- | ------ | --------------- | -------- |
| 0–3      | 4      | Record Type     | FI01     |
| 5–12     | 8      | Creditor Number | 01308881 |

{% hint style="info" %}
The Creditor number for each agency can be found in User -> Brands-> Select agency -> General -> Ticket.&#x20;
{% endhint %}

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### 2. Account Information – FI02

**Example:**

```
FI020861492065301000090278400000000000000000000000020260417065901
```

{% hint style="info" %}
For the testing environment, this line doesn't need to be modified.
{% endhint %}

***

### 3. Transaction – FI03

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

### 4. Summary / Totals – FI08

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

### 5. Footer – FI09

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
