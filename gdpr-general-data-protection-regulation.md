# GDPR (General Data Protection Regulation)

### Overview

The GDPR module in Tourpaq controls how personal customer data is handled, anonymized, retained, and protected across the system.

This functionality is designed to help companies comply with GDPR and internal privacy policies by:

* Restricting access to personal data
* Controlling how long customer data is stored
* Supporting anonymization of customer records
* Marking specific booking content as GDPR-sensitive
* Ensuring sensitive data is removed from operational and reporting areas when required

The GDPR configuration is intended for System Administrators only.

### Access and permissions

Only users with the role:

* System Administrator

should configure GDPR rules and retention settings.

The System Administrator role has access to:

* Setup
* Booking
* GDPR

Regular agents and operational users should not modify GDPR rules.

Related page:

* Users and Roles

### Purpose

The GDPR module in Tourpaq ensures that personal data of customers who no longer have active or&#x20;

The GDPR functionality exists to:

* Protect customer privacy
* Reduce unnecessary storage of personal information
* Support legal compliance
* Control access to sensitive data
* Allow anonymization of customers when data should no longer remain identifiable
* Ensure GDPR-sensitive extras and booking content are treated differently from normal operational data

Typical examples:

* Removing personally identifiable information after a retention period
* Marking medical extras as GDPR-sensitive
* Anonymizing inactive customers
* Preventing old customer records from exposing unnecessary personal data



### Continuous deletion <a href="#continuous-deletion" id="continuous-deletion"></a>

#### Access

The Continuous Deletion settings are available under:\
**Setup → GDPR → Continuous Deletion**

Only users with **System Administration rights** can activate or modify these settings.

<figure><img src=".gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

GDPR- Continuous Deletion service settings allows to be activated in different ways depending on which information related to customer is needed to be anonymized. Settings below are relevant only when continuous deletion is choosed.

#### Configuration Options

**1. Activate Continuous Deletion for Customers**

Automatically anonymizes customers who have returned home more than the configured number of days ago **and have no future bookings**.

Purpose:

Allows a customer profile to be anonymized so the person can no longer be identified.

Typical anonymized fields:

* Name
* Email
* Phone number
* Address
* Other personally identifiable information

#### How it works

When a customer is anonymized:

* The booking history may still remain for financial and operational reasons
* Personally identifiable data is removed or replaced
* Reports no longer expose customer identity
* Historical statistics can still remain available depending on configuration

When a customer is anonymized, the following data is affected:

* **Customer details:**\
  Name, address (except country and ZIP code), email, phone, and secondary information.
* **Passenger details:**\
  Name, passport number, nationality, insurance details, address, emergency contacts.
* **Emails and SMS:**\
  All related records are deleted. Email addresses are replaced with anonymized placeholders.
* **Comments:**\
  Removed and replaced with the word “Anonymized.”
* **SSR codes:**\
  Deleted.
* **Profit details:**\
  Passenger names are hidden.
* **Transport seating:**\
  Passenger names replaced with anonymized names.
* **Tee times:**\
  Passenger names replaced with anonymized names.
* **Payment type:**\
  Replaced with “GDPR Sensitive” for non-administrator or non-financial users.\
  (The payment type must first be marked as _GDPR Sensitive_ in _Method of Payment_.)

<figure><img src=".gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

#### Example

A customer traveled three years ago and requested removal of personal information.

The administrator anonymizes the customer.

Result:

* Booking totals remain in statistics
* Operational history remains intact
* The customer can no longer be identified by name, email, or phone



*   **Extras, discounts, and supplements:**\
    Any marked as _Highly Sensitive_ are anonymized.

    * For extras: a new category “GDPR Sensitive” appears in the booking overview.&#x20;

    This is typically used for:

    * Medical services
    * Health-related requests
    * Accessibility assistance
    * Sensitive passenger information
    * Other privacy-sensitive services

    #### Configuration

    When configuring an Extra, administrators can mark the Extra as GDPR-related.

    This indicates that the information:

    * Contains sensitive customer data
    * Requires restricted handling
    * May require anonymization or limited visibility

    #### System behavior

    When an Extra is GDPR-marked:

    * Access may be restricted depending on permissions
    * Data may be anonymized according to GDPR rules
    * Sensitive information should not appear unnecessarily in exports or reports
    * Visibility may differ between operational users and administrators

<figure><img src=".gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

* For discounts/supplements: displayed as “GDPR Sensitive” in the passenger grid.

<figure><img src=".gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

When extras marked as highly sensitive are assigned to a passenger, after customer anonymization, in the booking overview new category called "GDPR Sensitive" will be created and will include the products marked are sensitive which were assigned for passengers.

When discounts or supplements marked as highly sensitive are assigned to a passenger anonymized, those are shown are GDPR Sensitive in the passengers grid over a booking.

{% hint style="warning" %}
**Note:** When a customer is anonymized, **all related bookings** are affected.
{% endhint %}

**2. Activate Deletion for SSR Codes**

Automatically deletes selected SSR codes for passengers within the specified date range.

**3. Activate Deletion for Booking Comments**

Automatically deletes comments and any attachments from bookings within the defined range.

**4. Activate Deletion for Bonus Codes**

Automatically deletes bonus codes added to bookings within the defined range.

**5. Activate Continuous Deletion for Excursion Guests**

Anonymizes excursion guest customers (e.g., Destination App and Visit Sun users) older than the configured number of days.

**6. Activate Deletion for Highly Sensitive Extras or Discounts**

Anonymizes extras, discounts, and supplements marked as _GDPR Sensitive_ for all bookings of anonymized customers.

**7. Delete Transport Reporting Files**

Automatically deletes transport reporting files with departure dates older than the configured number of days.

**8. Delete Extra Reporting Files**

Deletes extra and extra category reporting files older than the configured number of days.

**9. Delete Hotel Reporting Files**

Deletes automatically generated hotel lists older than the configured number of days.

<figure><img src=".gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

#### GDPR Log

All anonymization activities are logged and can be reviewed under:\
**Setup → GDPR → Log**\
(Visible only when logged in as a Sysadmin user.)

### The right to be forgotten for customers and passengers <a href="#the-right-to-be-forgotten-for-customers-and-passengers" id="the-right-to-be-forgotten-for-customers-and-passengers"></a>

The right to be forgotten can be applied to a customer or can be applied for a passenger, so anonymization can be triggered individually. For a **customer**, this can be done by using "Anonymize" button in the "Manage Customer" page when logged with an user with system administrator rights.

<figure><img src=".gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

If the customer is already anonymized, the request date and time, the user who perform it and the report of the anonymization (date, time, anonymized customer id and corresponding bookings) can be seen under the "Anonymize" buton:

<figure><img src=".gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

Data anonymized is data described also for service anonymization (customer and passenger names, address, email address, phone number, emails and sms sent, SSR codes, booking comments and passenger details like nationality, passport number, insurance, address, emergency contacts, sensitive data). Also, the customer or data linked to it will appear in transport reporting files, hotel reporting files or extra reporting files or category reporting files as being anonymized.

Anonymisation can be triggered also for one **passenger** from a booking. Data for this particular passenger is anonymized: passengers, address, email address, phone, email, phone found in customer details and passenger details like nationality, passport no., insurance, address, emails, sms and tickets.

{% hint style="warning" %}
**Important:** Once anonymization is performed, **personal data cannot be recovered**.\
All anonymized data will appear in relevant reports (transport, hotel, extra, etc.) as **Anonymized**.
{% endhint %}
