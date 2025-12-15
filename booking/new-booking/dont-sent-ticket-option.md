# Don't sent ticket option

### **Overview**

The **“Don’t Send Ticket”** checkbox is a control on the booking page used to **suppress the automatic “Booking updated / Update booking” email** that can be triggered when you save changes on a confirmed booking.

This is useful when you need to make several internal adjustments and want to avoid sending multiple emails (often with ticket/documents) to the customer.

***

### **Purpose**

* Prevent customers from receiving multiple update emails while you work on a booking.
* Let agents control **when** the customer should be notified about changes.
* Useful for internal corrections (names, contact details), adding/removing extras, or batch updates.

***

### **Preconditions**

* The booking must be in **OK** status.
* You must make a change that would normally trigger a booking update email (for example: adding a product or changing booking-relevant details).
* You must have permission to edit the booking.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (6).png" alt=""><figcaption></figcaption></figure>

***

### **Field description**

| Field                 | Description                                                                                                                                                                                             |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Don’t Send Ticket** | When checked, the system will **not send the automatic booking update email** when you save the booking. The checkbox typically appears **only after you make a change** on a booking in **OK** status. |

***

### **Behavior & logic**

1. The checkbox is shown **only after a change is detected** on a booking in **OK** status.
2. If you **check** the box and then **Save**, the system suppresses the automatic **Booking updated / Update booking** email for that save.
3. If you **do not check** the box, the booking update email can be sent automatically (depending on your email configuration and what was changed).
4. After saving:
   * The checkbox is **reset**.
   * You must check it again for any later changes where you also want to suppress the update email.
5. This option **does not affect flight change emails** (those are handled separately and are sent as normal).

{% hint style="warning" %}
This setting is about **email sending**. It does **not** undo or prevent the booking changes themselves, and it does not “lock” ticket generation.
{% endhint %}

***

### **How to use**

1. Open a booking in **OK** status.
2. Make your changes.
3. When the **Don’t Send Ticket** checkbox appears, decide whether the customer should be notified right now.
4. If you do **not** want an automatic update email to be sent:
   * Check **Don’t Send Ticket**.
5. Click **Save**.

#### Verify what was sent

To confirm whether an email was sent for the booking, open the booking’s [**E‑mails**](e-mails.md) tab and review the log.

***

### **Use case example**

* You add a meal supplement to a confirmed booking, but you do **not** want the customer to receive an update email yet.
* You tick **Don’t Send Ticket** and click **Save**.
* The booking is updated, but the automatic update email is suppressed.
* Later, when everything is finalized, you can send the correct documents/ticket through your normal ticket/email workflow (for example via [**Print Tickets**](../../tickets/print-tickets.md), depending on your setup).

***

### **FAQ**

#### **1. What exactly is suppressed by “Don’t Send Ticket”?**

It suppresses the **automatic booking update email** (often named **Booking updated** or **Update booking**) that may be triggered when saving changes on an **OK** booking.

***

#### **2. Why does the checkbox only appear sometimes?**

Because it normally appears only when:

* The booking is already **OK**, **and**
* You made a change that the system recognizes as update‑relevant.

***

#### **3. Does it stop flight change emails?**

No. Flight change notifications are handled separately and are sent as normal.

***

#### **4. Does it stop me from printing or sending tickets manually?**

No. It only suppresses the **automatic update email** on save. Manual ticket sending/printing is separate (see [**Print Tickets**](../../tickets/print-tickets.md)).

***

#### **5. Does the checkbox stay enabled for future changes?**

No. It resets after you save. If you want to suppress emails again later, you must tick it again before saving.

***

#### **6. How can I confirm whether an email was sent or not?**

Open the booking’s [**E‑mails**](e-mails.md) tab and check the email log (type, sent date, and recipient address).
