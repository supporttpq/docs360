---
description: >-
  Edit passenger (pax) details in Tourpaq Office bookings. Update names,
  birthdate/age, add or remove passengers, and manage customer contact data and
  email/SMS recipients.
---

# Edit Passenger

## **Passengers Tab**

The Edit Passenger functionality in Tourpaq Office enables modification of passenger information for existing bookings. This interface provides comprehensive management of traveler details, including personal identification, contact information, age-based categorization, and communication preferences. The Edit Passenger window is accessed from the booking overview and allows addition, removal, or modification of passenger records after the initial booking creation. This page details the Passengers tab functionality, while the Customer Data tab is documented separately. Related operations include passenger cancellation, allotment adjustment, and communication management through the Email and SMS modules.

### **Overview**

The Edit Passenger window serves as the primary interface for managing passenger (traveler) information within a Tourpaq Office booking. This dialog enables authorized users to modify personal details, add or remove travelers, and maintain accurate passenger data throughout the booking lifecycle. The interface is divided into two distinct tabs: the Passengers tab for individual traveler management, and the Customer Data tab for primary contact and communication settings.

### **Purpose**

The Edit Passenger window fulfills the following business objectives:

**Primary Functions:**

* Modify passenger personal information (names, titles, dates of birth) for accuracy in travel documents
* Add additional passengers to existing bookings when group size increases
* Remove passengers from bookings when travelers cancel or drop out
* Update passenger age and birthdate to ensure correct price categorization
* Manage passenger contact details (email, phone, address) for communication
* Designate primary customer contact for booking correspondence
* Control email and SMS delivery to specific passengers
* Maintain data quality for airline passenger manifests and SSR requirements

**Use Cases:**

* Correcting passenger name spelling errors before ticket issuance
* Adding late-joining travelers to group bookings
* Removing cancelled passengers while retaining other travelers
* Updating passenger birthdates when age-based pricing changes
* Changing primary customer contact when booking ownership transfers
* Enabling email delivery to multiple passengers in family bookings
* Adjusting passenger titles for correct document generation
* Managing passenger information for airline check-in requirements

### Requirements

Before accessing and using the Edit Passenger functionality, the following prerequisites must be satisfied:

**User Access:**

* Active Tourpaq Office user account with booking modification permissions
* Assigned role with access to Edit Passenger functionality
* Permission to modify passenger data for the specific Brand

**Booking Prerequisites:**

* Existing saved booking in the Tourpaq Office
* Booking must not be in cancelled status
* Booking must be accessible to the logged-in user

**Data Requirements:**

* Passenger modifications must comply with airline name format rules if flight booking
* Birthdate changes must result in valid age categories (adult/child/infant)
* Contact information must be in valid format (email format, phone number format)
* Passenger count changes may require allotment adjustment

### Navigation

**Access Path:**

1. Log in to Tourpaq Office
2. Navigate to **Booking** menu or open existing booking from search results
3. Locate the booking requiring passenger modification
4. Open the booking details view
5. Locate the **Passengers** section in the booking overview
6. Click the **Edit** button in the Passengers section

**Alternative Access:**

* From booking search results, click booking number to open, then click Edit in Passengers section
* From Dashboard recent bookings list, click booking, then Edit in Passengers section

The Edit Passenger window opens as a modal dialog overlay on top of the booking details interface.

<figure><img src="../../../../.gitbook/assets/image (558).png" alt="Edit button in booking passenger section"><figcaption></figcaption></figure>

### Interface Overview

The Edit Passenger interface is organized into two primary tabs with distinct functional areas. This documentation focuses on the Passengers tab, which contains the passenger management grid.

<figure><img src="../../../../.gitbook/assets/image (563).png" alt="Edit Passenger window with passenger rows"><figcaption></figcaption></figure>

**Tab Structure:**

**1. Passengers Tab (Active by default)** This tab contains a grid-based interface displaying all passengers in the booking. Each row represents one traveler with editable fields for personal information.

**2. Customer Data Tab** This tab manages the primary customer contact information and communication preferences. Detailed documentation for this tab is available on the Customer Data page.

**Passengers Tab Layout:**

**Grid Section (Main Area)** The central area displays a multi-column grid with one row per passenger. The grid includes the following components:

