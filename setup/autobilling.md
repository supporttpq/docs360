# Autobilling

### Overview

Autobilling creates supplier invoices automatically.

It uses the costs you already entered in Tourpaq.

It follows the schedules you set per hotel, extra, transfer, and more.

### What Autobilling can invoice

Autobilling can create invoices for:

* **Hotel deposit**
* **Hotel early booking**
* **Hotel**
* **Extras** (products)
* **Extra early booking**
* **Transfers**
* **Discounts and supplements**
* **Handling**

### Before you start

You need two things:

1. The required background services must be enabled.
2. You must set up at least one creditor (supplier).

#### Required services

These services run in the background.

Most companies need Tourpaq Support to enable them.

* **IGS (Invoice Generating Service)**
  * Runs about every **30 minutes**.
  * Creates invoices based on your Autobilling settings.
* **EBL (Early Booking List)**
  * Runs **once per day** (often around **00:00** server time).
  * Sends the early booking list email (if you use early booking invoicing).
* **HDI (Hotel Deposit Invoice)**
  * Runs about every **30 minutes** after EBL has run.
  * Runs only if **EBL** is enabled.

{% hint style="info" %}
If you are unsure whether these services are enabled, contact Tourpaq Support.
{% endhint %}

### Creditor setup&#x20;

Autobilling needs a creditor.

A creditor is the supplier that receives the invoice email.

<figure><img src="../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

A creditor is created in **Users → Creditors**.

Fill in all required fields.

These fields matter most for Autobilling:

* **Name** and **Email**
* **Currency**
* **Account credit**
* **Automatic** (must be enabled to allow Autobilling)
* **Approval interval (days)** (how long the supplier has to approve or reject)
* **Payment days** (how long you have to pay after approval)
* **Invoice as PDF** (sends invoices as a PDF attachment)

You can add multiple email addresses in the email field.

Separate them with `;` (for example `a@company.com; b@company.com`).

#### Creditor schedules

The creditor includes schedule tabs.

They show what hotels, extras, and other items will be invoiced for that creditor.

To add an item to Autobilling:

* Open the hotel/extra/discount/handling.
* Select the **Creditor** in its Autobilling settings.
* Select the **Schedule** for when invoices should be created.

<figure><img src="../.gitbook/assets/autobilling11-88a0b1b636b2adf09b0f444e4257838f.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
If a product is used across multiple brands, Autobilling may not work if the brands use different currencies.
{% endhint %}

### Email setup

Autobilling sends emails to creditors.

Set this up in **Setup → E-mail center**.

Create these email types:

* **Creditor Invoice**
* **Early Booking Rooming List**

The creditor receives an email with:

* the invoice attached, and
* an approve/reject link (if enabled in your setup).

### Where to view invoices

Invoices are managed in **Finance**.

Access is typically limited to admin and finance users.

Common actions:

* Change status (Approved, Rejected, Paid, Archived)
* Download invoice (PDF, and sometimes XML)
* Regenerate an invoice

<figure><img src="../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

### Invoice statuses

Invoices usually follow this flow:

* **Pending**: the invoice was created and is waiting for approval.
* **Approved**: the supplier approved it.
* **Paid**: you marked it as paid.

<figure><img src="../.gitbook/assets/image (85).png" alt=""><figcaption></figcaption></figure>

Other statuses you may see:

* **Regenerated**: the invoice was rebuilt after a change.

<figure><img src="../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>

* **Archived**: the invoice was archived for record-keeping.

<figure><img src="../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If you change the creditor on a hotel, regenerating an invoice can reflect that change.
{% endhint %}

### Autobilling setup

You enable Autobilling per item (hotel, extra, discount, etc.).

Each item has an Autobilling section where you set:

* whether it should be invoiced,
* who the creditor is, and
* when invoices should be created.

#### Hotel invoices

Enable Autobilling on the hotel’s main tab.

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

These fields are required:

* **Automatic billing** (turns invoicing on/off)
* **Schedule** (daily/weekly/monthly). Weekly is common.
* **Creditor**
* **Account debit**
* **Account deposit** (if you use hotel deposits)
* **Department code**
* **Schedule before arrival** (optional). Sends invoices in advance.

{% hint style="info" %}
For hotel invoices to make sense, room costs and other costs must be set on the hotel.
{% endhint %}

Hotel combinations can also be invoiced.

Set Autobilling on the hotels that are part of the combination.

On the invoice, a booking made with a combination is shown under one of those hotels.

If you regenerate a hotel invoice, extras can appear on it.

