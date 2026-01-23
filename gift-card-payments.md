# Gift Card Payments

### **Overview**

The **Gift Card Payment** is an alternative to traditional cash payments. It behaves identically to a cash payment in terms of accounting and processing logic but is used to represent transactions made using a **company-issued gift card or voucher**.

This method is especially useful for promotions, prepaid packages, or customer credit issued in the form of a gift card.

***

### **Purpose**

The Gift Card Payment method serves to:

* Accurately record **non-cash, voucher-based transactions**
* Maintain a clear distinction between actual cash and **gift card redemptions**
* Enable users to quickly identify gift card payments in the booking interface
* Support scenarios where **customers pay using credit issued by the company**

***

### **Preconditions**

Before using or configuring the Gift Card Payment method, ensure:

* The payment method has been defined in the system with the correct attributes (see setup below).
* The employee managing the payment understands that this is **not physical cash**, but a **voucher-based** transaction.
* The **Gift Card Payment** method is marked as **active** and available for use.
* The **Economic tab** is accessible in the **Edit Booking** view.

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Instructions: Using Gift Card Payment**

1. Go to: `Admin Panel > Financial Settings > Payment Methods`
2.  Create a new payment method with the following details:

    | Field                 | Value                                                    |
    | --------------------- | -------------------------------------------------------- |
    | **Payment Code**      | `GIFTCARD` or similar                                    |
    | **Payment Full Name** | `Gift Card Payment`                                      |
    | **Type of Payment**   | `Debit` (money in)                                       |
    | **Credit Account**    | Same as used for Cash Payment                            |
    | **Debit Account**     | Same as used for Cash Payment                            |
    | **Is Cash Payment?**  | ✔️ (Checked)                                             |
    | **Active**            | ✔️ (Checked)                                             |
    | **Other Flags**       | Leave _Online_, _Bank import_, _Dankort_, etc. unchecked |
3. Save the method. It will now be available in the booking flow.

***

### **Booking UI Behavior**

* When a **Gift Card Payment** is registered in a booking, a **new icon** will be visible in the **Edit Booking → Economic tab**.
* This icon helps distinguish gift card transactions from regular cash payments at a glance.

<figure><img src=".gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### **FAQ**

* **How is Gift Card Payment different from Cash Payment?**\
  It is used to represent a company-issued gift card/voucher, but it behaves like a cash payment for accounting and processing.
* **Why is “Is Cash Payment?” checked if it is not physical cash?**\
  The setup uses the same cash-payment accounting/processing logic, even though the transaction represents a voucher-based payment.
* **Where do I see that a booking was paid with a gift card?**\
  When Gift Card Payment is registered, an icon appears in **Edit Booking → Economic tab**.
* **Do I need special access to use this payment method?**\
  You need access to the **Economic tab** in **Edit Booking**. Creating/configuring the method requires access to **Admin Panel → Financial Settings → Payment Methods**.
* **Which accounts should I use for Debit Account and Credit Account?**\
  The documentation specifies using the same **Debit Account** and **Credit Account** as Cash Payment.
* **Should I enable Online, Bank import, Dankort, or similar flags?**\
  No. The setup instructions state these flags are left unchecked.
