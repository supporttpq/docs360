# Conversation

### **Overview**

The **Conversation** (sometimes shown as **Conversation History**) tab displays the message log connected to the current booking. It helps you trace communication between a **guest** and your organization’s **Tourpaq users** (agents/support).

Use this tab when you need to:

* Review what was communicated with the guest earlier.
* Identify which user handled the dialog.
* Confirm timestamps, message content, and read status.

***

### **Purpose**

* Log and review booking-related conversations for service continuity.
* Provide an auditable history of communication (who said what and when).
* Support internal handover when multiple users work on the same booking.

***

### **Preconditions**

* A booking must exist.
* At least one message must have been exchanged for the booking.
* Messaging must be enabled for the relevant brand/setup (availability can vary by implementation).

{% hint style="info" %}
If this tab is empty, it usually means that no message thread exists for the booking yet, or that messaging is not enabled for the brand/channel used.
{% endhint %}

***

### **How to use this tab**

1. Open the relevant booking.
2. Go to **Conversation** / **Conversation History**.
3. Review the entries in chronological order.
4. Use the log to verify:
   * Who sent each message.
   * Whether/when it was read.
   * Which Tourpaq user was assigned to the incoming message (if applicable).

{% hint style="warning" %}
This tab is typically **read-only**. Messages are logged automatically and cannot be edited or deleted.
{% endhint %}

***

### **Field descriptions**

| Field         | Description                                                                                                                                                |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sent date** | Date/time when the message was sent.                                                                                                                       |
| **From**      | The sender of the message (guest or Tourpaq user).                                                                                                         |
| **Message**   | The message text/content.                                                                                                                                  |
| **Read day**  | Date/time when the recipient read the message. This can be empty if read receipts are not available for the channel or if the message has not been opened. |
| **Taken by**  | The Tourpaq user who received/was assigned the message (useful when routing is enabled and multiple users can handle the same booking).                    |
