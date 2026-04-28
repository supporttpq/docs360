---
description: >-
  Search and manage hotel records in Tourpaq Office for booking, contract, web,
  and supplier setup.
---

# Hotels

The **Hotels** page is the entry point for hotel master data in Tourpaq Office. It supports searching and validating hotel records before continuing setup in [Hotel creation](../hotel-creation/) and commercial configuration in [Hotel Contracts](../../hotel-contracts/). The same hotel records are used in booking flows and operational reporting, including [Booking overview](../../booking/booking-overview.md) and [All bookings](../../booking/all-bookings/).

### Navigation

Open **Hotel** → **Hotels**.

### Requirements

* Access to the **Hotel** module.
* Permissions to view hotel master data.
* Administrator permissions for **Create using wizard**, **Create**, **Edit**, and **Delete**.
* Setup data for **Destination** and **Resort** before new hotel creation. See [Destination](../../setup/destination.md) and [Resorts](../../setup/resorts.md).

{% hint style="info" %}
This page is typically used by administrator roles.
{% endhint %}

### Overview

The page supports three tasks:

1. Filter and locate a hotel record.
2. Validate key master data from the result table.
3. Open or create a hotel for further setup work.

### Purpose

Hotel master data is a dependency for:

* hotel selection in booking flows
* hotel allotment and release workflows
* supplier communication and supplier reporting
* web content and API output for accommodation
* finance flows that rely on supplier relations and contract data

### Interface overview

The screen contains:

* **Filters** for narrowing the hotel list.
* A **result table** with core hotel master fields.
* **Actions** for creating, editing, and deleting hotel records.

<figure><img src="../../.gitbook/assets/image (402).png" alt="Hotels list page showing filters, table, and actions"><figcaption><p>Hotels list: filters, results table, and actions.</p></figcaption></figure>

### Field descriptions

#### Filters

**Hotel**

Filters the list by a hotel record.

This field is not mandatory.

This filter is used to locate a specific hotel before continuing maintenance in [Hotel creation](../hotel-creation/) or reviewing commercial setup in [Hotel Contracts](../../hotel-contracts/).

**Destination**

Filters hotels by destination.

This field is not mandatory.

This filter relates to the destination structure used across Tourpaq. Destination setup is maintained in [Destination](../../setup/destination.md).

**Resort**

Filters hotels by resort.

This field is not mandatory.

This filter relates to the resort structure used in hotel grouping, booking selection, and reporting. Resort setup is maintained in [Resorts](../../setup/resorts.md).

**Display only Bed Banks**

Shows only hotels linked to a bed bank/provider source.

This field is not mandatory.

This filter is used for validating imported hotels and for troubleshooting provider-linked content. Provider/import setup is maintained in [System Setup – Hotel Providers](../../setup/system-setup/system-setup-hotel-providers/) and [System Setup – Hotel Import](../../setup/system-setup/system-setup-hotel-import.md).

**Show hidden**

Includes hotels hidden from normal selection.

This field is not mandatory.

This filter relates to the hotel status maintained on the hotel record in [Hotel creation](../hotel-creation/). Hidden hotels can still exist in historical bookings and remain visible in reporting depending on filters. See [All bookings](../../booking/all-bookings/).

**Clear**

Resets active filters.

This control is not mandatory.

This control affects only the list view. It does not change hotel master data.

#### Table columns

All columns are read-only on this page. Changes are made via **Edit**.

**Code**

Shows the hotel code.

This field is not mandatory on the list page.

This value is a core identifier for internal reference, exports, reporting, and integrations. The value is set during hotel creation in [Hotel creation](../hotel-creation/) or [Create using wizard](../hotel-creation/create-using-the-wizard.md).

**Name**

Shows the hotel name.

This field is not mandatory on the list page.

This value is used for operational identification and can affect downstream display depending on web configuration. Web-related setup is maintained in the hotel record under [Hotel creation](../hotel-creation/).

**Resort**

Shows the resort linked to the hotel.

This field is not mandatory on the list page.

This value controls grouping and search behavior in several workflows. It also impacts reporting slices by resort. Resort setup is maintained in [Resorts](../../setup/resorts.md).

**Supplier**

Shows the supplier linked to the hotel.

This field is not mandatory on the list page.

This value is used in supplier communication and supplier reporting. Supplier master data is maintained under [Suppliers](../../suppliers/).

**Address**

Shows the hotel address.

This field is not mandatory on the list page.

This value supports operational identification and can feed downstream documents and exports depending on setup.

**City**

Shows the hotel city.

This field is not mandatory on the list page.

This value helps distinguish hotels with similar names and improves reporting context.

