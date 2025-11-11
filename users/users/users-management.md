# Users Management

## **Users Dashboard – User Management**

### **Overview / Purpose**

The **Users dashboard** provides a centralized view of all users within the agency or company. It enables administrators to manage user roles, permissions, login activity, and overall system access. This ensures secure and efficient control over who can perform specific actions in Tourpaq.

### **How It Works**

* All registered users are displayed in a **user table** with key information (username, role, company, last login, etc.).
* Administrators can **search, filter, sort, and edit** users directly from this interface.
* Actions like creating new users, blocking/unblocking, or assigning permissions are managed from the same page.
* User access can be restricted temporarily (blocked) or permanently (deleted), depending on business and security needs.

<figure><img src="../../.gitbook/assets/image (334).png" alt=""><figcaption></figcaption></figure>

### **User Table Fields**

| **Field**             | **Description**                                                                |
| --------------------- | ------------------------------------------------------------------------------ |
| **Username**          | Unique identifier used by the user to log in.                                  |
| **First Name**        | First name of the user.                                                        |
| **Last Name**         | Last name of the user.                                                         |
| **Seller Signature**  | Internal seller code or identifier.                                            |
| **Company**           | Associated company name or identifier.                                         |
| **Role**              | Specifies user role (e.g., Guide, Administrator, Support, Sales, etc.).        |
| **Rights**            | Permissions granted to the user (e.g., view, edit, delete specific resources). |
| **Brands**            | Brands the user is affiliated with                                             |
| **Last Login**        | Timestamp of the user's most recent login.                                     |
| **User Blocked**      | Checkbox indicating if the user is blocked.                                    |
| **Actions**           | Icons to delete the user profile.                                              |

### **Key Features / Functions**

#### **View All Users**

* See a full list of active, inactive, or hidden users.
* Each entry shows: username, full name, role, company, signature, permissions, and last login.

#### **Search & Filter Users**

* Search by: username, first name, last name, signature, or role.
* Toggle visibility for inactive or hidden users.
* Apply filters to narrow down results quickly.

#### **Sort Columns** ↕&#x20;

* Reorder the user list by clicking on column headers (e.g., sort by **Username** or **Last Login**).

#### **Create New User**

* Add a new user with customized settings:
  * Name and signature
  * Role assignment
  * Company or agency association
  * Brand access
  * Rights and permissions

#### **Edit User Details**

* Update user information such as name, role, rights, or company.
* Change brand access or signatures.
* Adjust block/unblock status.

#### **Assign / Modify Permissions**

* Grant or revoke access to specific actions (e.g., edit bookings, view payments, overbook transports).

#### **Delete User** 🗑️

* Permanently remove a user (only possible if no dependent bookings or financial records exist).

#### **Block / User** 🚫&#x20;

* Blocked users remain in the system but cannot log in.
* Useful for temporary suspensions or seasonal employees.

#### **View Login Activity**

* Track the **Last Login** field to monitor user activity and troubleshoot access issues.

#### **Pagination**

* Navigate across multiple pages of users when the list is large.

***

### **Examples or Scenarios**

* An **administrator** creates a new sales agent user, assigns them to a specific agency, and grants booking rights.
* A **seasonal guide** finishes their contract, so the admin **blocks** their user account instead of deleting it.
* A **financial manager** reviews the login history to check whether a team member accessed the system recently.
* An **IT administrator** filters users by role to verify which accounts still have **administrator rights**.

***

### **Notes / Best Practices**

* Always **assign the lowest necessary permissions** to reduce security risks.
* Use **block/unblock** instead of deletion when a user may return later.
* Regularly review **Last Login** data to identify inactive accounts and maintain system hygiene.
* Deletion should only be used if the user has no linked bookings or financial records.
* Consider role-based filtering to quickly audit which users have high-level access (Administrator, Financial, Super Admin).
