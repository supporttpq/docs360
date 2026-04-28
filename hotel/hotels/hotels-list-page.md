---
description: >-
  Search, filter, and manage hotel records in Tourpaq Office. Review every field
  on the Hotels list page and see how each field affects booking, contracts,
  web, reporting, and supplier workflows.
---

# Hotels list page

The **Hotels** list page is the entry point for hotel master data in Tourpaq Office. It is used to find hotel records, create new hotels, and open existing hotels for setup work that continues in [Hotel creation](../hotel-creation/), [Hotel Contracts](../../hotel-contracts/), [Facilities](../../facilities.md), and [Hotel reporting](../hotel-creation/communication/hotel-reporting.md).

### Navigation

**Menu path**

Open **Hotel** → **Hotels**.

**Related entry points**

* **Global search** can be used to jump to a hotel, then continue in **Edit** from this list. See [Global search](../../setup/global-search.md).
* Hotel records shown here are the same entities used in booking workflows. See [Booking overview](../../booking/booking-overview.md).

### Requirements

* Access to the **Hotel** module.
* Administrator permissions for **Create using wizard**, **Create**, **Edit**, and **Delete**.
* Existing setup data for **Destination**, **Resort**, and usually **Supplier** before new hotel creation starts.

### Interface overview

The page is split into three areas:

* **Filters** at the top for narrowing the hotel set.
* A **result table** showing core hotel master data as columns.
* **Actions** for creating, editing, or deleting a hotel record.

The result table is the fastest way to validate that the correct hotel is selected before continuing with contract setup, room setup, web content, or supplier work.

### Overview

This page supports three core tasks:

1. Find hotel records with filters.
2. Review hotel master data in the result list.
3. Open or create hotel records for further setup.

Hotel records created from this page are used in booking flows, hotel contracts, web content, allotments, reporting, supplier communication, and API output.

### Purpose

The page keeps hotel master data searchable and consistent.

Accurate data here affects:

* hotel selection in booking flows
* contract and allotment setup
* supplier communication and invoicing
* website and API hotel display
* operational and financial reporting

### Configuration steps

{% stepper %}
{% step %}
#### Find the correct hotel record

Set filters such as **Hotel**, **Destination**, and **Resort**.

Validate the match using **Code**, **Name**, **Resort**, and **Supplier** in the result table.
{% endstep %}

{% step %}
#### Create a new hotel record (when required)

Select **Create using wizard** for guided setup.

Select **Create** for manual setup.

Continue with room types, brand assignment, and web configuration in [Hotel creation](../hotel-creation/).
{% endstep %}

{% step %}
#### Continue with downstream hotel setup

Maintain contracts and commercial setup in [Hotel Contracts](../../hotel-contracts/).

Maintain facilities and related display metadata in [Facilities](../../facilities.md).

Validate operational output in [Hotel reporting](../hotel-creation/communication/hotel-reporting.md).
{% endstep %}
{% endstepper %}

### Daily workflow (common)

{% stepper %}
{% step %}
#### Filter the list

Use **Hotel**, **Destination**, **Resort**, **Display only Bed Banks**, and **Show hidden** to narrow the result set.
{% endstep %}

{% step %}
#### Review the matching hotels

Check the table columns to confirm the correct hotel, resort, supplier, and integration type.
{% endstep %}

{% step %}
#### Continue with the next task

Use **Create using wizard** or **Create** for new setup.

Use **Edit** for maintenance.

Use **Delete** only when the hotel must be removed permanently.
{% endstep %}
{% endstepper %}

<figure><img src="../../.gitbook/assets/image (402).png" alt="Hotels list page showing filters, table, and actions"><figcaption><p>Hotels list page with filters, result columns, and actions.</p></figcaption></figure>

### System behavior

**Filtering**

* Filters narrow the result list only.
* **Clear** removes active filters and refreshes the list.
* **Display only Bed Banks** limits the view to bed bank-linked hotels. These hotels typically relate to provider and import setup in [System Setup – Hotel Providers](../../setup/system-setup/system-setup-hotel-providers/) and [System Setup – Hotel Import](../../setup/system-setup/system-setup-hotel-import.md).

**Hidden hotels**

* **Show hidden** includes hotels that are excluded from normal selection.
* Hidden hotels can still exist in historical bookings and operational reporting. See [All bookings](../../booking/all-bookings/).

**Create/Edit/Delete**

* **Create using wizard** and **Create** produce the same hotel entity. Differences are the data entry flow and required completeness at the first save.
* **Edit** opens the hotel record where changes can affect booking selection, contract logic, web display, exports, and reporting.
* **Delete** removes the hotel master record. Deletion can break references in contracts, integrations, and reporting. Hiding the hotel is often safer when the hotel must stop appearing operationally.

### Fields on the Hotels list page

#### Filters

**Hotel**

Filters the list by hotel record.

Use this field to find a specific hotel before editing master data, contracts, room setup, or web content. The hotel selected here is the same hotel entity used later in [Hotel creation](../hotel-creation/), [Hotel Contracts](../../hotel-contracts/), and booking flows.

**Destination**

Filters hotels by destination.

This filter is useful when several resorts belong to the same destination. It relates to destination structure used throughout Tourpaq, including setup data in [Destination](../../setup/destination.md) and resort assignment maintained in [Hotel creation](../hotel-creation/).

**Resort**

Filters hotels by resort.

This filter is commonly used before contract work, allotment work, and resort-level hotel maintenance. The selected resort is part of the hotel master data and affects booking selection, grouping, and reporting. Resort setup is maintained in [Resorts](../../setup/resorts.md).

**Display only Bed Banks**

