---
description: >-
  Step-by-step guide to the Tourpaq Office New Booking screen. Select brand,
  search transport and hotel availability, take allotment, add passengers and
  extras, then save the booking.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# New Booking

### **Overview**

The **New Booking** screen in **Tourpaq Office** (BackOffice) is used to **create a new booking** from scratch. You select a **Brand**, search **transport availability** and **hotel/room availability**, then add passengers, extras, discounts, and supplements.

Use this page as the detailed, step-by-step **booking creation workflow**. For the section overview and links to related topics, see the main [New Booking](../) page.

### **Purpose**

This tool is designed to:

* Create new bookings from scratch.
* Search and select **transport departures** and **hotel rooms** based on availability.
* Assign accommodation, board type, and optional services (extras, insurance).
* Manage passenger data in the booking window or via **passenger import**.
* Apply product logic such as **packages**, **discounts/supplements**, and price rules.

### Requirements

Before creating a booking, the following prerequisites must be satisfied:

**User Access:**

* Active Tourpaq Office user account with booking creation permissions
* Assigned role with access to the New Booking module
* Brand access permissions configured in the user profile

**System Configuration:**

* Brand setup completed with active products and pricing
* Transport departures configured with allotments
* Hotel contracts established with room inventory
* Price lists published for the travel period
* Extras and supplements are defined and activated
* Payment methods configured in system setup
* Email templates configured for booking confirmations

**Data Prerequisites:**

* Valid customer data available (name, phone, email)
* Transport allotments loaded for selected travel dates
* Hotel availability confirmed for booking period
* Active pricing rules and margin calculations

***

### Navigation

**Access Path:**

1. Log in to Tourpaq Office
2. Dashboard quick action button "New Booking"

<figure><img src="https://sonat.com/api/Document/Image/19670ef0-8b8a-4cda-8eb6-249681e07016/60a72aeb-a272-4428-a118-b6074b1b35b5/095769e7-32fd-4f22-8e55-e504ab071f34.webp?width=1915" alt="Tourpaq Office New Booking screen" width="900"><figcaption><p>New Booking screen (Tourpaq Office).</p></figcaption></figure>

***

### Interface Overview

The New Booking screen is organized into distinct functional sections that follow the booking creation workflow from top to bottom.

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

**Main Interface Sections:**

**1. Brand Selection (Top Section)** Located at the top of the screen, this section contains the Brand dropdown selector. Brand selection determines all subsequent availability, pricing, and product options throughout the booking process.

**2. Customer Details Section** Positioned below Brand selection, this area captures primary customer information including mobile number, name, email, and date of birth. The system performs customer lookup based on mobile number and creates new customer records when necessary.

**3. Passenger Configuration Panel** Located in the left column, this section defines the passenger composition including counts for adults, children, and infants. Passenger counts drive pricing calculations and availability searches.

**4. Transport Selection Area** The Transport section displays selected departure information and provides access to the transport search dialog. This area shows departure date, gateway details, transport codes, and stay duration.

**5. Hotel Selection Area** Positioned below Transport, this section displays chosen accommodation including hotel name, resort, room type, and board basis. The hotel search function is accessed from this area.

**6. Passenger Information Grid** The central section contains a detailed grid with one row per passenger. Each row includes fields for title, first name, last name, date of birth, extras selection, and discount/supplement assignment. This grid supports inline editing and bulk operations.

**7. Booking Totals Panel (Right Side)** A persistent panel on the right displays real-time pricing information including total amount, base price, discounts, and profit margin. This panel also shows booking metadata such as booking number, status, user, and confirmation flags.

**8. Action Buttons (Bottom)** The bottom of the screen contains primary action buttons including Save, Save Passenger, Take Allotment, Import Passengers, and Cancel Passenger or Booking.

### Field Description

This section provides comprehensive descriptions of all fields available in the New Booking interface. Fields are organized by the screen section in which they appear.

#### Brand Selection Section

**Brand**

* **Field Type:** Dropdown selector
* **Mandatory:** Yes
* **Description:** Selects the brand under which the booking will be created. The Brand determines all available products, pricing rules, allotment pools, email templates, payment methods, and business logic applied to the booking.
* **System Behavior:** Changing the Brand after selections have been made will reset all booking data and require reselection of transport, hotel, and passengers.
* **Related Functionality:** Links to Brand configuration in System Setup. Affects Transport availability, Hotel options, Price List rules, Discount eligibility, and Customer segmentation.
* **Data Source:** Active brands configured in Brand Management with user access permissions.

#### Customer Details Section

**Mobile Number**

* **Field Type:** Text input (phone number format)
* **Mandatory:** Yes
* **Description:** Primary customer contact number used for customer identification and communication. The system searches existing customers by mobile number. If no match is found, a new customer record is created.
* **Format Requirements:** Accepts international format with country code prefix.&#x20;
* **System Behavior:** On blur, the system queries the Customer database. If a match is found, customer details auto-populate. If no match exists, the interface enables creation of a new customer record.
* **Related Functionality:** Links to Customer Management module. Triggers customer history lookup. Affects SMS notification delivery and customer communication preferences.

**Email**

* **Field Type:** Text input (email format)
* **Mandatory:** Yes
* **Description:** Customer email address for booking confirmations, tickets, and communication.
* **Format Requirements:** Must contain valid email format (local@domain.ext). Validates format before save.
* **System Behavior:** Used as primary delivery address for booking confirmations and electronic tickets.
* **Related Functionality:** Links to Email Center for communication. Affects ticket delivery method. Integrates with automated email workflows.

**Date of Birth**

* **Field Type:** Date picker
* **Mandatory:** Conditional (required if "Mandatory DOB in Passenger Details in BackOffice" is enabled in Brand settings)
* **Description:** Customer date of birth. When provided, this value automatically populates to the lead passenger row in the passenger grid upon saving.
* **Format Requirements:** DD-MM-YYYY format. Must represent a date in the past.
* **System Behavior:** Upon booking save, the system copies this value to the first passenger's DOB field. Affects age-based pricing for the lead passenger. Used for passenger data validation.
* **Related Functionality:** Links to Passenger Details. Affects child pricing thresholds. Integrates with airline passenger data requirements (APIS).

**First Name**

* **Field Type:** Text input
* **Mandatory:** Yes (when creating new customer)
* **Description:** Customer given name. Populates from existing customer record or entered manually for new customers.
* **Format Requirements:** Alphabetic characters, hyphens, and spaces accepted. Maximum length typically 50 characters.
* **System Behavior:** Auto-fills from customer database if mobile number matches existing record. Transfers to lead passenger if passenger import is not used.
* **Related Functionality:** Links to Customer Database. Appears on booking confirmations and travel documents.

**Last Name**

* **Field Type:** Text input
* **Mandatory:** Yes (when creating new customer)
* **Description:** Customer family name or surname. Populates from existing customer record or entered manually for new customers.
* **Format Requirements:** Alphabetic characters, hyphens, and spaces accepted. Maximum length typically 50 characters.
* **System Behavior:** Auto-fills from customer database if mobile number matches existing record. Transfers to lead passenger if passenger import is not used.
* **Related Functionality:** Links to Customer Database. Appears on booking confirmations and travel documents.

#### Passenger Configuration Section

**Adults**

* **Field Type:** Numeric input spinner
* **Mandatory:** Yes&#x20;
* **Description:** Number of adult passengers (typically age 12+, exact threshold defined in Brand configuration). Determines pricing calculation, allotment consumption, and passenger grid rows.
* **Value Range:** Minimum 1, Maximum defined by system configuration (typically 99).
* **System Behavior:** Changing this value recalculates pricing, updates passenger grid rows, and validates against available allotment. Adult count affects room allocation logic and transport seat assignment.
* **Related Functionality:** Links to Price List age-based pricing rules. Affects Transport allotment validation. Integrates with Hotel room capacity calculations.

**Children**

* **Field Type:** Numeric input spinner
* **Mandatory:** No (default 0)
* **Description:** Number of child passengers. Child age ranges are defined in Brand configuration (typically 2-11 years). Children receive age-appropriate pricing and may have different allotment rules.
* **Value Range:** Minimum 0, Maximum defined by system configuration.
* **System Behavior:** Adding children creates additional passenger grid rows. System applies child pricing from Price List. Child allocation must comply with room occupancy rules (beds available, extra bed policies).
* **Related Functionality:** Links to Child Pricing configuration. Affects Price List discount calculations. Integrates with Hotel bed configuration and room capacity rules.

**Infants**

