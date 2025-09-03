# Payment File Import

### 📄 Overview

The **Payments** module provides functionalities to manually  import payments associated with bookings and customers. It includes a robust interface for registering new payments and a streamlined **Payment File Import** system for automating bank payments processing.

***

### 🎯 Purpose

Each company in the system can choose a certain bank where its payments will be made.

The bank will provide a file with payments together with the specification for importing them into the system.

Although the specification file will be different from bank to bank (thus, from company to company if different banks are chosen), the following data should be found in all the payment files:

* A booking identifier
* Payment date
* Amount

The payment date is customizable within the interface, with the default set to today’s date. However, if the payment data source is of the Accounting Date type, the default date is replaced with the specified accounting date.

Each payment from the system has a certain “method of payment” associated with it. For the payments that come from the bank, a special method of payment will be needed.

All the imported payments will appear in Payment Registration.

***

### 🧭 Instructions

#### &#x20;**Payment File Import**

1. Obtain the **payment file** from the bank (format varies per bank).
2. Navigate to the **Payment File Import** section.
3. Upload the file.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### 📌 Notes

* Payment files are validated upon upload. Any unmatched or erroneous records will be flagged for review.



