# SMS

### **Overview**

The **SMS** tab provides a log of all SMS messages sent to the customer in relation to the booking. It allows team members to track communication history, confirm that messages were sent, and review the exact text that the customer received.

***

### **Purpose**

* Track all SMS notifications associated with a booking.
* Verify that messages were sent successfully and to the correct phone number.
* Review the full content of each SMS sent to the customer.

***

### **Preconditions**

* The booking must have at least one valid customer phone number.
* SMS messages must have been triggered by system processes or manual actions (for example, booking confirmations, reminders).

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Instructions**

1. **Open the SMS tab**
   * Open the booking you want to review.
   * Click the **SMS** tab.
2. **Review the SMS log**
   * SMS messages are listed **chronologically**, with the most recent message at the top.
   *   For each SMS entry, the following information is displayed:

       | **Field**            | **Description**                                                |
       | -------------------- | -------------------------------------------------------------- |
       | **Send Date & Hour** | The exact timestamp when the SMS was sent.                     |
       | **Company**          | The company or brand that initiated the message.               |
       | **Phone Number**     | The recipient’s phone number.                                  |
       | **Message**          | The full text content of the SMS that was sent.                |
       | **Status**           | Indicates whether the message was successfully sent or failed. |

#### **Important**

* This tab is **view-only** – SMS messages **cannot be edited or deleted** from here.
* If a message has **Status = failed** (or similar), follow your internal procedure to investigate (for example, checking the phone number, SMS configuration, or contacting support).

***

### **FAQ**

#### **Why do I not see any SMS for this booking?**

Common reasons:

* No SMS has been triggered yet for this booking (for example, confirmations or reminders are not configured or have not been sent).
* The customer’s **phone number** is missing or invalid.
* SMS sending may be disabled or not configured for the selected **brand** or environment.

If you expect SMS to appear and the list is empty, check the booking’s phone details and your SMS setup, or contact your system administrator.

***

#### **Can I send a new SMS directly from this tab?**

No. The **SMS** tab is only a **log** of messages that have already been sent. To send new SMS messages, use the tools and workflows configured in your organisation (for example, dedicated SMS modules, automated flows, or communication centers), according to your internal guidelines.

***

#### **What does the Status field mean in practice?**

* A **successful** status means the SMS was handed over to the SMS provider without errors.
* A **failed** status indicates that the system or provider could not send the message.

For failed messages, verify the recipient’s phone number and consult your internal support or SMS provider monitoring if repeated errors occur.

***

#### **Can I change the content of SMS templates from here?**

No. The **Message** column only shows what was already sent for this booking. To change the **template text** used for future SMS messages, you must update the relevant SMS or email/SMS configuration pages in your setup (if you have access), or ask an administrator to do it.
