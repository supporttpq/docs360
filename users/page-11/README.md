# Users

## **Users and Roles in Tourpaq**

### **Overview / Purpose**

Tourpaq manages access to its system using **user roles**, which define what each user can view, edit, or manage. This ensures secure, role-based access and prevents unauthorized changes in bookings, payments, or configurations. Each role has its own scope of permissions, ranging from system-wide control to limited operational functions.

***

### **How It Works**

* Each user is assigned to a **company** and, optionally, one or more **agencies** within that company.
* A **role** determines the level of access. Only one role can be assigned to a user.
* Permissions can be extended through **additional rights**, which are configurable per user.
* Some roles (like Super Administrator) exist only once per Tourpaq installation, while others (like Agents, Guides, or Suppliers) can exist in multiple instances.
* User deletion is limited if the user has created bookings or financial entries.

***

### **Key Features / Functions by Role**

#### 🔑 **Super Administrator**

* Full system-wide access (only one exists in the system).
* Manage companies, agencies, users, and roles.
* Control system settings, enable/disable features, add countries/postcodes/SSR codes.
* Block/unblock users per company.
* Post internal messages.

#### 🔑 **System Administrator**

* Limited compared to Super Admin.
* Access to three main menus: **Setup, Booking, GDPR**.
* Can configure company settings, manage users, and adjust GDPR data deletion rules.

#### 🔑 **Administrator**

* Company-level manager with access to all company functions.
* Manage bookings, hotels, resorts, payments, emails.
* Can create agencies and users within their company.
* Additional rights: overbook hotels/transports, merge customers, add special offers, override seating rules, etc.

#### 🔑 **Sales (Agent)**

* Handles sales processes: create/edit bookings, manage payments, print tickets.
* Additional rights: overbooking, merge customers, view pricelists, edit hotel web tab, see unpaid bookings.

#### 🔑 **Financial**

* Same as Sales, but with **financial management rights**.
* Manage payment methods, import bank exports, handle unregistered or unpaid bookings.

#### 🔑 **Supplier**

* Designed for accommodation providers.
* Manage hotel room allotments, release rules, stop sales.
* View contracts, transport allotments, and statistics.

#### 🔑 **Extra Supplier**

* For providers of destination services (e.g., excursions).
* Access to extras lists, tee time lists, and destination guest lists.
* Can block product allotments.

#### 🔑 **Guide**

* On-site resort staff managing tours and services.
* Access to completed bookings, guest lists, tickets, payments.
* Can send push notifications to guests.
* Export hotel lists and statistics.

#### 🔑 **Guide Master**

* Supervises multiple guides.
* Access to guide activity reports, destination reports, and service cases.
* Can book extras on behalf of a destination.
* Manages GuestApp backoffice (maps, activities, insider tips).

***

### **Examples or Scenarios**

* A **Super Administrator** sets up a new company, creates agencies, and configures user roles.
* An **Administrator** at a travel agency creates new bookings, manages hotels, and oversees payments for their company.
* A **Sales agent** uses the system to sell trips, issue tickets, and process customer payments.
* A **Supplier** logs in to adjust hotel room allotments when cancellations occur.
* A **Guide** checks which guests are arriving today, prints tickets, and sends welcome push notifications via the Guest App.
* A **Guide Master** reviews guide performance and updates destination info for travelers.

***

### **Notes / Best Practices**

* Always assign the **minimum role necessary** to complete a user’s tasks.
* Remember: only **one Super Administrator** can exist in a system.
* **User deletion restrictions**: accounts with bookings or payments cannot be deleted.
* Use **additional rights** carefully, as they extend the power of lower-level roles (e.g., overbooking transports or hotels).
* Guides and Suppliers should only have access to the agencies or destinations relevant to their work.
* Regularly review and update user roles to match business needs and security compliance.
