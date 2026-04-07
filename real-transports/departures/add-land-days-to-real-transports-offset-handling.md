# Add LAND-Days to Real Transports (Offset Handling)

### Overview

This feature introduces the ability to control hotel **check-in** and **check-out dates** directly from the **Real Transport** configuration using an **OFFSET** value.

It allows alignment between transport timing (flight/transfer) and hotel stay dates, especially in cases where arrival or departure happens on a different calendar day than the stay period.

***

### Purpose

* Adjust hotel check-in relative to arrival transport
* Adjust hotel check-out relative to departure transport
* Support overnight flights, early arrivals, and late departures
* Provide flexibility in LAND package handling
* Ensure accurate stay duration calculation

***

### Key Concept

Each **Real Transport** represents a single direction:

* **Outbound (arrival to destination)**
* **Homebound (departure from destination)**

Because of this, a single **OFFSET field** is used, but its meaning depends on transport direction.

***

### Field Definition

#### OFFSET

A numeric field used to adjust hotel stay dates.

**Location:**

* New column in Real Transport grid
* Positioned to the right of the **DAYS** column

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Properties:**

* Accepts values from **-9 to +9**
* Supports both positive and negative values
* Sortable column

***

### Tooltip (UI Description)

> The OFFSET is used to adjust hotel check-in or hotel check-out.\
> For an outbound, the offset determines the hotel check-in, and for a homebound, the check-out is adjusted.\
> A positive value adjusts the check-in/out later, and a negative value adjusts the check-in/out earlier.

***

### Behavior by Transport Type

#### Outbound Transport

* OFFSET applies to **hotel check-in date**

| Offset | Result                        |
| ------ | ----------------------------- |
| 0      | Check-in same day as arrival  |
| +1     | Check-in 1 day after arrival  |
| -1     | Check-in 1 day before arrival |

**Use case:**

* Night flight arriving early morning → offset +1 to align with hotel policy

***

#### Homebound Transport

* OFFSET applies to **hotel check-out date**

| Offset | Result                           |
| ------ | -------------------------------- |
| 0      | Check-out same day as departure  |
| +1     | Check-out 1 day after departure  |
| -1     | Check-out 1 day before departure |

**Use case:**

* Late night departure → offset 0 or +1 depending on stay logic

***

### How to Configure

1. Navigate to: Transport → Real Transport
2. Locate or create a Real Transport
3. In the grid:
   * Find the **OFFSET** column
   * Enter a value between **-9 and +9**
4. Save changes

***

### Expected System Behavior

* OFFSET is applied during booking calculation
* Adjusts hotel stay dates dynamically
* Works differently depending on transport direction
* Reflected in:
  * Hotel booking dates
  * Pricing calculations (Price List)
  * Stay duration logic

***

### Important Notes

* OFFSET does not change transport dates, only hotel stay dates
* Must be carefully aligned with:
  * Hotel contracts
  * Allotment availability
  * Pricing rules

***

### Example

In the following example,, the offset is required in both directions (outbound and homebound).

Booking details:

* Number of passengers: 2 adults
* Departure: CPH (Kastrup Lufthavn)&#x20;
* Arrival: CHQ (Chania Lufthavn)
* Departure date: 08.05.2026
* Arrival date: 15.05.2026
*   Offset Departure: -1&#x20;

    <figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>


*   Ofsset Arrival: +1&#x20;

    <figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>


* Results:&#x20;
  * Early arrival -1 day (07.05.2026 - extra night requierd)
  * Late departure +1 day (16.05.2026 - extra night requierd)

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



***

### Summary

The OFFSET field adds precise control over how transport timing impacts hotel stays.\
It ensures consistency between flight schedules and accommodation logic, reducing manual corrections and improving booking accuracy.
