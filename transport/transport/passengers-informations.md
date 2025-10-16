# Passengers informations

### **Overview**

The **Passenger Information** section is used to define informational notes or errata that apply to bookings for specific stay periods. These messages typically provide additional details for customers or internal staff (**e.g., special conditions, restrictions, or exceptions**).

### **Purpose**

* To communicate relevant information related to bookings and stays (e.g., transport notes, exceptions, overlapping rules).
* To ensure passengers and staff are aware of important details connected to their travel.
* To manage conditions within specific booking and stay periods.

### **Tabs**

At the top, you can switch between different **brands.**\
Each brand can have its own passenger information messages and settings.

### **Fields Explanation**

<figure><img src="../../.gitbook/assets/image (399).png" alt=""><figcaption></figcaption></figure>

<table data-header-hidden><thead><tr><th width="310.25"></th><th></th></tr></thead><tbody><tr><td><strong>Field</strong></td><td><strong>Description</strong></td></tr><tr><td><strong>Stay From / Stay To</strong></td><td>Defines the date range for passenger stay. The message will apply only to passengers staying within this period.</td></tr><tr><td><strong>Booking Date From / To</strong></td><td>Defines the date range for when the booking was made. Only bookings created in this range will receive the message.              </td></tr><tr><td><strong>Information</strong></td><td>The message text that will be shown to passengers. Example: <em>“Please arrive at the airport 2 hours before departure.”</em></td></tr><tr><td><strong>Acknowledge</strong></td><td>Indicates whether the passenger must acknowledge or confirm they have read the information. When enabled (✔), the system requires confirmation from the passenger.</td></tr><tr><td><strong>Edit / Delete</strong></td><td>Use the pencil icon ✏️ to edit or the trash icon 🗑️ to delete an entry.</td></tr></tbody></table>

### **Buttons**

| <p><br><strong>Button</strong></p> | **Action**                                                                                                                      |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Create**                         | Opens a form to add a new passenger information entry. You can define the date ranges, message, and acknowledgment requirement. |
| **Save / Update**                  | Saves changes to the selected brand and transport.                                                                              |

### **Example**

For the transport **BLLCHQ-M1**, a passenger message was created with the following details:

| **Field**         | **Value**               |
| ----------------- | ----------------------- |
| Stay From         | 20-10-2025              |
| Stay To           | 31-10-2025              |
| Booking Date From | 01-10-2025              |
| Booking Date To   | 19-10-2025              |
| Information       | Transport Erata Default |
| Acknowledge       | Enabled ✔               |

This means all passengers traveling on this route between **20 October 2025 - 31 October 2025**, whose bookings were created in the same period, will receive the message _“Transport Erata Default.”_

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

The text from Passenger information will also be visible on the ticket:

<figure><img src="../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Notes**

* Different brands can have unique messages per transport and date range.
* The system ensures passengers see only messages relevant to their booking.
* You can define multiple records with overlapping or distinct date ranges for flexibility.
