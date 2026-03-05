---
description: >-
  Bulk copy Tourpaq Office price lists between brands. Apply tags, price
  adjustments, max rooms, and optional brand assignment updates. View migration
  log and search.
---

# Migrate Price List

## Overview

Only administrators can use **Migrate Pricelist**.

Use it to bulk copy **Tourpaq Office Price Lists (pricelists)** from one **brand** to another in the same company.

It copies the full price list setup, including PLTA lines (per departure), intervals (P1–P4), discounts (D1–D4), tags, and optional maximum room values.

To migrate price lists, select **Migrate Price List** from the **Price List** menu.

<figure><img src="../.gitbook/assets/image (50) (1).png" alt=""><figcaption></figcaption></figure>

## Purpose

The feature is designed to simplify and accelerate situations where:

* A new brand is added and needs the same price structure as an existing one.
* Price lists must be aligned across multiple brands.
* Seasonal or strategic changes require bulk updates rather than manual edits.

This reduces manual work and limits copy/paste errors.

## Steps to migrate price lists

1. **Access the Feature**
   * Select **Migrate Price List** from the **Price List** menu.
2. **Select source and destination brands**
   * **From Brand**: The source brand to copy price lists from.
   * **To Brand**: The destination brand to copy price lists to.
3. **Set Tag (Optional)**
   * Enable the **Set Tag** checkbox and select a tag from the dropdown.
   * The tag is applied to all migrated price list rows in the destination brand.
   * See also: [Price List Tags](../pricelist-tags.md).
4. **Adjust Prices (Optional)**
   * **Increase/Decrease Amount**: Adds/subtracts a fixed value on destination price fields. Positive increases. Negative decreases.
   * **Increase/Decrease Percentage**: Adjusts destination price fields by percentage. Positive increases. Negative decreases.
   * Only prices that already exist on the destination are adjusted.
   * **Order**: Percentage is applied first. Amount is applied second.
5. **Copy Max Rooms (Optional)**
   * Enable **Copy Max Room** to copy max room fields (M1–M4) from source to destination.
6. **Brand Assignments**
   * By default, the migration also replicates brand assignments for **transports, hotels, resorts, extras, and discounts**.
   * Enable **Copy Only Price Lists** to migrate price lists without changing brand assignments.
7. **Source Agency Filtering (Optional)**
   * Some entities (transports, resorts, destinations) can have a **Source Agency** in General Settings.
   * Enable this option to migrate only entities where **Source Agency = From Brand**.
   * Use this to avoid overwriting data when brands share the same underlying setup.
8. **Execute Migration**
   * Click **Migrate Prices** to perform the bulk copy.

<figure><img src="../.gitbook/assets/image (51) (1).png" alt=""><figcaption></figcaption></figure>

## Migration Log and Search

* All migrations are **logged** to track past actions.
* To search through migrations, click **Search Migrations** and filter by:
  * Brand
  * The user who performed the migration
  * Date of migration
* **Show Hidden:** Displays migrations older than the number of days specified in **System Setup → Hide Filters**.

## FAQ

**What does Migrate Pricelist do?**\
It copies price lists from one brand to another within the same company.

**Who can use this feature?**\
Only administrators.

**Can I adjust prices during migration?**\
Yes. You can apply an amount and/or percentage change during migration.

**Does migration change brand assignments for transports and hotels?**\
Yes, by default. Enable **Copy Only Price Lists** to avoid changing brand assignments.

**Can I apply tags to destination price lists?**\
Yes. Use **Set Tag** to apply a tag to migrated price list rows.

**What happens to “max rooms” values?**\
Enable **Copy Max Room** to copy max room values from the source price list.

**Is there a log of migrations?**\
Yes. All migrations are logged. You can search by brand, user, or date.

**Can migration selectively include only certain source data?**\
Yes. You can filter by **Source Agency** to migrate only selected entities.

**Does migration create new price structures automatically?**\
No. It copies existing price lists. It does not generate new pricing rules or structures.
