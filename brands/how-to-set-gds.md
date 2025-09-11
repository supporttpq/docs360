# How to set GDS

### **Overview / Purpose**

GDS (Global Distribution System) settings allow administrators to configure **status-related messages** that appear on tickets and to passengers. This ensures passengers receive clear instructions based on their booking status from the GDS provider.

***

### **How It Works**

* Administrators enter text messages that will appear on tickets and customer communications.
* Texts can be **status-specific**, depending on the booking’s GDS status.
* The system automatically displays the correct text to passengers and on tickets according to the current booking status.

<figure><img src="../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Key Features / Functions**

#### **Text to Add on Ticket**

* Enter any message in the **Text to add on ticket** box.
* This text appears at the bottom of the **“Betalingplan”** section on the ticket.
* To make the text **bold** on the ticket, check the corresponding **Bold** checkbox.

#### **Status-Specific Messages**

* **Galileo Pending**: Text shown when the booking is pending. Passengers see this message while waiting for confirmation.
* **HK (Hold & Confirm)**: Message shown when the booking is held and waiting for confirmation.
* **TKQ (Ticket Queue)**: Text shown when the booking is in the ticket queue.
* **TKOK (Ticket OK)**: Message shown once the ticket is successfully issued.

#### **Save Settings**

* Click **Save GDS** to apply all changes.

***

### **Examples / Scenarios**

1. **Pending Booking**
   * Text: “Your booking is pending. We will confirm your seat shortly.”
   * Passengers see this message until the booking moves to HK or TKOK status.
2. **Ticket Issued (TKOK)**
   * Text: “Your ticket has been issued. Please check your email for the PDF ticket.”
   * Appears automatically once the ticket is finalized.
3. **Bold Ticket Text**
   * Important notes or warnings can be emphasized by selecting the **Bold** option for ticket text.

***

### **Notes / Best Practices**

* Ensure messages are **clear and concise** so passengers understand their booking status.
* Use **bold text** sparingly to highlight critical instructions.
* Review and update GDS messages regularly to match operational procedures and provider requirements.
* Test the messages on sample tickets to confirm they display correctly for all statuses.
