---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Payment file import

Applies for Administrator and Financial

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

This is a function that allows importing in the system the payments that have been made to the bank by the customers.

Each company from the system can choose a certain bank where their payments will be made.

The bank will provide a file with payments together with the specification for importing them into the system.

Although the specification file will be different from bank to bank (thus, from company to company if different banks are chosen), the following data should be found in all the payment files:

* A booking identifier
* Payment date
* Amount

The payment date is customizable within the interface, with the default set to today’s date. However, if the payment data source is of the Accounting Date type, the default date is replaced with the specified accounting date.

Each payment from the system has a certain “method of payment” associated. For the payments that come from the bank, a special method of payment will be needed.

All the imported payments will appear in Payment Registration.
