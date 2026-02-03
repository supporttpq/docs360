# Departure Gateways

### Overview

The **Departure Gateways** page lists departure airports and gateways used in Tourpaq.

Use it to maintain clean master data for transports, bookings, and reporting.

<figure><img src="../.gitbook/assets/image (20) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### What you can do

* **Search** gateways by keyword.
* **Sort** by IATA code, name, or country.
* **Create** new gateways.
* **Delete** gateways you no longer need.

### Columns

1. **IATA Code**: The three-letter airport code (for example `BLL` for Billund).
2. **Name**: The airport or location name.
3. **Country**: The country the gateway belongs to.
4. **Actions**: Delete the row.

### Common tasks

#### Searching for a Departure Gateway

1. Type a keyword in the search field.
2. Review the filtered list.

#### Creating a New Entry

1. Click on the **Create** button.
2. Fill in **IATA code**, **name**, and **country**.
3. Save.

#### Deleting an Entry

1. Locate the departure gateway to remove.
2. Click the trash icon under **Actions**.
3. Confirm if prompted.

### Notes

* Some setups use placeholder IATA codes like `ZZZ` for special cases.
* Country names can appear in local language variants (for example `Spanien`).

{% hint style="warning" %}
Deleting a gateway can affect transports or data that reference it.\
If your system blocks deletion, the gateway is likely in use.
{% endhint %}

### FAQ

<details>

<summary>What should I enter as <strong>IATA code</strong>?</summary>

Use the airport’s official three-letter IATA code.

Some companies also use `ZZZ` for non-standard locations.

</details>

<details>

<summary>Why are country names shown in different languages?</summary>

Country names come from your system’s country list.

That list can include localized spellings (for example `Spanien`).

</details>

<details>

<summary>I can’t delete a gateway. Why?</summary>

Most common reasons:

* You don’t have permission to delete master data.
* The gateway is referenced by transports, bookings, or rules.

If it is still needed for history, keep it and stop using it going forward.

</details>

<details>

<summary>Can I create a gateway for a non-airport departure?</summary>

Yes, if your workflow needs it.

Use a clear name and follow your internal convention for the code.

</details>

### Related pages

* [Arrival Gateways](arrival-gateways.md)