* **Field Type:** Numeric input spinner
* **Mandatory:** No (default 0)
* **Description:** Number of infant passengers (typically under 2 years old). Infants typically do not consume hotel bed allocation and receive minimal or zero pricing.
* **Value Range:** Minimum 0, Maximum defined by system configuration.
* **System Behavior:** Infants do not reduce available allotment in most configurations. Infant pricing rules are applied from Price List. Infants do not receive cancellation fees when bookings are cancelled.
* **Related Functionality:** Links to infant pricing rules in Price List. Does not consume hotel bed inventory. May affect airline ticketing requirements.

#### Transport Selection Section

**Transport Edit Button**

* **Field Type:** Button
* **Mandatory:** Yes (transport selection required for package bookings)
* **Description:** Opens the Transport Search dialog allowing users to search available departures and select transport for the booking.
* **System Behavior:** Clicking this button displays the Select Transport modal dialog with availability search filters and results table.
* **Related Functionality:** Links to Transport Management module. Accesses Transport Allotment data. Integrates with GDS systems if configured.

#### Transport Search Dialog Fields

**From (Date Range)**

* **Field Type:** Date picker
* **Mandatory:** Yes
* **Description:** Start date for transport departure search range. The system returns all transport departures departing on or after this date.
* **Format Requirements:** Date format follows system locale settings. Must be current date or future date.
* **System Behavior:** Combined with "To" date to define search window. Affects which transport options appear in results table.
* **Related Functionality:** Filters Transport Departure data. Links to Transport Schedule configuration.

**To (Date Range)**

* **Field Type:** Date picker
* **Mandatory:** Yes
* **Description:** End date for transport departure search range. The system returns all transport departures departing on or before this date.
* **Format Requirements:** Date format follows system locale settings. Must be equal to or after "From" date.
* **System Behavior:** Defines upper boundary of search window. Results include all departures between From and To dates inclusive.
* **Related Functionality:** Filters Transport Departure data. Links to Transport Schedule configuration.

**Departure Gateway**

* **Field Type:** Dropdown selector
* **Mandatory:** No (defaults to All)
* **Description:** Filters transport search results to show only departures from the selected airport or gateway.
* **Data Source:** Active departure gateways configured in Gateway Management.
* **System Behavior:** When selected, only transports departing from this gateway appear in results. Leave empty to search all departure gateways.
* **Related Functionality:** Links to Departure Gateway configuration. Integrates with Route Management.

**Arrival Gateway**

* **Field Type:** Dropdown selector
* **Mandatory:** No (defaults to All)
* **Description:** Filters transport search results to show only arrivals at the selected destination airport or gateway.
* **Data Source:** Active arrival gateways configured in Gateway Management.
* **System Behavior:** When selected, only transports arriving at this gateway appear in results. Leave empty to search all arrival gateways.
* **Related Functionality:** Links to Arrival Gateway configuration. Integrates with Route Management.

**Transport code**

* **Field Type:** Text input
* **Mandatory:** No
* **Description:** Allows searching for a specific transport code to narrow results. Transport codes are unique identifiers assigned to each scheduled departure.
* **System Behavior:** When provided, filters results to show only transports matching the entered code. Supports partial matching.
* **Related Functionality:** Links to Transport configuration. Transport codes are defined in Transport Management module.

**Period**

* **Field Type:** Text input
* **Mandatory:** No
* **Description:** Optional field for searching transports based on predefined period intervals configured in system setup.
* **System Behavior:** When used, overrides From/To date range with period-based search logic.
* **Related Functionality:** Links to Period configuration in System Setup.

**Search waitlist also**

* **Field Type:** Checkbox
* **Mandatory:** No (default unchecked)
* **Description:** When enabled, includes transports with zero available allotment in search results. These transports can be booked as waitlist reservations.
* **System Behavior:** Checking this option displays transports marked as sold out or waitlisted. Waitlist bookings require manual confirmation when inventory becomes available.
* **Related Functionality:** Links to Waitlist Management. Integrates with allotment monitoring and waitlist confirmation workflows.

**Clear Button**

* **Field Type:** Button
* **Mandatory:** No
* **Description:** Resets all filter fields in the transport search dialog to default values.
* **System Behavior:** Clicking Clear removes all entered search criteria, allowing users to start a new search.

**Search Button**

* **Field Type:** Button (primary action)
* **Mandatory:** Yes (to execute search)
* **Description:** Executes the transport availability search based on selected filter criteria and displays results in the transport list table.
* **System Behavior:** Queries Transport database with filter parameters. Populates results table with matching departures. Displays availability and allotment information.
* **Related Functionality:** Queries Transport Allotment system. Checks Stop Sale flags. Validates Brand access permissions.

#### Transport Search Results Table Columns

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

**Status Column**

* **Field Type:** Visual indicator (color bar)
* **Mandatory:** Display only
* **Description:** Color-coded status indicator showing transport availability level. Different colors represent various availability states (ample availability, limited seats, waitlist, stop sale).
* **System Behavior:** Updates in real-time based on current allotment levels. Color scheme is configured in system settings.
* **Related Functionality:** Links to Allotment thresholds. Visual representation of Transport availability status.

**Date Column**

* **Field Type:** Date display
* **Mandatory:** Display only
* **Description:** Departure date of the transport in DD-MM-YYYY format or configured locale format.
* **System Behavior:** Displays the scheduled departure date from Transport configuration.

**Day Column**

* **Field Type:** Text display
* **Mandatory:** Display only
* **Description:** Day of the week for the departure date (e.g., Monday, Tuesday).
* **System Behavior:** Calculated from the Date field. Helps users quickly identify departure patterns.

**Departure Column**

* **Field Type:** Text display
* **Mandatory:** Display only
* **Description:** Departure gateway code or airport code where transport originates.
* **System Behavior:** Displays gateway code from Transport route configuration.
* **Related Functionality:** Links to Departure Gateway master data.

**Arrival Column**

* **Field Type:** Text display
* **Mandatory:** Display only
* **Description:** Arrival gateway code or airport code where transport terminates.
* **System Behavior:** Displays gateway code from Transport route configuration.
* **Related Functionality:** Links to Arrival Gateway master data.

**Transport Column**

* **Field Type:** Text display (hyperlink)
* **Mandatory:** Display only
* **Description:** Transport code identifier. This unique code represents the specific transport departure.
* **System Behavior:** May be clickable to view detailed transport information. Code format defined in Transport Management.
* **Related Functionality:** Links to Transport Details page. Transport codes are configured in Transport Management module.

**Type Column**

* **Field Type:** Text display
* **Mandatory:** Display only
* **Description:** Transport type code indicating the category of transport (e.g., C for charter, D for scheduled).
* **System Behavior:** Displays transport classification from Transport configuration.
* **Related Functionality:** Transport types defined in Transport Type configuration.

**Stay Column**

* **Field Type:** Numeric display
* **Mandatory:** Display only
* **Description:** Number of nights associated with the transport departure. Represents the standard stay duration for this departure.
* **System Behavior:** Calculated from Transport configuration. Affects hotel booking duration when transport is selected.
* **Related Functionality:** Links to Transport Stay Days configuration. Affects hotel search results and pricing periods.

**ALI 1, ALI 2, ALI 3, ALI 4 Columns**

* **Field Type:** Numeric display
* **Mandatory:** Display & selector&#x20;
* **Description:** Allotment capacity per allotment group. Shows available seats/capacity for up to four different allotment categories.
* **System Behavior:** Displays current available allotment from Allotment Management system. Values decrease as bookings consume inventory.
* **Related Functionality:** Links to Allotment Groups configuration. Real-time inventory display updated as bookings are created.

**OW OUT / OW HOME Columns**

* **Field Type:** Numeric display
* **Mandatory:** Display & selector
* **Description:** One-way outbound and one-way homebound availability. Shows capacity for passengers booking single-leg transport.
* **System Behavior:** Displays one-way availability separate from round-trip allotment.
* **Related Functionality:** Supports One-Way booking functionality. Links to Transport configuration for one-way rules.

**ALL. EXT. PROD. Column**

* **Field Type:** Numeric display with hover tooltip
* **Mandatory:** Display only
* **Description:** Allotment Extra Product. Shows additional allotment quantities that may be available beyond standard allotments.
* **System Behavior:** Hovering over this field displays detailed breakdown of extra product allotments.
* **Related Functionality:** Links to Extra Product Allotment configuration.

**Flight Number Column**

* **Field Type:** Text display
* **Mandatory:** Display only (if applicable)
* **Description:** Actual airline flight number when transport is operated by commercial airline. Empty for other transport types.
* **System Behavior:** Displays flight number from Transport configuration. Used for passenger documentation and airline integration.
* **Related Functionality:** Links to airline flight data. Used in GDS integrations and passenger manifest generation.

**Stop Sale Column**

