# Migrate Pricelist

## **Overview**

The _Migrate Pricelist_ function allows administrators to copy all price lists from one brand (agency) to another within the same company. It supports bulk migration, optional price adjustments, and optional updates to brand assignments, making it a powerful tool for onboarding new brands or synchronizing pricing across multiple brands.

To migrate pricelists, choose Migrate price list from the Price List menu.&#x20;

<figure><img src="../.gitbook/assets/image (50) (1).png" alt=""><figcaption></figcaption></figure>

## **Purpose**

The feature is designed to simplify and accelerate situations where:

* A new brand is added and needs the same price structure as an existing one.
* Price lists must be aligned across multiple brands.
* Seasonal or strategic changes require bulk updates rather than manual edits.

By automating the migration and allowing optional adjustments, the tool minimizes manual work and reduces the risk of errors.

## Steps to Migrate Price Lists

1. **Access the Feature**
   * Select **Migrate Price List** from the **Price List** menu.
2. **Select Source and Destination Agencies**
   * **From Brand:** Choose the source agency from which price lists will be copied.
   * **To Brand:** Select the destination agency that will receive the copied price lists.
3. **Set Tag (Optional)**
   * Enable the **Set Tag** checkbox and select a tag from the dropdown.
   * The selected tag will be applied to all price lists in the destination agency.
   * For more information on defining and using price list tags, refer to the related training video.
4. **Adjust Prices (Optional)**
   * **Increase/Decrease Amount:** Enter a value to be added or subtracted from all price fields on destination price lists. Positive numbers increase prices; negative numbers decrease prices. Only already set prices on the destination are affected.
   * **Increase/Decrease Percentage:** Enter a percentage to adjust all price fields. Positive numbers increase prices; negative numbers decrease prices. Only already set prices on the destination are affected.
   * **Note:** Amount and percentage can be applied **together**; the percentage is applied first, followed by the amount.
5. **Copy Max Rooms (Optional)**
   * Check the **Copy Max Room** checkbox to copy maximum room fields from source price lists to the destination.
6. **Brand Assignments**
   * By default, the migration also replicates brand assignments on **transports, hotels, resorts, extras, and discounts**.
   * To copy only price lists without changing brand assignments, check **Copy Only Price Lists**.
7. **Source Agency Filtering (Optional)**
   * Certain entities (transports, resorts, destinations) can have a **Source Agency** assigned in their General Settings.
   * Enable the option to migrate only those entities where the **source agency matches the selected From Brand**. This prevents overwriting prices when migrating between the same agencies.
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

## **FAQ**&#x20;

**What does Migrate Pricelist do?**\
It copies all price lists from one brand (agency) to another brand within the same company.&#x20;

**Who can use this feature?**\
Administrators can use Migrate Pricelist.&#x20;

**Can I adjust prices during migration?**\
Yes. You can apply an amount or percentage increase or decrease to prices during migration.&#x20;

**Does migration change brand assignments for transports and hotels?**\
By default it does. You can choose to copy only price lists without changing brand assignments.&#x20;

**Can I apply tags to destination price lists?**\
Yes. You can optionally set a tag that will be applied to all destination price lists.&#x20;

**What happens to “max rooms” values?**\
You can choose to copy maximum room values from source price lists to destination price lists.&#x20;

**Is there a log of migrations?**\
Yes. All migrations are logged, and you can search migrations by brand, user, or date.&#x20;

**Can migration selectively include only certain source data?**\
Yes. You can filter so that only entities with a specific source agency assignment are migrated.&#x20;

**Does migration create new price structures automatically?**\
No. It copies existing price lists from the source brand; it does not generate new prices beyond optional adjustments.&#x20;