* **Row Identifier Column (Left)** - Displays passenger number (Pax 1, Pax 2, etc.)
* **Editable Field Columns** - Contains input fields for passenger details
* **Action Column (Right)** - Contains delete button for passenger removal

**Column Headers:** The top row of the grid displays field labels identifying each data column. Headers are fixed and remain visible during scrolling.

**Action Buttons (Bottom)**

**Add new Button:**

* Located at the bottom-left below the passenger grid
* Creates a new passenger row when clicked
* Adds blank row for new traveler data entry

**Save Changes Button:**

* Located at the bottom-right of the dialog
* Commits all passenger modifications to the booking
* Validates data before saving

**Cancel Button:**

* Located adjacent to Save Changes button
* Closes the Edit Passenger window without saving modifications
* Discards all unsaved changes

**Grid Row Structure:**

Each passenger row contains the following sections from left to right:

1. Passenger identifier (Pax 1, Pax 2, etc.)
2. TITLE dropdown field
3. F. NAME text input field
4. L. NAME text input field
5. AGE numeric display field
6. BIRTHDATE date picker field
7. E-MAIL text input field
8. PHONE text input field
9. ADDRESS text input field
10. Delete icon button (trash icon)

The grid supports vertical scrolling when many passengers are present. Horizontal scrolling may be required depending on screen width and number of visible columns.

### Field Description

This section provides comprehensive descriptions of all fields available in the Edit Passenger interface Passengers tab. Fields are presented in the order they appear in the passenger grid from left to right.

#### Passenger Row Identifier

**Passenger Number (Pax N)**

* **Field Type:** Display only (text label)
* **Mandatory:** No (system-generated)
* **Description:** Sequential passenger identifier displaying the passenger position in the booking (Pax 1, Pax 2, Pax 3, etc.). The first passenger (Pax 1) is typically the lead passenger and primary customer contact.
* **System Behavior:** Automatically generated based on the order passengers were added to the booking. Cannot be edited directly. Numbers may be reassigned if passengers are removed from middle positions.
* **Related Functionality:** The passenger number determines the order of passengers in reports, documents, and passenger manifests. Pax 1 is treated as the lead passenger for customer communication purposes.
* **Data Source:** System-generated sequential numbering starting from 1.

#### Personal Information Fields

**TITLE**

* **Field Type:** Dropdown selector
* **Mandatory:** Yes
* **Description:** Passenger title or salutation indicating gender, age category, and formal designation. Common values include MR (Mister), MS (Miss), CHD (Child), INF (Infant)
* **Data Source:** Title values are configured in System Setup and may vary by Brand configuration. Standard titles include adult designations (MR, MS) and child designations (CHD, INF)
* **System Behavior:** Selection of title affects how the passenger name appears on tickets, vouchers, and travel documents. Some titles (CHD, INF) may trigger age-based validation rules. Title does not directly affect pricing but should correspond to the passenger's age category.
* **Format Requirements:** Single selection from predefined list. No custom titles can be entered.
* **Related Functionality:** Links to ticket generation where title appears on passenger documents. Integrates with airline systems for passenger manifest data. Affects formal communication and document presentation.
* **Validation Rules:** Title must be selected before saving. Title should logically correspond to passenger age (e.g., INF for infants under 1 year, CHD for children).

**F. NAME**

* **Field Type:** Text input
* **Mandatory:** Yes
* **Description:** Passenger first name (given name). This field must contain the passenger's first name exactly as it appears on travel documents (passport, national ID) when required for airline bookings.
* **Format Requirements:** Alphabetic characters, hyphens, apostrophes, and spaces are accepted. Special characters and numbers are typically not allowed. Maximum length is usually 50 characters. Exact format requirements may vary based on airline ticketing rules.
* **System Behavior:** The first name is used in ticket generation, voucher creation, passenger manifests, hotel rooming lists, and all customer communication. Name must match travel documents for airline bookings to avoid check-in issues.
* **Related Functionality:** Links to Ticketing module where name appears on travel documents. Integrates with airline SSR (Special Service Requests) systems. Appears on hotel rooming lists and transfer manifests. Used in Email and SMS communication personalization.
* **Validation Rules:** Field cannot be empty. Must contain at least 2 characters. Should not contain numbers or special characters (depending on airline rules). System may validate against passport data if integration exists.
* **Best Practices:** Enter name exactly as shown on passport or travel document. Avoid nicknames or shortened names. Use hyphens for hyphenated names. Include all given names if required by airline.

