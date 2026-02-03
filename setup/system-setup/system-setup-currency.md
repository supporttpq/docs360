# System Setup – Currency

### Overview

Currency settings control exchange rates and default currencies in Tourpaq.

They affect totals, statistics, and financial reporting across the system.

Go to **Setup → System Setup → Currency**.

{% hint style="warning" %}
Changing exchange rates impacts totals and reports.

Update rates carefully and validate on a test booking/report when possible.
{% endhint %}

### Purpose

* Define and maintain **currency exchange rates**.
* Configure **default company and brand currencies**.
* Keep **totals and statistics** consistent across bookings and reports.

### Configuration

#### Currency rates

* Go to **Setup → System Setup → Currency**.
* Click **Add** to create a rate.
* Click **Save** to apply changes.
* Select a rate and click **Delete** to remove it.

#### Company default currency

Set the currency used as the company default.

* Go to **Setup → System Setup → General Information**.
* Set **Default Currency**.

#### Brand currency

Set a currency per brand if you operate multiple brands.

* Go to **Users → Brands**.
* Select a brand and click **Edit**.
* Select a value in the **Currency** dropdown.

### Usage in bookings

#### Totals

* The currency is shown at the end of each total in the **Totals** panel.
* If **All brands** is selected, totals are shown in the **company default currency**.

#### Statistics

* Found under the **Statistics** tab in **All bookings**.
* Some statistics are shown in **brand currency** (depending on the selected options).
* If **All brands** is selected, totals are shown in **company currency**.

### Related settings

* [System Setup – General Information Settings](system-setup-general-information-settings.md)

### FAQ

<details>

<summary><strong>Why do totals change when I select “All brands”?</strong></summary>

Because totals are shown in the **company default currency**.

Tourpaq converts amounts when aggregating across brands.

</details>

<details>

<summary><strong>Where do I change the company’s default currency?</strong></summary>

Go to **Setup → System Setup → General Information**.

Update **Default Currency**.

</details>

<details>

<summary><strong>Where do I set a different currency per brand?</strong></summary>

Go to **Users → Brands**.

Edit the brand and set the **Currency** field.

</details>

<details>

<summary><strong>What should I do before updating exchange rates?</strong></summary>

Confirm the new rates with your finance process.

Then validate totals on a known booking/report after saving.

</details>

<details>

<summary><strong>What happens if an exchange rate is missing?</strong></summary>

Conversions can fail or show inconsistent totals.

Add the missing currency rate and re-run your report.

</details>
