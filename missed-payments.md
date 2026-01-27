# Missed Payments

### Overview

The **Missed Payments** page lists payment attempts that were **not successfully processed or recorded** in Tourpaq. It helps finance and support teams find these payments, understand what happened, and take action (for example: retry, move, or hide entries).

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### What this page is for

Use this page to:

* **Detect** failed payment captures or mismatched transactions
* **Investigate** the payment details (method, amount, transaction code, status)
* **Correct** the situation by retrying the booking/payment or moving the payment to the correct booking
* **Keep the list tidy** by hiding entries that are no longer relevant

{% hint style="info" %}
Available actions can depend on your permissions.
{% endhint %}

### Filters (narrow down the list)

At the top of the page you can filter the results:

* **Agency**: show payments for a specific agency.
* **Payment Method**: show payments for a specific method (for example, credit card or bank transfer).
* **Payment Start / Payment End**: show payments attempted within a specific date range.
* **Show Hidden**: include entries that have been hidden.
* **Clear**: reset all filters.

### Payment list (table)

Each row is one missed payment attempt.

#### Actions

The **ACTIONS** column contains icons you can use to manage a payment entry:

* **Hide** the payment entry
* **Retry to place booking**
* **Retry to place payment**
* **Move payment** to another booking
* **View Tourpaq booking offer**
* **View WebBooking offer**

#### Columns (what the fields mean)

| Column               | What it shows                                                                        |
| -------------------- | ------------------------------------------------------------------------------------ |
| **PAYMENT NO**       | Unique identifier for the payment entry.                                             |
| **PAYMENT METHOD**   | The method used (for example, card or bank).                                         |
| **AMOUNT**           | The payment amount.                                                                  |
| **DEBITS**           | Identifier related to the debit transaction.                                         |
| **TRANSACTION CODE** | Transaction code assigned by the payment system.                                     |
| **STATUS CODE**      | Technical status returned by the payment gateway (for example, “Capture Completed”). |
| **PAYMENT STATUS**   | Descriptive payment status (often mirrors the status code).                          |
| **AGENCY**           | Responsible agency.                                                                  |
| **CUSTOMER**         | Customer connected to the payment attempt.                                           |
| **BOOKING ID**       | Booking reference number linked to the payment (if available).                       |
| **PAYMENT DATE**     | Date the payment was attempted.                                                      |
| **REASON**           | Why the payment failed (if available).                                               |

### Typical workflow

{% stepper %}
{% step %}
### 1) Find the payment entry

Use **Agency**, **Payment Method**, and **Payment Start / Payment End** to narrow the list.
{% endstep %}

{% step %}
### 2) Review the payment details

Check fields like **Payment No**, **Transaction Code**, **Status Code**, **Payment Status**, **Booking ID**, and **Reason**.
{% endstep %}

{% step %}
### 3) Choose the next action

Use the icons in **ACTIONS** to retry, move, view offers, or hide the entry.
{% endstep %}
{% endstepper %}

### What happens after an issue is resolved

When a payment is corrected, it moves out of the “missed” category and appears in the appropriate financial overview.

***

### FAQ

* **What is a “missed payment” in Tourpaq?**\
  It is a payment attempt that is not successfully processed or not recorded correctly, and is therefore logged on the **Missed Payments** page.
* **How do I show payments for a specific time period?**\
  Use **Payment Start** and **Payment End** to filter by the payment attempt date.
* **What is the difference between “Status code” and “Payment status”?**\
  **Status code** is the technical status returned by the payment gateway. **Payment status** is a descriptive status that often mirrors the status code.
* **What does “Reason” mean, and why is it sometimes empty?**\
  **Reason** explains why the payment failed _if available_. If the payment system does not provide a reason, the field may be blank.
* **What does “Hide” do, and can I see hidden entries again?**\
  Hide removes entries from the main list view. Use **Show Hidden** to display hidden entries.
* **Can I reassign a payment to a different booking?**\
  Yes. The **Move payment to another booking** action is available in the **ACTIONS** column.