**L. NAME**

* **Field Type:** Text input
* **Mandatory:** Yes
* **Description:** Passenger last name (surname or family name). This field must contain the passenger's surname exactly as it appears on travel documents (passport, national ID) when required for airline bookings.
* **Format Requirements:** Alphabetic characters, hyphens, apostrophes, and spaces are accepted. Special characters and numbers are typically not allowed. Maximum length is usually 50 characters. Exact format requirements may vary based on airline ticketing rules.
* **System Behavior:** The last name is used in ticket generation, voucher creation, passenger manifests, hotel rooming lists, and all customer communication. Name must match travel documents for airline bookings to avoid check-in issues.
* **Related Functionality:** Links to Ticketing module where name appears on travel documents. Integrates with airline SSR (Special Service Requests) systems. Appears on hotel rooming lists and transfer manifests. Used in Email and SMS communication personalization.
* **Validation Rules:** Field cannot be empty. Must contain at least 2 characters. Should not contain numbers or special characters (depending on airline rules). System may validate against passport data if integration exists.
* **Best Practices:** Enter surname exactly as shown on passport or travel document. For names with particles (von, van, de), follow passport convention. Use hyphens for hyphenated surnames. Include all surnames if multiple family names are used.

**AGE**

* **Field Type:** Numeric display (auto-calculated)
* **Mandatory:** No (calculated field)
* **Description:** Passenger age in years calculated from the BIRTHDATE field relative to the travel departure date. This value determines the passenger's pricing category (Adult, Child, or Infant) and affects price calculations throughout the booking.
* **System Behavior:** Age is automatically calculated when BIRTHDATE is entered or modified. The system calculates age as of the departure date, not the current date. Age determines which price category applies from the Price List (Adult pricing, Child pricing, or Infant pricing). Age changes trigger automatic price recalculation for the affected passenger.
* **Calculation Method:** Age = (Departure Date - BIRTHDATE) / 365 days, rounded down to whole years. Age is evaluated at the time of departure, not at the time of booking.
* **Related Functionality:** Links to Price List configuration where age thresholds define Adult/Child/Infant categories. Affects pricing calculations for transport, hotel, and extras. Determines insurance eligibility and pricing. Influences room bed allocation rules. May affect airline ticketing requirements.
* **Age Category Thresholds (typical):**
  * Infant: Age 0-1 (under 2 years)
  * Child: Age 2-11
  * Adult: Age 12 and over
  * Exact thresholds are configurable per Brand in Brand Settings
* **Data Source:** Calculated from BIRTHDATE field. Cannot be edited directly.

**BIRTHDATE**

* **Field Type:** Date picker
* **Mandatory:** Yes (typically required, depends on Brand configuration)
* **Description:** Passenger date of birth. This field stores the passenger's birth date and is used to calculate age, determine pricing category, validate travel document requirements, and comply with airline data collection rules.
* **Format Requirements:** Date format DD-MM-YYYY (day-month-year) or format configured in system locale settings. Must represent a valid date in the past (cannot be future date). Date must be realistic for human age (typically not more than 120 years ago).
* **System Behavior:** When BIRTHDATE is entered or modified, the system immediately recalculates the AGE field. Age recalculation triggers price recalculation for the passenger. Birthdate is used to validate passenger category eligibility (Infant, Child, Adult). Birthdate data is transmitted to airline systems for passenger manifests.
* **Related Functionality:** Links to Price List age-based pricing rules. Determines eligibility for child pricing, infant pricing, or adult pricing. Required for airline bookings (APIS requirements). Used in insurance age validation. Affects Transport and Hotel age-based allocation rules.
* **Validation Rules:** Date must be in the past (before current date). Date must be valid calendar date (e.g., not 31 February). Passenger age calculated from birthdate must result in realistic age for travel (e.g., not negative, not over 120 years). Age category determined from birthdate must be compatible with selected TITLE (e.g., infant birthdate should use INF title).
* **Age-Based Pricing Impact:** Changing birthdate can move a passenger between pricing categories. For example, changing a birthdate that makes a passenger 11 years old vs 12 years old will switch pricing from Child to Adult rates. System recalculates pricing automatically when birthdate changes result in age category change.
* **Best Practices:** Verify birthdate accuracy before finalizing bookings. Ensure birthdate matches travel documents for airline bookings. Check age thresholds when passengers are near age category boundaries (e.g., turning 12 or turning 2 near travel dates).

