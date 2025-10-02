# Create Transport Rule

### Overview

The **Create Transport Rule** page allows you to define and configure transport rules that can be applied to bookings. A transport rule specifies validity dates, departure and arrival locations, transport types, pricing information, and additional settings that affect how the transport is handled in the booking workflow.

### Purpose

Transport rules are used to:

* Define available transport routes and validity periods.
* Configure pricing and payment rules for specific transports.
* Adjust check-in dates, hotel nights, and travel length based on transport details.
* Manage visibility, cancellation conditions, and filtering in the system.

### Field Explanation

<figure><img src="../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### General

* **Code**\* – Unique identifier for the transport rule (mandatory).
* **Date From**\* – Start date for the validity of the rule (mandatory).
* **Date To**\* – End date for the validity of the rule (mandatory).
* **Departure**\* – Departure location (mandatory).
* **Arrival**\* – Arrival location (mandatory).
* **Stay Days** – Define stay duration (optional, tab).
* **Allotment** – Configure allotment rules (optional, tab).

#### Transportation

* **Pick-up point required** – If checked, the booking must include a pick-up point.
* **Travel Length Correction +/-** – Adjust the travel duration by a specified number of days.
* **Shift check-in date +/-** – Shifts the hotel check-in date forward or backward.
* **Hotel nights correction +/-** – Adjust the total number of hotel nights based on transport.

#### Price Information

* **Infant price** – Set the price for infants.
* **Payment Rule** – Select a payment rule applicable to this transport.
* **Use change rule service** – If checked, activates the change rule service for this transport.

#### Outbound

* **Transport Type** – Select the transport type for the outbound journey (Real transport / External provider).

#### Homebound

* **Transport Type** – Select the transport type for the return journey (Real transport / External provider).

#### Settings

* **Status** – Defines the rule’s visibility in the system (e.g., Visible / Hidden).
* **Hide as filter on lists** – If checked, this rule will not appear as a filter option in lists.
* **Cancelation condition**\* – Select the cancellation condition that applies to this transport rule (mandatory).