**Country**

Shows the hotel country.

This field is not mandatory on the list page.

This value supports geographic segmentation and improves reporting context.

**Phone**

Shows the hotel phone number.

This field is not mandatory on the list page.

This value supports operational contact and follow-up when supplier communication is handled manually.

**Fax**

Shows the hotel fax number.

This field is not mandatory on the list page.

This value supports legacy communication flows where fax is still used.

**Order No.**

Shows the internal sort order number.

This field is not mandatory on the list page.

This value is typically used for controlling ordering in downstream lists, such as web lists or other consumers of hotel master data.

**Bed Bank**

Indicates whether the hotel is linked to a bed bank/provider.

This field is not mandatory on the list page.

This value supports troubleshooting of provider-sourced hotels and clarifies which hotels are managed directly versus imported. Related configuration exists in [System Setup – Hotel Providers](../../setup/system-setup/system-setup-hotel-providers/) and [System Setup – Hotel Import](../../setup/system-setup/system-setup-hotel-import.md).

#### Actions

**Create using wizard**

Starts the guided hotel creation flow.

This action is not mandatory.

This action is used to create a hotel with minimum required data first. The wizard is documented in [Create using wizard](../hotel-creation/create-using-the-wizard.md).

**Create**

Opens a blank hotel form.

This action is not mandatory.

This action is used when manual setup is required from the first step. Hotel fields are documented in [Hotel creation](../hotel-creation/).

**Edit**

Opens the selected hotel for maintenance.

This action is not mandatory.

Changes made via **Edit** can affect booking selection, contract logic, web display, exports, and reporting. Common next pages include [Hotel creation](../hotel-creation/) and [Hotel Contracts](../../hotel-contracts/).

**Delete**

Permanently removes the hotel record.

This action is not mandatory.

Deletion can break references in reporting, contracts, and integrations. Hiding the hotel via status is typically safer than deletion.

{% hint style="warning" %}
**Delete** is destructive.

Deletion can impact reporting and historical references.
{% endhint %}

### Configuration steps

{% stepper %}
{% step %}
#### Find and validate a hotel

Set **Hotel**, **Destination**, and **Resort** filters.

Validate the correct record via **Code**, **Name**, **Resort**, and **Supplier**.
{% endstep %}

{% step %}
#### Create a hotel record

Select **Create using wizard** or **Create**.

Continue setup in [Hotel creation](../hotel-creation/).
{% endstep %}

{% step %}
#### Continue downstream setup

Configure commercial logic in [Hotel Contracts](../../hotel-contracts/).

Configure metadata used for display and filtering in [Facilities](../../facilities.md).
{% endstep %}
{% endstepper %}

### System behavior

**Filters**

* Filters affect only the list view.
* **Clear** resets filters and refreshes results.
* **Display only Bed Banks** is a fast way to isolate imported/provider hotels.

**Hidden hotels**

* Hidden hotels are excluded from most selection flows.
* Hidden hotels can still appear in historical contexts and reporting, depending on filters and report logic. See [All bookings](../../booking/all-bookings/).

**Deletion**

* **Delete** removes the master record.
* Contract, reporting, and integration dependencies can be impacted.

### Examples

**Example: Troubleshoot a bed bank hotel**

1. Enable **Display only Bed Banks**.
2. Filter with **Destination** and **Resort**.
3. Validate **Bed Bank** and **Supplier** in the list.
4. Continue provider/import checks in [System Setup – Hotel Providers](../../setup/system-setup/system-setup-hotel-providers/) and [System Setup – Hotel Import](../../setup/system-setup/system-setup-hotel-import.md).

**Example: Locate a hidden hotel for maintenance**

1. Enable **Show hidden**.
2. Filter with **Hotel** or **Resort**.
3. Open with **Edit** and validate status and dependencies in [Hotel creation](../hotel-creation/).

### Related pages

* [Hotels list page](hotels-list-page.md)
* [Hotel creation](../hotel-creation/)
* [Create using wizard](../hotel-creation/create-using-the-wizard.md)
* [Facilities](../../facilities.md)
* [Hotel Contracts](../../hotel-contracts/)
* [Hotel reporting](../hotel-creation/communication/hotel-reporting.md)
* [Destination](../../setup/destination.md)
* [Resorts](../../setup/resorts.md)
* [Suppliers](../../suppliers/)
* [System Setup – Hotel Providers](../../setup/system-setup/system-setup-hotel-providers/)
* [System Setup – Hotel Import](../../setup/system-setup/system-setup-hotel-import.md)
* [Booking overview](../../booking/booking-overview.md)
* [All bookings](../../booking/all-bookings/)
