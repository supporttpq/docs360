# Hotel Contracts

## Hotel Contract List

### Overview

The **Hotel Contract List** page provides a central interface for managing contracts related to hotels within the system. It enables users to view, filter, and maintain contract entries, including key details like contract name, hotel name, code, and creation status.

### Purpose

This page serves to streamline the monitoring and validation of hotel contracts, allowing operators to:

* Track the status of contracts (imported, accepted, rejected)
* Filter and search by various attributes
* Manually remove outdated contracts
* Verify data consistency between hotel and transport modules

### Preconditions

Before using the Hotel Contract List, ensure that:

* Contracts are created or imported via the correct process&#x20;
* Hotels referenced in the contract exist in the system
* The user has appropriate permissions to view, edit, or delete contracts

### Instructions

#### 1. Accessing the Page

Navigate to **Hotels → Contract List** in the main navigation menu.

#### 2. Filtering Contracts

Use the filters at the top of the list:

* **Contract Name**&#x20;
* **Hotel Name**
* **Hotel Code**
* **Created Date**
* Toggle **Show Hidden** to reveal archived contracts

Click **Display** to apply filters or **Clear** to reset.

#### 3. Reading the Table

Each row displays:

* **Contract Name** – Clickable link to open contract details
* **Hotel Name** – As defined in the system
* **Hotel Code** – The internal code for identification
* **Created Date** – When the contract entry was made
* **Imported** – Indicates if the contract was imported or not
* **Created User** – The user who created the entry
* **Was Accepted / Rejected** – The current review status
* **Rejected Comment** – Displays rejection reason (if any)
* 🗑️ **Delete icon** – Used to manually remove the contract

#### 4. Creating a New Contract

Click the **Create** button in the upper-right corner to initiate a new contract entry.

### Screenshot

Below is a visual representation of the Hotel Contract List interface:

<figure><img src="../.gitbook/assets/image (294).png" alt=""><figcaption></figcaption></figure>