* **Field Type:** Icon/text indicator
* **Mandatory:** Display only
* **Description:** Indicates if a stop sale is active for this transport, preventing new bookings.
* **System Behavior:** Displays warning icon or text when stop sale flag is set. Transport cannot be selected for new bookings when stop sale is active.
* **Related Functionality:** Links to Stop Sale management. Configured in Transport Stop Sale settings.

**Select Button**

* **Field Type:** Button (row action)
* **Mandatory:** Yes (to choose transport)
* **Description:** Selects the transport in the corresponding row and applies it to the booking.
* **System Behavior:** Clicking Select closes the transport search dialog and populates the Transport section with selected departure details. Triggers hotel availability search with matching date range.
* **Related Functionality:** Consumes transport allotment when booking is saved. Updates Transport selection in booking.

#### Transport Duration Field

**Trip Interval**

* **Field Type:** Numeric input
* **Mandatory:** Yes (after transport selection)
* **Description:** Duration of the trip in days (nights). Defines the length of stay at the destination and affects hotel booking period.
* **Value Range:** Minimum 1, maximum typically limited by transport configuration (e.g., 1-28 days).
* **System Behavior:** Setting trip interval calculates the return transport date based on outbound departure + interval days. Affects hotel night calculations and pricing.
* **Related Functionality:** Links to Transport Stay Days. Affects hotel availability search dates. Determines pricing period in Price List.

#### Hotel Selection Section

**Hotel Edit Button**

* **Field Type:** Button
* **Mandatory:** Yes (hotel selection required for package bookings)
* **Description:** Opens the Hotel Search dialog allowing users to search available accommodation and select hotel and room type for the booking.
* **System Behavior:** Clicking this button displays the Select Hotel modal dialog with hotel filters and availability results.
* **Related Functionality:** Links to Hotel Management module. Accesses Hotel Allotment and room availability data.

#### Hotel Search Dialog Filter Fields

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

**Resort**

* **Field Type:** Dropdown selector
* **Mandatory:** No (defaults to All Resorts)
* **Description:** Filters hotel search results to show only properties located in the selected resort area.
* **Data Source:** Active resorts configured in Resort Management linked to the selected destination.
* **System Behavior:** When selected, only hotels within the chosen resort appear in results. Leave as "All Resorts" to view hotels across all resort areas.
* **Related Functionality:** Links to Resort configuration. Resorts are defined in Setup module.

**Hotel**

* **Field Type:** Dropdown selector
* **Mandatory:** No (defaults to All Hotels)
* **Description:** Filters search results to show a specific hotel property.
* **Data Source:** Active hotels configured in Hotel Management with availability for the selected travel period.
* **System Behavior:** When selected, displays only the chosen hotel with its available room types. Used for direct hotel selection when hotel is known.
* **Related Functionality:** Links to Hotel Management. Shows hotels with active contracts for the Brand and period.

**Stars**

* **Field Type:** Multi-select dropdown
* **Mandatory:** No
* **Description:** Filters hotels by star rating category. Multiple star ratings can be selected simultaneously.
* **Data Source:** Star ratings configured in hotel master data (typically 2-star through 5-star).
* **System Behavior:** When selections are made, only hotels matching the selected star categories appear in results. Leave empty to show all star ratings.
* **Related Functionality:** Links to Hotel star rating classification in Hotel Management.

**Pension**

* **Field Type:** Multi-select dropdown
* **Mandatory:** No
* **Description:** Filters available board types (meal plans) such as Bed & Breakfast, Half Board, Full Board, All Inclusive.
* **Data Source:** Board types configured in Board Type Management and available in hotel contracts.
* **System Behavior:** When selections are made, only room/board combinations matching the selected pension types appear. Leave empty to show all board types.
* **Related Functionality:** Links to Board Type configuration. Board types are defined in Extras Setup module.

**Show only free rooms**

* **Field Type:** Checkbox
* **Mandatory:** No
* **Description:** When enabled, displays only hotel rooms with available allotment greater than zero.
* **System Behavior:** Checking this option filters out sold-out rooms, showing only bookable inventory. Improves search results by removing unavailable options.
* **Related Functionality:** Queries Hotel Allotment system. Links to room availability calculations.

**Display all rooms**

* **Field Type:** Checkbox
* **Mandatory:** No
* **Description:** When enabled, shows all configured rooms regardless of availability status, including sold-out options.
* **System Behavior:** Overrides "Show only free rooms" filter. Useful for viewing complete hotel inventory even when sold out.
* **Related Functionality:** Displays all Hotel Rooms configured in Hotel Management.

**Display Names**

* **Field Type:** Checkbox
* **Mandatory:** No
* **Description:** Toggles between displaying hotel names or hotel codes in the results table.
* **System Behavior:** When checked, shows full hotel names. When unchecked, displays hotel codes. User preference for viewing results.
* **Related Functionality:** Affects display format of Hotel column in results table.

**Display PriceList Hotel Names**

* **Field Type:** Checkbox
* **Mandatory:** No
* **Description:** When enabled, displays hotel names as defined in the Price List configuration rather than hotel master data names.
* **System Behavior:** Useful when Price List uses different naming conventions or marketing names for hotels. Shows customer-facing names.
* **Related Functionality:** Links to Price List Hotel Name configuration.

#### Hotel Search Results Table Columns

**Status Column (Hotel Results)**

* **Field Type:** Visual indicator (icon)
* **Mandatory:** Display only
* **Description:** Color-coded availability status indicator for the hotel/room combination. Indicates inventory levels or special conditions.
* **System Behavior:** Visual representation of room availability status. Colors indicate ample availability, limited inventory, or special conditions.
* **Related Functionality:** Links to room allotment thresholds.

**Hotel Column**

* **Field Type:** Text display
* **Mandatory:** Display and clickable (show hotel description)
* **Description:** Hotel code or name depending on "Display Names" filter setting. Identifies the accommodation property.
* **System Behavior:** Shows hotel identifier from Hotel Management. Format controlled by display filters.
* **Related Functionality:** Links to Hotel master data record.

**Stars Column**

* **Field Type:** Visual display (star icons)
* **Mandatory:** Display only
* **Description:** Graphical representation of hotel star rating classification (e.g., ★★★★ for 4-star).
* **System Behavior:** Displays star classification from Hotel configuration. Provides quick visual quality indicator.
* **Related Functionality:** Star rating configured in Hotel Management.

**Resort Column**

* **Field Type:** Text display
* **Mandatory:** Display only
* **Description:** Resort code indicating the geographic area or resort location of the hotel.
* **System Behavior:** Shows resort classification from Hotel configuration.
* **Related Functionality:** Links to Resort master data.

**Room Column**

* **Field Type:** Text display
* **Mandatory:** Display only
* **Description:** Room type and board type description. Combines room category with meal plan information.
* **System Behavior:** Displays room type name and pension type from Hotel configuration. Format: "Room Type - Board Type" (e.g., "Double Room - Half Board").
* **Related Functionality:** Links to Room Type configuration and Board Type settings.

**MB Column (Minimum Beds)**

* **Field Type:** Numeric display
* **Mandatory:** Display only
* **Description:** Minimum number of beds or occupancy required for the room type.
* **System Behavior:** Shows minimum occupancy from Room Type configuration. Affects passenger allocation validation.
* **Related Functionality:** Links to Hotel room capacity rules.

**XB Column (Extra Beds Adults)**

* **Field Type:** Numeric display
* **Mandatory:** Display only
* **Description:** Number of extra beds available for adult passengers beyond minimum occupancy.
* **System Behavior:** Shows extra bed capacity from Room Type configuration. Allows exceeding minimum occupancy with additional charges.
* **Related Functionality:** Links to Extra Bed pricing rules and room capacity configuration.

**XB CH Column (Extra Beds Children)**

* **Field Type:** Numeric display
* **Mandatory:** Display only
* **Description:** Number of extra beds available specifically for child passengers.
* **System Behavior:** Shows child extra bed capacity from Room Type configuration. May have different pricing than adult extra beds.
* **Related Functionality:** Links to child extra bed pricing and room capacity rules.

**Avail. Column**

* **Field Type:** Numeric display
* **Mandatory:** Display only
* **Description:** Available allotment count for the hotel/room combination during the selected period.
* **System Behavior:** Displays current available rooms from Hotel Allotment system. Updates in real-time as bookings are made. Shows minimum availability across all nights in the booking period.
* **Related Functionality:** Links to Hotel Allotment Management. Availability calculated from allotment data.

**P1 Column (Price Interval 1)**

* **Field Type:** Currency display
* **Mandatory:** Display only
* **Description:** Price per person for the first pricing interval configured in the Price List.
* **System Behavior:** Shows pricing from Price List for the standard interval. Currency format follows system configuration.
* **Related Functionality:** Links to Price List configuration. Pricing calculated based on duration and passenger composition.

