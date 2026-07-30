---
description: >-
  Configure exchange rates and default currencies for Tourpaq totals,
  statistics, and reporting.
---

# System Setup – Currency

### Overview

Currency settings control exchange rates and default currencies in Tourpaq.

They support booking totals, statistics, and financial reporting. These settings work with company defaults and brand configuration.

{% hint style="warning" %}
Changing exchange rates impacts totals and reports.

Validate changes with a test booking and report.
{% endhint %}

### Requirements

Configure currency settings only when these requirements are met:

* **Administrator** rights for **System Setup**.
* Finance-approved exchange rates and currency defaults.
* A test booking and relevant report for validation.

### Navigation

Open the currency settings:

1. In Tourpaq Office, open **Setup**.
2. Click **System Setup**.
3. Click **Currency**.

### Purpose

Currency settings support these tasks:

* Define and maintain **currency exchange rates**.
* Configure **default company and brand currencies**.
* Keep **totals and statistics** consistent across bookings and reports.

### Interface overview

The **Currency** page manages exchange-rate entries. Use these controls:

* **Add** creates an exchange-rate entry.
* **Save** stores currency changes.
* **Delete** removes the selected exchange-rate entry.

### Configuration

#### Currency rates

Use the **Currency** page to create or remove exchange-rate entries:

1. Click **Add**.
2. Enter the required exchange-rate details.
3. Click **Save**.

To remove an exchange-rate entry:

1. Select the rate to remove.
2. Click **Delete**.

#### Company default currency

Set the currency used as the company default:

1. In Tourpaq Office, go to **Setup → System Setup → General Information**.
2. Set **Default Currency**.

#### Brand currency

Set a currency per brand for multiple-brand operations:

1. In Tourpaq Office, go to **Users → Brands**.
2. Select the brand.
3. Click **Edit**.
4. Select a value in the **Currency** dropdown.

### System behavior

Tourpaq applies currency settings throughout booking and reporting workflows:

* Each booking total shows its selected currency in the **Totals** panel.
* Brand-specific settings determine currencies for brand-specific statistics.
* **All brands** converts aggregated totals to the company default currency.
* Missing exchange rates can cause failed conversions or inconsistent totals.

### Usage in bookings

#### Totals

Totals use the selected currency as follows:

* The currency is shown at the end of each total in the **Totals** panel.
* If **All brands** is selected, totals are shown in the **company default currency**.

#### Statistics

Statistics use the selected currency as follows:

* Found under the **Statistics** tab in **All bookings**.
* Some statistics are shown in **brand currency** (depending on the selected options).
* If **All brands** is selected, totals are shown in **company currency**.

### Examples

#### Single-brand booking

A brand uses **EUR** in its **Currency** setting. Booking totals and applicable statistics display in EUR.

#### Combined brand reporting

Two brands use different currencies. Select **All brands** to show combined totals in the company default currency.

### Related settings

* [System Setup](./)
* [System Setup – General Information Settings](system-setup-general-information-settings.md)
