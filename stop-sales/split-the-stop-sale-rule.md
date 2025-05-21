# Split the Stop Sale Rule

### Overview

The Remove or Split functionality allows users to modify an existing Stop Sale rule by either removing it entirely or splitting it into multiple distinct periods. This process provides greater flexibility in managing room allotments and sale restrictions.

***

### Accessing the Stop Sales Page

1. Navigate to the Hotel menu.
2. Select Stop Sales.
3. The Stop Sales page will be displayed, listing all defined rules.

&#x20;    \- The default filter applies the current date to the Start/End date fields.

<figure><img src="../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

***

### Steps to Remove or Split a Stop Sale Rule

Step 1: Filter and Select Rule

* Use the available filters to narrow down the list.
* Select an enabled stop sale rule from the list.

<figure><img src="../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>

Step 2: Click Edit

* Click the Edit button corresponding to the selected rule.
* A "Remove or Split" button will appear.

Step 3: Initiate Remove or Split

* Click on the "Remove or Split" button.
* A new section titled "Remove or Split Stop Sale" appears beneath the rule.

Step 4: Specify Number of Records

* Enter the desired number of splits in the "Record number to split stop sale in" field.
* The interface will generate that number of rows for user input.
  * Each row will default to the Start/End dates of the original rule.
  * All rows will have the Enabled checkbox marked by default.

Step 5: Define Periods and Actions

*   For each new row, configure:

    * Start/End Date: Define the period.
    * Action: Choose between Remove or Agreed Allotment.

    <figure><img src="../.gitbook/assets/image (184).png" alt=""><figcaption></figcaption></figure>

Validations:

* The split periods must fully cover the date range of the original rule.
* No overlapping periods are allowed among the split entries.

Step 6: Execute or Cancel

* Click Split to apply the changes.
* If validations pass:
  * Rule is updated and saved.
  * The section closes.
  * The page refreshes, displaying each split rule as an individual entry.
* If validations fail:
  * An error message is displayed.
  * The changes are not saved.
* Alternatively, click Cancel to discard changes and close the section.

***

### Post-Split Behavior

* Once split, each resulting rule behaves as a standalone entry.
* They can be edited or removed independently.

***

### Check Results in Stop Sales Logs

Step 1: View Logs

* After executing the split (Step 7 above), click View Details for each new rule.
* The Stop Sales Logs page is displayed.
  * Filters are automatically applied based on the rule's period and room.

Step 2: Check Log Records

* Verify that Initial R. No and Final R. No reflect the setup.
* Confirm the correct actions (Removed, Agreed Allotment) are shown.

<figure><img src="../.gitbook/assets/image (186).png" alt=""><figcaption></figcaption></figure>

***

### &#x20;Check Results in Allotment per Day on Hotel

Step 1: Access Hotel Edit Page

* After completing the split, go to the Hotel Edit Page.

Step 2: Open "Allotment per Day" Tab

* Navigate to the Allotment per Day tab.
* Apply filters for the dates and room involved in the split.

Step 3: Check Allotment

* The daily allotment for the selected room is displayed.
* Allotment reflects updates based on the split rule setup.

<figure><img src="../.gitbook/assets/image (187).png" alt=""><figcaption></figcaption></figure>

***

### Check Results in Pricelist

Step 1: Access Pricelist

* After splitting the stop sale rule, go to Pricelist Menu -> Pricelist.

Step 2: Apply Filters

* Filter by date and room in accordance with the split rules.

Step 3: Verify FHA

* The FHA (Free Hotel Allotment) field is populated.
* It reflects the available number of rooms:
  * FHA = Final R. No - Booked Rooms

<figure><img src="../.gitbook/assets/image (188).png" alt=""><figcaption></figcaption></figure>

***

### Notes

* Only enabled rules can be modified using Remove or Split.
* The system ensures data integrity through strict validation checks.
* This feature is crucial for dynamic rate and availability management.
