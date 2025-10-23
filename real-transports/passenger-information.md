# Passenger Information

### **Overview**

The **Passenger Information** section is used to define informational notes or errata that apply to bookings within specific stay periods.\
These messages typically provide additional details for customers or internal staff — for example, **special conditions, restrictions, or exceptions** related to a booking.

### **Purpose**

* To communicate relevant information connected to bookings and stays (e.g., transport notes, exceptions, overlapping rules).
* To ensure both passengers and staff are informed about important travel details.
* To manage special conditions or exceptions within defined booking and stay periods.

The behavior and purpose of **Passenger Information for Real Transports** are similar to those used in **Charter Transports**.

### **Tabs**

At the top, you can switch between different **brands.**\
Each brand can have its own passenger information messages and settings.

### **Fields Description**

<figure><img src="../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The text from Passenger information will also be visible on the ticket:

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### **Notes**

* Different brands can have unique messages per transport and date range.
* The system ensures passengers see only messages relevant to their booking.
* You can define multiple records with overlapping or distinct date ranges for flexibility.
