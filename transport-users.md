# Transport Users

### **Overview**

The **Transport Users** page displays a list of users who are assigned to manage or interact with specific transports within the system. Each entry links a user account to one or more transport codes and, when applicable, an airline. This page is typically used by administrators to review, add, or update which users are associated with transport operations.

***

### **Purpose**

* To provide a centralized overview of all users involved in transport handling.
* To show which transport codes are assigned to each user.
* To identify airline-specific associations.
* To allow administrators to create or manage transport user assignments.

***

### **Page Structure & Fields**

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

#### **Table Columns**

| **Column**     | **Description**                                                                                                                                                                   |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**       | The display name assigned to the transport user. In many cases, the system may anonymize this for data protection (e.g., "Anonymized User").                                      |
| **User**       | The username linked to the transport user. This represents the actual system account (e.g., _suto_, _jeti_, _rowebtransport_).                                                    |
| **Transports** | A list of transport codes assigned to the user. Users may be associated with one or multiple transport identifiers. Each code represents a specific transport route or operation. |
| **Airline**    | The airline associated with the user, if applicable (e.g., _Airseven_). Some users may not have an airline assigned.                                                              |

### **Actions**

#### **Create Button**

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

* Located in the top-right corner.
* Opens a form to **add a new Transport User**.
* Enables assigning:
  * User name
  * Email
  * Transport codes
  * Airline (optional)

***

### **Usage Instructions**

1. **View Existing Users**
   * Browse the list to see all registered transport users, their usernames, and assigned transports.
2. **Check Transport Assignments**
   * Under the _Transports_ column, expand the list of codes to verify which routes or operations each user handles.
3. **Identify Airline-Specific Users**
   * Look under the _Airline_ column to find users tied to a particular airline.
4. **Create a New Transport User**
   * Click **Create** → Fill in user details → Assign transports → Save.
5. **Pagination & Display Options**
   * Use the controls at the bottom:
     * Page selector
     * Items per page (e.g., _25/page_)

***

### **Tips**

* Ensure that each transport operation has an assigned responsible user to maintain correct operational workflow.
* Use consistent naming conventions for easier auditing.
* Review transport-user assignments periodically—especially when staff, routes, or airlines change.
