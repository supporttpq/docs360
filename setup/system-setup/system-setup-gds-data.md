# System Setup – GDS Data

### Overview

**GDS Data** configures Global Distribution System (GDS) integration for transport and ticketing.

The configuration supports reservations, ticketing, PNR retrieval, and booking synchronization.

It supports the [GDS Bookings](../../gds-queue-place/gds-bookings.md) workflow and provider-specific transport setup.

### Purpose

Use **GDS Data** to centralize provider credentials, ticketing rules, queues, and search behavior.

The configuration controls Tourpaq's exchange of booking and ticketing data with GDS providers.

### Requirements

Before configuring **GDS Data**, complete these requirements:

* Obtain the GDS provider credentials and booking-office codes.
* Obtain the provider's ticketing, payment, and queue rules.
* Ensure administrator access to **System Setup**.

### Navigation

In Tourpaq Office, open **System Setup → GDS Data**.

### Interface overview

**GDS Data** contains provider connection, ticketing, search, payment, PNR, and ticket-output settings.

All listed fields require valid configuration for proper GDS integration.

### Connection and booking-office fields

| Field                                       | Requirement | Description                                            |
| ------------------------------------------- | ----------- | ------------------------------------------------------ |
| **Currency**                                | Required    | Sets the currency used for GDS transactions.           |
| **User / Password**                         | Required    | Stores the credentials supplied by the GDS provider.   |
| **Branch**                                  | Required    | Sets the branch code used for ticketing and reporting. |
| **Pseudo City Code / Own Pseudo City Code** | Required    | Identifies the booking office for GDS reservations.    |
| **Confirmation Email**                      | Required    | Receives Travelport booking confirmations.             |

These fields establish the provider connection used by [GDS Bookings](../../gds-queue-place/gds-bookings.md).

### Ticketing and payment fields

| Field                            | Requirement | Description                                                         |
| -------------------------------- | ----------- | ------------------------------------------------------------------- |
| **Days Number for Ticketing**    | Required    | Sets the allowed ticketing days after reservation creation.         |
| **Queue Number**                 | Required    | Assigns GDS bookings to the ticketing queue.                        |
| **Payment Rule**                 | Required    | Applies payment rules to GDS reservations.                          |
| **Card Details**                 | Required    | Stores payment owner, type, number, expiration year/month, and CVC. |
| **Show Ticket Number on Ticket** | Required    | Displays ticket numbers on printed tickets.                         |

These settings affect submission and ticketing in [Submit a GDS Booking](../../gds-queue-place/submit-a-gds-booking/).

### Search and fare fields

| Field                      | Requirement | Description                                              |
| -------------------------- | ----------- | -------------------------------------------------------- |
| **Max GDS Search Results** | Required    | Limits the results returned by GDS searches.             |
| **Price Change Margin**    | Required    | Sets the permitted margin for GDS booking price changes. |
| **Fares Indicator**        | Required    | Controls the indicator used for fare calculations.       |

These settings affect GDS flight search results and pricing behavior.

### PNR and flight-maintenance fields

| Field                           | Requirement | Description                                                       |
| ------------------------------- | ----------- | ----------------------------------------------------------------- |
| **Days Number for Check PNR**   | Required    | Sets the days before departure for PNR status checks.             |
| **Time Frame Before Departure** | Required    | Sets when Tourpaq removes flights from bookings before departure. |

Tourpaq uses these settings to maintain PNR and flight information in GDS bookings.

### Transport selection rules

| Field                           | Requirement | Description                                                |
| ------------------------------- | ----------- | ---------------------------------------------------------- |
| **Use Division PNR by Classes** | Required    | Divides bookings by class to support pricing optimization. |

This setting affects how Tourpaq structures PNRs for GDS transport.

### Configuration steps

Configure **GDS Data** as follows:

1. In **System Setup**, open **GDS Data**.
2. Enter **Currency**, **User / Password**, and **Branch**.
3. Enter **Pseudo City Code / Own Pseudo City Code** and **Confirmation Email**.
4. Configure ticketing, payment, search, PNR, and flight-maintenance fields.
5. Save the GDS configuration.
6. Test the configuration through a GDS booking workflow.

### System behavior

Tourpaq uses **User / Password**, **Branch**, and booking-office codes to authenticate with the GDS.

Tourpaq applies ticketing, payment, and queue settings when processing GDS reservations.

Tourpaq retrieves PNR, flight, ticket, and booking updates through the configured provider connection.

Invalid credentials or settings can prevent booking submission or ticket generation.

### Examples

#### Ticketing queue example

**Queue Number** assigns GDS reservations to the provider ticketing queue.

Tourpaq uses that queue during the GDS booking and ticketing workflow.

#### PNR monitoring example

**Days Number for Check PNR** sets the pre-departure period for PNR status checks.

Tourpaq uses the setting to monitor GDS booking status before departure.

### Related pages

* [GDS Bookings](../../gds-queue-place/gds-bookings.md) describes GDS reservation processing.
* [Submit a GDS Booking](../../gds-queue-place/submit-a-gds-booking/) describes booking submission and ticketing.
* [Setup for Transport Dynamic Packaging (GDS)](../../gds-queue-place/setup-for-transport-dynamic-packaging-gds.md) describes GDS transport setup.
