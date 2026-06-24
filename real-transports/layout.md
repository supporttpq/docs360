# Layout

## Overview

The **Layout** tab in a Real Transport configuration is used to assign and manage seating layouts for specific departure dates. It allows administrators to connect aircraft seat layouts to departures and define seat pricing.

This functionality ensures that passengers can be assigned seats during the booking process and that seat availability is accurately managed across the system.

***

## Purpose

The Layout feature enables administrators to:

* Assign seat layouts to transport departures.
* Manage seating arrangements for specific travel dates.
* Provide seat selection functionality during booking.

***

## Navigation

Go to: **Transport → Real Transport → Open a Real Transport → Layout**

The Layout tab displays all layouts configured for the selected transport.

***

## Layout Screen

The screen consists of:

* Filters
* Departure layout list
* Layout editor

<figure><img src="../.gitbook/assets/rt layout.png" alt=""><figcaption></figcaption></figure>

***

## Filters

### Select All Manager

**Purpose**

Allows users to select and display departures managed by a specific allocation or transport manager.

**Instructions**

* Select a manager or departure period from the dropdown.
* The list refreshes and displays matching departures.

**Example**

```
26-06-2026 - 26-06-2026
```

***

## Departure Layout List

The table displays all configured layouts for the selected transport.

| Column              | Description                                                |
| ------------------- | ---------------------------------------------------------- |
| **Edit**            | Opens the layout configuration for the selected departure. |
| **Dept. Date**      | The departure date associated with the layout.             |
| **Day**             | Day of the week for the departure.                         |
| **Layout**          | The assigned seating layout.                               |
| **Seat Type Price** | Displays seat categories and their prices.                 |

***

## How to Configure a Layout

1. Open the required Real Transport.
2. Navigate to the **Layout** tab.
3. Locate the desired departure date.
4. Click the **Edit** icon.
5. Select the appropriate seating layout.
6. Save the changes.

***

### Automatic Seating

When **Automatic Seating** is enabled on the Real Transport:

* Passengers without assigned seats are automatically allocated to available seats.
* The configured layout determines which seats are available.
* Seat type restrictions and availability rules are respected.

***

## Example Configuration

| Setting            | Example Value    |
| ------------------ | ---------------- |
| Departure Date     | `26-06-2026`     |
| Layout             | `Ses Layout`     |
| Seat Type          | `A320 Seat Type` |
| Seat Price         | `0 EUR`          |
| Comfort Seat Price | `0 EUR`          |

#### Result

For the departure on **26-06-2026**:

* The **Ses Layout** seating plan is used.
* Passengers can select seats during booking.
* Seat availability is controlled by the layout.
* Passenger manifests include assigned seat numbers.
* Automatic seating can allocate remaining passengers to free seats.
