# Extra Orders

<figure><img src="../../.gitbook/assets/image (306).png" alt=""><figcaption></figcaption></figure>

### **Overview**

The **Extra Orders** tab shows **additional purchases and transactions** connected to a booking (for example: excursions, upgrades, or other extra services). The same view also includes the **Service Cases** section, where you can see any **support cases/tickets** registered for the booking.

Use this page when you need to:

* Review what additional services were purchased after the booking was created.
* Check payment references and confirmation status.
* Open order details and handle refunds.
* See related service cases raised for the same booking.

***

### **Purpose**

* Purchase **excursions (Extra Orders)** directly from the booking page (office/back-office).
* Track additional payments or services related to a booking.
* Monitor service-related issues or requests raised by customers.
* Support cancellation and refund workflows (depending on permissions and payment method).
* Provide a single overview for back-office users (e.g., support, accounting, agents).

***

### **Preconditions**

* You must have access to the **Booking details** view and the **Extra Orders** tab.
* At least one **extra order** or **service case** must exist for data to be shown.
* Refund handling requires that transactions are processed through an integrated **payment system** and that your user has the required permissions.

***

### **Instructions**

#### **Viewing and managing Extra Orders**

1. Open the relevant booking.
2. Go to the **Extra Orders** tab.
3. Review the list:
   * Each row represents a single **extra order**.
4. Use **Details** to view the itemized contents of the order.
5. Use **View Refunds** to review existing refunds or initiate a refund (if available).
6. Use the **Book** button to purchase an **extra order (excursion)** directly from the booking page.

<figure><img src="../../.gitbook/assets/image (308).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (309).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If you cannot see **Book** or **View Refunds**, it usually means either (1) your user role does not have permission, or (2) the selected payment method/provider does not support the action from this view.
{% endhint %}

#### **Viewing Service Cases**

1. Scroll to the **Service Cases** section (below Extra Orders).
2. Review any service cases linked to the booking.

Service Cases are typically used to document and track follow-ups such as customer complaints, service requests, missing information, or other booking-related issues.

***

### **Field Descriptions**

#### **Extra Orders section**

| Field                    | Description                                                      |
| ------------------------ | ---------------------------------------------------------------- |
| **EXTRA ORDER NO**       | Unique identifier for the extra service order.                   |
| **HOTEL NAME**           | Name of the hotel where the extra service was booked.            |
| **CREATE DATE**          | Date and time when the extra order was created.                  |
| **TOTAL PRICE**          | Total price of the extra order (including any fees).             |
| **CARD FEE**             | Additional fee applied for card transactions (if applicable).    |
| **PAYMENT ORDER ID**     | Internal reference ID for the payment/order in the payment flow. |
| **TRANSACTION CODE**     | Payment provider/banking reference code.                         |
| **METHOD**               | Payment method used (codes depend on your configuration).        |
| **ROOM NO.**             | Room number associated with the extra order (if applicable).     |
| **PAYMENT CONFIRMATION** | Indicates whether the payment has been confirmed.                |
| **IS CANCELLED**         | Indicates whether the extra order has been cancelled.            |
| **CANCEL REASON**        | Reason for cancellation (if cancelled).                          |
| **USER**                 | Username of the user who created/handled the order.              |
| **DETAILS**              | Opens the detailed breakdown of the extra order.                 |
| **VIEW REFUNDS**         | Opens the refund view for the order (if supported).              |

{% hint style="warning" %}
A **cancelled** order is not necessarily the same as a **refunded** order. Always use **View Refunds** (and/or the payment reference fields) to verify whether money has been returned.
{% endhint %}

#### **Service Cases section**

The Service Cases table layout can vary by setup, but commonly includes:

* **Customer** (name or contact reference)
* **Hotel**
* **Reason / category**
* **Description**
* **Room number** (if relevant)
* **Created date** (and sometimes status/owner)

***

### **FAQ**

#### **1. What is the difference between “Extras” and “Extra Orders”?**

**Extras** are typically added as part of the booking components (often per passenger/room) during the booking flow. **Extra Orders** are additional purchases/transactions registered on the booking (commonly used for excursions or post-booking add-ons).

***

#### **2. Why can’t I see the “Book” button?**

Most common reasons:

* Your user role does not have permission to create extra orders.
* No bookable excursion/extra is available for the booking’s dates/brand/destination.

***

#### **3. The payment is not confirmed — what should I check?**

Check the payment references:

* **Payment Order ID**
* **Transaction Code**
* **Payment Confirmation**

If the payment should have been captured/confirmed, verify it in your payment provider/back-office process and refresh the booking view.

***

#### **4. Is “Cancelled” the same as “Refunded”?**

Not always. Cancellation is the order status, while refunds depend on the payment transaction flow. Use **View Refunds** (and payment references) to confirm what has been refunded and when.

***

#### **5. Where do I see what the customer actually bought?**

Open the order using **Details** to see the itemized content (products/services) included in the extra order.

***

#### **6. I don’t see any Service Cases — does that mean there are none?**

Usually, yes. If your organization registers service cases in a separate workflow/tool, they will only appear here once they are created and linked to the booking (and if you have permission to view them).