#### Contact Information Fields

**E-MAIL**

* **Field Type:** Text input (email format)
* **Mandatory:** No (typically optional for all passengers except primary customer)
* **Description:** Passenger email address. This field stores the email address for the passenger and is typically used for the primary customer (Pax 1) or other passengers who should receive booking communications directly.
* **Format Requirements:** Must be valid email format: [localpart@domain.extension](mailto:localpart@domain.extension). Maximum length typically 100 characters. Validates standard email format rules (@ symbol required, valid domain structure, no spaces).
* **System Behavior:** Email address is used when sending booking confirmations, tickets, vouchers, and other customer communications if the passenger is designated to receive emails. Primary customer (Pax 1) email is typically the default recipient for all booking correspondence. Additional passenger emails can be used if communication to multiple recipients is configured.
* **Related Functionality:** Links to Email Center for booking communication delivery. Integrates with Email Templates for automated confirmations. Connects to Customer Data tab where email delivery preferences are configured. Used in ticket delivery when electronic tickets are enabled.
* **Validation Rules:** If provided, must be valid email format. Domain must have valid structure. System may validate for common typos (e.g., gmial.com vs gmail.com). Field can be left empty for non-primary passengers.
* **Best Practices:** Collect email for primary customer (Pax 1) at minimum. Verify email address accuracy to prevent communication delivery failures. Consider collecting emails for all adult passengers in group bookings for redundant communication.

**PHONE**

* **Field Type:** Text input (phone number format)
* **Mandatory:** No (typically optional for all passengers except primary customer)
* **Description:** Passenger phone number. This field stores the contact phone number for the passenger and is typically populated for the primary customer (Pax 1) or other passengers who require direct contact capability.
* **Format Requirements:** Accepts numeric input with optional country code prefix, hyphens, spaces, parentheses. International format recommended: +\[country code]-\[area code]-\[number]. Maximum length typically 20 characters.
* **System Behavior:** Phone number is used for customer contact purposes, SMS delivery (if configured), emergency contact situations, and customer service follow-up. Primary customer (Pax 1) phone number is typically the main booking contact number.
* **Related Functionality:** Links to SMS module for text message delivery. Used in customer communication records. May integrate with telephone contact systems for outbound customer service calls. Stored in Customer Database for contact history.
* **Validation Rules:** If provided, should contain minimum number of digits (typically 7-15 digits). May validate country code format if international format required. Field can be left empty for non-primary passengers.
* **Best Practices:** Collect phone number for primary customer (Pax 1) at minimum. Include country code for international customers. Verify number accuracy for SMS delivery if used. Consider mobile numbers over landlines for better reachability.

**ADDRESS**

* **Field Type:** Text input (multi-line or single line)
* **Mandatory:** No (typically optional)
* **Description:** Passenger address. This field stores the postal address for the passenger and is typically populated only for the primary customer (Pax 1) or when required for specific supplier or regulatory requirements.
* **Format Requirements:** Free-text input accepting street address, city, postal code, country. Maximum length varies (typically 200-500 characters). Multiple address lines may be supported depending on field configuration.
* **System Behavior:** Address is primarily stored for customer records and may be used in invoicing, correspondence, or when supplier contracts require customer address data. Address data is typically not transmitted to airlines or hotels unless specifically required.
* **Related Functionality:** Links to Customer Database for permanent customer record storage. May be used in invoice generation if customer invoicing is configured. Could be required for certain insurance products or regulatory compliance.
* **Validation Rules:** Minimal validation typically applied. Field can be left empty unless specific supplier or Brand requires address data. No format validation applied in most configurations.
* **Best Practices:** Collect address for primary customer if invoicing or legal requirements exist. Address is less critical for basic travel bookings but important for package tour operators with specific regulatory requirements.

