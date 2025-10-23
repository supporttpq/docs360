---
description: >-
  Here’s a structured documentation page designed to help to understand and
  implement or work with the Export Module in Tourpaq Office. This guide
  includes an overview, purpose, precondition.
---

# Export

### ✅ Overview

Tourpaq Office supports exporting structured data for various business roles: hotel suppliers, guides, transport managers, and reporting personnel. Exports are generated in **Excel-compatible XML format** and are filtered based on **date intervals**, **transport**, **resorts**, **hotels**, and more.

***

### 🎯 Purpose

The export module was designed to:

* Provide relevant, filtered data to external partners.
* Support integration with other systems via structured XML.
* Enable custom exports per business role (guides, suppliers, managers).
* Track changes to bookings over time for transparency and operations tracking.

***

### ⚙️ Preconditions

Before generating an export:

* User must be authenticated with export permissions.
* Bookings, transports, hotels, and related data must be available in the system.
* The export templates must be configured in the system backend.
* Optional: Booking history tracking must be enabled for change logs.

***

### 🧩 Export Types & Explanation

#### 1. **Hotel List Export**

* **Goal**: Provide hotel partners with grouped booking summaries.
* **Grouped by**: Hotel → Stay interval → Room type → Booking
* **Columns**:
  * Holiday interval (stay period)
  * Room code and name
  * Room units booked
  * Passenger count
  * Booking number and booking date
* **Header**: Includes agency info, supplier contact, hotel name/code, export date
* **Footer**: Total number of passengers for the hotel

***

#### 2. **Rooming List Export**

* **Goal**: Detailed room assignments and passenger-level data
* **Grouped like hotel list**, with additional fields:
  * Passenger name, gender, age
  * Flight in/out numbers
  * Room number inside booking
  * Optional company-specific columns:
    * Extra pension/car/VIP/tours
* **Used by**: Hotel front desk, logistics, on-site coordinators

***

#### 3. **Guide List Export**

* **Goal**: Help guides prepare for on-the-ground operations
* **Grouping**: Hotel → Stay period → Room type → Booking
* **Columns**:
  * All rooming list data +
  * Transfer status
  * Insurance code
  * Contact info (email, phone)
  * Guest comments (preferences, feedback)
  * Supplements selected

***

#### 4. **Passenger List Export**

* **Goal**: Provide a clean list of passengers for a stay period
* **Grouped by**: Transport interval → Hotel
* **Header**: Shows used filters (country, resort, flight)
* **Columns**:
  * Stay period
  * Hotel code/name
  * Booking info
  * Passenger details
  * Transfer presence
* **Footer**:
  * Totals by transport (with breakdown by age)
  * Totals by hotel
  * Totals by transfer presence

***

#### 5. **Canceled Booking Export**

* **Goal**: Show all canceled bookings (excluded from other exports)
* **Grouped by**: Hotel → Stay period → Room type
* **Columns**:
  * Stay interval
  * Room code and name
  * Booked units
  * Passenger count
  * Booking number and name
  * Cancellation date

***

#### 6. **Bookings Change List Export**

* **Goal**: Track all significant booking changes since a selected date
* **New Filter**: `Changes From` (start date for change log)
* **Types of Changes**:
  * **New bookings**: Created or changed from ERROR to OK
  * **Canceled bookings**: Changed from OK to ERROR (excluding transient or reverted changes)
  * **Modified bookings**: Any updates to hotel, room, passenger, period, etc.
* **Data Grouping**:
  * Hotel → Stay period → Booking
* **Columns per change**:
  * Booking no., date
  * Change date
  * Change type
  * Old value (From) & new value (To)
  * Element code/name if available
* **Passenger-level changes include**:
  * Gender, age, name updates
  * Transfer added/removed
  * Discounts or extras (car, pension, VIP, etc.)

***

### 🔍 Export Filters (All Templates)

| Filter                           | Description                                                                |
| -------------------------------- | -------------------------------------------------------------------------- |
| **Agency / Brand**               | Limits exports to one or more agencies                                     |
| **Arrival Date Interval**        | Bookings where the stay begins within this period                          |
| **Booking Date Interval**        | Bookings created in this period                                            |
| **Report Type**                  | Choose from hotel list, rooming, guide, passenger, canceled, change list   |
| **Transport**                    | Multi-select filter by travel options used                                 |
| **Country / Resort**             | Filter by destination country or specific resort(s)                        |
| **Hotel**                        | Export only data related to selected hotels                                |
| **Cancellation Date (Optional)** | Only for canceled exports; limits results to bookings canceled in range    |
| **Changes From**                 | Specific to Change List; defines starting point for change history logging |

***

### 📦 Notes & Special Behaviors

* **Repeatable blocks**: Many exports (hotel, rooming, guide) are structured in repeatable XML blocks per hotel.
* **Optional company fields**: Some exports include dynamic columns depending on company settings (e.g. VIP codes, party package names).
* **Passenger focus**: Passenger exports are ungrouped, flat listings with optional statistical footers.
* **Error state**: Bookings in `ERROR` status are conditionally included depending on context (e.g. revalidated as OK or canceled).

***

### 🧠 Tips for Developers

* Use XML templates with clear structure and schema validation.
* Booking history module must track every relevant field for change logs to be accurate.
* Pay attention to status transitions: `ERROR` ↔ `OK` define inclusion/exclusion in exports.
* Many exports share structure logic (inherit or reuse parsers where possible).
* Data anomalies usually stem from edge cases in booking status transitions or outdated rules.
