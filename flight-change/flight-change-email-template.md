# Flight Change - Email Template

### **Overview**

Within the **Email Center** menu, you can create and manage **email and SMS templates** used to inform customers about flight changes and to collect their confirmations.

These templates ensure that passengers receive clear and accurate communication tailored to the type of flight change detected by the system.

***

### Preconditions

Before using the **Flight Change** feature, the following prerequisites must be fulfilled:

1. **Configure a default email template**
   * A default email named **Flight Changes Email** must be configured for every agency where the Flight Change feature will be used.
   * This email is mandatory and is used as the default template when sending flight change notifications.
2. **Activate the required email templates**
   * The **Flight Changes Email** template must be **Active**.
   * All email templates of the **Flight Change** type that are intended to be used must also be **Active**.

If the default email is not configured or is inactive, Tourpaq doesn't send flight change emails.

***

### **Template Types**

To support the different types of flight changes, you can create the following **dedicated templates**. They appear in the **Email Center** only when the company feature **Scheduled Flight Change** is on.

| **Template Name**                                               | **Purpose**                                                                                      |
| --------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| _Flight Changes Tiny Earlier_ and _Flight Changes Tiny Later_   | Used when the time changes by no more than the **Tiny** limit.                                   |
| _Flight Changes Small Earlier_ and _Flight Changes Small Later_ | Used when the time changes by more than the **Tiny** limit and no more than the **Small** limit. |
| _Flight Changes Large Earlier_ and _Flight Changes Large Later_ | Used when the time changes by more than the **Small** limit.                                     |
| _Flight Changes Flight Number_                                  | Used when the flight number changes.                                                             |

Earlier and Later show the direction of the time change. Set the limits in minutes, separately for earlier and later changes, in **System Setup** → **Flight Change Queue** → **Flight Change Configuration**.

> **Note:**\
> If a specific template matching the flight change type is **not found** or is not active, the system automatically uses the **default "Flight Changes Email"** template as a fallback.

***

### **Template Variables**

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
