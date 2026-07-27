---
description: >-
  Create a transport supplier for transport assignment, reporting, extras, and
  communication.
---

# Create a Transport Supplier

### Overview

Create a **Transport Supplier** to represent a provider of flights, buses, transfers, or other transport services.

The supplier record supports supplier assignment on Transport and Real Transport records. It also controls supplier-specific reporting, communication, and extra availability. See [Transport Suppliers](./) for supplier management and usage.

### Purpose

Use this form to create a reusable supplier record before assigning it to transport.

The selected **Tour Operator** connects the supplier to its operating context. The **Reporting Type** supports supplier reporting and exports. Supplier assignment can determine which extras appear for a booking. After saving, configure supplier reporting delivery through [Communication Configuration – Transport Supplier](communication-configuration-transport-supplier.md).

***

### Navigation

To add a new Transport Supplier, go to:

**Menu > Transport Suppliers > Create New Supplier. A new page will be opened where you need to complete the mandatory fields.**

***

### Form Fields Overview

The form to create a new transport supplier includes the following mandatory and optional fields:

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (38).png" alt=""><figcaption></figcaption></figure>

#### 1. **Name** (Mandatory)

* **Description**: The full name of the transport supplier.
* **Example**: "TransCar", "BlueBus Logistics"

#### 2. **Tour Operator** (Mandatory)

* **Description**: The tour operator associated with this transport supplier.

#### 3. **Reporting Type** (Not mandatory)

* **Description**: Select the reporting used by the Transport Supplier.
* **Action**: Select from the available options.

#### 4. **Hide as filter on lists** (Not mandatory – Checkbox)

* **Description**: When checked, this supplier will be hidden from lists.

#### 5. **Status** (Not mandatory)

* **Options**:
  * **Visible**: Supplier is active and appear in to the main page with all Transports Suppliers
  * **Hidden**: Supplier is hidden from the Transport Suppliers list

***

### Saving the Form

Once all required fields are completed:

1. Double-check all entries for correctness.
2. Click **Save** (button located at the bottom of the form).
3. After the Save button has been pressed and the new Transport Supplier has been created, a new tab, **Communication**, will appear.

***

### Notes

* All fields marked with a red asterisk (\*) are **mandatory**.
* Ensure the supplier is not duplicated in the system before creating a new entry.
* Reporting Type selection impacts how data is aggregated in export reports.
