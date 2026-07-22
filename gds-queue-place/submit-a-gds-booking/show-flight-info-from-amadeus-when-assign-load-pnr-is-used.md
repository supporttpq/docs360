# Show flight info from Amadeus when Assign/Load PNR is used

## Overview

When a booking is connected to an existing Amadeus PNR using **Assign PNR** or **Load PNR**, Tourpaq now copies the flight information directly from Amadeus into the booking.

This ensures that the booking always reflects the actual flights stored in the airline reservation system, even when those flights are not available in Tourpaq's own flight inventory.

As a result, the correct flight details are displayed throughout the booking and on customer travel documents.

***

A common workflow is:

1. A flight reservation is created in Amadeus.
2. A booking is later created in Tourpaq.
3. The existing Amadeus PNR is linked to the Tourpaq booking.

This enhancement ensures that the booking always displays the actual itinerary stored in the linked Amadeus PNR.

***

## How it Works

### Assign PNR

**Assign PNR** is used to connect an existing Amadeus reservation (PNR) to a Tourpaq booking.

When the PNR is assigned:

* Tourpaq retrieves the current flight itinerary from Amadeus
* the flight information is copied into the booking
* the copied flight information becomes the itinerary displayed in Tourpaq
* the same information is used when generating tickets and travel documents

This happens automatically when the Assign PNR action is completed successfully.

***

### Load PNR

**Load PNR** refreshes booking information from the linked Amadeus reservation.

This is typically used after changes have been made directly in Amadeus, such as:

* flight changes
* airline schedule changes
* rebooking onto different flights
* updated departure or arrival times

Whenever **Load PNR** is performed:

* Tourpaq retrieves the latest flight information from Amadeus
* the existing flight information stored on the booking is updated
* the booking immediately reflects the latest Amadeus itinerary

***

## System Behaviour

After a successful **Assign PNR** or **Load PNR** operation:

* the flight itinerary is copied from Amadeus
* the booking displays the Amadeus flight information
* ticket printing uses the copied Amadeus flight information
* the displayed itinerary remains synchronized with the linked Amadeus reservation whenever **Load PNR** is executed

{% hint style="warning" %}
If changes are made later in Amadeus, the system will automatically check the PNR X days before departure (depending on the number set in System Setup) and update the reservation with the latest flight information.&#x20;
{% endhint %}

<figure><img src="../../.gitbook/assets/check pnr.png" alt=""><figcaption></figcaption></figure>

***

**Example of workflow:**

1. A flight reservation is created in Amadeus.
2. A booking is later created in Tourpaq.
3. The existing Amadeus PNR is linked to the Tourpaq booking.

This enhancement ensures that the booking always displays the actual itinerary stored in the linked Amadeus PNR.

\
The flights are booked directly into Amadeus.Later, the user creates the booking in Tourpaq and links the existing PNR using **Assign PNR**.

Although the same flights are no longer available in Tourpaq's flight inventory, the booking displays the flights exactly as they exist in Amadeus.

If the airline subsequently changes the itinerary, the user simply performs **Load PNR**, and the updated flight details are copied into the booking and shown on the ticket.

***

## Summary

| Action       | Result                                                                     |
| ------------ | -------------------------------------------------------------------------- |
| Assign PNR   | Copies the current flight itinerary from Amadeus into the Tourpaq booking. |
| Load PNR     | Refreshes the booking with the latest flight itinerary from Amadeus.       |
| Booking Page | Displays the copied Amadeus flight information.                            |
| Ticket       | Uses the copied Amadeus flight information.                                |
