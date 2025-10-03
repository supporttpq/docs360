# Invoice Hotel Payments

### Overview

The "Invoice Hotel Payments" interface provides a detailed summary of hotel booking payments associated with invoices. It allows users to filter, view, and export payment details based on various parameters.

<figure><img src=".gitbook/assets/image (27) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Features

* **Date Filters:** Users can select a **Booking Start** and **Booking End** date to refine results.
* **Invoice Search:** Search by invoice number for specific records.
* **Status & Creditor Filters:** Filter by invoice status and creditor to view relevant transactions.
* **Hotel Selection:** Allows filtering payments based on specific hotels.
* **Canceled Bookings Option:** Users can choose to display only canceled bookings by checking the provided checkbox.
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
* **BOOKING CLX:** Indicates whether the booking was canceled (YES/NO).
