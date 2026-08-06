# Create New Real Transport

## Overview

The **New Real Transport** feature is used to create and manage transport entities that represent actual transportation services operated by suppliers.

This configuration allows administrators to define transport routes, assign suppliers, configure automatic seat allocation, and control how the transport is displayed and reported throughout the platform.

<figure><img src="../.gitbook/assets/rt new.png" alt=""><figcaption></figcaption></figure>

***

## Purpose

The Real Transport configuration enables you to:

* Create operational transport services.
* Define departure and arrival locations.
* Connect transports to suppliers and reporting structures.
* Configure automatic passenger seating.
* Control transport visibility in filters and lists.
* Support homebound transport selection.
* Provide additional customer information fields visible during booking and reporting.

***

## Prerequisites

Before creating a Real Transport, ensure that:

* Departure and Arrival locations already exist in the system.
* Transport suppliers have been configured.
* Required reporting types are available.
* Airlines

***

## How to Configure a Real Transport

Navigate to:

**Transport → Real Transport → Create**

The configuration screen contains two sections:

1. **General**
2. **Automatic Seating**

***

## General Section

**Code** \* - Defines the unique identifier for the transport.

**Instructions**

* The code must be unique.
* Use a naming convention that clearly identifies the service.

***

**Departure** \* - Specifies the transport departure location.

**Instructions**

* Select an existing departure location from the dropdown list.
* This field is mandatory.

**Example:** `Stockholm`

***

**Arrival** \* - Specifies the transport destination.

**Instructions**

* Select an existing arrival location.
* This field is mandatory.

**Example:** `Barcelona`

***

I**nfo Customer 1 / 2 / 3 -** These fields allow administrators to store additional information that can be displayed to customers during booking.

Typical uses include:

* Check-in instructions
* Meeting point information
* Terminal details
* Supplier notes

**Examples**

| Field           | Example Value                              |
| --------------- | ------------------------------------------ |
| Info Customer 1 | `Check-in opens 2 hours before departure.` |
| Info Customer 2 | `Meet guide at Terminal 3.`                |
| Info Customer 3 | `Bring valid passport.`                    |
|                 |                                            |

<figure><img src="../.gitbook/assets/05.08.2026_16.23.01_REC.png" alt=""><figcaption></figcaption></figure>

***

**Airline -** Associates the transport with a specific airline.

**Instructions**

* Select an airline from the dropdown list.
* Primarily used for flight-based transports.

**Example:** `Scandinavian Airlines (SAS)`

***

**Tour Operator -** Specifies the responsible tour operator for the transport.

**Instructions**

Enter the operator name if the transport belongs to a specific operator.

**Example:** `RWB Tours`

***

**Reporting Type** \* - Select from the dropdown the reporting used for this transport

**Instructions**

Select the appropriate reporting type from the dropdown list.

Examples may include:

* Passenger name List
* Pick up list (Bus)
* Train
* Paxport
* etc

***

**Parent -** Links the transport to a parent transport.

**Instructions**

Select an exisating real transport as a parent

***

**Transport Supplier -** Defines the supplier responsible for operating the transport.

**Instructions**

Select an existing supplier.

**Example:** `saxaxa`

***

**Hide as Filter on Lists -** Hide the real transport in the lists throught the system

* Enabled - The transport will **not** appear as a selectable filter.
* Disabled - The transport can be selected in filters throughout the system.

***

**Use for Homebound -** Check this when is it used for return home

* Enabled - The transport becomes available for homebound assignments.

***

## Automatic Seating Section

The **Automatic Seating** functionality automatically distributes passengers into available seats.

This feature reduces manual seat assignment and ensures that unseated passengers are allocated before departure.

***

**Use Automatic Seating -** Activates automatic seat distribution.

When enabled, the system automatically assigns seats to passengers who do not already have seats.

When disabled, seat assignment must be performed manually.

***

**Hour Before Departure -** How many hours before departure the system will automatically place the passengers into the airplane

**Instructions**

Enter the number of hours before departure when the system should execute seat allocation.

**Example**

| Value | Result                                                      |
| ----- | ----------------------------------------------------------- |
| `24`  | Seats are automatically assigned 24 hours before departure. |
| `12`  | Seats are assigned 12 hours before departure.               |

***

**Email Address(es)** - Specifies recipients who should receive notifications related to automatic seating.

**Instructions**

Enter one or more email addresses.

Multiple email addresses can be separated by comma.

**Example:** operations@company.com, transport@company.com

***

## Example Configuration

| Field                 | Example                  |
| --------------------- | ------------------------ |
| Code                  | STOBCN                   |
| Departure             | `Stockholm`              |
| Arrival               | `Barcelona`              |
| Airline               | `SAS`                    |
| Tour Operator         | `RWB Tours`              |
| Reporting Type        | `PNL`                    |
| Transport Supplier    | `saxaxa`                 |
| Use Automatic Seating | Enabled                  |
| Hour Before Departure | `24`                     |
| Email Address         | `operations@company.com` |

#### Result

* The flight is available in bookings.
* Passengers can be assigned to the transport.
* Unseated passengers automatically receive seats 24 hours before departure.
* The transport is included in manifests and supplier reports.
* Operational staff receive seating notifications by email.
