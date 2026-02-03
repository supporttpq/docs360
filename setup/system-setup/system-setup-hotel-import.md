# System Setup – Hotel Import

### Overview

Hotel Import defines default settings used when importing hotel data and hotel contracts.

It standardizes:

* Price adjustments (single room, board supplements, gala dinners)
* Default hotel release hour
* Whether board basis extras are created during hotel contract import

Go to **Setup → System Setup → Hotel Import**.

{% hint style="warning" %}
Changes can affect future imports and contract behavior.

Validate changes on a test contract/import when possible.
{% endhint %}

### Purpose

Use these settings to keep imported hotel data consistent and reduce manual corrections.

They help you:

* Automate price adjustments for certain services.
* Apply consistent release timing.
* Reduce manual errors during imports.

### Preconditions

Before configuring the **Hotel Import** settings:

1. You must have **administrator access** to System Setup.
2. Basic hotel data should already exist in the system or be ready for import.
3. You should understand the company’s pricing policies for single rooms, board supplements, and gala dinners.

### Fields

<figure><img src="../../.gitbook/assets/image (393).png" alt=""><figcaption></figcaption></figure>

#### Hotel Release Hour

* **What it does:** Sets the default release time used on imported hotel releases.
* **Default:** `07:00` if not set.
* **Format:** 24-hour time (`HH:MM`).
* **Example:** `06:00` means releases are set to 06:00 (6 AM).

#### Single Room Supplement Price

* **What it does:** Adds a percentage markup for single room bookings.
* **Format:** Percentage.
* **Example:** `2` means +2% on the base price.

#### Board Supplement Price

* **What it does:** Adds a percentage markup for board (meal plan) supplements.
* **Format:** Percentage.
* **Example:** `2` means +2% on top of the base room price.

#### Gala Dinner Price

* **What it does:** Adds a percentage markup when a gala dinner is included.
* **Format:** Percentage.
* **Example:** `2` means +2% on the booking price when gala dinner is included.

#### Do not create extras for board basis

* **What it does:** Prevents creating extras for board basis when importing a hotel contract.
* **Format:** Checkbox.
* **When to use:** If your setup does not use board basis as extras.

### How to use

1. Go to **Setup → System Setup → Hotel Import**.
2. Set the **Hotel Release Hour** according to company standards.
3. Enter the percentage values for **Single Room Supplement**, **Board Supplement**, and **Gala Dinner Price** as per pricing policy.
4. Configure **Do not create extras for board basis** if needed.
5. Save changes.

### Related pages

* [Hotel Contracts](../../hotel-contracts/)
* [Releases](../../hotel/hotel-creation/releases/)

### Troubleshooting

* **Release time looks wrong after import:** Confirm **Hotel Release Hour** is set and saved.
* **Unexpected price changes:** Re-check the percentage fields (single/board/gala).
* **Missing board extras after import:** Ensure **Do not create extras for board basis** is not enabled.
* **Board extras created but you don’t want them:** Enable **Do not create extras for board basis** and re-import/recreate the contract flow as needed.

### FAQ

<details>

<summary><strong>Do these settings affect existing hotel contracts?</strong></summary>

These settings are used as defaults during import.

Existing contracts may not change automatically.

</details>

<details>

<summary><strong>What time format should I use for Hotel Release Hour?</strong></summary>

Use 24-hour time: `HH:MM`.

Example: `06:00`, `14:30`.

</details>

<details>

<summary><strong>What does “2” mean in the price fields?</strong></summary>

It means 2 percent.

`2` = +2% markup.

</details>

<details>

<summary><strong>When should I enable “Do not create extras for board basis”?</strong></summary>

Enable it if your company does not use board basis as extras.

This avoids creating extra products during contract import.

</details>

<details>

<summary><strong>Why are board basis extras useful?</strong></summary>

They can be useful if you sell board upgrades as separate line items.

If you don’t, disabling creation keeps your extras list cleaner.

</details>
