# Flight Change - Email Template

In the Email Center menu, you will create various flight change email/SMS templates, used to inform/confirm customers of changes to their flight.

#### Flight Change templates&#x20;

To support the different type of change the following new templates are required:

| Template                     |
| ---------------------------- |
| Flight Change Large, earlier |
| Flight Change Small, earlier |
| Flight Change Tiny, earlier  |
| Flight Change Tiny, later    |
| Flight Change Small, later   |
| Flight Change Large, later   |
| Flight Change Flight number  |

If the specific template above is not found, the fallback is the current "Flight change email" template.

All the Flight Change email templates will can use the following variables:

| Variable       | Content                                      |
| -------------- | -------------------------------------------- |
| Airline        | Name of airline                              |
| Flight Number  | Flight number                                |
| Departure date | Date; in local time at the departure gateway |
| Departure time | Time; in local time at the departure gateway |
| Arrival date   | Date; in local time at the arrival gateway   |
| Arrival time   | Time; in local time at the arrival gateway   |

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
