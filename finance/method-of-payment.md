# Method of Payment

Applicable for Administrator and Financial

This is a module where payment types can be inserted into the system. Each time a payment is made, the payment method must also be specified.

<figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

There are 2 different payments in the system:

* Debit payments
* Credit payments

Debit payments will correspond to those that will “take money”, and credit payments will correspond to those that will “give money”. For instance, if a customer goes to the bank and pays for his trip, the payment needs to be inserted in the system, and it will be a “debit” one.

There will be some special payment methods that will need to be differentiated from the rest:

* The online payments
* The payments imported from the bank
* The payments are made using Dankort cards.
* The guide payments
* Agent Machine Payment
* Gift Card Payments

### Create a new payment method

<figure><img src="../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

All these being said, below are the fields that should be inserted when defining a method of payment:

* Payment code
* Payment full name
* Type of payment (debit or credit)
* Credit account
* Debit account
* Specify if it is an online payment.
* Specify if it will be used for the imported payments from the bank
* Specify if it will be used for the payments made using Dankort cards.

**Please note**: **If choosing a VISA card type and paying with a Visa/Dankort card on the DIBS platform, DIBS will accept this, and the Tourpaq method of payment will be the one assigned to VISA, not to Visa/Dankort**.

* Specify if it will be used for the payments made by guides.
* Specify if it will be a cash payment.
* Specify if it will be active or not

When a method of payment is inserted into the system, it will be associated with the current company.
