# Create New Departure Gateway

### Overview

A Departure Gateway represents the origin airport or departure location used in bookings and flight integrations.\
It defines geographical data, timezone settings, and online availability.

Proper configuration is important for correct time calculations, reporting, and web booking visibility.

***

### Navigation

Setup → Destinations → Departure Gateways → Create

***

### Required Fields

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

IATA Code - Three-letter airport code, for example OSL, ARN, CPH. Must be unique in the system. Used in flight matching and integrations.

Name - Full airport or city name as it should appear in the system and online.

Country - Select the country where the departure gateway is located. Used for reporting and insurance logic.

TimeZone - Select the correct timezone for the gateway.\
This setting drives:

* Flight departure time handling
* Time-based calculations
* Transfer planning logic

Must match the physical airport location.

### Optional Fields

Latitude / Longitude - Geographical coordinates of the airport.

Internet (Checkbox) - If enabled Departure gateway is available for online booking.

These values must correspond with the selected timezone.

URL Alias - Used for web routing or SEO friendly URLs if applicable. Optional unless required by web configuration.&#x20;

### Expected Behavior

When saved:

* Gateway becomes selectable in bookings
* Available in flight configuration
* Visible online if Internet is enabled
* Time calculations use defined timezone and offsets

### Best Practice

* Use official IATA codes
* Add coordinates if transfer calculations depend on distance
* Keep naming consistent with airline standards
