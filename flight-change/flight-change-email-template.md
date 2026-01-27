# Flight Change - Email Template

#### **Overview**

Within the **Email Center** menu, you can create and manage **email and SMS templates** used to inform customers about flight changes and to collect their confirmations.

These templates ensure that passengers receive clear and accurate communication tailored to the type of flight change detected by the system.

***

#### **Template Types**

To support the different types of flight changes, the following **dedicated templates** are required:

| **Template Name**         | **Purpose**                                                             |
| ------------------------- | ----------------------------------------------------------------------- |
| _Flight Change – Tiny_    | Used for minor time adjustments (e.g., a few minutes earlier or later). |
| _Flight Change – Small_   | Used for moderate schedule changes.                                     |
| _Flight Change – Large_   | Used for major schedule adjustments or flight number changes.           |
| _Flight Change – Earlier_ | Used when the new departure time is earlier than the original.          |
| _Flight Change – Later_   | Used when the new departure time is delayed.                            |

> **Note:**\
> If a specific template matching the flight change type is **not found**, the system automatically uses the **default "Flight Change Email"** template as a fallback.

***

#### **Template Variables**

All **Flight Change Email Templates** can include the following **variables** to personalize content dynamically:

| Variable                 | Content                                                                         |
| ------------------------ | ------------------------------------------------------------------------------- |
| HomeboundDateOfDeparture | The date on which the return flight departs from the destination airport.       |
| HomeboundDateOfArrival   | The date on which the return flight arrives at the origin airport.              |
| HomeboundDepartureTime   | The local time at which the return flight departs from the destination airport. |
| HomeboundArrivalTime     | The local time at which the return flight arrives at the origin airport.        |
| HomeboundAirline         | The operating airline for the return flight.                                    |
| HomeboundFlightNumber    | The flight number assigned by the airline for the return flight.                |
| OutboundDateOfDeparture  | The date on which the outbound flight departs from the origin airport.          |
| OutboundDateOfArrival    | The date on which the outbound flight arrives at the destination airport.       |
| OutboundDepartureTime    | The local time at which the outbound flight departs from the origin airport.    |
| OutboundArrivalTime      | The local time at which the outbound flight arrives at the destination airport. |
| OutboundAirline          | The operating airline for the outbound flight.                                  |
| OutboundFlightNumber     | The flight number assigned by the airline for the outbound flight.              |

<figure><img src="../.gitbook/assets/image (586).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (587).png" alt=""><figcaption></figcaption></figure>