#### Action Fields

**Delete Icon (Trash Icon)**

* **Field Type:** Action button (icon)
* **Description:** Clicking the trash icon button initiates the passenger removal process. This action deletes the passenger row from the booking when Save Changes is clicked.
* **System Behavior:** Clicking the delete icon marks the passenger row for deletion. The row typically becomes highlighted or marked to indicate pending deletion. Deletion is not final until Save Changes is clicked. Deleting a passenger removes all associated passenger data (name, age, extras, pricing). System recalculates booking totals when passenger is removed. Allotment is NOT automatically released when passenger is deleted (manual adjustment required through Edit Passenger and Take Allotment).
* **Related Functionality:** Links to allotment management where manual adjustment is required after passenger removal. Connects to pricing recalculation engine. May trigger cancellation fee calculation if cancellation rules apply. Affects passenger count validation for room allocation.
* **Validation Rules:** Cannot delete all passengers (at least one passenger must remain). System may prevent deletion if passenger has specific assignments (e.g., assigned seat, assigned room). Deletion of last passenger may trigger full booking cancellation workflow instead.
* **Best Practices:** Verify correct passenger is selected before deletion. Review impact on room allocation and transport seats before deleting passengers. Remember to adjust allotment manually after passenger deletion to release inventory. Consider using Cancel Passenger function instead for formal passenger cancellations with fee application.

#### Bottom Action Buttons

**Add new Button**

* **Field Type:** Button (action)
* **Description:** Clicking the Add new button creates a new blank passenger row at the bottom of the passenger grid. This allows adding additional travelers to the booking after initial creation.
* **System Behavior:** Clicking Add new inserts a new row in the passenger grid with all fields blank. New row is assigned the next sequential passenger number (e.g., if 3 passengers exist, new row becomes Pax 4). New passenger row must be populated with required fields before saving. System validates new passenger data when Save Changes is clicked. Adding passenger increases passenger count for pricing and allotment calculations.
* **Related Functionality:** Links to allotment validation where system checks if additional passengers can be accommodated. Connects to pricing calculation for adding passenger costs. May trigger allotment warnings if insufficient transport or hotel capacity exists. Integrates with room allocation logic for bed assignment.
* **Validation Rules:** Adding passengers may require allotment adjustment. System validates sufficient inventory exists for additional passengers. Passenger count increase may require hotel room reconfiguration. Transport allotment must accommodate additional seats.
* **Best Practices:** Verify allotment availability before adding passengers. Check room capacity for hotel bookings before adding passengers. Take allotment again after adding passengers to reserve inventory. Verify pricing calculation includes new passenger in totals.

**Save Changes Button**

* **Field Type:** Button (primary action)
* **Mandatory:** Yes (to commit modifications)
* **Description:** Clicking the Save Changes button commits all passenger modifications to the booking record. This action validates all passenger data, applies changes to the database, recalculates pricing, and closes the Edit Passenger window.
* **System Behavior:** When Save Changes is clicked, the system validates all passenger records for required fields, correct data formats, and business rule compliance. If validation passes, all changes are committed to the booking database. Passenger additions, deletions, and modifications take effect. Pricing is recalculated based on updated passenger data. Age-based pricing adjustments are applied. Window closes and returns to booking overview. If validation fails, error messages display indicating issues requiring correction.
* **Related Functionality:** Links to booking validation engine. Triggers price recalculation through Price List system. Updates allotment records if passenger count changed. Modifies booking history log with passenger changes. May trigger email notifications if configured.
* **Validation Rules:** All mandatory fields must be completed for all passengers. TITLE, F. NAME, L. NAME, and BIRTHDATE are typically required. Email format must be valid if provided. Phone number format must be valid if provided. Birthdate must result in valid age (not future, not unrealistic). Age category must be compatible with selected title. At least one passenger must exist in booking.
* **Error Handling:** If validation fails, window remains open with error messages displayed. Specific field validation errors are highlighted on respective fields. Generic validation errors display at top of window. User must correct errors before Save Changes will succeed.

**Cancel Button**

