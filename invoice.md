---
description: Invoice listing
---

# Invoice

### Overview

The **Invoice Listing Dashboard** provides a comprehensive interface for managing, tracking, and processing invoices within a financial or accounting system. It displays a table of all invoices filtered by the selected date range, offering options to view, download, and take action on each invoice.

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Filters and Controls

Users can filter the displayed invoices based on various parameters:

* **Date Range**:
  * **From date**: Starting point for invoice listing (e.g., 01-04-2025).
  * **To date**: Ending point for invoice listing (e.g., 07-08-2025).
* **Invoice Number**: Search by invoice number.
* **Status**: Filter invoices by their processing status (e.g., pending, approved, or rejected).
* **Archive Status**: Filter between archived and not archived invoices.
* **Creditor**: Search/filter invoices by creditor name.
* **Internal Comment**: Optional field to filter based on internal notes.
* **Display/Clear Buttons**:
  * **Display**: Applies the selected filters.
  * **Clear**: Resets all filters.
* **Invoice Tool Options**:
  * **Download Invoice PDF**
  * **Download Accounting**
  * **Archive**
  * **Pay**

### Invoice Table Columns

The table displays the following columns for each invoice:

| Column                   | Description                                                                                                                                                                                             |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Checkbox**             | Allows selection of multiple invoices for bulk actions.                                                                                                                                                 |
| **INV.NO**               | Unique invoice number (clickable links).                                                                                                                                                                |
| **TYPE**                 | Type of invoice (e.g., hotel invoice, handling invoice, extra invoice).                                                                                                                                 |
| **NAME**                 | Description of invoice or service (often includes the supplier and date).                                                                                                                               |
| **CREDITOR**             | Name of the invoice creditor (supplier or service provider).                                                                                                                                            |
| **INT.COMM**             | Internal comment or reference tag (e.g., PT, AC).                                                                                                                                                       |
| **AMOUNT**               | Invoice total in relevant currency (e.g., €, USD).                                                                                                                                                      |
| **DUE DATE**             | Payment due date.                                                                                                                                                                                       |
| **APP. DUE DATE**        | Date when invoice was approved or registered.                                                                                                                                                           |
| **DOWNLOAD INVOICE XML** | Option to download the invoice in XML format.                                                                                                                                                           |
| **DOWNLOAD ACCOUNTING**  | Option to download accounting record related to the invoice.                                                                                                                                            |
| **STATUS**               | <p>Current processing status of the invoice:</p><ul><li><strong>Pending</strong> (yellow)</li></ul><ul><li><strong>Rejected</strong> (red)</li></ul><ul><li><strong>Approved</strong> (green)</li></ul> |
| **COMMENTS**             | Link to view comments or notes on the invoice.                                                                                                                                                          |
| **ARCHIVED**             | Icon to indicate whether the invoice is archived                                                                                                                                                        |
