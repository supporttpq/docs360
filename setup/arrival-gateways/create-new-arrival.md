# Create New Arrival

#### Overview

The **New Arrival** configuration is used to create a new arrival destination in the system.\
An arrival can represent an airport, city, train station, or other transport hub used in bookings, transfers, insurance, and integrations.

This setup ensures that the arrival point can be correctly selected in bookings and connected to flight, transfer, insurance, and mapping logic.

### Expected Behavior

The system must allow administrators to:

* Create a new arrival destination
* Define transport and geographical details
* Assign insurance area
* Control availability for online booking

The arrival must become selectable in relevant booking flows after saving.

### Customer Outcome

* Accurate destination data in bookings
* Correct time calculations for arrival and transfers
* Proper insurance zone mapping
* Improved integration with external systems
* Clean and structured destination database

### Navigation

Setup → Destinations → Arrivals → Create New

### Field Specifications

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**IATA Code -** Official three-letter airport code. Required when the arrival represents an airport.

Name - Display name of the arrival destination. This is the name shown in booking and operational views.

Plain Text (not flight) - Used when the arrival is not a flight-based location.

Country - Select the country where the arrival is located. Used for reporting and insurance logic.

Latitude - Geographical latitude. Used for map integrations and transfer calculations.&#x20;

Longitude - Geographical longitude. Used together with latitude for location-based services.&#x20;

TimeZone - Select the applicable timezone. Required for correct arrival time calculations.&#x20;

Insurance Area - Assign the arrival to a specific insurance zone. Used for travel insurance calculations and compliance.

Internet (Checkbox) - If enabled, the arrival is available in online booking environments.&#x20;

Source Agency - Optional mapping to a source agency if applicable. Used for integrations or external system mapping.&#x20;

URL-Alias - Optional field for web or SEO-related references. Can be used for web booking routes.

### Validation Rules

Before saving:

* IATA code must be correct and unique (if applicable)
* Country and TimeZone must be selected
* Insurance area must be assigned
* Coordinates should be verified for accuracy

### Impact

Creating a new arrival:

* Makes it selectable in bookings
* Enables correct time calculations
* Connects the destination to insurance rules
* Supports transfer and operational planning

Incorrect configuration may result in time miscalculations or booking inconsistencies.
