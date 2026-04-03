---
description: >-
  Generate Tourpaq Office price lists with manual or scheduled rules by resort,
  hotel, transport, departure dates, and fix quotas.
---

# Price List Generator

## Overview

Use **Price List Generator** (Generate Price List service) to create **Tourpaq Office price lists** in bulk.

It creates price list entries based on **resort** or **transport** rules.

Use it when you set up new seasons, extend allotments, or add new hotel/transport combinations.

{% hint style="warning" %}
This feature creates **price lists** (entries/structures).

It does **not** calculate or create the selling prices inside the price list (P1–P4, D1–D4, etc.).
{% endhint %}

## What it’s used for

Use Price List Generator to:

* Generate missing price lists for a destination, resort, hotel, or transport.
* Create **scheduled rules** that run automatically when hotel allotment is generated or extended.
* Reduce manual work when you need many price lists created consistently.
* Keep coverage across departure periods, resorts, and transports.

### Prerequisites

You need:

* Access rights to the price list / setup modules.
* Hotel and transport setup in place (including allotments and fix quotas).

## Filters

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)   (4).png" alt="Price List Generator filters and results list"><figcaption><p>Filter and display existing or scheduled price list generation rules.</p></figcaption></figure>

Use the filters to find existing rules and validate what the generator will create.

* **Departure from**: Departure start date.
* **Departure to**: Departure end date.
* **Arrivals**: Filter by arrival point.
* **Resorts**: Filter by one or more resorts.
* **Transports**: Filter by transport (optional).
* **Display**: Show matching rules in the list.
* **Clear**: Reset filters and show all rules.

## Result columns

Each row is a **price list generation rule**.

* **Agency**: The agency/brand context for the rule. Example: `Tourpaq DK`.
* **Arrival**: Arrival destination. Required.
* **Resort**: Resort for which the price lists are generated.
* **Hotel**: Hotel included in the rule (optional, depending on your setup).
* **Departure From / To**: Departure date range covered by the rule.
* **Transport**: Transport code/identifier (optional).
* **Fix Quotas**:
  * Validity period used when generating price lists for a transport.
  * Required if **Transport** is selected.
* **Actions**:
  * **Edit**: Open the rule for editing.
  * **Delete**: Delete the rule.
  * **History**: View changes made to the rule.

## Actions and buttons

* **Create**: Add a new price list generation rule.
* **Scheduled Rules to Generate Price List**: View the list of scheduled rules.

## Scheduled rules (red rows)

Rows with a **red background** are **scheduled rules**.

They are queued and will run when **hotel allotment is generated or extended**.

The row stays red until the service has processed it.

## Create a generation rule

1. Click **Create**.
2. Fill in the required fields:
   * **Agency**
   * **Arrival**
   * **Resort**
   * **Departure from** / **Departure to**
3. Optional: Select **Transport** (and hotel, if relevant in your setup).
4. Click **Save**.
5. If you selected **Transport**, open **Fix Quota** and select the correct fix quota interval.
6. Click **Save** again to queue the rule.

## Edit a rule

1. Use filters to find the rule.
2. Click **Edit** on the row.
3. Update fields and fix quota interval as needed.
4. Click **Save**.
5. If the row turns red, it is queued and waiting for the service.

## Verify the generator ran

1. Set the same filters (arrival/resort/transport/departure range).
2. Click **Display**.
3. Confirm the expected rules and date ranges exist.
4. Confirm queued rules are no longer red after the service run.

## Key benefits

* Automatic generation of many price lists across date ranges and destinations.
* Less manual work for administrators and pricing managers.
* Better consistency across resorts, hotels, and transports.
* Faster seasonal rollouts when allotments change.

## Best practices

* Review scheduled rules regularly.
* Avoid overlapping departure date ranges.
* Align rule intervals with the correct **fix quota** periods.
* Keep transport and resort naming consistent for easier searching.

## FAQ

### What does Price List Generator create?

It creates **price lists** (entries/structures).

It does **not** create selling prices inside the price list.

### What do I need to fill in to create a generation rule?

At minimum:

* **Agency**
* **Arrival**
* **Resort**
* **Departure from** / **Departure to**

If you select a **Transport**, you must also select **Fix Quotas**.

### What is a fix quota, and why is it required?

A fix quota defines the **validity period** used when generating price lists for a transport.

Your rule interval must be within the parent fix quota interval.

### Why is a row highlighted in red?

Red rows are **scheduled rules**.

They are queued and waiting for the generator service to run.

### When will a scheduled rule run?

Rules are typically queued when **hotel allotment is generated or extended**.

The row stays red until the service has processed it.

### How do I verify the generator worked?

1. Set the same filters (arrival/resort/transport/date range).
2. Click **Display**.
3. Confirm the expected records exist.

### Does generating a price list overwrite existing prices?

The generator creates the **price list entries** for the selected combinations.

Avoid overlapping date ranges to reduce unexpected results.

### I saved a rule, but nothing happens. What should I check?

* The rule is still red (queued) and the service has not run yet.
* The date range is valid and does not overlap existing rules.
* The Fix Quota interval contains your rule interval.
* Required hotel/transport setup and allotments exist.

## Related pages

* [Price List](price-list/pricelist.md)
* [Price List Setup](price-list/pricelist-setup.md)
* [Profit margin rules](profit-margin-rules.md)
* [Price regulation rules](price-regulation-rules.md)
