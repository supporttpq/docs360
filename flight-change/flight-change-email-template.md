# Flight Change - Email Template

#### **Overview**

Within the **Email Center** menu, you can create and manage **email and SMS templates** used to inform customers about flight changes and to collect their confirmations.

These templates ensure that passengers receive clear and accurate communication tailored to the type of flight change detected by the system.

***

#### **Template Types**

To support the different types of flight changes, the following **dedicated templates** are required:

| **Template Name**        | **Purpose**                                                             |
| ------------------------ | ----------------------------------------------------------------------- |
| _Flight Change – Tiny_   | Used for minor time adjustments (e.g., a few minutes earlier or later). |
| _Flight Change – Small_  | Used for moderate schedule changes.                                     |
| _Flight Change – Large_  | Used for major schedule adjustments or flight number changes.           |
| _Flight Change – Sooner_ | Used when the new departure time is earlier than the original.          |
| _Flight Change – Later_  | Used when the new departure time is delayed.                            |

> **Note:**\
> If a specific template matching the flight change type is **not found**, the system automatically uses the **default "Flight Change Email"** template as a fallback.

***

#### **Template Variables**

All **Flight Change Email Templates** can include the following **variables** to personalize content dynamically:

| Variable       | Content                                      |
| -------------- | -------------------------------------------- |
| Airline        | Name of airline                              |
| Flight Number  | Flight number                                |
| Departure date | Date; in local time at the departure gateway |
| Departure time | Time; in local time at the departure gateway |
| Arrival date   | Date; in local time at the arrival gateway   |
| Arrival time   | Time; in local time at the arrival gateway   |

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
