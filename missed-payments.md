# Missed Payments

#### Overview

The **Missed Payment** page provides an overview of payments that were not successfully processed or recorded in the system. It helps finance and support teams identify, investigate, and resolve failed payment attempts efficiently.

This page displays all relevant details of failed or incomplete payments and provides tools to retry, move, or hide payments as needed.

#### Purpose

The purpose of the **Missed Payment** page is to ensure that all unprocessed or failed payments are easily traceable and manageable within Tourpaq.\
It helps agencies:

* Detect failed payment captures or mismatched transactions.
* Take corrective actions such as retrying payments or moving them to the correct booking.
* Maintain accurate financial records and minimize revenue discrepancies.

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Filtering Options

At the top of the page, several filters are available to narrow down payment results:

* **Agency** – Filters payments by the responsible agency.
* **Payment Method** – Filters based on the method used (e.g., Credit Card, Bank Transfer).
* **Payment Start / Payment End** – Defines the date range for payment attempts.
* **Show Hidden** – Displays payments that have been hidden or archived.
* **Clear** – Resets all filters to show the complete list of missed payments.

***

#### Payment List Table

The central table displays a list of all missed payments and their details.

| Column               | Description                                                                                                                                                                                                                                     |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ACTIONS**          | <p>Contains icons to manage or correct payment entries:<br>• Hide selected payments<br>• Retry to place booking<br>• Retry to place payment<br>• Move payment to another booking<br>• View Tourpaq booking offer<br>• View WebBooking offer</p> |
| **PAYMENT NO**       | The unique identifier assigned to the payment.                                                                                                                                                                                                  |
| **PAYMENT METHOD**   | The method used for the transaction (e.g., CARD, BANK).                                                                                                                                                                                         |
| **AMOUNT**           | The amount of the payment attempt.                                                                                                                                                                                                              |
| **DEBITS**           | Identifier related to the debit transaction.                                                                                                                                                                                                    |
| **TRANSACTION CODE** | The unique transaction code assigned by the payment system.                                                                                                                                                                                     |
| **STATUS CODE**      | The technical status returned by the payment gateway (e.g., _Capture Completed_).                                                                                                                                                               |
| **PAYMENT STATUS**   | The descriptive payment status, often mirroring the status code.                                                                                                                                                                                |
| **AGENCY**           | The agency responsible for the payment.                                                                                                                                                                                                         |
| **CUSTOMER**         | The customer involved in the payment attempt.                                                                                                                                                                                                   |
| **BOOKING ID**       | Reference number of the related booking.                                                                                                                                                                                                        |
| **PAYMENT DATE**     | The date when the payment was attempted.                                                                                                                                                                                                        |
| **REASON**           | Explains why the payment failed (if available).                                                                                                                                                                                                 |

#### How It Works

When a payment fails to process or record correctly, it is automatically logged on the **Missed Payment** page.\
From here, authorized users can:

* Review payment details and identify the cause of failure.
* Retry the payment or reassign it to another booking.
* Hide completed or irrelevant records to keep the list clean.

Once the issue is resolved, the corrected payment will move out of the “missed” category and appear in the appropriate financial overview.
