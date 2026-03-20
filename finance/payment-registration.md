---
description: >-
  Manually register booking payments, filter payment records, and export payment
  reports in Tourpaq Office Finance.
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

# Payment Registration

### Overview

**Payment Registration** is the Tourpaq Office **Finance** screen for **payment records**.

Use it to **find payments**, **reconcile booking balances**, and **manually register booking payments**.

You can see:

* **Booking payments** (payments connected to a specific booking)
* **Guide payments** (payments handled by guides)

{% hint style="info" %}
You can **only create booking payments** in Payment Registration. **Guide payments are view-only** here.
{% endhint %}

### What you can do

* Filter and review payment records in the payment list
* Register a new payment on a booking (manual payment entry)
* Export payment results for reporting, reconciliation, or audits

### Before you start

* You must be logged in with the required permissions (typically **Financial** or **Administrator**)
* To register a payment, you need the **booking number/reference** and the **amount**
* If you need to import many bank payments, use [Payment File Import](payment-file-import.md)
* If you need to import many refunds, use [Refund File Import](refund-file-import.md)
* If a payment method is missing, check [Method of Payment](method-of-payment.md)

***

### View and filter payments

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (16).png" alt="Payment Registration filters and results"><figcaption><p>Filter payment records and review results in Payment Registration.</p></figcaption></figure>

1. Set **Payment start date** and **Payment end date**.
2. (Optional) Set **Departure start date** and/or **Departure end date**.
3. (Optional) Select a **Payment method** (for example `CARD`, `CASHIN`, `BANKIN`, `GIFT`).
4. (Optional) Use additional filters such as:
   * **Debit/Credit**
   * **Payment purpose** (for example _All Payments_ or _Booking Only_)
   * **Guide**
   * **Transport**
   * **GiftCard No**
   * **Booking reference/number**
5. Click **Display** to load the results.

{% hint style="warning" %}
**Booking vs. guide payments:**

* If you select a **Guide** (or **All guides**), Tourpaq shows **guide payments** (and booking-related filters may be hidden).
* If you filter by **Booking**, **Departure dates**, or other booking-related values, Tourpaq shows **booking payments**.

A payment is either a **booking payment** _or_ a **guide payment**—not both.
{% endhint %}

<details>

<summary>How “empty” date filters work</summary>

Leaving a date field empty means “don’t filter by this date”.

* **Payment start date empty**
  * If **Payment end date** is set, you’ll get payments **before** the end date.
  * If **Payment end date** is also empty, Tourpaq will **not** filter by payment date.
* **Payment end date empty**
  * If **Payment start date** is set, you’ll get payments **after** the start date.
  * If **Payment start date** is also empty, Tourpaq will **not** filter by payment date.
* **Departure start/end date empty** works the same way for the departure date filter.

Example:

* Payment start date = `26.03.2025`
* Payment end date = `31.03.2025`
* Departure end date = `30.04.2025`

This shows payments made between `26.03.2025` and `31.03.2025` for bookings departing **before** `30.04.2025`.

</details>

***

### Register a new booking payment

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Create payment form"><figcaption><p>Create a manual booking payment with method, date, booking reference, and amount.</p></figcaption></figure>

{% stepper %}
{% step %}
### Open the create form

Click **Create**.
{% endstep %}

{% step %}
### Fill in the payment details

Enter the key fields:

* **Method of payment** (for example `BANKIN` or `CASHIN`)
* **Payment date**
* **Booking number/reference**
* **Amount**

Optional (only if relevant):

* **GiftCard No**
* **Extra order**
* **Comments** (recommended so it’s easier to understand the payment later)
{% endstep %}

{% step %}
### Save

Click **Save** to register the payment.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
If you don’t see your new payment in the list right away, adjust your **payment date filters** and click **Display** again.
{% endhint %}

***

### Export payments (payment report)

1. Apply the filters you want.
2. Click **Export** to export the **currently displayed** results.

This export is your payment report for the selected filters.

***

### FAQ

#### 1. Can I register guide payments here?

No. Payment Registration is used to **create booking payments**. Guide payments can be **viewed** here when you filter by **Guide**, but they are not created in this module.

#### 2. I selected a guide and now I can’t filter by booking number—why?

When you filter by **Guide**, Tourpaq switches to **guide payments**, which are not connected to a booking in the same way, so booking-related filters may be hidden.

#### 3. What dates should I use if I can’t find a payment?

Start by widening **Payment start date** and **Payment end date**, then click **Display**. If it’s tied to a booking, also check your **Departure** date filters.

#### 4. What’s the difference between Debit and Credit?

* **Debit** typically means money coming **into** the company (a payment received).
* **Credit** typically means money going **out** (for example a refund).

If you’re unsure, confirm with your finance setup.

#### 5. Where do imported bank payments show up?

After a successful import, they appear in this list.

See [Payment File Import](payment-file-import.md).

#### 6. A payment method is missing from the dropdown—what should I do?

Ask an Admin/Financial user to add or activate it in [Method of Payment](method-of-payment.md).

#### 7. Does Export include all payments in the system?

No. Export uses the **current filters** and exports only the results you have displayed.
