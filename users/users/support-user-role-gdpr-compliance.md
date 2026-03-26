# Support User Role (GDPR Compliance)

### Overview

In Tourpaq exist a user type as **Support user role,** designed for external or internal support teams that require broad system access without exposing **personal data**.

The role mirrors **Administrator permissions** in functionality but enforces strict data privacy rules to ensure GDPR compliance.

***

### Purpose

* Enable support teams to assist multiple companies without accessing sensitive personal data
* Replace the need to use Administrator accounts for support purposes
* Ensure compliance with GDPR and internal data protection policies
* Prevent unauthorized access to personal and exported data

***

### Definition of Personal Data

The following information is considered **personal data** and must be protected:

* Full name of individuals
* Address details
* Phone numbers
* Email addresses

***

### Key Behavior

<figure><img src="../../.gitbook/assets/image (751).png" alt=""><figcaption></figcaption></figure>

#### Access Rights

The **Support role** has:

* Full functional access equivalent to Administrator
* Access to configuration, bookings, transports, hotels, and system setup

However:

* All personal data is **anonymized**
* Certain sections containing sensitive or exported data are **restricted**

***

### Anonymization Rules

Wherever personal data appears in the system, it must be:

* Masked or replaced (e.g., "Anonymized User")
* Not readable or reversible
* Consistent across all modules

***

### Restricted Access

#### 1. Exported Data Access

Support users **cannot access exported data**, as exports may contain personal information.

***

#### 2. Communication Tabs (Blocked)

Access is blocked in the following modules:

* Suppliers → Communication tab
* Transport Supplier → Communication tab
* Hotel → Communication tab
* Transport → Communication tab
* Real Transport → Communication tab
* Extras → Communication tab

***

#### 3. Saved Emails (Blocked)

Support users cannot access stored communications in:

* E-ticket Overview
* Booking page (email history)

***

#### 4. User Management (Fully Restricted)

Support users **do NOT have access** to:

* Users → User page

This prevents:

* Viewing personal user details
* Managing or accessing user accounts

***

### Expected System Behavior

* Support users can navigate and operate the system normally
* Personal data is never visible in any module
* Restricted sections are:
  * Hidden, or
  * Inaccessible (permission denied)
* Export-related and communication data are fully protected

***

### Example Scenarios

#### Scenario 1 – Booking Access

Support user opens a booking:

* Can view structure, pricing, services
*   Cannot see passenger names or contact details&#x20;

    <figure><img src="../../.gitbook/assets/image (754).png" alt=""><figcaption></figcaption></figure>

***

#### Scenario 2 – Troubleshooting

Support user investigates transport or hotel setup:

* Full access to configuration
* No access to related communication logs containing personal data

***

#### Scenario 3 – Email History

Support user tries to access email logs:

*   Access is denied&#x20;

    <figure><img src="../../.gitbook/assets/image (755).png" alt=""><figcaption></figcaption></figure>

***

### Scenario 4 - All Bookings

* Support user has access to the All Bookings page
*   Can not see customer details (Name, Surname, phone). &#x20;

    <figure><img src="../../.gitbook/assets/image (753).png" alt=""><figcaption></figcaption></figure>

### Security Considerations

* Ensures separation between **operational support** and **personal data access**
* Reduces risk when supporting external companies
* Aligns with GDPR principles:
  * Data minimization
  * Access control
  * Privacy by design

***

### Summary

The Support role provides a secure way to deliver full system support capabilities while completely restricting access to personal data and sensitive communications.

This is a critical step toward a fully GDPR-compliant platform and safer multi-company support operations.
