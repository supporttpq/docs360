# SSR Codes

SSR Codes are used to define and manage Special Service Request (SSR) mappings for airline, supplier, and ticketing integrations. These mappings ensure that passenger service requests are correctly transferred between the booking platform and external systems.

Typical SSR services include:

* Wheelchair assistance
* Meal requests
* Extra baggage
* Medical assistance
* Passenger support services

The feature supports multiple external report and integration types, including:

* Paxport
* Radixx
* DAT
* Air Berlin
* WorldTicketing
* Air Seven
* SunClass

***

## Purpose of the Feature

The purpose of the SSR Codes feature is to standardize how passenger special service requests are handled across booking flows, ticketing, supplier exports, and operational reporting.

The configuration ensures that:

* Passenger requests are stored consistently
* Airline-specific SSR formats are supported
* Supplier integrations receive the correct codes
* Booking exports and reports remain compatible with external systems

Without proper SSR mappings, special passenger services may not be transferred correctly to airlines or suppliers.

***

## How the Feature is Configured

SSR Codes are configured by the System Administrator from the SSR Codes administration page.

Each SSR configuration contains mapping information used internally and externally during integrations.

### Available Fields

| Field                     | Description                                  |
| ------------------------- | -------------------------------------------- |
| **SSR Code**              | Airline or supplier SSR identifier           |
| **Description**           | Human-readable description of the SSR        |
| **PAX Port**              | Internal passenger port mapping              |
| **Sun Class Code**        | Optional SunClass-specific mapping           |
| **Assigned Report Types** | External systems where the SSR applies       |
| **Show on ticket**        | The selected SSR will be shown on the ticket |

***

## Assigned Report Types

Assigned Report Types determine which integrations or export formats use the SSR mapping.

Supported report types include:

* Paxport
* Radixx
* DAT
* Air Berlin
* WorldTicketing
* Air Seven
* SunClass

One SSR code may be assigned to multiple report types if the same mapping is supported by several integrations.

***

## System Administrator Responsibilities

The System Administrator is responsible for configuring and maintaining SSR mappings, including:

* Creating SSR codes
* Editing existing SSR mappings
* Updating descriptions
* Configuring PAX Port values
* Configuring Sun Class mappings
* Assigning report types
* Deleting obsolete mappings

Changes to SSR mappings impact future bookings, exports, ticketing processes, and operational reports.

***

## How the Feature Manifests in the System

### Booking Flow

During booking creation, SSR selections are attached to passengers and stored in the reservation.

The assigned report type determines how the SSR information is exported to suppliers or airline systems.

#### Example

A passenger requires wheelchair assistance.

| Field                 | Value                        |
| --------------------- | ---------------------------- |
| SSR Code              | `WCHR`                       |
| Description           | Passenger steps + wheelchair |
| Assigned Report Types | Paxport, DAT                 |

#### Result

* The booking stores the SSR request
* Export files generated for Paxport and DAT include the `WCHR` code
* Airline systems receive the passenger assistance request

***

### Web Booking

In the web booking flow, passengers may select SSR-related services directly during the reservation process.

Typical selectable SSR services include:

* Extra baggage
* Meal requests
* Wheelchair assistance
* Medical support services

The system validates the selected services against the configured SSR mappings.

#### Example

A passenger selects:

* Vegetarian meal
* Extra baggage

The booking stores:

| Service         | SSR Code |
| --------------- | -------- |
| Vegetarian meal | `VLML`   |
| Extra baggage   | `XBAG`   |

#### Result

When exported through Radixx, the configured Radixx SSR mappings are used automatically.

***

### Reporting and Export Files

SSR mappings are also used in operational reports and supplier export files.

Different report types may require different formatting or mapping values for the same SSR service.

#### Example

| Report Type    | SSR Output |
| -------------- | ---------- |
| DAT            | `WCHC`     |
| WorldTicketing | `XBAG`     |
| SunClass       | `V`        |

In the SunClass example, the exported value may use the configured Sun Class Code instead of the original SSR code.

***

## Example Configuration Scenarios

### Example 1: Wheelchair Assistance

| Field                 | Value                        |
| --------------------- | ---------------------------- |
| SSR Code              | `WCHR`                       |
| Description           | Passenger steps + wheelchair |
| PAX Port              | `WCHR`                       |
| Assigned Report Types | Paxport, DAT, Radixx         |

#### System Behavior

* Passenger selects wheelchair assistance
* SSR is attached to the booking
* Supplier exports include the configured SSR mapping

***

### Example 2: Vegetarian Meal

| Field                 | Value                               |
| --------------------- | ----------------------------------- |
| SSR Code              | `VLML`                              |
| Description           | Ovo-Lacto Vegetarian Meal Requested |
| Sun Class Code        | `V`                                 |
| Assigned Report Types | SunClass                            |

#### System Behavior

* Passenger selects vegetarian meal during booking
* Booking stores SSR `VLML`
* SunClass exports convert the SSR to mapping value `V`
