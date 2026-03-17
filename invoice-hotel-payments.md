---
description: >-
  View and export hotel invoice payments in Tourpaq Office Finance. Filter by
  booking period, invoice number, creditor, hotel, and status, then export
  payment lines for reconciliation.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# Invoice Hotel Payments

### Overview

Invoice Hotel Payments shows hotel booking payment lines linked to supplier invoices.

Use it to filter, review, and export hotel invoice payments for reconciliation and reporting.

<figure><img src=".gitbook/assets/image (27) (1) (1) (1) (1) (1) (1).png" alt="Invoice Hotel Payments filters and results table"><figcaption><p>Filter hotel invoice payment lines by booking period, invoice, creditor, status, and hotel.</p></figcaption></figure>

### Features

* **Date Filters:** Users can select a **Booking Start** and **Booking End** date to refine results.
* **Invoice Search:** Search by invoice number for specific records.
* **Status & Creditor Filters:** Filter by invoice status and creditor to view relevant transactions.
* **Hotel Selection:** Allows filtering payments based on specific hotels.
* **Cancelled bookings option:** Users can choose to display only cancelled bookings.
* **Export Functionality:** The **Export** button allows users to download the data in a structured format.

### Data Table Columns

* **INVOICE:** Unique invoice number associated with the transaction.
* **HOTEL:** Hotel identifier where the booking was made.
* **BOOKING:** Booking reference number.
* **CREDITOR:** The entity responsible for the transaction.
* **AMOUNT:** Payment amount in the given currency.
* **CURRENCY:** The transaction currency (USD in this case).
* **DESCRIPTION:** Brief description of the transaction (e.g., Hotel Room Payment).
* **INVOICE STATUS:** Displays the status of the invoice (e.g., Pending).
* **BOOKING CLX:** Indicates whether the booking was cancelled (YES/NO).

### Usage example

**Scenario:** Export invoice hotel payments for bookings created in November 2025.

1. Define **Booking start** and **Booking end** dates (e.g., 04-11-2025 to 04-12-2025).
2. (Optional) Set **invoice number**, **status**, **creditor**, and **hotel** filters.
3. Click **Export** to generate the report.

<figure><img src=".gitbook/assets/image (554).png" alt="Exporting invoice hotel payments"><figcaption><p>Export invoice hotel payments to a file for finance reporting and reconciliation.</p></figcaption></figure>

<figure><img src=".gitbook/assets/image (555).png" alt="Invoice hotel payments export output"><figcaption><p>Export output example: one row per payment line with invoice number, booking reference, creditor, amount, currency, and invoice status.</p></figcaption></figure>

### Export columns

The export includes the currently displayed rows and columns such as:

* **Invoice**: Unique invoice number.
* **Hotel**: Hotel code.
* **Creditor**: Creditor name.
* **Amount**: Payment amount.
* **Currency**: Transaction currency.
* **Description**: Payment description (for example Hotel Room Payment).
* **Invoice status**: Status (for example Pending).

***

### FAQ

* **What is Invoice Hotel Payments used for?**\
  Use it to review hotel booking payment lines linked to supplier invoices and export them for reconciliation and reporting.
* **Why can’t I find a payment line I expect to see?**\
  Start by widening the **Booking start/Booking end** range. Then filter by **invoice number**, **creditor**, and **status**.
* **Does Export include all records in the system?**\
  No. Export includes the **currently displayed** rows based on your filters.
* **What does BOOKING CLX mean?**\
  It indicates whether the booking is cancelled (YES/NO).
* **What currency will I see in the list/export?**\
  The currency is shown per row in **CURRENCY**. It depends on the booking/invoice setup.
* **Where do I manage the invoice itself?**\
  Use **Finance → Invoice** to open, download, archive, or pay invoices (permissions required). See [Invoice](invoice.md).
