# Migrate Pricelist

### Overview

The **Migrate Price List** function allows users to perform a **bulk copy of all price lists from one agency to another**. This operation can only be performed **between agencies within the same company**.

To migrate pricelists, choose Migrate price list from the Price List menu.&#x20;

<figure><img src="../.gitbook/assets/image (50) (1).png" alt=""><figcaption></figcaption></figure>

### Steps to Migrate Price Lists

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

### Migration Log and Search

* All migrations are **logged** to track past actions.
* To search through migrations, click **Search Migrations** and filter by:
  * Brand
  * User who performed the migration
  * Date of migration
* **Show Hidden:** Displays migrations older than the number of days specified in **System Setup → Hide Filters**.
