# Actions - Hotel Contract Configurations

### Purpose

The **Actions** tab allows administrators to perform **contract-level bulk actions** such as reimporting specific data sections, sharing contract content, or syncing selective data from external sources. It improves workflow efficiency by reducing the need to update each tab manually.

***

<figure><img src="../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

***

### Preconditions

* A contract must be saved and assigned to a supplier.
* The contract must be eligible for import&#x20;
* The user must have access rights to hotel contract administration and importing.

***

### Interface Sections

**Import Tab**

Displays a checklist of available sections that can be reimported:

| Section                      | Description                                                       |
| ---------------------------- | ----------------------------------------------------------------- |
| **Hotel Allotment**          | Reimports allotments for each period and room type.               |
| **Room Cost**                | Updates room cost per period.                                     |
| **Stay And Pay**             | Syncs special deals such as “Stay 7, Pay 6”.                      |
| **Early Booking**            | Reimports early booking discount rules.                           |
| **Cut Down Hotel Allotment** | Applies reductions to pre-defined allotments.                     |
| **Extra Bed Cost**           | Syncs prices for additional beds.                                 |
| **Extra Cost Rule**          | Reimports optional extras like airport pickup or minibar fees.    |
| **Release**                  | Updates release periods (e.g., minimum lead time before booking). |
| **Board Supplements**        |  Imports supplements like Half Board or Full Board.               |
| **Gala Dinner**              | Reimport Gala Dinner                                              |
| **Deposits**                 | Imports deposit payment structure.                                |
| **Facilities**               | Imports facilities (e.g., Wi-Fi, Pool, Parking).                  |

**Button:**\
🔁 **Reimport Hotel Contract** – Triggers the reimport for selected data types.

***

### Related Workflows

* **Initial Import:** When a new hotel contract is added and the import from an external file (XML, XLSX, or API) is performed.
* **Data Correction:** When adjustments are made to the source system and you want to sync those updates into the hotel contract without full deletion/reimport.
* **Partial Update:** After a new season is added, only room costs or allotments may be updated using this screen.

***

#### Notes

* This functionality **does not delete** data that is not selected. It only updates/replaces selected sections.
* Always verify results after reimport, especially in the **Rooms**, **Periods**, and **Costs** tabs.
* A confirmation will appear if unsaved changes exist on the contract.

<figure><img src="../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure>

#### Shere Tab

* Export Hotel contract (PDF) - Allow to export the contract
* Send Email - Offer the possibility to send created contract to supplier and also as many emails address you want. The supplier has the possibility to accept or reject hotel contract.

<figure><img src="../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

To be able to use this function is required to create an email template for Hotel Contract, otherwise an warning will be displayed.

## Save Hotel Contract without production details

During hotel contract negotiations, certain information may not yet be available (e.g., board codes, product names, or supplements). The system allows the staff to save a hotel contract without being forced to provide these details immediately. However, complete data must be validated at the time of import to ensure accuracy and consistency.

#### Purpose

The purpose of this requirement is to make contract creation more flexible by separating validations into two levels:

1. **Save-level validation** → Allows saving contracts even when some fields are unknown.
2. **Import-level validation** → Ensures all mandatory fields are present before the contract is imported and made operational.

This approach enables contract staff to store draft agreements without blocking their workflow while maintaining strict data quality at import.

#### Functional Requirements

1. **Validation Levels**
   * Save-level: Minimal validation, allowing optional fields to remain empty.
   * Import-level: Strict validation applied before importing the contract.
2. **Fields validated at Import only (on Board tab):**
   * **Extra Category** → Mandatory only for import.
   * **Product** → Mandatory only for import.
   * **Name** → Mandatory only for import.
   * **Code** → Mandatory only for import.
3. **PDF Export**
   * When generating the PDF, the system will use the _List Name_ from the Board Types for board references.
   * This ensures independence from individual naming conventions.
4. **Contract Staff Actions**
   * **Send Mail** and **Export to PDF** remain functional even if the optional data (saved but not imported) is missing.
