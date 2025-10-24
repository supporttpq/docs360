# Offers

### **Overview**

The **Offers** page provides an overview of all customer offers created in the system.\
Each offer represents a proposed travel package that can be sent to a customer, followed up, or converted into a confirmed booking.

The page allows users to:

* Filter, view, and manage existing offers
* Track offer status and follow-up actions
* Create new offers

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

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

#### **Filters and Search Fields**

| **Field**                                     | **Description**                                                                                   |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| **First name / Last name**                    | Search for offers by the customer’s first and/or last name.                                       |
| **Email**                                     | Filter offers by the customer’s email address.                                                    |
| **Created period (From / To)**                | Define a date range to display offers created within a specific time period.                      |
| **Status**                                    | Filters by offer status (e.g., _Unsent_, _Available_,  _Expired_, _Sold, Closed_).                |
| **Close reason**                              | Filters offer based on why they were closed                                                       |
| **Follow-up start date / Follow-up end date** | Filters offer based on the follow-up period scheduled for the customer.                           |
| **Customer type**                             | Filters based on customer type (e.g., _Customer_, _None, Ofertee_).                               |
| **Offer no**                                  | Search for a specific offer using its unique Offer Number.                                        |
| **Departure date / Arrival date**             | Filters offers according to the travel dates proposed in the offer.                               |
| **Create user**                               | Filters by the user who created the offer.                                                        |
| **Hotel**                                     | Filters offers by hotel name included in the proposal.                                            |
| **Display names**                             | Toggles between showing internal system names.                                                    |
| **Display / Clear**                           | **Display** applies the selected filters, while **Clear** resets all filters to show all results. |
| **More filters**                              | Expands additional filtering options for detailed search.                                         |

***

#### **Main Table Columns**

| **Column**           | **Description**                                                                                                                                                                                                                                                                   |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Offer No**         | Unique identifier automatically generated for each offer. Clickable to open the offer details.                                                                                                                                                                                    |
| **Brand**            | Indicates the brand under which the offer was created (e.g., _Tourpaq DK_).                                                                                                                                                                                                       |
| **Type**             | Defines who the offer is made for — usually _Customer_ or _Offertee_.                                                                                                                                                                                                             |
| **Customer/Offeree** | Displays the name of the customer or contact person receiving the offer.                                                                                                                                                                                                          |
| **Create User**      | The system user who created the offer.                                                                                                                                                                                                                                            |
| **Create Date**      | The date the offer was initially created.                                                                                                                                                                                                                                         |
| **Update User**      | The last user who modified the offer.                                                                                                                                                                                                                                             |
| **Update Date**      | The last date the offer was updated.                                                                                                                                                                                                                                              |
| **Follow-up Date**   | The scheduled date for the next follow-up with the customer.                                                                                                                                                                                                                      |
| **Status**           | <p>Current status of the offer. Common values: </p><ul><li><em>Unsent</em>: Offer was created but not yet sent to the customer.</li><li><em>Expired</em>: Offer validity period has ended.</li><li><em>Sold</em>: Offer has been accepted and converted into a booking.</li></ul> |
| **Status Details**   | Additional notes on the offer’s state, such as _Not sent to customer_ or _Expired on \[date]_. \|                                                                                                                                                                                 |
| **Internal Comment** | Free-text field for internal notes visible only to office users.                                                                                                                                                                                                                  |
| 🗑️ (Delete icon)    | Deletes the selected offer from the list (if user permissions allow)                                                                                                                                                                                                              |

#### **Actions**

| **Action**                     | **Description**                                                                                              |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| **Create**                     | Opens the “New Offer” form where users can define travel details, customer information, and pricing.         |
| **Offers / Statistics toggle** | Switch between the list of offers and aggregated statistics (e.g., number of offers sent, conversion rates). |

***

#### **Typical Workflow**

1. **Create** a new offer.
2. **Send** it to the customer.
3. **Follow up** using the scheduled follow-up date.
4. If accepted, **convert the offer to a booking** (status becomes _Sold_).
