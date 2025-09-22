# Setup for Transport Dynamic Packaging (GDS)

Transport Dynamic Packaging Anchored on Pricelist is connecting Tourpaq to the GDS system and enables it to book transport over GDS and sell it under an existing pricelist (fix price). This document specification describes how this feature works in Tourpaq.

### General​ <a href="#general" id="general"></a>

GDS transports are available only if the transport is set to use dynamic itineraries.

<figure><img src="../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

### Legs​ <a href="#legs" id="legs"></a>

When using GDS flights, **Legs** need a general setting like this.

<figure><img src="../.gitbook/assets/image (21) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The rest of the settings for configuring **Legs** are the same as those used for Real Transports

### Flight Search​ <a href="#flight-search" id="flight-search"></a>

Every night the system is checking for the best flight available for each departure on all transport that is using dynamic itineraries. The system will store timetables, flight numbers and airlines. When a transport is using OWN real transports and GDS flights, the following list of rules that decides when GDS segments are booked instead of OWN segments is used:

1. Selling of guarantee seats in according to load matrix (see below)
2. Cost price is lower on GDS\\
3. GDS price is lower that “Max price from GDS\\

The flight found can be views under fix quota/view fligths:

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

When a **past reservation** is cancelled and the **associated flight is no longer active**, the system will automatically trigger the reactivation service to restore the flight. This ensures the booking change can be processed correctly.

Before cancellation:

<figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

After the booking cancellation, the flight will be reactivated within a few seconds.

<figure><img src="../.gitbook/assets/image (7) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The system automatically reactivates past flights **only** when a change is made to a booking—such as adding or canceling passengers.

* If the service is triggered manually from **Transport → Leg**, it will affect **only future flights**.
* If the service is triggered directly from a **booking**, it will run **only for the specific departure**, regardless of whether the departure date is in the past or future.

<figure><img src="../.gitbook/assets/image (9) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Alternative flights​ <a href="#alternative-flights" id="alternative-flights"></a>

This feature makes the GDS integration more flexible as it allows more flights options for the same departure dates. These are taken dynamically from GDS.

It is visible in the office part. After creating a booking with a GDS transport, when searching for flight, a forth check box appears. This check box searches only for alternative flights. They are displayed in the same manner as a regular GDS flight, with the exception that the user can now choose which flight he would like to use.
