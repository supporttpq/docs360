# Hotel Contracts

## Hotel Contract List

### Overview

The **Hotel Contract List** is the overview screen for hotel contracts. Use it to find contracts fast, check statuses, and open details.

### Purpose

Use this page to:

* Track the status of contracts (imported, accepted, rejected)
* Filter and search across hotels and contracts
* Open a contract to review or update it
* Remove contracts you no longer want to keep in the list

### Preconditions

Before using the Hotel Contract List, ensure that:

* Contracts are created or imported via the correct process
* Hotels referenced in the contract exist in the system
* The user has appropriate permissions to view, edit, or delete contracts

***

### Instructions

#### Accessing the page

Navigate to **Hotels → Contract List** in the main menu. Some setups label it as **Hotel → Hotel Contracts**.

#### Filtering contracts

Use the filters at the top of the list:

* **Contract Name**
* **Hotel Name**
* **Hotel Code**
* **Created Date**
* Toggle **Show Hidden** to include hidden contracts

Click **Display** to apply filters or **Clear** to reset.

#### Reading the table

Each row displays:

* **Contract Name** – Click to open the contract
* **Hotel Name** – As defined in the system
* **Hotel Code** – The internal code for identification
* **Created Date** – When the contract entry was created
* **Imported** – Whether the contract came from an import
* **Created User** – Who created the contract entry
* **Accepted / Rejected** – Review status, if used in your workflow
* **Rejected Comment** – Reason for rejection, if applicable
* 🗑️ **Delete** – Removes the contract entry from the list

{% hint style="warning" %}
Deleting a contract removes it from the list. If you need it again, you may need to recreate it or re-import it.
{% endhint %}

#### Creating a new contract

Click the **Create** button in the upper-right corner to initiate a new contract entry.

### Screenshot

Below is a visual representation of the Hotel Contract List interface:

<figure><img src="../.gitbook/assets/image (294).png" alt=""><figcaption></figcaption></figure>

***

### Related pages

* [Hotel contract - General](hotel-contract-contract-name.md)
* [Rooms – Hotel Contract Configuration](rooms-hotel-contract-configuration.md)
* [Periods – Hotel Contract Configuration](periods-hotel-contract-configuration.md)
* [Board Supplements - Hotel Contract Configuration](board-supplements-hotel-contract-configuration.md)

### FAQ

#### What does “Imported” mean?

It indicates the contract entry was created via an import flow. If it is not imported, it was created manually in Tourpaq.

#### What do “Accepted” and “Rejected” mean?

They reflect your internal review workflow. Use them to mark contracts as ready for use or needing changes.

#### Why can’t I find a contract I know exists?

Try these quick checks:

* Clear filters, then click **Display**
* Search by **Hotel Code** (usually the most precise)
* Enable **Show Hidden**
* Confirm you have permissions to view that hotel/contract

#### What is a “Hidden” contract?

Hidden contracts are excluded from the default list view. Turn on **Show Hidden** to include them in search results.

#### Who can create or delete contracts?

It depends on your user role permissions. If you do not see **Create** or **Delete**, ask an admin to grant access.