Shows only hotels that come from, or are linked to, a bed bank source.

Use this checkbox when checking imported or integrated accommodation content. It relates directly to provider/import setup in [System Setup – Hotel Providers](../../setup/system-setup/system-setup-hotel-providers/) and [System Setup – Hotel Import](../../setup/system-setup/system-setup-hotel-import.md), and to the **Bed Bank** indication in the result list.

**Show hidden**

Includes hotels that are hidden from normal selection.

This filter relates to the hotel **Status** maintained in [Hotel creation](../hotel-creation/). Hidden hotels are usually excluded from daily selection flows, but still matter for history, reporting, and controlled maintenance.

**Clear**

Removes the active filters.

Use it before starting a new search or when switching from one hotel maintenance task to another.

#### Table columns

**Code**

Shows the hotel code.

This value is a core identifier in Tourpaq. It is used for internal reference, hotel maintenance, integrations, reporting, exports, and API-based hotel output. For new hotels, the code is created during [Hotel creation](../hotel-creation/) or [Create using the wizard](../hotel-creation/create-using-the-wizard.md).

**Name**

Shows the hotel name.

The name identifies the property across Office workflows and can also affect how the hotel appears in downstream channels, depending on setup. It is one of the key fields checked before contracts, web, room, or supplier work continues.

**Resort**

Shows the resort linked to the hotel.

This field connects the hotel to destination structure in Tourpaq. It affects search, reporting, and how hotels are organized for booking and operational work.

**Supplier**

Shows the supplier connected to the hotel.

This field is important for supplier communication, hotel reporting, invoicing, and integration-based hotel handling. It becomes especially relevant when the hotel is part of supplier workflows such as confirmations and reporting. Supplier master data is maintained under [Suppliers](../../suppliers/), including [Hotel Supplier](../../suppliers/hotel-supplier.md).

**Address**

Shows the hotel address.

This field supports operational identification of the property and helps staff confirm that the correct hotel record is being maintained. It can also support downstream communication and document accuracy.

**City**

Shows the hotel city.

This field supports operational clarity and makes it easier to distinguish similar hotel names across destinations and resorts. It also improves list review and reporting context.

**Country**

Shows the hotel country.

This field supports geographic identification and reporting context. It is especially useful when similar destinations or resorts exist across markets.

**Phone**

Shows the hotel phone number.

This field supports operational contact with the property. It is relevant in service handling, supplier follow-up, and manual hotel communication scenarios.

**Fax**

Shows the hotel fax number.

This field is optional in practice, but still documented because it is part of the hotel record. If used, it supports legacy supplier communication flows.

**Order No.**

Shows the internal order number for the hotel.

This field relates to hotel sorting and downstream output. In hotel setup, **Order No.** is used for controlling the order in website lists or other consumers that read hotel master data.

**Bed Bank**

Indicates whether the hotel is linked to a bed bank.

This column helps distinguish directly maintained hotels from integration-based hotel records. It relates to supplier source, contract model, and troubleshooting of imported hotel content.

#### Actions

**Create using wizard**

Opens the guided hotel creation flow.

This action is not mandatory, but it is the fastest option for a new hotel. It relates directly to [Create using the wizard](../hotel-creation/create-using-the-wizard.md), where minimum required hotel data is entered before the hotel record is saved.

**Create**

Opens the standard hotel setup form.

This action is not mandatory, but it is used when full manual control is needed from the start. It leads into [Hotel creation](../hotel-creation/), where required fields, room types, brands, allotments, and other hotel settings are maintained.

**Edit**

Opens the selected hotel for maintenance.

This action relates to nearly all hotel functionality in Tourpaq, including room types, allotments, facilities, web content, communication, deposits, and contracts. Use this action when the hotel already exists and the setup must be reviewed or changed.

**Delete**

Permanently removes the hotel record.

This action is not mandatory and should be used with caution. Deleting a hotel can affect reporting, historical references, integrations, and downstream hotel setup. If the hotel should stop appearing in normal work, hiding the hotel is usually safer than deletion.

{% hint style="warning" %}
**Delete** is destructive.

If the hotel has historical importance, related setup, or reporting value, hiding the hotel is usually the safer option.
{% endhint %}

### Examples

**Example: Find an imported bed bank hotel for troubleshooting**

1. Enable **Display only Bed Banks**.
2. Narrow the list with **Destination** and **Resort**.
3. Validate **Bed Bank** and **Supplier** in the result table.
4. Open with **Edit** and continue with provider/import investigation in [System Setup – Hotel Providers](../../setup/system-setup/system-setup-hotel-providers/) or [System Setup – Hotel Import](../../setup/system-setup/system-setup-hotel-import.md).

**Example: Locate a hidden hotel for controlled maintenance**

1. Enable **Show hidden**.
2. Filter by **Hotel** or **Resort**.
3. Open with **Edit** and verify whether the hotel should remain hidden due to historical bookings. Reporting validation can be done in [All bookings](../../booking/all-bookings/) and [Hotel reporting](../hotel-creation/communication/hotel-reporting.md).

### Related pages

* [Hotel creation](../hotel-creation/)
* [Create using the wizard](../hotel-creation/create-using-the-wizard.md)
* [Facilities](../../facilities.md)
* [Hotel Contracts](../../hotel-contracts/)
* [Hotel reporting](../hotel-creation/communication/hotel-reporting.md)
* [Destination](../../setup/destination.md)
* [Resorts](../../setup/resorts.md)
* [Suppliers](../../suppliers/)
* [System Setup – Hotel Providers](../../setup/system-setup/system-setup-hotel-providers/)
* [System Setup – Hotel Import](../../setup/system-setup/system-setup-hotel-import.md)
