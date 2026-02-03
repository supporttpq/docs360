# Currency rates

## Currency rates

### Overview

Currency rates decide how amounts are converted and shown across Tourpaq.

They affect totals and statistics in bookings.

This matters when you use more than one currency.

### Purpose

Use this page to:

* Add, edit, or delete currency rates.
* Choose a default currency for the company.
* Choose a currency per brand.

<figure><img src="../.gitbook/assets/image (35) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Changing currency rates can change totals in bookings and reports.

Update rates carefully. Then double-check a known booking or report.
{% endhint %}

### Manage currency rates

Go to **Setup → System Setup → Currency**.

* **Add a rate**
  1. Click **Add**.
  2. Enter the currency and rate.
  3. Click **Save**.
* **Edit a rate**
  1. Select the rate in the list.
  2. Update the value.
  3. Click **Save**.
* **Delete a rate**
  1. Select the rate in the list.
  2. Click **Delete**.

### Set default currencies

* **Company Currency**
  * Go to **Setup → System Setup → General Information**.
  * Select a value in **Default Currency**.
* **Brand Currency**
  1. Navigate to **Users → Brands**.
  2. Click **Edit** next to the brand.
  3. Select a value in the **Currency** dropdown.

### Currency in Bookings

<figure><img src="../.gitbook/assets/image (36) (1).png" alt=""><figcaption></figcaption></figure>

* **Totals Panel**
  * Totals are shown in the currency of the selected **Brand** (top-left).
  * If you select **All Brands**, totals are converted to the **company currency**.
* **Statistics Panel**
  * Open **All bookings → View All Bookings & Statistics → Statistics**.
  * With **Additional Sales per Seller / Turnover** enabled, totals follow the selected brand’s currency.
  * With **All Brands** selected, totals are converted to the **company currency**.

### Related page

* [System Setup – Currency](system-setup/system-setup-currency.md)

### FAQ

<details>

<summary><strong>Why do my totals change when I select “All Brands”?</strong></summary>

Because Tourpaq shows combined totals in the company’s default currency.

It converts amounts before adding them up.

</details>

<details>

<summary><strong>Where do I change the company’s default currency?</strong></summary>

Go to **Setup → System Setup → General Information**.

Update **Default Currency**.

</details>

<details>

<summary><strong>Can each brand use its own currency?</strong></summary>

Yes.

Go to **Users → Brands**, edit the brand, and set **Currency**.

</details>

<details>

<summary><strong>I can’t see the Currency tab. What’s wrong?</strong></summary>

You may not have access to **Setup → System Setup**.

Ask an admin in your company to check your permissions.

</details>

<details>

<summary><strong>What should I check after changing a currency rate?</strong></summary>

Open a booking you know well and compare the totals.

Then check a report that uses currency conversion.

</details>

<details>

<summary><strong>What happens if a currency rate is missing?</strong></summary>

Tourpaq may not be able to convert amounts correctly.

Add the missing currency rate, then re-check totals and reports.

</details>
