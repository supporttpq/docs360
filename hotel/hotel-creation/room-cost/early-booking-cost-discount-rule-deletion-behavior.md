# Early Booking Cost Discount Rule – Deletion Behavior

### Overview

Deleting an **Early Booking Cost Discount Rule** on a hotel also deletes the related autobilling invoice data stored in the `EarlyBookingDepositInvoiceLine` table.

This happens regardless of invoice status. This is current Tourpaq behavior.

### What happens when you delete the rule

* Tourpaq triggers a **cascading delete**.
* Tourpaq removes the related rows from `EarlyBookingDepositInvoiceLine`.
* This behavior is **not** driven by the autobilling job. It is handled by Tourpaq system logic.

### Impact

* The invoice will no longer show the Early Booking Discount details.
* The invoice total may still remain unchanged after deletion.

{% hint style="danger" %}
Even if the Early Booking Discount details are removed, the invoice sum can remain the same. This is expected in the current implementation.
{% endhint %}

### Steps to reproduce

{% stepper %}
{% step %}
### Find an Early Booking Deposit invoice

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Download the invoice and verify the discount details exist

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Open the hotel rule that generated the invoice

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Delete the rule

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Download the same invoice again

<figure><img src="../../../.gitbook/assets/image (6) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The Early Booking Discount details are no longer available.
{% endstep %}
{% endstepper %}

### Expected behavior (current design)

Deleting a rule deletes its related invoice data to keep the data model consistent.

### FAQ

#### Does deleting the rule change the invoice amount?

Not always. The Early Booking Discount details can be removed while the invoice total remains unchanged.

#### Does the invoice status matter?

No. The cascade runs regardless of invoice status.

#### Is this related to the autobilling job?

No. The deletion is triggered by the rule deletion itself, not by autobilling.

#### Can I restore the deleted discount details?

There is no self-service restore in the UI. If you need the historical lines back, contact Tourpaq support and provide the invoice number and hotel rule context.

#### How can I avoid losing the details?

Download and archive the invoice before deleting the rule. Avoid deleting rules that have already been used for invoicing unless you are sure you do not need the historical details.