This happens when the extra uses the same Autobilling settings as the hotel.

It also requires **Add own schedule** to be turned off for the extra.

### Hotel Deposit​ <a href="#hotel-deposit" id="hotel-deposit"></a>

Set this in the **Hotel → Deposit** tab.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

A deposit requires:

* **Deposit date**: when the deposit invoice is created.
* **Payment type**: auto-filled by the system.
* **Amount**: the deposit amount.
* **Payback date**: when the deposit is paid back or deducted.

The deposit is deducted from the final hotel invoice only when it is marked as **Paid**.

Deposit timing is usually agreed in the supplier contract.

**Special deposit rule** can pre-calculate deposit amounts for multiple deposit dates.

It requires room allotments and costs to be set on the hotel.

### Hotel Early Booking​ <a href="#hotel-early-booking" id="hotel-early-booking"></a>

Set this from the hotel’s room cost settings.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Required fields:

* **Send list date**: sends the Early Rooming List email.
* **Deposit date**: creates an invoice for booked rooms.
* **Deposit percent**: the percent to pay now.

The early booking deposit is deducted from later hotel invoices.

If the early booking list email does not arrive, you can use **Export → List** with report type **Rooming list**.

Use the same filters as your early booking room cost rules.

#### Extra invoices

Enable Autobilling on the extra’s main tab.

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

These fields are required:

* **Automatic billing**
* **Creditor**
* **Department code**
* **Account debit**
* **Schedule**
* **Add own schedule**
  * Off: the extra is invoiced together with the hotel invoice (when possible).
  * On: the extra gets its own separate invoice.

{% hint style="info" %}
For extras, both prices and costs must be set.
{% endhint %}

### Extra Early Booking <a href="#extra-early-booking" id="extra-early-booking"></a>

Works the same way as **Hotel Early Booking**.

#### Discount and supplement invoices

Enable Autobilling on the discount/supplement’s main tab.

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

These fields are required:

* **Automatic billing**
* **Creditor**
* **Department code**
* **Account debit**
* **Schedule**
* **Add own schedule**
  * Off: can be invoiced together with the hotel invoice.
  * On: gets its own invoice.

Prices and costs must also be set.

#### Transfer invoices

Enable Autobilling for transfers in **Transport → Transfer prices**.

These fields are required:

* **Automatic billing**
* **Creditor**
* **Department code**
* **Account debit**
* **Schedule**
* **Add own schedule**

Prices and costs must also be set.

#### Handling invoices

Enable Autobilling for handling in **Users → Suppliers → Handling**.

<figure><img src="../.gitbook/assets/image (363).png" alt=""><figcaption></figcaption></figure>

These fields are required:

* **Creditor**
* **Account debit**
* **Schedule**
* **Add own schedule**

Costs are also required.

In many setups, handling costs can be set only when a hotel is assigned to the supplier.

If a supplier is removed from a hotel and you regenerate the invoice, handling for that hotel is removed.

If the invoice only contained that hotel, it may be marked as **Deleted**.

### Related pages

* [How to create a creditor](../autobilling/how-to-create-a-creditor.md)
* [Creditor invoices](../autobilling/creditor-invoices.md)

### FAQ

<details>

<summary><strong>Why is Autobilling not creating invoices?</strong></summary>

Most common reasons:

* The background services are not enabled.
* The item (hotel/extra/transfer/etc.) does not have **Automatic billing** enabled.
* No **Creditor** is selected on the item.
* Prices or costs are missing on the item.

</details>

<details>

<summary><strong>Can I send invoices to more than one email address?</strong></summary>

Yes.

Add multiple email addresses in the creditor email field.

Separate them with `;`.

</details>

<details>

<summary><strong>What does “Add own schedule” do?</strong></summary>

It decides whether an item is invoiced together with the hotel invoice.

If enabled, the item gets its own separate invoice.

</details>

<details>

<summary><strong>What do the invoice statuses mean?</strong></summary>

* **Pending**: created and waiting for approval.
* **Approved**: approved by the supplier.
* **Paid**: marked as paid in Finance.
* **Regenerated**: rebuilt after a change.
* **Archived**: stored for record-keeping.

</details>

<details>

<summary><strong>Can I regenerate an invoice after changes?</strong></summary>

Yes, if you have access to Finance invoice actions.

Regeneration is often used after cost corrections or supplier changes.

</details>

<details>

<summary><strong>Why do hotel combination bookings show as a different hotel on the invoice?</strong></summary>

Hotel combinations are invoiced using the hotels inside the combination.

That is why the invoice shows the underlying hotel.

</details>
