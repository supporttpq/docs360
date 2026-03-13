---
description: >-
  Create a Tourpaq Office user for a new employee. Covers roles, rights, brand
  scope, security, and first-login behavior.
---

# Onboard a new employee (Tourpaq Office access)

This page describes how to create and configure a **User** in **Tourpaq Office** for a new employee.

User access is defined by **Role**, extended by **Rights**, and limited by **Brands**. Those settings control menus and data visibility. Role definitions are documented in [Users and Roles in Tourpaq](./).

### Overview

Onboarding in Tourpaq Office includes:

* Creating a user account with a unique **Username**.
* Assigning a single **Role**.
* Granting optional **Rights** when exceptions are needed.
* Limiting access using **Company** and **Brands**.
* Enabling security controls like **Two-Factor Authentication (2FA)** and **Enable password validity days**.

### Purpose

Correct onboarding supports:

* Access aligned with job function.
* GDPR-aligned visibility of personal data.
* Traceability in audit trails.
* Stable behavior in booking, finance, exports, and automated communications.

### Requirements

* Permissions to create and edit users.
  * Typically **Administrator** or **Super Administrator**.
* Role and access scope decided before creation.
  * Includes **Role**, **Brands**, and any required **Rights**.
  * Reference: [Users and Roles in Tourpaq](./).
* If restricted visibility is required:
  * Reference: [User limited view](user-limited-view.md).
* If 2FA is required:
  * 2FA must be enabled at company/system level.
  * The user profile must contain valid contact fields for the selected 2FA method.
  * Reference: [2 Factor Authentication](../../2-factor-authentication.md).

### Navigation

User onboarding starts from the Users list:

* **Users → Users → Users Management**

The same page supports search, edits, blocking, and deletion.

### Interface overview

#### Users Management (list)

The list shows one row per user.

Common actions:

* Create a new user.
* Open an existing user for edits.
* Set **User Blocked** to prevent login.
* Delete a user (only when deletion rules allow it).

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1).png" alt="Users Management list with user identity, role, brands, and block/delete controls"><figcaption></figcaption></figure>

#### User profile (create/edit)

The user profile stores identity and access settings.

Typical configuration areas:

* Identity fields (name + internal signature).
* Access scope (company, agencies, brands).
* Access model (role + rights).
* Security settings (2FA-related fields, password policy fields).

### Field description

#### Users Management fields (Users Management)

* **Username**
  * Unique login identifier.
  * Mandatory.
  * Used in audit trails like booking **History**. See [History](../../booking/new-booking/history.md).
* **First Name**
  * Given name for display in Tourpaq Office.
  * Used in user listings and some templates.
* **Last Name**
  * Family name for display in Tourpaq Office.
  * Used in user listings and some templates.
* **Seller Signature**
  * Internal identifier used for sales attribution.
  * Commonly used when filtering reports by seller.
* **Company**
  * The company the user belongs to.
  * Controls tenant-level data boundaries.
* **Role**
  * Primary permission set.
  * Only one role can be assigned per user.
  * Role selection affects which menus appear.
  * See [Users and Roles in Tourpaq](./).
* **Rights**
  * Additional permissions layered on top of **Role**.
  * Used to grant exceptions like overbooking, exports, or admin tools.
  * Related to GDPR access restrictions. See [User limited view](user-limited-view.md).
* **Brands**
  * Brands that the user can access.
  * Brand selection impacts brand-specific configuration, templates, and operational data.
  * Missing brand access can block brand-scoped templates and settings, including offers and emails.
* **Last Login**
  * Timestamp of the latest successful login.
  * Useful for access audits and inactive account cleanup.
* **User Blocked**
  * When enabled, login is denied.
  * Keeps the user record for auditing and history.
* **Actions**
  * Delete action.
  * Deletion can be blocked by audit dependencies.

#### User profile fields (core access model)

Field names and availability depend on role and installation.

* **Username**
  * Mandatory.
  * Must be unique.
  * Must remain stable for auditability.
* **First Name**
  * Mandatory in most setups.
  * Used for display in lists and selection dialogs.
* **Last Name**
  * Mandatory in most setups.
  * Used for display in lists and selection dialogs.
* **Password**
  * Mandatory for new users.
  * Used for the first authentication factor at login.
  * Can be subject to expiration when **Enable password validity days** is enabled. See [Password expiration](password-expiration.md).
* **Seller Signature**
  * Optional in some roles.
  * Strongly recommended for Sales/Financial users for reporting.
* **Company**
  * Mandatory.
  * Defines the company boundary for access.
