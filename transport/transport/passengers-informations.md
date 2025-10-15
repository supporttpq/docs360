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

<table data-header-hidden><thead><tr><th width="310.25"></th><th></th></tr></thead><tbody><tr><td><strong>Field</strong></td><td><strong>Description</strong></td></tr><tr><td><strong>Stay From</strong></td><td>The start date of the hotel or travel stay period for which this information applies.<strong>Usage:</strong> Notes will only apply if the passenger’s stay begins on or after this date . </td></tr><tr><td><strong>Stay To</strong></td><td>The end date of the hotel or travel stay period for which this information applies.<strong>Usage:</strong> Ensures the message is only relevant until this date.                                     </td></tr><tr><td><strong>Booking Date From</strong></td><td>The earliest date when bookings must be made for the passenger’s information to apply. <strong>Usage:</strong> Prevents the rule from applying to earlier bookings.                  </td></tr><tr><td><strong>Booking Date To</strong></td><td>The latest date when bookings can be made for the information to apply. <strong>Usage:</strong> Ensures the rule is limited to a certain booking period.                                    </td></tr><tr><td><strong>Information</strong></td><td>The actual message or note that will be displayed or associated with the booking.<strong>Usage:</strong> Describes transport notes, errata, or booking conditions.                      <strong>Example</strong>: <code>Transport errata default</code></td></tr><tr><td><strong>Acknowledge</strong></td><td>Indicates whether this information must be confirmed (acknowledged) by the user or system.                    <strong>Values:</strong>                                                                                          ✅ <strong>Enabled</strong> → Acknowledgement required; ensures the message is seen.                                                                    ❌ <strong>Disabled</strong> → Acknowledgement not required.       <strong>Example:</strong> If enabled, the user must confirm having read the note before continuing. </td></tr><tr><td><strong>Edit / Delete</strong></td><td>Use the pencil icon ✏️ to edit or the trash icon 🗑️ to delete an entry.</td></tr></tbody></table>

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

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

The text from Passenger information will also be visible on the ticket:

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### **Notes**

* Different brands can have unique messages per transport and date range.
* The system ensures passengers see only messages relevant to their booking.
* You can define multiple records with overlapping or distinct date ranges for flexibility.
