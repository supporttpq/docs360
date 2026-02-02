# System Setup – Auto Europe (Car Rental Integration)

### Overview

Auto Europe integration lets Tourpaq fetch car rental products through Auto Europe.

Car rental is typically offered via **Extras** in Tourpaq.

Go to **Setup → System Setup → Auto Europe**.

{% hint style="warning" %}
Credentials are sensitive.

Limit access and change them if you suspect exposure.
{% endhint %}

### Purpose

* Enable booking of car rental services alongside other travel components.
* Automate car rental availability and pricing within Tourpaq.
* Centralize management of Auto Europe credentials for all agencies under the company.

### Prerequisites

* An active Auto Europe agreement.
* Auto Europe credentials (username/password).
* Tourpaq configuration for car rental as **Extras** (if not already set up).

### How it works

Tourpaq uses the Auto Europe credentials to authenticate and retrieve car rental availability/pricing.

Those products can then be offered in booking flows via **Extras**.

### Configuration steps

1. **Obtain Credentials**
   * Contact Auto Europe to request a **username** and **password** for system access.
2. **Enter Credentials in Tourpaq**
   * Go to **Setup → System Setup → Auto Europe**.
   * Enter the provided **username** and **password**.
3. **Activate the Integration**
   * After credentials are saved, contact **Tourpaq Support** to activate Auto Europe in the system.

### Usage notes

* Only administrators can configure and activate the integration.
* If credentials are wrong, Tourpaq cannot fetch car rental data.
* Car rental availability depends on your Auto Europe setup and market coverage.

### Troubleshooting

* **No car rentals shown:** Confirm the integration is activated and credentials are correct.
* **Authentication error:** Re-enter credentials and confirm they match Auto Europe.
* **Extras show but prices are missing:** Verify Auto Europe coverage and any required parameters in your Extras setup.

### Related pages

* [Extras](../../extras-setup/extras/)

### FAQ

<details>

<summary><strong>Is Auto Europe a separate product in Tourpaq?</strong></summary>

No. It is an integration.

Car rental is usually offered through the **Extras** flow.

</details>

<details>

<summary><strong>Who can set up Auto Europe?</strong></summary>

Admins can enter credentials.

Activation is typically done by Tourpaq Support after credentials are saved.

</details>

<details>

<summary><strong>Do credentials apply to all agencies/brands?</strong></summary>

In most setups, System Setup credentials are company-wide.

If you need separate credentials per brand, confirm with Tourpaq Support.

</details>

<details>

<summary><strong>What should I test after activation?</strong></summary>

Create a test booking and verify:

* Car rental extras are visible.
* Prices load correctly.
* The booking can be completed with the selected car rental.

</details>