* **Role**
  * Mandatory.
  * Defines the default permission scope.
* **Brands**
  * Mandatory when the installation uses brands.
  * Limits access to brand-scoped configuration and workflows.
* **Rights**
  * Optional.
  * Used for exceptions beyond the role.

#### Security-related fields (commonly used)

* **Enable password validity days**
  * When enabled, password expiration rules apply to the user.
  * Requires a configured number of validity days.
  * Related page: [Password expiration](password-expiration.md).

For 2FA behavior and required user data fields, see:

* [2 Factor Authentication](../../2-factor-authentication.md)

### Configuration steps

{% stepper %}
{% step %}
### 1) Choose role and access scope

Define the minimum access level:

* Role (Sales, Financial, Administrator, Guide Team, Supplier, etc.).
* Required **Brands**.
* Any special **Rights**.

Reference: [Users and Roles in Tourpaq](./).
{% endstep %}

{% step %}
### 2) Open Users Management

Open:

* **Users → Users → Users Management**

Locate the Create action.
{% endstep %}

{% step %}
### 3) Create the user profile

Enter identity and login fields:

* **Username**
* **First Name**
* **Last Name**
* **Password**
* **Seller Signature** (when sales attribution is required)

Set access fields:

* **Company**
* **Role**
* **Brands**

Grant optional access:

* **Rights**

Save the user.
{% endstep %}

{% step %}
### 4) Apply GDPR access limitations (when required)

If the role should not expose personal data, apply limited visibility settings.

Reference: [User limited view](user-limited-view.md).
{% endstep %}

{% step %}
### 5) Configure password policy (when required)

Enable password expiration on the user profile:

* Enable **Enable password validity days**.

Confirm validity behavior and deadlines.

Reference: [Password expiration](password-expiration.md).
{% endstep %}

{% step %}
### 6) Configure 2FA (when required)

If 2FA is enabled for the company, ensure the user profile contains valid contact data.

Reference: [2 Factor Authentication](../../2-factor-authentication.md).
{% endstep %}

{% step %}
### 7) Verify first login and adjust access

After first login, verify:

* Correct menus are visible.
* Required **Brands** are selectable.
* Restricted areas are not accessible.

Adjust **Role**, **Brands**, or **Rights** if gaps appear.
{% endstep %}
{% endstepper %}

### System behavior

#### Role and rights resolution

* **Role** defines the default menu access and permission scope.
* **Rights** extend permissions beyond the role.
* Restricted-view features can remove access even when role permits it.
  * Reference: [User limited view](user-limited-view.md).

#### Brand scope

* **Brands** act as a visibility boundary for brand-scoped setup and data.
* Missing brand access can block workflows that depend on brand configuration.
  * Example: offer texts, email templates, payment settings.
  * Related pages: [Select text for Offers](../../offers/select-text-for-offers.md), [E-mail center](../../email-setup/e-mail-center.md).

#### Blocking and deletion

* **User Blocked** denies login.
* Blocking preserves history.
* Deletion can be prevented when bookings or financial entries exist.
  * Blocking is typically preferred for traceability.

#### Password expiration behavior

When password validity is enabled:

* Warnings appear when expiration is near.
* Forced password change can occur when expiration is imminent.
* Full expiration can require an admin reset.

Reference: [Password expiration](password-expiration.md).

#### 2FA behavior

When 2FA is enabled:

* Login requires a second factor after username + password.
* Verification can be SMS, email, or authenticator app.

Reference: [2 Factor Authentication](../../2-factor-authentication.md).

### Examples

#### Sales agent for one brand

* **Role**: Sales (Agent)
* **Brands**: Single brand assignment
* **Seller Signature**: Set for reporting
* **Rights**: Only what is required (avoid admin rights)

Expected result:

* Booking workflows available.
* Setup menus limited.

#### Financial user with enforced security

* **Role**: Financial
* **Enable password validity days**: Enabled
* 2FA: Enabled when the company policy requires it
* 2FA: Enabled when company policy requires it

Expected result:

* Finance menus available.
* Regular password rotation enforced.

#### Seasonal employee

* **Role**: Depends on function
* End of season action: enable **User Blocked**

Expected result:

* Login disabled.
* Booking history and audit references preserved.

### Related pages

* [Users and Roles in Tourpaq](./)
* [Users Management](users-management.md)
* [User limited view](user-limited-view.md)
* [Password expiration](password-expiration.md)
* [2 Factor Authentication](../../2-factor-authentication.md)
* [Security measures](../../security-measures.md)