**D1 / G1 Columns**

* **Field Type:** Currency display
* **Mandatory:** Display only
* **Description:** Discount price (D1) or Group price (G1) per person for the first interval. Alternative pricing tiers available in Price List.
* **System Behavior:** Shows reduced pricing when discount or group rates are configured. May be empty if no alternative pricing exists.
* **Related Functionality:** Links to Price List discount and group pricing rules.

**N, D, G Selection Checkboxes**

* **Field Type:** Radio button group or checkbox
* **Mandatory:** Yes (one must be selected)
* **Description:** Selects the pricing tier for the booking: N (Normal Price), D (Discount Price), or G (Group Price).
* **System Behavior:** Only one option can be selected per hotel row. Selection determines which price is applied to the booking. Available options depend on Price List configuration.
* **Related Functionality:** Links to Price List price type configuration.

**Magic Stick Icon (Pencil Icon)**

* **Field Type:** Action icon button
* **Mandatory:** No
* **Description:** Allows manual reset or adjustment of the free room count for the hotel/room combination.
* **System Behavior:** Clicking this icon opens a dialog to modify availability or reset allotment counts. Used for manual inventory adjustments.
* **Related Functionality:** Links to Hotel Allotment management. Requires appropriate user permissions.

**Select Button (Hotel Results)**

* **Field Type:** Button
* **Mandatory:** Yes (to choose hotel)
* **Description:** Selects the hotel and room combination in the corresponding row and applies it to the booking.
* **System Behavior:** Clicking Select closes the hotel search dialog and populates the Hotel section with selected accommodation details. Enables the Take Allotment button.
* **Related Functionality:** Prepares hotel selection for allotment consumption. Updates Hotel display in booking interface.

#### Take Allotment Button

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

**Take Allotment**

* **Field Type:** Button (primary action)
* **Mandatory:** Yes (to reserve inventory)
* **Description:** Reserves the selected transport and hotel inventory for the booking. This action commits the available allotment to this booking and triggers pricing calculation.
* **System Behavior:** Clicking this button consumes allotment from Transport and Hotel pools, calculates total booking price including all discounts and supplements, and updates the Total Amount display in real-time. All auto-selected extras and passenger age adjustments are included in the calculation.
* **Related Functionality:** Links to Allotment Management system. Updates inventory levels. Triggers Price List calculation. Activates passenger information grid for editing.

#### Passenger Information Grid

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

The passenger grid contains one row per passenger. Each row includes multiple fields for passenger details, extras selection, and pricing.

**Passenger Row Number**

* **Field Type:** Display only (sequential number)
* **Mandatory:** Display only
* **Description:** Row number indicating passenger sequence (1, 2, 3, etc.). The first row represents the lead passenger.
* **System Behavior:** Automatically numbered based on passenger count. Lead passenger (row 1) receives special treatment for customer data transfer.

**Gender/Title**

* **Field Type:** Dropdown selector
* **Mandatory:** Yes
* **Description:** Passenger title or gender designation (e.g., MR, MS, MRS, MSTR, MISS).
* **Data Source:** Title options configured in system setup.
* **System Behavior:** Required for all passengers. Used in documentation and passenger manifests. May affect airline booking requirements.
* **Related Functionality:** Links to passenger documentation generation. Required for travel documents.

**First Name (Passenger)**

* **Field Type:** Text input
* **Mandatory:** Yes
* **Description:** Given name of the passenger. Must match travel document exactly when required for airline bookings.
* **Format Requirements:** Alphabetic characters, hyphens, apostrophes, spaces accepted. Maximum length typically 50 characters. No special characters.
* **System Behavior:** For lead passenger (row 1), auto-populated from Customer Details when Date of Birth is saved. Other passengers require manual entry unless using passenger import.
* **Related Functionality:** Links to passenger manifest generation. Appears on tickets and vouchers. May be validated against passport data for international flights.

**Last Name (Passenger)**

* **Field Type:** Text input
* **Mandatory:** Yes
* **Description:** Family name or surname of the passenger. Must match travel document exactly when required for airline bookings.
* **Format Requirements:** Alphabetic characters, hyphens, apostrophes, spaces accepted. Maximum length typically 50 characters. No special characters.
* **System Behavior:** For lead passenger (row 1), auto-populated from Customer Details when Date of Birth is saved. Other passengers require manual entry unless using passenger import.
* **Related Functionality:** Links to passenger manifest generation. Appears on tickets and vouchers. May be validated against passport data for international flights.

**Date of Birth (Passenger Grid)**

* **Field Type:** Date picker
* **Mandatory:** Yes (for accurate age-based pricing)
* **Description:** Passenger date of birth. Used to determine passenger category (adult, child, infant), apply age-based pricing, and validate travel requirements.
* **Format Requirements:** DD-MM-YYYY format. Must represent a date in the past.
* **System Behavior:** Age is automatically calculated from DOB. Age determines pricing category. For lead passenger, auto-populated from Customer Details DOB field when booking is first saved. System recalculates pricing when DOB is changed.
* **Related Functionality:** Links to age threshold configuration in Brand settings. Affects Price List calculations. Required for airline passenger data (APIS). Determines child/infant categorization.

**Extras Columns (Per Category)**

* **Field Type:** Dropdown selector (multiple columns)
* **Mandatory:** No (depends on extras configuration)
* **Description:** Each column represents an Extras Category (e.g., Insurance, Transfer, Baggage, Ski Rental). Users select extras from the dropdown for each passenger.
* **Data Source:** Active extras configured in Extras Management for the selected Brand, filtered by eligibility rules and availability.
* **System Behavior:** Selecting an extra immediately updates the Total Amount calculation. Some extras may be auto-selected based on configuration. Yellow "C" icon allows applying the same extra to all eligible passengers. Price of each extra is added to passenger total. Extras with day-based pricing show day count in parentheses.
* **Related Functionality:** Links to Extras configuration. Pricing calculated from Extras price rules. Affects final booking total. Integrates with Extra Product inventory if applicable.
* **Sorting Behavior:** When "Order extras in the booking window" is enabled in System Setup, extras categories are displayed according to the Category Order Booking value defined in each category. Categories with order < 10 appear before TRANSPORT. Categories with order 10-19 appear before HOTEL and ROOM. Categories with order ≥ 20 appear after HOTEL and ROOM. Categories without order values appear last. Categories with the same order number are sorted alphabetically.

**Yellow "C" Icon (Copy to All)**

* **Field Type:** Action icon button
* **Mandatory:** No
* **Description:** Appears in the header of extras columns. Clicking this icon applies the same extra to all eligible passengers in the booking.
* **System Behavior:** Copies the extra selected in one passenger row to all other passenger rows where the extra is eligible. Useful for group bookings where all passengers need the same extras. Total Amount updates with all additions.
* **Related Functionality:** Links to Extras eligibility rules. Respects age restrictions and other applicability criteria.

**Show/Hide Discount/Supplements Button**

* **Field Type:** Toggle button
* **Mandatory:** No
* **Description:** Expands or collapses the discount and supplement section for each passenger.
* **System Behavior:** Clicking reveals additional columns for discount and supplement selection. Default state is typically hidden to reduce visual complexity.
* **Related Functionality:** Links to Discount/Supplement configuration.

**Add Discount/Supplement Button**

* **Field Type:** Button
* **Mandatory:** No
* **Description:** Opens a dialog to select and apply discounts or supplements to one or all passengers.
* **System Behavior:** Clicking displays available discounts and supplements based on booking eligibility. Multiple discounts/supplements can be selected simultaneously. Selected items are added to the passenger row and price is recalculated.
* **Related Functionality:** Links to Discounts/Supplements configuration. Affects Price List calculations. Updates Total Amount in real-time.

**Discount/Supplement Selection Fields**

* **Field Type:** Dropdown selectors or checkboxes
* **Mandatory:** No
* **Description:** Individual fields for selecting discounts (price reductions) and supplements (price additions) per passenger.
* **Data Source:** Active discounts and supplements configured in Disc/Suppl management, filtered by eligibility rules.
* **System Behavior:** Selecting a discount reduces the passenger total. Selecting a supplement increases the passenger total. Changes immediately affect Total Amount display. Multiple discounts and supplements can be combined if configuration allows.
* **Related Functionality:** Links to Discount/Supplement rules and pricing. May affect profit margin calculations. Integrates with campaign and promotional pricing.

**Save Passenger Button**

