# System Setup – SMS Configuration (Twilio)

### **Overview**

The **SMS Configuration** section manages the integration between Tourpaq and Twilio, enabling the system to send automated SMS notifications to customers and staff.

### **Purpose**

* Provide real-time communication via SMS.
* Automate notifications such as booking confirmations, reminders, and alerts.
* Ensure reliable delivery using Twilio’s messaging platform.

### **Configuration Fields**

| **Field**                 | **Description**                                                               |
| ------------------------- | ----------------------------------------------------------------------------- |
| **Twilio Account Number** | The account SID provided by Twilio for authentication.                        |
| **Twilio Account Token**  | The authentication token for the Twilio account.                              |
| **Twilio Phone Number**   | The phone number registered with Twilio (in E.164 format) used as the sender. |

### **Usage Notes**

* Ensure all fields are correctly entered to enable SMS functionality.
* SMS notifications will not work if any credentials are missing or incorrect.
* Use valid E.164 format for the phone number to avoid delivery errors.
