# Extras - General page

The **Extras** page is where you manage supplementary services or items that can be attached to bookings — things like meal plans, transfers, or special dinner packages. Each extra has a unique code, a display name, and belongs to a category.

### Overview

The page contains:

* Search and filtering functionality
* Overview of configured Extras
* Access to create, edit, and delete Extras

The list displays:

* Extra code
* Name
* Category
* Pickup/Dropoff information
* One-way behavior

***

### Purpose

The purpose of the page is to:

* Configure optional products and services
* Manage pricing add-ons
* Connect extras to operational workflows
* Control customer-visible and internal services

***

### Requirements

| Requirement         | Description                                                   |
| ------------------- | ------------------------------------------------------------- |
| User permissions    | Access to Extras setup                                        |
| Existing categories | Extras Categories should be configured before creating Extras |
| Related contracts   | Some Extras require Hotel or Transport setup                  |

***

### Navigation

```
Extras Setup → Extras
```

***

## 📸 Screenshot – Extras Overview

<figure><img src="../../.gitbook/assets/extras main.png" alt=""><figcaption></figcaption></figure>

***

## Interface Overview

The page is divided into:

1. Filter section
2. Extras list overview
3. Create functionality

***

## 📸 Screenshot – Extras Filters

<figure><img src="../../.gitbook/assets/extras filters.png" alt=""><figcaption></figcaption></figure>

***

## Field Description – Filters

| Field Name       | Description                                                                                                            |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Code/Name        | Searches by Extra code or name                                                                                         |
| Extra Categories | Dropdown to filter by category (e.g. _Pension_, _Gala dinner_). Select a category to show only extras belonging to it. |
| Show hidden      | Checkbox that, when enabled, includes extras that have been marked as hidden. By default, hidden extras are not shown. |
| Clear            | Resets all active filters. The badge next to the button shows how many filters are currently applied.                  |
| Create           | Opens creation page for new Extra                                                                                      |

***

## 📸 Screenshot – Extras List

<figure><img src="../../.gitbook/assets/extras list.png" alt=""><figcaption></figcaption></figure>

***

## Field Description – List Columns

| Field Name    | Description                                                                                                                                           |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| CODE          | A unique identifier for the extra (e.g. `B_ALX_AI_new`). Used internally for mapping and integrations. Clicking the code opens the extra for editing. |
| NAME          | Name of the Extra (e.g. _Board ALX AI_). This is what typically appears in booking interfaces and reports.                                            |
| CATEGORY      | The category this extra belongs to (e.g. _Pension_, _Gala dinner_). Categories help group and filter extras.                                          |
| PICKUP POINT  | For transfer-type extras, the location where the traveller is picked up. May be empty for non-transfer extras.                                        |
| DROPOFF POINT | For transfer-type extras, the destination where the traveller is dropped off. May be empty for non-transfer extras.                                   |
| ONE-WAY       | Indicates if Extra is valid for one-way bookings only                                                                                                 |
| Delete icon   | Deletes the Extra                                                                                                                                     |

***

## Configuration Steps

### Create a New Extra

1. Open **Extras**
2. Click **Create**
3. Configure:
   * Code
   * Name
   * Category
   * Pricing
   * Visibility settings
4. Save the configuration

***

### Search for Existing Extras

1. Enter search criteria:
   * Code/Name
   * Category
2. Click outside the field or apply filter
3. Review matching results

***

### Delete an Extra

1. Locate the Extra in the list
2. Click the delete icon
3. Confirm deletion

***

### Pagination

The table is paginated. Use the page number controls at the bottom to navigate, or change the number of rows displayed per page using the items-per-page dropdown (default: 25).

{% hint style="info" %}
Codes are case-sensitive and must be unique across all extras. Agree on a naming convention with your team before creating new ones. Users & rolesLocations&#x20;
{% endhint %}

***

## Examples

### Example 1 – Gala Dinner

| Configuration | Value                  |
| ------------- | ---------------------- |
| Category      | Gala dinner            |
| Visibility    | Hidden on ticket       |
| Pricing       | Included in base price |

Result:\
The customer pays for the dinner, but it is not displayed separately on the e-ticket.

***

### Example 2 – Board Supplement

| Configuration | Value           |
| ------------- | --------------- |
| Category      | Pension         |
| Board Basis   | HB – Half Board |

Result:\
The Extra supplements the hotel board basis pricing.

***

### Example 3 – Transfer Extra

| Configuration | Value   |
| ------------- | ------- |
| Pickup Point  | Airport |
| Dropoff Point | Hotel   |
| One-way       | Enabled |

Result:\
The Extra becomes available only for one-way transport bookings.

***

## Related Pages

* Extras Categories
* Hotel Contracts
* Booking Engine
* Passenger Extras
* E-ticket Setup
* Product Pricing
* Transfers
