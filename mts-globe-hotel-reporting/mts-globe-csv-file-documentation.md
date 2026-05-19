# MTS Globe CSV File Documentation

### Overview

<figure><img src="../.gitbook/assets/19.05.2026_15.48.27_REC.png" alt=""><figcaption></figcaption></figure>

This file contains booking-related information that is sent to MTS Globe for hotel reporting purposes. The report includes:

* Passenger information
* Booking references
* Travel dates
* Product information
* Flight details
* Pricing information
* Notes and operational details

The file format is CSV (Comma-Separated Values) and is designed to support automated processing by external supplier systems.

***

## Purpose

The purpose of this file is to:

* Share booking information with MTS Globe
* Report hotel reservations and related services
* Provide passenger and operational travel details
* Support supplier handling and operational workflows
* Synchronize booking information between Tourpaq and MTS Globe

***

## File Structure

### File Type

CSV (Comma-Separated Values)

### Example File Name

* BRAV\_new\_20250925.csv

***

## File Content Overview

The file contains one row per booking service or booking item.

A single booking reference may appear multiple times when:

* Multiple services exist
* Transfers are included
* Hotel and transport services are separated
* Additional booking components are reported individually

***

## Column Documentation

| Column              | Description                                 | Example                 | Purpose                            |
| ------------------- | ------------------------------------------- | ----------------------- | ---------------------------------- |
| Office              | Internal office code generating the booking | LPA                     | Identifies the operational office  |
| Distributor         | Distributor or supplier code                | BRAV                    | Identifies the booking distributor |
| Brand               | Brand associated with the booking           | BRAV                    | Used for brand segmentation        |
| Reference           | Booking reference number                    | AZH16FZ4VQC             | Unique booking identifier          |
| Pax Name            | Main passenger name                         | KOLEN, ROSA JOHANNA     | Primary booking passenger          |
| ADT                 | Number of adults                            | 3                       | Total adult passengers             |
| Additional Adults   | Additional adult passenger names            | KOLEN, ROSITA JOHANNES  | Additional travellers              |
| Adult\_Ages         | Ages of adult passengers                    | 58,68,48                | Passenger age information          |
| CHD                 | Number of children                          | 2                       | Total child passengers             |
| CHD Ages            | Ages of children                            | 7,8                     | Child age information              |
| Child Names         | Names of children                           | Example Child Name      | Child passenger details            |
| INF                 | Number of infants                           | 0                       | Total infant passengers            |
| Infant Names        | Infant passenger names                      | Example Infant          | Infant details                     |
| Book Date           | Booking creation date                       | 2025-09-20              | Date the booking was created       |
| Start Date          | Service or travel start date                | 2025-09-25              | Arrival or service start           |
| End Date            | Service or travel end date                  | 2025-10-02              | Departure or service end           |
| P.Type              | Product type                                | HOTEL / TRANSFER        | Identifies service category        |
| P.Code              | Product code                                | HTL001                  | Supplier product code              |
| Unit                | Room or service unit                        | DBL                     | Operational unit information       |
| Base                | Board basis or service basis                | HB                      | Accommodation basis                |
| PickUpDropOff Hotel | Pickup or dropoff hotel                     | Hotel Example           | Transfer hotel information         |
| DropOffInterTf      | Transfer indicator                          | YES / NO                | Operational transfer handling      |
| Flight Airline      | Airline code                                | FR                      | Passenger flight airline           |
| Flight No           | Flight number                               | FR1234                  | Flight identification              |
| Flight DEP Airport  | Departure airport                           | WAW                     | Passenger departure airport        |
| Flight ARR Airport  | Arrival airport                             | LPA                     | Passenger arrival airport          |
| Flight DEP TIME     | Flight departure time                       | 05:00                   | Scheduled departure time           |
| Flight ARR TIME     | Flight arrival time                         | 13:00                   | Scheduled arrival time             |
| AGENT               | External booking agent                      | Example Agent           | Agent or reseller                  |
| Cost                | Supplier cost amount                        | 800.00                  | Internal supplier cost             |
| Cost Currency       | Currency of supplier cost                   | EUR                     | Supplier cost currency             |
| Price               | Sales price amount                          | 980.00                  | Customer sales price               |
| Price Currency      | Currency of sales price                     | EUR                     | Sales currency                     |
| Note                | Operational booking note                    | Non-smoking room please | Supplier or operational comments   |
| Quantity            | Quantity of booked services                 | 1                       | Number of booked units             |

***

