# E-tickets Overview

### **Overview**

The **E-Tickets Overview** page provides a complete summary of all e-ticket emails that have been generated and sent to customers.\
It allows operational staff and customer service teams to easily:

* search for specific bookings
* check whether a ticket was sent
* view open/failed/successful deliveries
* re-send or review e-mails
* diagnose issues before departure

This module is essential for ensuring that all travelers receive their flight tickets on time.

***

### **Purpose**

The page is designed to:

* give teams **full visibility** over all e-ticket communication
* provide **quick search tools** for finding customers who did not receive their ticket
* display **delivery tracking**: sent, opened, confirmed, failed
* allow filtering by **transport**, **email type**, **date**, **status**, or **customer information**
* allow export for audits or operational follow-ups

It centralizes all communication around e-tickets into a single page.

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## **Filters**

The filter section allows you to narrow down the list of emails.

#### **Available Filters**

| Filter                                  | Description                                                                          |
| --------------------------------------- | ------------------------------------------------------------------------------------ |
| **Booking number**                      | Search for a specific booking number                                                 |
| **Email**                               | Search by customer email address                                                     |
| **Sent from / Sent to**                 | Filter based on the date the e-ticket was sent                                       |
| **Transport**                           | Filter by specific transport code(s)                                                 |
| **Departure from / Departure to**       | Filter by passenger departure date                                                   |
| **Email Type**                          | Choose the type of e-ticket email (e.g., Thank you for booking, Ticket confirmation) |
| **Status**                              | Filter by status: Sent, Opened, Failed, Confirmed, Not Sent                          |
| **Hide Confirmed**                      | Hide entries where the customer has already confirmed reading                        |
| **Show only communication email types** | Shows only e-ticket communication templates                                          |

All filters can be used simultaneously.

#### **Display / More Filters**

The **Display** button shows/hides additional advanced filter fields.\
**Clear** resets all filters.

***

## **Table Overview**

Each row represents one e-ticket email sent to a customer.

| Column             | Description                                                 |
| ------------------ | ----------------------------------------------------------- |
| **Departure**      | The passenger’s departure date                              |
| **Transport**      | Transport code (airline + routing)                          |
| **Booking Number** | Booking reference number                                    |
| **Email Type**     | Template used for this ticket (e.g., Thank you for booking) |
| **Customer Name**  | Passenger name on the booking                               |
| **Telephone**      | Customer phone number                                       |
| **Email Address**  | Destination email                                           |
| **Sent Date**      | When the email was sent                                     |
| **Opened**         | Timestamp when customer opened the email                    |
| **Confirmed**      | Confirmation received (if confirmation is required)         |
| **Failed Status**  | If sending failed, the reason is displayed                  |
| **Status**         | Overall status (sent, failed, not sent, opened…)            |

***

## **Opening an E-Ticket (Preview)**

Click on **any row** to open a preview of the actual e-ticket email that was sent.

This is useful for:

* customer support calls
* checking if information was correct
* verifying branding or attachments
* confirming content before re-sending

***

## **Export**

In the top-right corner, the **Export** button allows you to download the entire filtered list in Excel format.

Useful for:

* documenting delivery issues
* auditing communication logs
* mass-checks before departure days
* sharing with airline or support teams

***

## **Summary**

The **E-Tickets Overview** provides:

* full visibility of all customer ticket emails
* powerful filtering for operational checks
* delivery tracking (sent/opened/failed)
* email previews for troubleshooting
* export for reporting and audit

It is an essential tool for customer service and departure operations.

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

