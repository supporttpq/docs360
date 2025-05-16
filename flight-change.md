# Flight change

A flight change is automatically generated when:

* The departure or arrival time is edited
* The flight number is changed

The flight change is identified as Tiny, Small, and Large depending on the flight time adjustments. The intervals are configurable.

The flight change is also identified as sooner or later, depending on the amount of time adjusted. A 10-minute delay is classified as tiny later.

The flight change is queued in a flight change system, and they are manually released or dropped.

If the same flight is changed twice, then two flight changes are queued for the same flight, and it is a manual process to delete one of the flight changes.

The flight change system gives an overview of destination/flight changes, and there are several filtering possibilities.

When a flight change is submitted to a guest (this is a carefully designed mail), the user can click a link to confirm the receipt.

If the user fails to confirm the receipt, the system will resend the flight change a couple of times and then try with an SMS asking the user to check mail and confirm.

In the flight change system, it is straightforward to see which guests have not yet confirmed the receipt of the flight change.

If the guest fails to respond to the flight change, then the flight change is forwarded to a service mail that can take proper action (call the passenger, etc.).

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### 🔍 Filter Section (Top Panel)

| Field Name            | Description                                                                      |
| --------------------- | -------------------------------------------------------------------------------- |
| **Departure Gateway** | Dropdown to filter by the origin airport of the flight.                          |
| **Arrival Gateway**   | Dropdown to filter by the destination airport.                                   |
| **Flight No.**        | Text field to search for a specific flight number.                               |
| **Type of Change**    | Dropdown to filter by the nature of the flight change (e.g., delay, reschedule). |
| **Status**            | Dropdown to filter by the current status of the change (e.g., Queued, Sent).     |
| **Airline**           | Dropdown to filter flights by airline.                                           |
| **Booking**           | Text field to search by booking number.                                          |
| **Transport**         | Dropdown to filter by transport identifier or vehicle.                           |
| **Departure Date**    | Calendar picker to select the flight's departure date.                           |
| **Created Date**      | Calendar picker to select when the change record was created.                    |
| **Departure Time**    | Time selector to narrow results by flight departure time.                        |
| **Show confirmed**    | Checkbox to include confirmed changes.                                           |
| **Show dropped**      | Checkbox to include dropped/ignored changes.                                     |
| **Display**           | Button to apply current filter settings.                                         |
| **Clear**             | Button to reset all filters (with count of active filters).                      |

***

### 📋 Table Columns

| Column Name           | Description                                                                                  |
| --------------------- | -------------------------------------------------------------------------------------------- |
| **Created**           | Date when the flight change entry was created.                                               |
| **Booking**           | The booking that is affected by the flight change (link to the booking)                      |
| **Transport**         | The transport that is affected by the flight change (Link to the actual transport)           |
| **Airline**           | Name of the airline operating the flight.                                                    |
| **Flight No.**        | The flight number for the flight that has a flight change.                                   |
| **Departure Gateway** | The airport or location from where the flight departs.                                       |
| **Departure**         | The departure time in the local time of the departure airport                                |
| **Arrival Gateway**   | The destination airport or location of the flight.                                           |
| **Arrival Time**      | Scheduled arrival time at the destination.                                                   |
| **Type**              | Description of the flight change (e.g., “Flight Change Small Later”, “Tiny Later”).          |
| **Status**            | Current status of the flight change process (e.g., **Queued**, **Sent**, **Resend Second**). |

The flight change sent us different templates depending on the type of change. This allows the company to decide the content based on the type of change.

When Send or Send SMS is selected, the flight change will be sent at once, independently of the Hour to send in the template.