* **Field Type:** Button (per-row action)
* **Mandatory:** Yes (to commit passenger changes)
* **Description:** Saves all changes made to the passenger row including name, DOB, extras, and discounts/supplements.
* **System Behavior:** Clicking Save Passenger validates passenger data, commits changes to the booking record, recalculates pricing if needed, and updates the booking state. Changes are not persisted until this button is clicked.
* **Related Functionality:** Updates passenger data in booking database. Triggers validation rules. May send notifications if configured.

#### Booking Totals Panel

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

The Booking Totals panel is located on the right side of the screen and displays financial and metadata information for the booking.

**Total Amount (Expanded Section)**

* **Field Type:** Currency display (expandable section)
* **Mandatory:** Display only
* **Description:** The final selling price of the booking after all discounts are applied. This is the amount the customer pays. Displayed prominently in green highlight.
* **System Behavior:** Updates in real-time as selections are made (transport, hotel, extras, discounts, supplements). Recalculates immediately when passenger age changes, extras are added/removed, or discounts are applied. Does not require Save Passenger or Save to update.
* **Related Functionality:** Calculated from Price List, discount rules, supplement rules, and extra pricing. Represents customer invoice amount.

**Price**

* **Field Type:** Currency display
* **Mandatory:** Display only (visible when Total Amount section is expanded)
* **Description:** Base price before discounts are applied. Includes transport, hotel, extras, and supplements at full price.
* **System Behavior:** Visible when the Total Amount section is expanded. Shows the gross price before discount reductions.
* **Related Functionality:** Calculated from Price List and extras pricing.

**Discount**

* **Field Type:** Currency display
* **Mandatory:** Display only (visible when Total Amount section is expanded)
* **Description:** Sum of all discounts applied to the booking. Includes hotel price list discounts and passenger-level discounts.
* **System Behavior:** Visible when the Total Amount section is expanded. Shows the total value of price reductions.
* **Related Functionality:** Calculated from discount rules and price list adjustments.

**Total Profit**

* **Field Type:** Currency display
* **Mandatory:** Display only (visible when Total Amount section is expanded)
* **Description:** The profit margin earned on the booking. Calculated as selling price minus supplier costs (transport cost, hotel cost, extras cost).
* **System Behavior:** Visible when the Total Amount section is expanded. Only displays after the full booking is saved. Updates after costs are finalized.
* **Related Functionality:** Calculated from supplier cost configuration, profit margin rules, and negotiated rates.

**Booking Number**

* **Field Type:** Display only (text)
* **Mandatory:** Display only
* **Description:** Unique identifier assigned to the booking upon first save. Format may include sub-booking indicators (e.g., "3633 + 1" where "+1" indicates a sub-booking).
* **System Behavior:** Generated automatically when booking is first saved. Permanent identifier used in all booking-related operations and communications.
* **Related Functionality:** Links booking to payment records, customer history, and system logs. Referenced in booking searches.

**Status**

* **Field Type:** Display only (text/badge)
* **Mandatory:** Display only
* **Description:** Current state of the booking (e.g., OK, Pending, Cancelled, Waitlist).
* **System Behavior:** Updates based on booking operations (save, cancel, payment, confirmation). Color-coded for visual identification.
* **Related Functionality:** Affects booking processing workflows. Determines available actions. Linked to status-based automation rules.

**User**

* **Field Type:** Display only (text)
* **Mandatory:** Display only
* **Description:** System username of the person who created the booking. Identifies the responsible agent or sales person.
* **System Behavior:** Set automatically when booking is created based on logged-in user. Cannot be changed after creation.
* **Related Functionality:** Links to user permissions and sales reporting. Used in commission calculations.

**Added**

* **Field Type:** Display only (date/time)
* **Mandatory:** Display only
* **Description:** Date and time when the booking was first created in the system.
* **System Behavior:** Timestamp recorded when booking is first saved. Used for reporting and audit purposes.
* **Related Functionality:** Links to booking history. Used in analytics and reporting.

**Updated**

* **Field Type:** Display only (date/time)
* **Mandatory:** Display only
* **Description:** Date and time of the most recent modification to the booking.
* **System Behavior:** Updates automatically whenever the booking is saved with changes.
* **Related Functionality:** Links to booking history log. Tracks booking modification timeline.

**Is Group Booking**

* **Field Type:** Checkbox
* **Mandatory:** No
* **Description:** Flags the booking as a group reservation. Affects processing, reporting, and may trigger group-specific business rules.
* **System Behavior:** When checked, the booking is classified as a group booking. May affect allotment rules, pricing, and workflow processes.
* **Related Functionality:** Links to group booking management. May affect reporting categories.

**Remember Extras**

* **Field Type:** Checkbox
* **Mandatory:** No
* **Description:** When enabled, selected extras are saved as preferences for future modifications or related bookings.
* **System Behavior:** Checking this option stores the current extra selections for recall in future operations.
* **Related Functionality:** Links to user preferences and booking templates.

**Hotel Confirmed**

* **Field Type:** Checkbox
* **Mandatory:** No
* **Description:** Indicates whether the accommodation portion of the booking has been confirmed with the hotel supplier.
* **System Behavior:** Manual flag used to track confirmation status. May be set automatically by system integrations or manually by users.
* **Related Functionality:** Links to hotel confirmation workflows. May affect notification rules and reporting.

**Transfer Confirmed**

* **Field Type:** Checkbox
* **Mandatory:** No
* **Description:** Indicates whether transport/transfer services have been confirmed with suppliers.
* **System Behavior:** Manual flag used to track confirmation status. May be set automatically by system integrations or manually by users.
* **Related Functionality:** Links to transport confirmation workflows. May affect notification rules and reporting.

#### Action Buttons (Bottom Section)

**Save Button**

* **Field Type:** Button (primary action)
* **Mandatory:** Yes (to finalize booking)
* **Description:** Saves the complete booking including all passenger details, selected services, and pricing. Commits the booking to the database and releases allotment.
* **System Behavior:** Clicking Save validates all required fields, generates a booking number (if first save), commits all data to the database, consumes allotment from inventory pools, triggers email notifications (if configured), and closes the New Booking screen. If validation fails, displays error messages indicating required corrections.
* **Related Functionality:** Updates Allotment system. Creates customer booking record. Triggers Email Center for "Thank you for booking" email if configured. Integrates with payment processing. Note: If "Don't send ticket" is selected before first save, the automatic "Thank you for booking" email is suppressed.

**Import Passengers Button**

* **Field Type:** Button
* **Mandatory:** No
* **Description:** Opens the passenger import dialog allowing bulk upload of passenger data from an Excel file.
* **System Behavior:** Clicking displays the import interface where users can upload Excel files containing passenger information. Validates file format and data. Maps passenger details to booking. Supports partial imports (fewer passengers than booking total).
* **Related Functionality:** Links to passenger import functionality. Supports Excel file format (.xlsx). Validates passenger data against business rules. Allows specification of extras and day-based products in import file.

**Cancel Passenger or Booking Button**

* **Field Type:** Button (destructive action)
* **Mandatory:** No
* **Description:** Initiates cancellation of one or more passengers or the entire booking. Located in bottom-right corner of Passenger section.
* **System Behavior:** Clicking displays a dialog with cancellation options: Cancel Passenger (removes selected passengers) or Cancel Entire Booking (removes all passengers and services). Applies cancellation rules and fees. Releases allotment for cancelled passengers. Recalculates pricing. Updates booking status. Requires confirmation before proceeding.
* **Related Functionality:** Links to Cancellation Rules. Affects allotment recovery. Triggers refund processing. Updates booking history. Note: Allotment is not automatically reduced; manual intervention required in Edit Passenger and Take Allotment to update.

### Configuration Steps

This section provides numbered technical procedures for creating a new booking in Tourpaq

#### Creating a Standard Package Booking

This part covers the complete workflow for creating a typical package booking with transport and hotel.

**Step 1: Access New Booking Interface**

1. Log in to Tourpaq Office with valid credentials
2. Navigate to the main menu bar at the top of the screen
3. Click the **Booking** menu item
4. Select **New Booking** from the dropdown menu
5. The New Booking screen opens as a modal overlay

***

**Step 2: Select Brand**

1. Locate the Brand dropdown at the top of the New Booking screen
2. Click the dropdown to display available brands
3. Select the appropriate Brand under which the booking will be created

<figure><img src="../../../.gitbook/assets/image (518).png" alt="Select Brand in New Booking"><figcaption></figcaption></figure>

***

**Step 3: Enter Customer Details**

1. Enter the customer's mobile number in the **Mobile Number** field
2.  Press Tab or click outside the field to trigger customer lookup&#x20;

    <figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>
3. If customer exists:
   * Customer details (name, email, DOB) auto-populate
   * Verify the details are correct
