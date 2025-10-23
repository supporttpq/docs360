# Extras List

### ✅ Overview

The **Extras Lists Export Module** is used to generate exports related to **extras** (e.g., ski rental, extra services) for operational partners such as suppliers. These exports help suppliers manage service delivery based on confirmed bookings and extras ordered by passengers.

Exports can be generated in **Excel XML** or **PDF** format, in both **English and German**, and include optional cost data.

***

### 👤 Availability

* **User Role**: **Administrator only**
* **Locations in Office**:
  1. **Export → Extras Lists** _(full access to filters and types)_
  2. **Users → Suppliers → \[A Supplier] → Communication tab**
  3. \*_Extras Setup → Extras → \[An Extra] → Communication tab_

Each of the above uses the same filter logic but may restrict the export to the specific supplier or extra selected.

***

### 🎯 Purpose

This module allows administrators to:

* Generate structured lists of extras grouped by suppliers and bookings.
* Provide real-time or scheduled updates to suppliers.
* Output lists in various formats (PDF with/without costs, Excel).
* Support logistics for rental services (e.g., Ski equipment – Skiset).

***

### ⚙️ Fields & Filters

| Field                  | Description                                                                           |
| ---------------------- | ------------------------------------------------------------------------------------- |
| **Supplier**           | Filter to a specific **supplier** providing extras.                                   |
| **Report type**        | Select the export format (see below).                                                 |
| **Arrival period**     | Filters bookings where **arrival** falls within the selected range.                   |
| **Booking period**     | Filters bookings **created** during this date range.                                  |
| **Compress as ZIP**    | When selected, export will be downloaded in **ZIP** format.                           |
| **Categories**         | Filter extras by a predefined **category** (e.g., ski rentals, VIP, food).            |
| **Extras**             | Multi-select field to filter by one or more specific **extras**.                      |
| **Display all extras** | Ignores selection and includes **all extras** related to the filtered bookings.       |
| **Columns**            | Only selected columns will appear in the output (active if "Select Columns" is used). |

***

### 🧾 Report Types

| Report Type                   | Description                                                                                 |
| ----------------------------- | ------------------------------------------------------------------------------------------- |
| **Extra List (DE)**           | Excel/XML export in **German**                                                              |
| **Extra List (EN)**           | Excel/XML export in **English**                                                             |
| **Extra List PDF (DE)**       | PDF version of the extra list in **German**                                                 |
| **Extra List PDF (EN)**       | PDF version of the extra list in **English**                                                |
| **Extra List PDF with Costs** | PDF list **including extra prices**, suitable for accounting or reconciliation              |
| **Ski rental (Skiset)**       | Special export template for **ski equipment rentals**, typically used with Skiset suppliers |

***

### 🧰 Buttons / UI Actions

<figure><img src="../.gitbook/assets/image (24) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

| Button                 | Action                                                                        |
| ---------------------- | ----------------------------------------------------------------------------- |
| **Export**             | Generates the selected report using current filters                           |
| **Columns for export** | Opens the **Columns** filter interface to customize which fields are exported |

***

### 🛠️ How to Generate Extras Lists

#### ✅ Option 1: Centralized Export

**Navigation**: `Export → Extras Lists`

* Use full filter set to define **supplier**, **dates**, **brands**, and **extras**.
* Click **Export** to download.

***

#### ✅ Option 2: Supplier Communication Tab

**Navigation**: `Users → Suppliers → [Choose Supplier] → Communication`

* Automatically filters by selected supplier.
* Additional filters like dates and brand can be applied.
* Used to quickly generate extras reports for that specific supplier.

***

#### ✅ Option 3: Extra Setup Communication Tab

**Navigation**: `Extras Setup → Extras → [Choose Extra] → Communication`

* Auto-filters by selected extra.
* Used when working with a specific extra service.
