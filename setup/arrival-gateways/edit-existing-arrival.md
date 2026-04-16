# Edit Existing Arrival

#### Overview

The **Edit Arrival** function allows administrators to update an existing arrival destination.\
This includes modifying identification data, geographical details, timezone settings, insurance mapping, and online availability.

Changes apply to all future bookings. Existing bookings will retain previously stored arrival data unless the booking is manually updated.

### Expected Behavior

The system must allow:

* Updating arrival details
* Changing insurance area mapping
* Enabling or disabling online availability
* Maintaining data integrity for historical bookings

All changes must be saved before they become active.

### Customer Outcome

* Accurate and up-to-date destination information
* Correct time and transfer calculations
* Proper insurance classification
* Clean and consistent destination database

### Navigation

Setup → Destinations → Arrivals

1. Locate the arrival in the list.
2. Click Edit.
3. Modify required fields.
4. Click Save.

### Editable Fields

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

IATA Code - Can be updated if necessary.

Important:\
If the arrival is already used in bookings or integrations, changing the IATA code may impact flight mapping or external systems.

Name - Can be modified to improve clarity or correct naming. This affects how the arrival appears in selection lists.

Plain Text (not flight) - Can be adjusted if the arrival represents a non-airport location.

Country - Can be updated if initially configured incorrectly. May impact insurance and reporting.

Latitude / Longitude - Should be updated if mapping or transfer calculations require correction. Incorrect coordinates may affect transfer routing or distance-based logic.&#x20;

TimeZone - Changing timezone affects:

* Arrival time calculations
* Transfer scheduling
* Time-based integrations

Must be verified carefully before saving.

Insurance Area - Can be changed if insurance zone mapping needs correction. May impact insurance pricing and policy validation.

Internet (Checkbox) - If disabled Arrival will no longer appear in online booking.

Source Agency- Can be updated if integration mapping changes.

URL Alias - Can be modified for web booking or routing adjustments.

### Important Considerations

Before editing an existing arrival:

* Verify whether the arrival is already used in active bookings
* Validate insurance mapping impact
* Ensure integrations depending on IATA code are considered

Changes do not automatically update historical booking data.
