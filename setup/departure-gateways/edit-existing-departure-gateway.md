# Edit Existing Departure Gateway

### Overview

The **Edit Departure Gateway** function allows administrators to update configuration details of an existing departure location.

Changes affect future bookings and operational logic. Existing bookings retain stored data unless manually updated.

Accurate configuration is important for:

* Flight time calculations
* Reporting
* Online booking availability
* Integration consistency

***

### Navigation

Setup → Destinations → Departure Gateways

1. Locate the gateway in the list.
2. Click Edit.
3. Update required fields.
4. Click Save.

***

### Editable Fields

IATA Code - Can be modified if necessary.

Important:\
Changing the IATA code may impact:

* Flight imports
* Integration mappings
* Historical data references

Only change if absolutely required and verified.

Name - Can be updated for clarity or correction. Affects display in:

* Booking screens
* Reports

Display only. No calculation impact.

Country - Can be changed if initially configured incorrectly. May impact reporting or insurance logic.

Latitude / Longitude - Update if coordinates were incorrect or missing.

Used for:

* Distance calculations
* Transfer logic
* Map integrations

Incorrect values may result in wrong distance calculations.

GMT Offset - Standard UTC offset.

GMT Offset Summertime - Daylight saving time offset. These must match the selected timezone.\
Incorrect configuration may result in:

* Wrong departure time handling
* Incorrect duration calculations
* Transfer timing errors&#x20;

TimeZone - Changing timezone affects:

* Departure time calculations
* Flight duration logic
* Integration timestamps

This field must be verified carefully before saving. Avoid changing if active bookings depend on it.&#x20;

URL Alias - Used for web routing. Can be updated if web structure changes. Does not affect operational logic.

### Expected System Behavior

After saving:

* Updates apply to new bookings
* Existing bookings retain stored departure information
* Online visibility reflects Internet setting
* Time calculations follow new timezone configuration

***

### Important Considerations

Before editing:

* Check whether the gateway is used in active or upcoming bookings
* Verify integration dependencies
* Confirm timezone accuracy
* Ensure GMT offsets match daylight saving rules

Incorrect changes may affect operational planning.