4. If customer does not exist:
   * System prompts for new customer creation
   * Enter **First Name** in the provided field
   * Enter **Last Name** in the provided field
   * Enter **Email** address (mandatory if Brand configuration requires it)
   * Enter **Date of Birth** in DD-MM-YYYY format (mandatory if Brand configuration requires it)

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Booking cannot proceed until required fields are completed.

When:

* A Date of Birth is entered in Customer Details
* And the booking is saved

Then:

*   The DOB is automatically inserted into the lead passenger row in the Pax grid.

    <figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



5. Verify all mandatory fields are completed (indicated by system validation)

***

**Step 4: Configure Passenger Composition**

1. Locate the Passenger Configuration panel on the left side
2. Set the number of **Adults** using the spinner control or direct numeric entry (minimum 1 required)
3. Set the number of **Children** if applicable (default 0)
4. Set the number of **Infants** if applicable (default 0)
5. Verify total passenger count is correct
6. System validates passenger counts against maximum limits

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

**Step 5: Search and Select Transport**

1. Locate the Transport section in the booking interface
2. Click the **Edit** button in the Transport section
3. The Select Transport dialog opens
4. Configure search filters:&#x20;

&#x20;            a. Set **From** date by clicking the date picker and selecting the earliest acceptable departure date&#x20;

&#x20;            b. Set **To** date by clicking the date picker and selecting the latest acceptable departure date c. Optional: Select **Departure Gateway** from dropdown to filter by origin airport d. Optional: Select **Arrival Gateway** from dropdown to filter by destination airport e. Optional: Enter **Transport code** to search for specific transport f. Optional: Check **Search waitlist also** to include sold-out transports

1. Click the **Search** button to execute the search
2. Review search results in the transport list table:
3. Check **Date** column for departure date
4. Review **ALI 1-4** columns for available allotment
5. Check **Status** column color indicator for availability level
6. Review **Flight Number** if airline transport
7. Verify **Stop Sale** column shows no stop sale indicator
8. Select the desired transport by clicking the **Select** button in the appropriate row
9. The Select Transport dialog closes
10. Transport details populate in the Transport section
11. Set the **Trip Interval** (stay duration in days) in the field provided
12. System calculates return date based on departure + interval

The **Select Transport** dialog is your **transport availability search**. Use it to find and select a transport (flight, bus, or other transport types) for the booking. It supports filters and a result table with departures in the selected date range.

**Filter section**

At the top of the dialog, users can refine the search using the following filters:

**Date range**

* **From** – Start date for the search period.
* **To** – End date for the search period.

The system returns all transports departing between these two dates.

**Gateways**

* **Departure Gateway** – Filters transports that depart from a specific gateway/airport.
* **Arrival Gateway** – Filters transports that arrive at a selected gateway/airport.

**Transport code**

* Input for narrowing results to a specific transport code (e.g., flight code).

**Period**

* Optional field used for searching transports based on a predefined period/interval.

**Additional options**

* **Search waitlist also** – Includes transports that have no available allotment and are in waitlist mode.
* **Clear** – Resets all filters.

**Search button**

* Executes the search based on the selected filters.

**Transport list table**

The lower section shows all matching transport departures. Each row represents a transport option and contains the following columns:

| Column               | Description                                                      |
| -------------------- | ---------------------------------------------------------------- |
| **Status**           | Visual indicator of availability (color bar).                    |
| **Date**             | Departure date of the transport.                                 |
| **Day**              | Corresponding weekday (e.g., Monday).                            |
| **Departure**        | Departure gateway/airport.                                       |
| **Arrival**          | Arrival gateway/airport.                                         |
| **Transport**        | Transport code (e.g., flight code).                              |
| **Type**             | Transport type (e.g., C, D).                                     |
| **Stay**             | Number of nights associated with that transport.                 |
| **ALI 1–ALI 4**      | Allotment capacity per allotment group.                          |
| **OW OUT / OW HOME** | One-way out and one-way home availability.                       |
| **ALL. EXT. PROD.**  | Allotment Extra Product (hover to see the number of allotments). |
| **Flight Number**    | Actual flight number (if applicable).                            |
| **Stop Sale**        | Shows if stop sale is active for this transport.                 |
| **Select**           | Button used to choose this transport for the booking.            |

The table supports vertical scrolling when many departures are available.

**Selecting a transport**

1.  Click **Edit** in the **Transport** section.

    <figure><img src="../../../.gitbook/assets/image (514).png" alt=""><figcaption></figcaption></figure>
2. Select the **Period** (departure/arrival range) to check availability.
3. Click **Search** to retrieve available transports.
   * Each result includes **transport allotment** and a hoverable popup showing extra quotas.
4.  Select the desired **transport**.

    <figure><img src="../../../.gitbook/assets/image (516).png" alt=""><figcaption></figcaption></figure>
5.  Set the **trip interval** (duration in days).

    <figure><img src="../../../.gitbook/assets/image (517).png" alt=""><figcaption></figcaption></figure>

***

#### Step 5 – Add hotel & room

The **Select Hotel** dialog is your **hotel and room availability** search. Use it to filter hotels by resort, star rating, board type (pension), and room availability. Then select a hotel/room line and **take allotment**.

<figure><img src="../../../.gitbook/assets/image (511).png" alt=""><figcaption></figcaption></figure>

**Filter options**

The top section contains multiple filters:

* **Resort** – Dropdown for selecting a specific resort or viewing _All Resorts_.
* **Hotel** – Dropdown for selecting a specific hotel or viewing _All Hotels_.
* **Stars** – Multi-select dropdown for filtering by hotel star rating.
* **Pension** – Multi-select dropdown for filtering available board types.

Additional checkboxes allow further control:

* **Show only free rooms** – Displays only rooms with availability.
* **Display all rooms** – Shows all rooms regardless of availability.
* **Display Names** – Toggles between hotel names and internal codes.
* **Display PriceList Hotel Names** – Shows the hotel names defined in the price list.

**Hotel list table**

The main table lists hotels that match the selected filter criteria. Each row represents a hotel/room combination and displays the following information:

| Column              | Description                                                                       |
| ------------------- | --------------------------------------------------------------------------------- |
| **Status**          | Indicates availability status with color-coded icons.                             |
| **Hotel**           | Code or name of the hotel, depending on filter settings.                          |
| **Stars**           | Star classification displayed visually.                                           |
| **Resort**          | Code of the resort.                                                               |
| **Room**            | Room type or board type description.                                              |
| **MB / XB / XB CH** | Capacity fields and extra bed rules (Minimum Beds, Extra Beds Adults/Children).   |
| **Avail.**          | Availability count for the selected period.                                       |
| **P1**              | Price per interval 1.                                                             |
| **D1 / G1**         | Discount or group price per interval.                                             |
| **N, D, G**         | Selection options (checkboxes) for Normal Price, Discount Price, and Group Price. |
| **Magic Stick**     | Pencil icon allowing reset of free room count.                                    |

A **Select** button in the top-right corner becomes active when a hotel/room line is chosen. The user can confirm the selection and return to the booking flow.

<figure><img src="../../../.gitbook/assets/image (512).png" alt=""><figcaption></figcaption></figure>

**Workflow – selecting a hotel**

1. Open the **Select Hotel** dialog by clicking **Select Hotel** in the booking.
2. (Optional) Apply filters:
   * Resort
   * Hotel
   * Stars
   * Pension
   * Availability and display options
3. Review the filtered hotel list and scroll if needed.
4. Click the desired hotel/room line to highlight it.
5. Click **Select** in the upper-right corner of the dialog.
6. Continue the booking process and proceed to **Take allotment**.

**Take allotment**

<figure><img src="../../../.gitbook/assets/image (513).png" alt=""><figcaption></figcaption></figure>

After the user selects **Take Allotment**, the system updates the **Total Amount** immediately. The calculation includes:

* All applicable **discounts** and **supplements**.
* **Auto-selected extras** and all extras added manually by the user for every passenger.
* **Passenger age** adjustments.

***

#### Step 6 – Passenger information

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

1. Edit **Passenger details**:

* Gender, First Name, Last Name, Age.

{% hint style="info" %}
When:

* A Date of Birth is entered in Customer Details
* And the booking is saved

Then:

* The DOB is automatically inserted into the lead passenger row in the Pax grid.
{% endhint %}

* Add **Extras**:
  * Per passenger, or use the yellow **C** icon to apply extras to all eligible passengers.
    * If the "Order extras in the booking window" option is activated in the system setup, the extras will be sorted according to the Category Order value.

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Sorting rules

Categories are sorted as follows:

1. Categories with **Category order booking < 10**\
   Displayed before TRANSPORT
2. Categories with **Category order booking between 10 and 19**\
   Displayed before HOTEL and ROOM
3. Categories with **Category order booking ≥ 20**\
   Displayed after HOTEL and ROOM