* **Field Type:** Button (secondary action)
* **Description:** Clicking the Cancel button closes the Edit Passenger window without saving any modifications made during the current editing session.
* **System Behavior:** All changes made in the Edit Passenger window are discarded. Passenger additions are not saved. Passenger deletions are not applied. Field modifications revert to previous values. Window closes and returns to booking overview with original passenger data intact.
* **Related Functionality:** No database changes occur. No integrations are triggered. Booking state remains unchanged.
* **Use Case:** Used when user opens Edit Passenger by mistake, or decides not to proceed with planned modifications, or discovers errors that require abandoning changes.

***

## FAQ

#### What’s the difference between a **passenger (pax)** and the **customer**?

* A **passenger (pax)** is an individual traveler on the booking.
* The **customer** is the main contracting/contact person for the booking (typically the person who receives confirmations, invoices, and messages).

You edit traveler information in **Passengers**, and communication/contact selection in **Customer Data**.

#### Why is it important that names match the passport/travel document?

Tickets, airline messages (SSR), and supplier documents can require an exact match. If a name is incorrect, it can cause:

* Document/ticket mismatches
* Failed check-in or manual handling requirements
* Extra work with suppliers to correct passenger details

#### Does changing **Birthdate** or **Age** affect the price?

Yes. Age and birthdate drive price logic such as:

* Adult/Child/Infant categorization
* Child-price rules
* Insurance eligibility
* Some discounts/supplements and supplier rules

If prices look wrong, verify the **birthdate** first.

#### Why does the **Age** not look correct?

Typically, age is calculated from **birthdate**. If age looks wrong:

* Confirm the birthdate is entered correctly (day/month/year).
* Make sure the travel dates are correct (age is usually evaluated “at time of travel”).

#### Can I add passengers after I already started the booking?

Yes.

* Use **Add new** to add another pax.
* Always **Save Changes** when you are done.

If the booking’s allotments (hotel/transport) were already taken, you may need to re-check availability and/or take allotment again (depending on your workflow).

#### What happens when I remove a passenger?

Removing a passenger will normally:

* Remove that pax from the booking’s passenger list
* Trigger recalculation of totals and per-pax services
* Potentially change eligibility for discounts/supplements or pricing rules

If you are removing passengers after services have been allocated (seats, rooms, extras), double-check that allotment and connected services still match the intended passenger count.

### Customer Data tab (contact person + communication)

#### Who receives **Email** and **SMS** messages?

* The passenger marked as **Customer** is typically the primary recipient.
* Additional passengers can be opted in via the **EMAIL** and **SMS** checkboxes (they will receive the same communication as the customer).

#### Can I send confirmations/documents to more than one person?

Yes—enable **EMAIL** (and/or **SMS**) for additional passengers who should receive the same message as the customer.

#### What should I do if the wrong person is receiving messages?

1. Open **Edit Passenger**.
2. Go to **Customer Data**.
3. Set the correct passenger as **Customer**.
4. Adjust **EMAIL** / **SMS** checkboxes for other passengers.
5. **Save Changes**.

### Troubleshooting

#### I updated passenger details but the booking documents still show the old data

* Ensure you clicked **Save Changes** in the Edit Passenger window.
* If documents were already generated/sent, you may need to regenerate or resend them depending on your email/ticket flow.

#### I can’t save changes

Common causes:

* Missing mandatory fields (often title/first name/last name/birthdate)
* Invalid date format in birthdate
* Invalid characters in name fields (depending on ticketing rules)

### Related Pages

The Edit Passenger functionality integrates with and relates to numerous other modules in TourPaq Office. The following pages provide additional information for passenger management operations and related booking functionality:

**Core Passenger Pages:**

* [**Customer Data**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/new-booking/edit-passenger/customer-data) - Customer Data tab documentation for primary contact management and communication preferences
* [**Passenger Details**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/passenger-details) - Extended passenger information including passport details, nationality, and travel document data
* [**New Booking**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/new-booking) - Initial passenger data entry during booking creation process

**Booking Management:**

* [**Booking Overview**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/booking-overview) - High-level view of booking structure including passengers section
* [**All Bookings**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/all-bookings) - Comprehensive booking search and access to passenger modification
* [**New Booking (Overview)**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking) - Section entry point for booking-related operations

