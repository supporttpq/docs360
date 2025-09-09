# User limited view

### **Overview / Purpose**

To comply with **GDPR legislation**, Tourpaq provides functionality for restricting user access to sensitive information. This ensures that only authorized users can view or manage personal data, reducing the risk of unauthorized access and protecting customer privacy.

Two user types are responsible for controlling access permissions:

1. **Super Administrator**
2. **Administrator**

***

### **How It Works**

* **Super Administrators** hold the highest level of control and can restrict or grant access to nearly all areas of the system.
* **Administrators** can also restrict user access but only to a limited set of additional settings.
* Restrictions can apply both at the **system level** (modules, pages, or menus) and at the **data level** (visibility of personal information such as customer details in reports, bookings, or exports).

***

### **Key Features / Functions**

#### 🛡️ **Super Administrator Restrictions**

Super administrators can restrict user access to the following areas:

* **Booking Table & Booking Management:**
  * View All Bookings
  * New Booking
  * Find Booking
  * Customer Center
  * Merge Customers
  * Offers
* **System Setup & Administration:**
  * Access to system configuration menus and setup tools
* **Data Privacy Controls:**
  * Restrict visibility of personal customer details in:
    * Financial exports
    * Hotel lists
    * Extras lists
    * Tee times lists
    * Flight transfer lists
    * Booking details
    * “View All Bookings”

***

#### ⚙️ **Administrator Restrictions**

* Administrators have **limited access rights** to restrict user access.
* Their control is focused only on **additional settings**, without full control over system-wide access like a super administrator.

***

### **Examples or Scenarios**

* A **super administrator** configures restrictions so sales agents cannot access the **Merge Customers** function to avoid unapproved customer data modifications.
* An **administrator** prevents certain users from viewing personal data in the **Hotel list** to comply with GDPR rules.
* A **seasonal guide** user is granted booking access but restricted from seeing personal information in **financial exports**.

***

### **Notes / Best Practices**

* Always follow the **principle of least privilege**: users should only have access to the data and functions required for their role.
* Use **data visibility restrictions** (e.g., hiding personal details in lists) to ensure GDPR compliance while maintaining operational efficiency.
* Review and audit **user permissions** regularly, especially for high-level roles like administrators and super administrators.
* Blocking access is often preferable to deletion, as it preserves audit trails while ensuring compliance.