4. Categories **without a Category order booking value**\
   Displayed last
5. Categories with the **same order number**\
   Sorted alphabetically

* If the "Order extras in the booking window" option is not enabled in the system setup, the new extras will be arranged according to the old ordering :

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

1. Add **Discounts/Supplements**:
   * Click **Show/Hide Discount/Supplements**.
   * Click **Add Discount/Supplement**.
   * Select available options for one or all passengers.
   * Multiple discounts or supplements can be added simultaneously.
2. Click **Save Passenger** to save changes.

{% hint style="success" %}
The **Total Amount** updates instantly whenever the user modifies any passenger-related information:

* Selecting or unselecting **supplements** or **discounts**.
* Selecting or unselecting **extras**.
* Changing the **passenger’s age**.

All changes are reflected immediately in the price.
{% endhint %}

***

#### Step 7 – Booking totals

The **Booking panel** provides a quick summary of financial details, booking metadata, and status indicators for a reservation. It is used by staff to monitor pricing, profitability, and the confirmation state of related services (hotel, transfer, etc.).

The **Total Amount** always reflects the user’s latest selections. The price includes all eligible **discounts**, **supplements**, **auto-selected extras**, and any **age-based price adjustments**.

The system continuously recalculates the Total Amount as the user interacts with the booking. The displayed price always reflects the current state of the booking and does not wait for **Save Passenger** or **Save** to trigger updates.

<figure><img src="../../../.gitbook/assets/image (507).png" alt=""><figcaption></figcaption></figure>

**Field explanations**

**Financial summary (green area)**

* **Total amount** – The final selling price of the booking (after discounts).
* **Price** – Price without discounts, including extras, supplements, etc.
* **Discount** – The sum of discounts on the hotel, price list adjustments, and the discounts added to each passenger.
* **Total Profit** – The margin earned after subtracting supplier costs from the selling price.

{% hint style="success" %}
The **Total Profit** is displayed when expanding the green area that shows the Total Amount, and it will be shown after the full booking is saved.
{% endhint %}

**Booking details**

* **Booking Number** – The unique identifier for the booking. Example: `3633 + 1` (the `+1` indicates a sub-booking).
* **Status** – The current state of the booking (e.g., _OK_, _Pending_, _Cancelled_).
* **User** – The system user or agent who created/owns the booking.
* **Added** – The date when the booking was created.
* **Updated** – The date when the booking was last modified.

**Flags (checkbox options)**

* **Is Group Booking** – Indicates if the booking is part of a group reservation.
* **Remember Extras** – Ensures that selected extras are saved for future modifications.
* **Hotel Confirmed** – Marks whether the accommodation portion of the booking has been confirmed.
* **Transfer Confirmed** – Marks whether the transport/transfer services have been confirmed.

***

#### Step 8 – Finalize booking

1. Review all booking details (transport, hotel, passengers, extras, economics).
2. Click **Save** to complete the booking.
3. Send the ticket:
   * If you have configured a ‘Thank you for booking’ email the system will automatically send. In the Email Center, you have the option to delay sending an email.

{% hint style="warning" %}
Note: If “Don’t send ticket” is selected on a new booking before saving the booking for the first time, the customer will not receive the “Thank you for booking” email.
{% endhint %}

***

#### Step 9 – Cancel passenger or booking

The **Cancel passenger or booking** button allows users to cancel an entire booking or remove individual passengers from a booking, depending on the situation. It is located at the bottom-right corner of the **Booking → Overview → Passengers** section.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Overview**

This feature gives booking administrators full control over cancellations. Depending on the configuration of the booking and the selected passenger, the system will:

* Cancel **one or more passengers**, or
* Cancel the **entire booking**, if all passengers are selected or if cancellation rules require a full cancellation.

The function ensures that all transport, hotel, extras, and supplements connected to the passenger(s) are removed or recalculated correctly.

**Purpose**

Use this button when:

* A traveler drops out of the trip.
* A booking needs to be partially canceled.
* A booking must be fully canceled, including all passengers and services.

**How it works**

**1. Select passenger(s)**

* If one passenger is selected → the system cancels only that passenger.
* If all passengers are selected or the booking contains only one passenger → the system offers a **full booking cancellation**.

**2. Click the button**

Click **Cancel passenger or booking** in the bottom-right corner.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**3. Choose the cancellation type**

A dialog will appear asking you to choose between:

* **Cancel Passenger**
* **Cancel Entire Booking**

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The available options depend on the structure of the booking.

**4. Confirm cancellation**

After confirming, Tourpaq:

* Removes all services connected to the cancelled passenger(s).
* Recalculates pricing.

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Updates allotment, transport seats, extras, and commissions.
  * The allotment is **not** updated automatically. If the number of passengers in the booking is not manually reduced, Tourpaq will automatically insert a **TBA passenger** to occupy the seat or room left vacant by the cancelled guest. This ensures the booking maintains its original capacity, and the cancelled space is not released back into the available allotment.
  * This step requires manual intervention by the sales user in **Edit Passenger** and then **Take Allotment** to update it.
* Marks the booking or passenger as _Cancelled_.

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Expected behavior**

**Cancel passenger**

The system will:

* Remove all services (transport, hotel, extras, insurance, supplements) tied to the passenger.
* Update price calculations.
* Preserve remaining passengers and services.
* Require manual allotment update:
  * In the **Passenger** box, change the number of passengers in the booking.
  * Click **Take Allotment**.
  * Save the booking.
* Keep the booking active if at least one passenger remains.

**Cancel entire booking**

The system will:

* Remove all passengers and services.
* Release all allotments.
* Update all connected modules (Transport, Hotel, GDS, Extras, etc.).
* Mark the booking as _Cancelled_.
* Trigger relevant notifications if configured.

**Warnings & notes**

* **Cancellation rules apply** – If cancellation rules or charges are configured for the brand, they will be applied automatically.
* **Manual actions may be needed** – If external systems (e.g., GDS, API) are used, check if manual cancellation is required outside Tourpaq.
* **Bonus codes/discounts** – Removing a passenger may change eligibility for discounts, supplements, or bonuses. Recalculation happens automatically.

**Cancellation rules**

When a booking is cancelled, a **cancellation fee** is set for each passenger. Cancellation rules are applied for calculating this fee. The fee is calculated taking into account the remaining days left to departure.

<figure><img src="../../../.gitbook/assets/image (556).png" alt=""><figcaption></figcaption></figure>

* If cancellation insurance is paid, when cancelling the passengers you can choose whether the insurance **covers** the booking or **does not cover** the booking.
* If cancellation insurance is paid and **Cover** is selected, the amount of the cancellation fee will be the cancellation insurance.
* If cancellation insurance is paid and **Does not cover** is selected, the cancellation fee will contain the price of the cancellation insurance and the amount set in cancellation rules.
* Infants do not get a cancellation fee.

You can also adjust the cancellation amount applied to the booking. This can be done by selecting **Edit Passenger** and then updating the value under **Total per passenger**. This allows you to manually modify the cancellation fee when needed.

<figure><img src="../../../.gitbook/assets/image (557).png" alt=""><figcaption></figcaption></figure>

***

<img src="../../../.gitbook/assets/file.excalidraw (1).svg" alt="" class="gitbook-drawing">

### Live price updates (user experience)

Users always see the correct **Total Amount** without needing to save the passenger or the booking. This live update behavior ensures:

* Accurate and transparent pricing.
* Immediate feedback when modifying selections.
* A smoother and more predictable booking process.

The system provides a responsive and reliable pricing experience, matching the user’s actions in real time.

***

### Advanced features

#### Import passengers (optional)

The Passenger Import functionality support improved flexibility and efficiency when managing large groups.

The system:

* Allow importing fewer passengers than the total number of passengers in the booking
* Support specifying ski rental and other day-based extras directly in the Excel import file
* Allow removal of automatically assigned extras during import
* Reduce the need for manual adjustments, such as adding placeholder passengers.

#### Specification

#### 1. Support for Day-Based Extras (e.g. Ski Rental)

The import file support specifying extras that include a number of days.

These are extras configured in **Prices** with defined “days”.

Behavior:

* The Excel file allow specifying:
  * Extra name or identifier
  * Number of days (if applicable)
* The system assign the extra to the passenger with the correct number of days
* The pricing logic follow the configured extra rules

This enables specifying ski rental and similar products directly during import.

<figure><img src="../../../.gitbook/assets/image (676).png" alt=""><figcaption></figcaption></figure>

***

#### 2. Support for Removing Selected Extras per Passenger

The import file support removal of extras at passenger level.

Behavior:

* If the Excel file contains **"N/A"** in the Extra column for a passenger:
  * All selected products within the specified Extra Category will be removed for that passenger
