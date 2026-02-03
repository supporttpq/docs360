# Arrival Gateways

### Overview

**Arrival Gateways** is a reference list of airports used as arrival points. Use it to search, sort, create, and delete arrival gateways.

<figure><img src="../.gitbook/assets/image (19) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Features

* **Search:** Find gateways by typing in the search bar.
* **Sorting:** Sort by columns like IATA code, Plaintext, and Insurance area.
* **Create:** Add a new gateway with the **Create** button.
* **Delete:** Remove a gateway using the trash bin icon.

### Column Breakdown

1. **IATA Code:** The three-letter airport code (for example, `PMI`).
2. **Plaintext:** The display name for the gateway.
3. **Plaintext (Not Flight):** The display name used in contexts not tied to flights.
4. **Insurance area:** Classification used for insurance reporting (for example, Europe).
5. **Actions:** Delete the gateway.

### Common tasks

{% stepper %}
{% step %}
### Search for a gateway

1. Type in the search bar.
2. Review the filtered list.
{% endstep %}

{% step %}
### Create a gateway

1. Click on the **Create** button.
2. Enter the required fields.
3. Save.
{% endstep %}

{% step %}
### Delete a gateway

1. Find the gateway in the list.
2. Click the trash bin icon in **Actions**.
3. Confirm deletion if prompted.
{% endstep %}
{% endstepper %}

### Notes

* **Insurance area** values are company-defined. They can differ by brand.
* **Extended Europe** usually means “Europe + extra covered countries”. The exact list depends on your insurance setup.
* **World** typically means destinations outside your European insurance areas.

**What is "Extended Europe"?**

It typically includes:

* All **EU and EEA countries**
* **Non-EU European countries** like:
  * **Switzerland**
  * **Norway**, **Iceland**, and **Liechtenstein** (members of EEA, but not EU)
  * Often **UK** (post-Brexit, sometimes treated separately)
  * **Western Balkan countries** (e.g., Serbia, Montenegro, Bosnia and Herzegovina)
  * **Turkey** and **some parts of Eastern Europe** (e.g., Ukraine, Moldova, depending on the insurer)
  * Sometimes **Caucasus countries** like **Georgia**, **Armenia**, and **Azerbaijan**

So "Extended Europe" is a **marketing or practical term** used by insurers to indicate you're covered in **more countries than just the EU**.

**When would "Extended Europe" be relevant?**

* If you're traveling or driving beyond Scandinavia into **non-EU Eastern Europe** or **Turkey**
* If you want broader coverage that includes **less typical destinations** within Europe.

1. "World" signifies destinations outside of the European insurance coverage.
2. Some locations are categorized differently based on insurance policies.

This interface is designed to streamline airport gateway management efficiently and intuitively.

### FAQ

<details>

<summary><strong>What’s the difference between “Plaintext” and “Plaintext (Not Flight)”?</strong></summary>

Use **Plaintext** as the standard display name. Use **Plaintext (Not Flight)** when the system needs a name outside flight contexts.

</details>

<details>

<summary><strong>What is the “Insurance area” used for?</strong></summary>

It groups gateways for insurance-related logic and reporting. The available values come from your configuration.

</details>

<details>

<summary><strong>Can I reuse the same IATA code for multiple gateways?</strong></summary>

Arrival gateways are typically unique per IATA code. If you need multiple names, prefer adjusting the display fields instead.

</details>

<details>

<summary><strong>What happens if I delete an arrival gateway?</strong></summary>

The gateway is removed from the list. Anything referencing it may fail or need remapping. If you are unsure, validate dependencies first.

</details>

<details>

<summary><strong>Do you support placeholder IATA codes (for example, <code>ZZZ</code>)?</strong></summary>

Some setups use placeholder codes for non-standard airports or manual handling. If you use placeholders, keep the naming consistent across arrival and departure gateways.

</details>
