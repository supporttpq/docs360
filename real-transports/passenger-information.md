# Passenger Information

### **Overview**

The **Passenger Information** tab allows you to define messages or information that will be shown to passengers associated with a specific transport.\
This information can include travel instructions, airport details, or destination-specific notes. It can be configured per **brand**, **transport**, and **date range**.

***

### **Purpose**

Use this feature to:

* Display important travel notes or reminders for passengers on selected transports.
* Provide specific instructions valid for certain travel or booking periods.
* Ensure passengers receive accurate and updated information through the booking system or communication channels.

***

### **How to Access**

Go to:\
**Transport → \[Select Transport] → Passenger Information**

***

### **Tabs**

At the top, you can switch between different **brands.**\
Each brand can have its own passenger information messages and settings.

***

### **Fields Description**

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

| **Field**                  | **Description**                                                                                                                                                    |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Stay From / Stay To**    | Defines the date range for passenger stay. The message will apply only to passengers staying within this period.                                                   |
| **Booking Date From / To** | Defines the date range for when the booking was made. Only bookings created in this range will receive the message.                                                |
| **Information**            | The message text that will be shown to passengers. Example: _“Please arrive at the airport 2 hours before departure.”_                                             |
| **Acknowledge**            | Indicates whether the passenger must acknowledge or confirm they have read the information. When enabled (✔), the system requires confirmation from the passenger. |
| **Edit / Delete**          | Use the pencil icon ✏️ to edit or the trash icon 🗑️ to delete an entry.                                                                                           |

***

### **Buttons**

| **Button**        | **Action**                                                                                                                      |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Create**        | Opens a form to add a new passenger information entry. You can define the date ranges, message, and acknowledgment requirement. |
| **Save / Update** | Saves changes to the selected brand and transport.                                                                              |

***

### **Example**

For the transport **CPH–CHQ–RC7134**, a passenger message was created with the following details:

| **Field**         | **Value**           |
| ----------------- | ------------------- |
| Stay From         | 03-10-2025          |
| Stay To           | 31-10-2025          |
| Booking Date From | 03-10-2025          |
| Booking Date To   | 31-10-2025          |
| Information       | Test passenger info |
| Acknowledge       | Enabled ✔           |

This means all passengers traveling on this route between **3 October 2025 – 31 October 2025**, whose bookings were created in the same period, will receive the message _“Test passenger info.”_

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

The text from Passenger information will also be visible on the ticket:

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

***

### **Notes**

* Different brands can have unique messages per transport and date range.
* The system ensures passengers see only messages relevant to their booking.
* You can define multiple records with overlapping or distinct date ranges for flexibility.
