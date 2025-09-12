# Transport Suppliers

### Overview

The **Transport Suppliers** page is used to manage the list of transport providers integrated into the system. Each supplier is associated with a tour operator and a specific reporting format. This interface supports adding, viewing, and deleting transport suppliers.

The Transport Supplier is used by the Transport and Real Transport to identify the supplier of the flight. The Transport Supplier can be used for:

* A common way to describe the communication, so all Transports that uses this supplier use the Transport Supplier communication
* The Transport Supplier can be used in Resources in Extra to select the relevant extras (e.g. different baggage options for two different transport suppliers)

***

### 🔍 Filters and Controls

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### 1. **Search by Name**

* A text input to filter the list of suppliers by name.
* Case-insensitive and partial match supported.

#### 2. **Reporting Type Filter**

* A dropdown allowing selection of a specific reporting type.
* Only suppliers linked to the selected reporting type will be shown.

#### 3. **Show All Checkbox**

* When checked, it displays the hidden Transports Suppliers

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* unchecked, filtering is applied.

#### 4. **Clear Button**

* Clears all active filters and shows the default list.

***

### 📄 Table Columns

| Column             | Description                                                                |
| ------------------ | -------------------------------------------------------------------------- |
| **NAME**           | The name of the transport supplier (e.g., DG2 Transp Supp, adTest, test2). |
| **TOUR OPERATOR**  | Identifies the tour operator associated with the supplier.                 |
| **REPORTING TYPE** | Indicates the reporting format or export type used for this supplier.      |

Clicking on the column headers (marked with sort icons) will sort the entries ascending or descending.

***

### 🗑️ Actions

* **Delete Icon (🗑️)**: Click to delete a supplier entry.
  * A confirmation prompt will appear to avoid accidental deletions.

***

### ➕ Create Button

* Located in the top-right corner.
* Opens a form or modal to add a new transport supplier.
  * Required fields likely include: Name, Tour Operator, Reporting Type.

***

### 📄 Pagination and Page Size

* **Pagination Controls**: Allows navigation through multiple pages if more than 25 suppliers exist.
* **Page Size Dropdown**: Select how many entries are shown per page (default: 25).

***

### 📌 Notes

* Always ensure the correct Tour Operator and Reporting Type are selected to ensure data consistency.
