# PMS Integration

## Overview

The PMS (Property Management System) Integration in Tourpaq enables accommodation providers and tour operators to synchronize hotel inventory, availability, pricing, and reservation data between Tourpaq and external hotel management systems.

By integrating directly with supported PMS platforms, Tourpaq reduces manual administration, improves data accuracy, and ensures that hotel information remains consistent across sales channels and operational systems.

PMS integrations form part of Tourpaq's broader integration framework, which supports dynamic packaging, hotel provider connectivity, and automated booking workflows.

***

## Purpose

The PMS Integration is designed to:

* Synchronize room availability between Tourpaq and hotel systems.
* Reduce manual handling of hotel reservations.
* Improve inventory accuracy and minimize overbookings.
* Automate reservation delivery to hotels.
* Support dynamic packaging and online booking workflows.
* Maintain consistent accommodation data across connected platforms.

***

## Business Benefits

### For Tour Operators

* Real-time accommodation availability.
* Faster reservation processing.
* Reduced operational workload.
* Improved booking accuracy.
* Better scalability when working with large hotel portfolios.

### For Hotels

* Automatic receipt of reservations.
* Reduced manual registration of bookings.
* Improved occupancy management.
* Better visibility of room inventory.

***

## Supported Integration Framework

Tourpaq supports integrations with external hotel providers and accommodation systems through its hotel integration architecture.

Examples of supported accommodation integrations include:

* Opera integration
* Seekda integration

The exact PMS systems available depend on the customer's Tourpaq setup and integration agreement.

***

## How PMS Integration Works

The integration follows a standard accommodation synchronization workflow:

```
Hotel PMS
      ↓
Availability & Pricing
      ↓
Tourpaq
      ↓
Booking Creation
      ↓
Reservation Confirmation
      ↓
Hotel PMS
```

When availability is updated in the PMS, the information becomes available in Tourpaq.

When a booking is created in Tourpaq, reservation details can be transmitted back to the connected hotel system depending on the integration type.

***

## Data Exchange

Depending on the PMS implementation, the following information may be exchanged.

### Hotel Information

* Hotel name
* Hotel code
* Address information
* Hotel descriptions
* Facilities
* Images

### Availability

* Available rooms
* Allotments
* Stop sales
* Restrictions

### Pricing

* Room rates
* Seasonal prices
* Dynamic pricing
* Supplements

### Reservation Data

* Booking number
* Arrival date
* Departure date
* Passenger details
* Room allocation
* Reservation status
