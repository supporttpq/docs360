# Early Booking Cost Discount Rule – Deletion Behavior

**Overview**

When an **Early Booking Cost Discount Rule** is deleted from a hotel, the related information in the **autobilling invoice** (specifically in the _EarlyBookingDepositInvoiceLine_ table) is also deleted.\
This behavior occurs regardless of the invoice status and is part of the current Tourpaq implementation logic.

***

**Behavior Details**

* The deletion of an **Early Booking Cost Discount Rule** triggers a **cascading delete** in Tourpaq.
* This cascade removes the related data from the **EarlyBookingDepositInvoiceLine** table.
* The behavior is **not linked to the autobilling process** or the invoice’s status — it is handled entirely within the **Tourpaq system logic**.

***

**Steps to Reproduce**&#x20;

1.  Search for an **Early Booking Deposit Invoice**.\


    <figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>
2.  Download the invoice and confirm that the Early Booking Discount information is present.\


    <figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>
3.  Navigate to the corresponding **hotel rule** used to generate that invoice.\


    <figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>
4.  Delete the rule and confirm it has been successfully removed.\


    <figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>
5.  Download the same invoice again.

    <figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>



**The information will no longer be available.**

***

**Expected Behavior**\
Deleting a rule removes its related invoice data to maintain data consistency.\
