# Actions - Hotel Contract Configurations

#### Purpose

The **Actions** tab allows administrators to perform **contract-level bulk actions** such as reimporting specific data sections, sharing contract content, or syncing selective data from external sources. It improves workflow efficiency by reducing the need to update each tab manually.

***

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

***

#### Preconditions

* A contract must be saved and assigned to a supplier.
* The contract must be eligible for import&#x20;
* The user must have access rights to hotel contract administration and importing.

***

#### Interface Sections

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

#### Related Workflows

* **Initial Import:** When a new hotel contract is added and the import from an external file (XML, XLSX, or API) is performed.
* **Data Correction:** When adjustments are made to the source system and you want to sync those updates into the hotel contract without full deletion/reimport.
* **Partial Update:** After a new season is added, only room costs or allotments may be updated using this screen.

***

#### Notes

* This functionality **does not delete** data that is not selected. It only updates/replaces selected sections.
* Always verify results after reimport, especially in the **Rooms**, **Periods**, and **Costs** tabs.
* A confirmation will appear if unsaved changes exist on the contract.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

#### Shere Tab

* Export Hotel contract (PDF) - Allow to export the contract
* Send Email - Offer the possibility to send created contract to supplier and also as many emails address you want. The supplier has the possibility to accept or reject hotel contract.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

To be able to use this function is required to create an email template for Hotel Contract, otherwise an warning will be displayed.
