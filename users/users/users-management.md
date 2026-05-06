# Users Management

## **Users Dashboard – User Management**

### **Overview / Purpose**

The **Users dashboard** provides a centralized view of all users within the agency or company. It enables administrators to manage user roles, permissions, login activity, and overall system access. This ensures secure and efficient control over who can perform specific actions in Tourpaq.

### **How It Works**

* All registered users are displayed in a **user table** with key information (username, role, company, last login, etc.).
* Administrators can **search, filter, sort, and edit** users directly from this interface.
* Actions like creating new users, blocking/unblocking, or assigning permissions are managed from the same page.
* User access can be restricted temporarily (blocked) or permanently (deleted), depending on business and security needs.

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Field Description – Filters (Top Section)

<figure><img src="../../.gitbook/assets/users filters.png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="172.75">Field Name</th><th width="275.75">Description</th><th>Notes / System Impact</th></tr></thead><tbody><tr><td>Username</td><td>Filter by username</td><td>Supports search and dropdown selection</td></tr><tr><td>First name</td><td>Filter by first name</td><td>Free text search</td></tr><tr><td>Last name</td><td>Filter by last name</td><td>Free text search</td></tr><tr><td>Signature</td><td>Filter by seller signature</td><td>Used for identifying booking ownership. Represents the Seller ID in the booking. It is defined when a user is created and is used in <strong>All Bookings</strong> in the <strong>Owne</strong>r filter ((show code checkbox must be checked) </td></tr><tr><td>Role</td><td>Filter by user role</td><td>Useful for role-based audits</td></tr><tr><td>Show hidden</td><td>Include hidden users in results</td><td>Shows inactive/hidden users. For a user to have hidden status, and no longer appear across the system, the status must be set to Hidden in Edit User.</td></tr><tr><td>Display</td><td>Applies filters</td><td>Refreshes the list</td></tr><tr><td>Clear</td><td>Resets filters</td><td>Clears all filter inputs</td></tr><tr><td>Create</td><td>Creates a new user</td><td>Opens <strong>Create User</strong> page</td></tr></tbody></table>

### **User Table Fields**

| **Field**            | **Description**                                                                                 |
| -------------------- | ----------------------------------------------------------------------------------------------- |
| **Username**         | Unique identifier used by the user to log in.                                                   |
| **First Name**       | First name of the user.                                                                         |
| **Last Name**        | Last name of the user.                                                                          |
| **Seller Signature** | Internal seller code or identifier. It is defined in **Edit User** as **Seller ID in booking.** |
| **Company**          | Associated company name or identifier.                                                          |
| **Role**             | Specifies user role (e.g., Guide Teams, Administrator, Support, Sales, etc.).                   |
| **Rights**           | Permissions granted to the user (e.g., view, edit, delete specific resources).                  |
| **Brands**           | Brands the user is affiliated with                                                              |
| **Last Login**       | Timestamp of the user's most recent login.                                                      |
| **User Blocked**     | Checkbox indicating if the user is blocked.                                                     |
| **Actions**          | Icons to delete the user profile.                                                               |

### **Key Features / Functions**

#### **View All Users**

* See a full list of active, inactive, or hidden users.
* Each entry shows: username, full name, role, company, signature, permissions, and last login.

#### **Search & Filter Users**

* Search by: username, first name, last name, signature, or role.
* Toggle visibility for inactive or hidden users.
* Apply filters to narrow down results quickly.

#### **Sort Columns** ↕

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

#### **Block / User** 🚫

* Blocked users remain in the system but cannot log in.
* Useful for temporary suspensions or seasonal employees.

#### **View Login Activity**

* Track the **Last Login** field to monitor user activity and troubleshoot access issues.

#### **Pagination**

* Navigate across multiple pages of users when the list is large.

***

### **Examples or Scenarios**

* An **administrator** creates a new sales agent user, assigns them to a specific agency, and grants booking rights.
* A **seasonal guide team** finishes their contract, so the admin **blocks** their user account instead of deleting it.
* A **financial manager** reviews the login history to check whether a team member accessed the system recently.
* An **IT administrator** filters users by role to verify which accounts still have **administrator rights**.

***

### **Notes / Best Practices**

* Always **assign the lowest necessary permissions** to reduce security risks.
* Use **block/unblock** instead of deletion when a user may return later.
* Regularly review **Last Login** data to identify inactive accounts and maintain system hygiene.
* Deletion should only be used if the user has no linked bookings or financial records.
* Consider role-based filtering to quickly audit which users have high-level access (Administrator, Financial, Super Admin).
* The **Rights** column directly reflects the permissions configured in **Edit User → Additional Settings**.
* The **Role** defines default permissions, while **Rights** shows overrides and extensions.
* The **Brands** column restricts access to specific brand environments, impacting bookings, exports, and configuration visibility.
* The **User Blocked** checkbox provides quick access control without deleting the user.
