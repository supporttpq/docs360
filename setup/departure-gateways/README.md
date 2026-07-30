# Departure Gateways

### Overview

The **Departure Gateways** page lists departure airports and gateways used in Tourpaq.

Use it to maintain clean master data for transports, bookings, and reporting.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (20) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

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

### Related pages

* [Arrival Gateways](../arrival-gateways/)
