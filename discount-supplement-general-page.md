# Discount/Supplement General Page

## Discounts/Supplements

### Introduction

The **Discounts/Supplements** page is used to manage pricing adjustments applied to bookings, products, transports, hotels, and other services in Tourpaq. The functionality supports both discounts and supplements and is an important part of pricing configuration and campaign management.

***

### Overview

The page contains:

* Search and filtering tools
* A list overview of configured discounts/supplements
* Access to create, edit, and delete pricing rules

The list view provides a quick overview of:

* Discount/supplement type
* Pricing behavior
* Scope
* Applicability

***

### Purpose

The purpose of this page is to:

* Configure pricing adjustments
* Create campaigns and promotions
* Manage manual and automatic supplements
* Control pricing logic across products and services

***

### Requirements

| Requirement       | Description                                                                 |
| ----------------- | --------------------------------------------------------------------------- |
| User permissions  | Access to Discounts/Supplements configuration                               |
| Pricing setup     | Products, hotels, transports, or services should already exist              |
| Related contracts | Discounts/supplements often depend on existing hotel or transport contracts |

***

### Navigation

```
Setup → Discounts/Supplements
```

***

## 📸 Screenshot – Discounts/Supplements Overview

<figure><img src=".gitbook/assets/Disc overvier.png" alt=""><figcaption></figcaption></figure>

***

## Interface Overview

The page is divided into two main areas:

1. Filter and search section
2. Discounts/Supplements list overview

***

## 📸 Screenshot – Filter Section

<figure><img src=".gitbook/assets/disc filter section.png" alt=""><figcaption></figcaption></figure>

***

## Field Description – Filters

| Field Name            | Description                                |
| --------------------- | ------------------------------------------ |
| Discounts/Supplements | Search by discount or supplement name/code |
| List name             | Filter by configured list name             |
| Bonus code            | Filter by bonus code                       |
| Show hidden           | Includes hidden discounts/supplements      |
| Display               | Applies selected filters                   |
| Clear                 | Clears all active filters                  |
| Booking period        | Filters by booking date range              |
| Duration from         | Filters by minimum stay duration           |
| Departure period      | Filters by departure date range            |
| Duration to           | Filters by maximum stay duration           |
| Price From            | Filters by minimum price value             |
| Price To              | Filters by maximum price value             |
| Category              | Filters by category (dropdown).            |
| Destination           | Filters by destination (dropdown).         |
| Transport             | Filters by transport (dropdown).           |
| Real Transport        | Filters by real transport (dropdown).      |
| Resort                | Filters by resort (dropdown).              |
| Hotel                 | Filters by hotel (dropdown).               |
| Rooms                 | Filters by room type (dropdown).           |

{% hint style="info" %}
**Tip:** Click + **More filters** to expand the full filter panel if some filters are collapsed.
{% endhint %}

***

## 📸 Screenshot – Discounts/Supplements List

<figure><img src=".gitbook/assets/disc list.png" alt=""><figcaption></figcaption></figure>

***

## Field Description – List Columns

Each row in the list represents one discount or supplement record.

<table><thead><tr><th width="222.75">Field Name</th><th width="254.5">Description</th><th>Notes / System Impact</th></tr></thead><tbody><tr><td>CODE</td><td>Unique identifier for the discount/supplement</td><td>Codes are system-wide references used in booking rules and exports. Click the code to open the record for editing.</td></tr><tr><td>NAME</td><td>Display name of the discount/supplement</td><td>This name is displayed in internal tools and reports.</td></tr><tr><td>DISCOUNT/SUPPLEMENT</td><td>Defines if entry is a discount or supplement</td><td>Indicates whether the record <strong>reduces</strong> the price (<em>Discount</em>) or <strong>adds</strong> to it (<em>Supplement</em>).</td></tr><tr><td>GENERAL/SPECIFICATE</td><td>Defines scope of applicability</td><td><p></p><p>Controls how broadly the record is applied:</p><ul><li><strong>General</strong> — applies across all applicable bookings without further filtering.</li><li><strong>Specificate</strong> — applies only to bookings that match specific criteria defined in the record (e.g. a particular hotel, room type, or departure period).</li></ul></td></tr><tr><td>FIXED/MANUAL</td><td>Defines pricing behavior</td><td><p></p><p>Determines how the price adjustment is triggered:</p><ul><li><strong>Fixed</strong> — automatically applied when the booking matches the defined conditions.</li><li><strong>Manual</strong> — must be added to a booking deliberately by an agent.</li></ul></td></tr><tr><td>PRICE</td><td>Monetary value</td><td>Applied to booking calculations</td></tr><tr><td>FAMILY DISCOUNT</td><td>Indicates family discount support</td><td>Indicates whether this record qualifies as a <strong>family discount</strong> (icon: ✅ yes / ❌ no). Family discounts may be subject to specific eligibility rules defined in system settings.</td></tr><tr><td>GENERIC SERVICES</td><td>Indicates link to generic services</td><td>Indicates whether the record applies to <strong>generic services</strong> (icon: ✅ yes / ❌ no). Generic services are add-ons or inclusions not tied to a specific product line.</td></tr><tr><td>ONE-WAY</td><td>Indicates one-way applicability</td><td>Used for transport pricing</td></tr></tbody></table>

### Actions

| Action              | How                                                                                                |
| ------------------- | -------------------------------------------------------------------------------------------------- |
| **Edit a record**   | Click the record's **Code** link to open it.                                                       |
| **Delete a record** | Click the 🗑️ trash icon at the end of the row. Deletion is permanent — confirm before proceeding. |

***

## Configuration Steps

### Create a New Discount/Supplement

1. Open **Discounts/Supplements**
2. Click **Create**
3. Configure:
   * Name
   * Type
   * Pricing behavior
   * Applicability
4. Define booking and departure periods
5. Assign destinations/hotels/transports if required
6. Save configuration

***

### Filter Existing Discounts/Supplements

1. Enter filter criteria
2. Click **Display**
3. Review matching configurations

***

### Delete a Discount/Supplement

1. Locate the row
2. Click the delete icon
3. Confirm deletion

***

### Pagination

Results are paginated. Use the numbered controls at the bottom of the page to navigate between pages, and the **items-per-page** selector (default: 10) to adjust how many rows are shown at once.

***

## Examples

### Example 1 – Early Booking Discount

| Configuration    | Value         |
| ---------------- | ------------- |
| Type             | Discount      |
| Booking Period   | January–March |
| Departure Period | Summer season |
| Pricing          | Fixed         |

Result:\
Customers booking early receive automatic reduction.

***

### Example 2 – Fuel Supplement

| Configuration | Value            |
| ------------- | ---------------- |
| Type          | Supplement       |
| Pricing       | Manual           |
| Transport     | Selected flights |

Result:\
Additional transport fee applied manually.

***

### Example 3 – Family Discount

| Configuration   | Value        |
| --------------- | ------------ |
| FAMILY DISCOUNT | Enabled      |
| Rooms           | Family rooms |

Result:\
Special family pricing becomes available.

***

## Related Pages

* Hotel Contracts
* Product Pricing
* Special Offers
* Generic Services
* Transport Pricing
* Booking Engine Pricing Logic
