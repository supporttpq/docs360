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

1.  Search for an **Early Booking Deposit Invoice**.<br>

    <figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
2.  Download the invoice and confirm that the Early Booking Discount information is present.<br>

    <figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
3.  Navigate to the corresponding **hotel rule** used to generate that invoice.<br>

    <figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
4.  Delete the rule and confirm it has been successfully removed.<br>

    <figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
5.  Download the same invoice again.

    <figure><img src="../../../.gitbook/assets/image (6) (1) (1).png" alt=""><figcaption></figcaption></figure>



**The information will no longer be available.**

{% hint style="danger" %}
Note: Be aware that even though the invoice data is deleted, the sum of the invoice remains. This is expected behavior.
{% endhint %}

***

**Expected Behavior**\
Deleting a rule removes its related invoice data to maintain data consistency.<br>
