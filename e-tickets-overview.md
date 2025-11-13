# E-tickets Overview

This page provides an overview of the electronic tickets (E-Tickets) generated and sent to customers. It allows monitoring the status of emails sent with electronic tickets and managing any errors.

<figure><img src=".gitbook/assets/image (163).png" alt=""><figcaption></figcaption></figure>

### Main elements of the page

#### **a) Search filters**

The user can filter the displayed tickets using the following options:

* **Booking number** – Allows searching by booking number.
* **Email** – Allows filtering by customer email address.
* **Sent from / Sent to** – Filters tickets by the time interval in which they were sent.
* **+ More filters** – Possibility to add additional filters.
  * To use filter "Show only communication email types" you must select "All Brands"
* **Clear** – Clears all active filters.
* **Export** – Button that allows downloading the list of tickets in a compatible format (e.g., Excel, CSV).

#### **b)** Main Table – E-Ticket List

The table displays essential details about each ticket submitted, including the following columns:

| Coloana            | Descriere                                                                       |
| ------------------ | ------------------------------------------------------------------------------- |
| **Departure**      | Departure date associated with the ticket.                                      |
| **Transport**      | Transport Code of the means of transport used.                                  |
| **Booking Number** | Number of the reservation associated with the ticket.                           |
| **Email Type**     | Type of email sent (e.g. confirmation, cancellation, update, payment reminder). |
| **Customer Name**  | Name of the customer who made the reservation.                                  |
| **Telephone**      | Customer's telephone number.                                                    |
| **Email Address**  | Email address where the ticket was sent.                                        |
| **Sent Date**      | Date and time the email was sent.                                               |
| **Opened**         | Indicates whether the email was opened by the customer.                         |
| **Confirmed**      | Confirms whether the ticket was processed correctly.                            |
| **Failed Status**  | Displays any sending errors.                                                    |
| **Status**         | Final status of the email (e.g. "sent", "failed").                              |

### **Workflow**

1. Monitoring sent e-tickets
   * Users can quickly see which tickets have been sent and their status.
   * Specific tickets can be searched for using the available filters.
2. Identifying and handling issues
   * If an email has a "failed" status, you can check the email address and resend it manually.
   * If a customer did not receive the email, you can check whether it was opened and acknowledged.
3. Exporting and Reporting
   * The list of tickets can be exported for analysis or archiving.

### **Possible problems and solutions**

| Issue                        | Possible cause                                     | Solution                                            |
| ---------------------------- | -------------------------------------------------- | --------------------------------------------------- |
| The email was not opened.    | The customer has not checked it out yet.           | Contacting the customer for confirmation            |
| "failed" status when sending | Invalid email address or technical problem         | Checking and correcting the address, then resending |
| Email is not confirmed.      | The customer did not complete the required action. | Sending a reminder or contacting the customer       |

