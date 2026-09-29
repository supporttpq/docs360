---
description: >-
  Manage extra orders in Tourpaq Office bookings. Review post-booking add-ons
  like excursions, check payment confirmation, open order details, and handle
  refunds. Includes linked service cases.
---

# Extra Orders

<figure><img src="../../.gitbook/assets/image (372).png" alt="Extra Orders tab of a booking with three Extra Orders: one cancelled automatically by the service, one paid by guide payment and one created from WebBooking, and the Book button top right"><figcaption><p>Extra Orders tab. The Book button opens the list of excursions the booking can order.</p></figcaption></figure>

### **Overview**

The **Extra Orders** tab in **Tourpaq Office** shows **post-booking add-ons** and transactions connected to a booking (for example excursions, upgrades, and extra services). The same view also includes **Service Cases**, where you can review support cases linked to the booking.

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

* You must have access to the **Booking details** view and the **Extra Orders** tab.(Admin or Guide user type)
* At least one **extra order** or **service case** must exist for data to be shown.
* At least one guide must be assigned to the resort on the booking.
* The extra used for the extra order must have the resort on the booking assigned in the resource table.
* Refund handling requires that transactions are processed through an integrated **payment system** and that your user has the required permissions.
* The Extra is assigned to the brand of the booking with an option that includes **Guide sale** — see [Extras](../../extras-setup/extras-general-page/extras.md).
* The Extra uses **Manual** or **Generic** allotment, and has allotment on a date within the stay — see [Allotments](../../extras-setup/extras-general-page/allotments.md).

***

### **Instructions**

#### **Viewing and managing Extra Orders**

1. Open the relevant booking.
2. Go to the **Extra Orders** tab.
3. Review the list:
   * Each row represents a single **extra order**.
4. Use **Details** to view the itemized contents of the order.
5. Use **View Refunds** to review existing refunds or initiate a refund (if available).
6. Click **Book** to order an excursion for the booking. The **Search Extra Orders** window lists every excursion with allotment during the stay, with **Allotment Date**, **Name**, **Allotments** (booked / total), **Adult Price**, **Child Price** and **Currency**. Click **Book** on a line to order it. Excursions with **Manual** and **Generic** allotment are both listed.

<figure><img src="../../.gitbook/assets/image (368).png" alt="Search Extra Orders window listing excursions by allotment date with booked and total allotment, adult and child prices in DKK and a Book button per line"><figcaption><p>Search Extra Orders window. The Book button on each line orders that excursion.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (309).png" alt="Extra order details view showing itemized products and amounts"><figcaption></figcaption></figure>

{% hint style="info" %}
If you cannot see **Book** or **View Refunds**, it usually means either (1) your user role does not have permission, or (2) the selected payment method/provider does not support the action from this view.
{% endhint %}

{% hint style="danger" %}
**TO VERIFY** — On staging (29-09-2026) the Manual allotment Extra `Udflugt - manual allotment JJR`, which has allotment on 12-10-2026 and 15-10-2026, was not listed in **Search Extra Orders** for bookings 200205125 and 200202985 (stay 10-10-2026 to 17-10-2026), although the ticket names these bookings as eligible. The list also contained excursions from several islands. Confirm the eligibility rules (resort filter, already ordered, brand) before publishing step 6.
{% endhint %}

{% hint style="info" %}
An Extra Order created from WebBooking before departure is paid with the booking. It shows no **PAYMENT ORDER ID** or **METHOD** on this tab, and **ROOM NO.** shows `Not reserved yet`. If it is cancelled, the amount appears as a negative balance in [Balance Administration](../../balance-administration.md) rather than as a refund.
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
