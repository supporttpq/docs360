# Hotels

### Overview

The **Hotels** page allows administrators to manage the list of hotels available in the system. Each hotel entry can be linked to a resort, supplier, and other identifying details. These records form the foundation for building hotel contracts, assigning bookings, and integrating with suppliers or bed banks.

{% hint style="info" %}
This feature is intended for **administrator** users.
{% endhint %}

### Common tasks

This module ensures all hotel-related information is standardized and available for booking management, reporting, and integrations with external suppliers (e.g., bed banks, Tourpaq Supplier).

### Purpose

{% stepper %}
{% step %}
### Find a hotel

Use **Hotel**, **Destination**, and **Resort** filters.

Enable **Show hidden** to include hotels not available for selection.
{% endstep %}

{% step %}
### Create a hotel

Use **Create using wizard** for the fastest setup.

Use **Create** if you want a blank hotel record first.

Next: [Hotel creation](hotel-creation/) or [Create using wizard](hotel-creation/create-using-the-wizard.md).
{% endstep %}

{% step %}
### Maintain an existing hotel

Use **Edit** to update master data.

Use **Hide** (via the hotel status) to stop it showing in selection lists.
{% endstep %}
{% endstepper %}

### Page Structure

<figure><img src="../.gitbook/assets/image (402).png" alt="Hotels list page showing filters, table, and actions"><figcaption><p>Hotels list: filters, results table, and actions.</p></figcaption></figure>

#### Filters

At the top of the page, filters help narrow down the list of hotels:

* **Hotel** – Search or filter by hotel name.
* **Destination** – Filter hotels by destination.
* **Resort** – Filter hotels by resort.
* **Display only Bed Banks** – When selected, only hotels provided by bed banks are shown.
* **Show hidden** – Includes hotels marked as hidden (not selectable in most flows).
* **Clear** – Resets all applied filters.

#### Table Columns

* **Code** – The unique code for the hotel.
* **Name** – The full name of the hotel.
* **Resort** – The resort where the hotel is located.
* **Supplier** – The supplier providing this hotel (e.g., _Oliv_, _Tourpaq Supplier_).
* **Address** – The hotel’s address.
* **City** – City where the hotel is located.
* **Country** – Country where the hotel is located.
* **Phone** – The hotel’s contact phone number.
* **Fax** – The hotel’s fax number (optional).
* **Order No.** – Internal ordering or sorting number.
* **Bed Bank** – Indicates the hotel originates from, or is linked to, a bed bank integration.

#### Actions

* **Create using wizard** – Creates a hotel with the minimum required data in one flow. See [Create using wizard](hotel-creation/create-using-the-wizard.md).
* **Create** – Opens a blank hotel form. See [Hotel creation](hotel-creation/).
* **Edit (pencil icon)** – Updates hotel details (supplier, status, fields used in booking and web).
* **Delete (trash icon)** – Permanently removes the hotel.

{% hint style="warning" %}
Delete is destructive. It can break reporting, contracts, and historical references.

If the hotel should stop being used, **hide it** instead.
{% endhint %}

### Related pages

* [Hotel creation](hotel-creation/)
* [Create using wizard](hotel-creation/create-using-the-wizard.md)
* [Facilities](../facilities.md)
* [Hotel Contracts](../hotel-contracts/)
