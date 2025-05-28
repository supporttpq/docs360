# Compensation & Deduction

Sometimes it’s necessary to compensate the customer for a complaint. And sometimes the compensation offered to the customer can be deducted from the direct responsible. Therefore, depending on who’s fault is it, proper way for compensation and deduction can be used.

The setup for compensation\&deduction is done in the dedicated section on the service case edit page.

For compensation you need to:

1. Fill in the amount -> agency’s currency is used.
2. Select how the compensation is offered from the drop-down list:

* If cash \~ a special discount (that needs to be defined in the system) will be applied on the booking that will register a negative balance and will follow actual finance process.

<figure><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

\~ mandatory “account” and “branch” fields need to be completed; the information from these two fields is automatically transferred in the Economic tab of the booking, in the corresponding fields, and "Release payment" is activated.

<figure><img src="../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

\~ If the compensation amount is modified, SCD discount will be also updated on the booking.

<figure><img src="../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

\~ If there are more service cases created on the same booking, with compensation, SCD discount will have the same behavior (will update the amount). So the last compensation set on that booking (no matter on which service case) will be updated on the SCD. If there is a need to compensate all amounts, it has to be done "manually" by editing the SCD on the booking with the total amount that needs to be compensate.

<figure><img src="../.gitbook/assets/image (15) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* If giftcard, a giftcard must be generated with the proper amount, and after that is done, compensation can be marked as sent if the giftcard number generated is inserted. This can be visible, marked as “Giftcard sent”, also in the service case overview

<figure><img src="../.gitbook/assets/image (16) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (17) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Compensation can be offered also on destination: cash or other. In this case, “closed on destination” checkbox can be selected. This is for statistics purposes only.

<figure><img src="../.gitbook/assets/image (18) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. Select who’s fault is it from the drop-down list

For the compensation that needs to be deducted, you need to check the “deduct money” checkbox and fill in the mandatory comment field.

Deduction can be done only for hotel or agent’s fault.

When is hotel’s fault, a deduction will be automatically created on hotel’s page, having the amount calculated in creditor’s currency and the comment is also brought automatically from the service case page. Having the deduction on the hotel, normal process will follow, including this deduction on the next invoice.

<figure><img src="../.gitbook/assets/image (19) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

When a compensation is set, the service case goes automatically in closed status.