## Detailed Field Explanations

### Office

Represents the internal operational office responsible for the booking.

Example:

* LPA

This value is used for operational segmentation and reporting.

***

### Distributor

Defines the distributor or supplier group related to the booking.

Example:

* BRAV

This field is commonly used for partner identification.

***

### Reference

The unique booking identifier.

Example:

* AZH16FZ4VQC

This reference is critical for:

* Booking tracking
* Amendments
* Cancellation handling
* Supplier synchronization

***

### Passenger Information

The file supports multiple passenger categories:

#### Adults

* ADT
* Additional Adults
* Adult\_Ages

#### Children

* CHD
* CHD Ages
* Child Names

#### Infants

* INF
* Infant Names

This structure allows suppliers to:

* Prepare accommodation allocations
* Validate occupancy
* Handle operational requirements

***

### Travel Dates

#### Book Date

Represents when the booking was originally created.

#### Start Date

Represents the beginning of the service period.

#### End Date

Represents the end of the service period.

These fields are essential for:

* Hotel operations
* Availability checks
* Transfer coordination
* Reporting schedules

***

### Product Information

#### P.Type

Defines the type of service being reported.

Examples:

* HOTEL
* TRANSFER
* EXTRA

#### P.Code

Supplier or internal product code.

#### Unit

Represents the booked room or service unit.

#### Base

Defines the board basis or package basis.

Examples:

* BB (Bed & Breakfast)
* HB (Half Board)
* AI (All Inclusive)

***

### Flight Information

Flight information supports transfer coordination and operational planning.

Included fields:

* Flight Airline
* Flight No
* Flight DEP Airport
* Flight ARR Airport
* Flight DEP TIME
* Flight ARR TIME

This information is especially important for:

* Airport transfers
* Arrival coordination
* Departure handling

***

### Pricing Information

#### Cost

Internal supplier cost.

#### Price

Customer-facing sales price.

#### Currency Fields

The file stores currencies separately for:

* Cost
* Price

This supports:

* Multi-currency operations
* Financial reporting
* Supplier reconciliation

***

### Operational Notes

The Note field contains operational or supplier-specific instructions.

Example:

> Non-smoking room on the first floor please

This information may include:

* Room requests
* Operational comments
* Supplier instructions
* Customer preferences

***

## Booking Row Behavior

### Multiple Rows per Booking

The same booking reference may appear multiple times.

This usually happens when:

* Multiple products exist
* Transfers are included
* Different service components are exported separately

Example:

| Reference   | Product Type       |
| ----------- | ------------------ |
| AZH16FZ4VQC | HOTEL              |
| AZH16FZ4VQC | ARRIVAL TRANSFER   |
| AZH16FZ4VQC | DEPARTURE TRANSFER |

***

## Reporting Categories

The CSV structure supports three reporting types:

| Report Type        | Purpose                       |
| ------------------ | ----------------------------- |
| New Bookings       | Newly created bookings        |
| Amended Bookings   | Updated bookings              |
| Cancelled Bookings | Cancelled or removed bookings |

***

## Operational Usage

The CSV file can be used for:

* Supplier communication
* Hotel rooming lists
* Transfer coordination
* Operational reconciliation
* Financial validation
* Booking synchronization

***

## Validation Recommendations

When generating or validating the CSV file, verify:

* Booking references are unique and valid
* Passenger counts match names provided
* Flight information is complete when transfers exist
* Currency fields are populated correctly
* Dates are formatted consistently
* Mandatory operational fields are not empty

***

## Example Record

| Field              | Example Value                              |
| ------------------ | ------------------------------------------ |
| Office             | LPA                                        |
| Distributor        | BRAV                                       |
| Reference          | AZH16FZ4VQC                                |
| Pax Name           | KOLEN, ROSA JOHANNA                        |
| ADT                | 3                                          |
| CHD                | 2                                          |
| Start Date         | 2025-09-25                                 |
| End Date           | 2025-10-02                                 |
| Flight DEP Airport | WAW                                        |
| Flight ARR Airport | LPA                                        |
| Cost               | 800.00                                     |
| Price              | 980.00                                     |
| Note               | Non-smoking room on the first floor please |

***

## Summary

The MTS Globe CSV file is a structured booking export used for supplier communication and operational synchronization.

The format includes:

* Passenger information
* Booking references
* Product details
* Travel dates
* Flight information
* Pricing information
* Operational notes

The structure supports automated FTP reporting and enables MTS Globe to process hotel and travel services efficiently.