* This applies even if the extra was automatically added to the booking

<figure><img src="../../../.gitbook/assets/image (677).png" alt=""><figcaption></figcaption></figure>

Example use case:

* Baggage is automatically added to the first two passengers
* A passenger doesn't need baggage
* Excel file specifies "N/A" in Bagage category
* System removes the Bagage for that passenger

This gives full control over passenger-level extra allocation.

***

#### 3. Import with Fewer Lines Than Booking Passengers

The system supports importing a file where the number of rows is lower than the number of passengers in the booking.

Behavior:

* If the import file contains **X rows**
* The data applied to the **top X passengers** in the booking
* Remaining passengers remain unchanged

<figure><img src="../../../.gitbook/assets/image (678).png" alt=""><figcaption></figcaption></figure>

***

#### 4. Group Growth Scenario Support

It must be possible to:

* Create a booking with a larger reserved group size
* Import only the currently confirmed passengers
* Add additional passengers later via subsequent imports

***

You can import multiple passengers via an **Excel file**.

**Accepted file format**

* Only **Excel files (.xlsx)** are supported.
* Required static columns:
  * `TITLE`, `F NAME`, `L NAME`, `DATE OF BIRTH`.
* Optional static columns:
  * `CCL. INS.`, `INSURANCE`.
* Dynamic columns:
  * Each column must match the **Extras Category Name**.
  * Values must be **Extras Codes**.

**Static columns**

The columns **TITLE**, **F NAME**, **L NAME**, and **DATE OF BIRTH** must always be included in the import file and must match the exact names specified. The optional columns **CCL. INS.** and **INSURANCE** may be included if applicable but are not required.

| Column name       | Description                                                                           |
| ----------------- | ------------------------------------------------------------------------------------- |
| **TITLE**         | The title of the passenger. This must be a value selected from a dropdown list.       |
| **F NAME**        | The first name of the passenger. Any string value is acceptable.                      |
| **L NAME**        | The last name of the passenger. Any string value is acceptable.                       |
| **DATE OF BIRTH** | The passenger’s date of birth in the format `dd-mm-yyyy`.                             |
| **CCL. INS.**     | The cancellation insurance for the passenger. This should be a value from a dropdown. |
| **INSURANCE**     | The travel insurance code for the passenger. This should be a value from a dropdown.  |

**Dynamic columns (extras)**

Dynamic columns allow additional optional information about passenger extras. Each dynamic column corresponds to an **Extras Category Name** (case-insensitive) and requires the corresponding **Extras Code** value.

| Field                    | Description                                                                                   |
| ------------------------ | --------------------------------------------------------------------------------------------- |
| **Extras Category Name** | Name as in the table header (must match category name).                                       |
| **Extras Code**          | The code(s) selected from the dropdown, separated by commas (optional). It can be left empty. |

Example usage:

| Column name           | Value                        |
| --------------------- | ---------------------------- |
| **EXTRAS\_CATEGORY1** | `EXTRAS_CODE`                |
| **EXTRAS\_CATEGORY2** | `EXTRAS_CODE1, EXTRAS_CODE2` |
| **EXTRAS\_CATEGORY3** | _(empty)_                    |

**Import behavior**

1. If the import **fails**:
   * All changes to the passengers will be **reverted**.
2. If the import **succeeds with warnings**:
   * Rows with warnings are **highlighted** with a specific color.
   * An **info icon** appears for these rows, displaying all warnings as a tooltip.

Common warnings include:

* The selected category is not available for selection.
* The selected extra is not available for the category.
* Cancellation insurance is not available for selection.
* Travel insurance is not available for selection.
* This category does not support multiselect (only the first value from the list is used).

![](https://docs.tourpaq.com/assets/images/row_with_warnings-19946acdb755f600a02305f2edcef55e.png?width=1754)

An example file for importing passengers can include columns in the following format:

<table><thead><tr><th width="82.4444580078125"></th><th width="93.5555419921875"></th><th width="99.111083984375"></th><th width="118"></th><th width="78"></th><th></th><th width="153.5555419921875"></th><th></th></tr></thead><tbody><tr><td>TITLE</td><td>F NAME</td><td>L NAME</td><td>DATE OF BIRTH</td><td>CCL. INS.</td><td>INSURANCE</td><td>Multiple-EC</td><td>BAGGAGE</td></tr><tr><td>MR</td><td>TBA1</td><td>TBA1</td><td>19-11-1988</td><td>399</td><td>X</td><td>Multiple-P1 [4D], Multiple-P1 [3D]</td><td>BAG-20</td></tr><tr><td>MS</td><td>TBA2</td><td>TBA2</td><td>03-01-1926</td><td></td><td></td><td>Multiple-P1 [3D]</td><td>N/A</td></tr></tbody></table>

#### Package products

When selecting a product that is flagged as a **package** for a passenger, all products that are inside the package are selected (after saving the passenger) with a price of `0`. Only the package itself has the price set.

For a product to be set as **package**, you need to check the option inside **Edit Product Page → Basic Setup → Other Settings → Package Type**.

![](https://docs.tourpaq.com/assets/images/package_and_product_example-fb064df3c22226835850f8ad23aef525.png?width=1645)

For a product to be set as a **content type of a package**, you need to check the option inside **Edit Product Page → Basic Setup → Other Settings → Content Type**.

![](https://docs.tourpaq.com/assets/images/package_and_product_example-fb064df3c22226835850f8ad23aef525.png?width=1645)

You can modify the products that are inside the package in **Edit Product Page → Package Content** tab.

![](https://docs.tourpaq.com/assets/images/package_and_product_example3-83e4c48b16f44d9028b8a8ffcff1d567.png?width=1665)

**Warning messages**

*   If you select the **package**, you cannot select the products inside the package as well. You will get a warning message like this:

    ![](https://docs.tourpaq.com/assets/images/package_and_product_warning-ecd616e463d185d98ad5ac65be13b1a3.png?width=1797)
*   All products inside the package must be **eligible** for the package to be selected. If they are not all eligible, you will get this warning message:

    ![](https://docs.tourpaq.com/assets/images/package_and_product_warning_2-182f4c506926ede24ffbcb6c77f7a3c9.png?width=1809)

***

### FAQ

#### 1. Why can’t I find any transports or hotels for my dates?

Check the following:

* The **date range** is correct and within valid travel periods for the Brand.
* You selected the correct **departure** and **arrival gateways** (for transport).
* You did **not** filter away options with too strict **Resort/Hotel/Stars/Pension** filters.
* Valid **allotments** and **price lists** exist for the chosen period.

If nothing appears after widening the filters, the issue is usually missing setup (allotment or prices) for that Brand/period.

#### 2. What happens if I change the number of passengers after I have taken allotment?

If you change the **passenger count** after pressing **Take Allotment**:

* You must adjust passengers in **Passenger information**.
* You may need to press **Take Allotment** again so transport and hotel allotments match the new number.
* Prices and discounts will be recalculated automatically.

Always review the **Booking totals** after changing passenger numbers.

#### 3. When should I use the passenger import feature instead of adding passengers manually?

Use **Import passengers** when:

* You have many passengers (e.g. groups) and data already exists in a spreadsheet.
* You want to pre‑assign **extras**, **insurances**, or other products per passenger via dynamic columns.

For 1–3 passengers it is usually faster to add them manually.

#### 4. Why does the Total Amount differ from what the customer saw on WebBooking?

Possible reasons include:

* Different **Brand** or **sales channel** settings.
* Additional **discounts/supplements** applied in the office booking.
* Manual changes to **extras**, **room type**, or **transport** in New Booking.

Compare:

* Selected **transport, hotel, room, and board**.
* Applied **discounts/supplements** in passenger details.
* Any office‑only products or rules.

If everything matches but the price still differs, contact your internal pricing or system administrator to review the configuration.

### **Related pages**

Use these pages when you need to go beyond the initial booking draft:

* [New Booking (overview)](../) — Section entry point and related booking flows.
* [New Booking search support](new-booking-search-support.md) — Extra help for transport/hotel search and selection.
* [Edit Passenger](edit-passenger/) — Add/remove passengers and update pax data after saving.
* [Economics](../economics.md) — Deposits, instalments, payment status, refunds, and payment methods.
* [Print Tickets](../../../tickets/print-tickets.md) — Print/email ticket PDFs and bulk reprint.
* [Don’t send ticket option](../dont-sent-ticket-option.md) — Avoid sending automatic update emails while editing.
* [Waiting list (WL)](../waitting-list.md) — Handle sold-out departures/rooms with WL/WLOK statuses.
* [Cancellation Rules](../../../cancellation-rules.md) — How cancellation fees are calculated and applied.