**Passenger-Related Operations:**

* [**Cancel Passenger or Booking**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/new-booking#step-9-cancel-passenger-or-booking) - Formal passenger cancellation with fee calculation and allotment release
* [**Import Passengers**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/new-booking#import-passengers-optional) - Bulk passenger data import from Excel files for group bookings
* [**Copy Booking**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/copy-booking) - Duplicate bookings with passenger data for repeat customers

**Pricing and Age Categories:**

* [**Price List**](https://tourpaq.gitbook.io/staging-tourpaq-docs/price-list/pricelist) - Price list configuration including age-based pricing thresholds
* [**Child Price**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/child-price) - Child pricing rules and age category definitions
* [**2 x Child Prices + Child Price Discount**](https://tourpaq.gitbook.io/staging-tourpaq-docs/2-x-child-prices-+-child-price-discount) - Multiple child pricing scenarios

**Customer Management:**

* [**Customers**](https://tourpaq.gitbook.io/staging-tourpaq-docs/customer/customers) - Customer database and permanent customer records
* [**Customer Info / Details on Customer Card**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/customer-info-details-on-customer-card) - Detailed customer profile and booking history
* [**Merge Customers**](https://tourpaq.gitbook.io/staging-tourpaq-docs/merge-customers) - Consolidating duplicate customer records

**Communication:**

* [**E-mails**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/e-mails) - Email communication history and passenger email delivery
* [**SMS**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/sms) - SMS communication with passengers and phone number usage
* [**Email Center**](https://tourpaq.gitbook.io/staging-tourpaq-docs/email-setup/e-mail-center) - Email template configuration and delivery management
* [**Dynamic E-mail/SMS Center**](https://tourpaq.gitbook.io/staging-tourpaq-docs/email-setup/dynamic-e-mail-sms-center) - Advanced communication workflows

**Travel Documents:**

* [**Print Tickets**](https://tourpaq.gitbook.io/staging-tourpaq-docs/tickets/print-tickets) - Ticket generation using passenger names and details
* [**E-tickets Overview**](https://tourpaq.gitbook.io/staging-tourpaq-docs/e-tickets-overview) - Electronic ticketing and passenger data requirements
* [**SSR - Special Service Requests for Airlines**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/ssr) - Airline special requests linked to passenger records

**Hotel and Transport:**

* [**Hotel Room**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/hotel-room) - Room allocation and bed assignment based on passenger count
* [**Transport Seating**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/transport-seating) - Seat assignment and passenger manifest generation
* [**Hotel Beds**](https://tourpaq.gitbook.io/staging-tourpaq-docs/hotel-beds) - Hotel bed configuration and passenger capacity rules

**Extras and Insurance:**

* [**Extras**](https://tourpaq.gitbook.io/staging-tourpaq-docs/extras-setup/extras) - Extras configuration and age-based eligibility
* [**Cancellation Insurance**](https://tourpaq.gitbook.io/staging-tourpaq-docs/cancellation-insurance) - Cancellation insurance linked to passenger age
* [**Travel Insurance**](https://tourpaq.gitbook.io/staging-tourpaq-docs/travel-insurance) - Travel insurance products and age-based pricing

**System Configuration:**

* [**Brands**](https://tourpaq.gitbook.io/staging-tourpaq-docs/brands) - Brand configuration including mandatory passenger field settings and age thresholds
* [**System Setup**](https://tourpaq.gitbook.io/staging-tourpaq-docs/setup/system-setup) - System-wide passenger data requirements and validation rules
* [**GDPR (General Data Protection Regulation)**](https://tourpaq.gitbook.io/staging-tourpaq-docs/gdpr-general-data-protection-regulation) - Privacy compliance for passenger personal data

**Financial Operations:**

* [**Economics**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/economics) - Payment processing and refunds related to passenger changes
* [**Cancellation Rules**](https://tourpaq.gitbook.io/staging-tourpaq-docs/cancellation-rules) - Cancellation fee calculation when passengers are removed

**History and Tracking:**

* [**History**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/history) - Booking modification history including passenger changes
* [**Comments**](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/comments) - Internal notes documenting passenger modifications
