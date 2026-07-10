# GDS Extra day

### Overview

When a booking is created using **GDS flights**, Tourpaq automatically calculates the hotel allotment based on the traveller's actual stay at the destination.

If the selected flight itinerary arrives at the destination on the following day (or, where applicable, on the previous day due to time zone differences), the hotel allotment is adjusted accordingly. This ensures that hotel inventory is reserved only for the dates the traveller is staying at the destination.

The validation applies to all selected GDS flight combinations, including itineraries with stopovers.

### Purpose

The purpose of this feature is to ensure that hotel allotment always reflects the actual accommodation period instead of the overall travel duration.

By considering the date offset of GDS flight itineraries, Tourpaq prevents hotel allotments from starting or ending on incorrect dates when flights cross time zones or arrive on a different calendar day.

### How it works

When a GDS flight combination is selected, Tourpaq evaluates the complete itinerary before calculating the hotel stay.

The validation considers:

* flight itineraries with an arrival **+1 day**
* flight itineraries with an arrival **-1 day**, where applicable
* alternative GDS flight combinations selected during the booking process
* itineraries with one or more stopovers where the final destination is reached on the following day

The hotel allotment is then calculated using:

* the **actual arrival date** at the destination as the hotel check-in date
* the **departure date** from the destination as the hotel check-out date

The return arrival date in the traveller's home country does not affect the hotel allotment.

### Example

A traveller selects the following GDS itinerary:

| Flight    | Schedule                                                |
| --------- | ------------------------------------------------------- |
| CPH → HKT | Departure **08 Dec 2026**, Arrival **09 Dec 2026 (+1)** |
| HKT → CPH | Departure **28 Dec 2026**, Arrival **29 Dec 2026 (+1)** |

Tourpaq calculates the hotel allotment as:

| Hotel Stay | Date            |
| ---------- | --------------- |
| Check-in   | **09 Dec 2026** |
| Check-out  | **28 Dec 2026** |

Although the total travel duration is **19 days**, the hotel stay is correctly calculated as **18 nights**, matching the traveller's actual stay at the destination.
