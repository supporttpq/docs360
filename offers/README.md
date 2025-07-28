# Offers

### **Overview**

The **Offers** page is a central hub for managing both offer proposals and incoming customer travel requests. It enables sales and support staff to efficiently track, organize, and act upon offers based on various filtering and status criteria.

***

### **Purpose**

To provide a flexible and organized view of all travel-related offers, allowing:

* Fast retrieval based on customer or travel data.
* Status tracking and follow-up scheduling.
* Internal collaboration via offer comments and updates.

***

### **Preconditions**

* User must have access to the **Offers** module in Tourpaq Office.
* Offers must be created either manually by an agent or through integrated customer interactions.
* Customer and travel data should be available in the system for accurate filtering.

<figure><img src="../.gitbook/assets/image (266).png" alt=""><figcaption></figcaption></figure>

### **Search Filters**

The filter panel allows users to refine the view using multiple criteria:

| **Filter Field**                     | **Description**                                                                 |
| ------------------------------------ | ------------------------------------------------------------------------------- |
| First Name / Last Name / Email       | Search for offers associated with specific customer data.                       |
| **Status**                           | Filter offers based on lifecycle state (e.g., _Available_, _Unsent_, _Closed_). |
| **Close Reason**                     | Choose from predefined reasons why an offer was closed.                         |
| **Follow-up Start/End Date**         | Search offers with follow-up actions within a date range.                       |
| **Customer Type**                    | Identify offers by the type of customer (e.g., _New_, _Returning_).             |
| **Offer No.**                        | Locate a specific offer using its unique ID.                                    |
| **Departure Date / Arrival / Hotel** | Search offers based on planned trip details.                                    |

***

### **Offers Table**

Displays a real-time list of all offers matching selected filters. Each row contains:

| **Field**              | **Description**                                              |
| ---------------------- | ------------------------------------------------------------ |
| **Offer No.**          | Unique identifier for the offer.                             |
| **Brand**              | Tour company or brand managing the offer.                    |
| **Type**               | Indicates whether it’s a customer request or offer proposal. |
| **Customer / Offeree** | Name of the customer the offer is addressed to.              |
| **Create User**        | The system user who created the offer.                       |
| **Create Date**        | Date and time the offer was initially saved.                 |
| **Update User**        | The user who last modified the offer.                        |
| **Update Date**        | Date and time of the last update.                            |
| **Follow-up Date**     | When a follow-up should occur.                               |
| **Status**             | Current state of the offer (e.g., _Available_, _Not Sent_).  |
| **Status Details**     | Additional information such as “Available until DD.MM.YYYY.” |
| **Internal Comment**   | Internal notes for tracking offer reasoning or next steps.   |

### **Related Workflows**

| **Workflow**                    | **Description**                                                                       |
| ------------------------------- | ------------------------------------------------------------------------------------- |
| **Creating a New Offer**        | Navigate to the Offer menu > Click "Create Offer" > Fill in customer and travel data. |
| **Follow-Up Management**        | Set or adjust follow-up dates directly from the offer or the table view.              |
| **Sending Offers to Customers** | Offers marked as “Not Sent” can be sent via email directly from the Offer view.       |
| **Closing an Offer**            | Select a close reason and status manually when an offer is no longer active.          |
| **Offer Conversion**            | Convert an active offer into a booking once accepted by the customer.                 |
