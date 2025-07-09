---
hidden: true
noIndex: true
---

# Flexible Transports

Flexible transports is a feature that allows the creation of flexible rules to generate new transport combinations based on existing ones. It utilizes the departure date from the outbound transport and the return date from the homebound transport.

<figure><img src=".gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure>

**Note**: In a booking, when a generated transport is selected, the transport allotments will be allocated directly from the parent homebound and outbound transports.

### Define departure dates

To create new transport combinations from existing transports, it is essential to define a departure date. This date determines the range of combinations that will be generated between the specified Start Date and End Date, based on the selected departure and return days.

| Field          | Description                                                                                        |
| -------------- | -------------------------------------------------------------------------------------------------- |
| DayOfTheWeek   | The departure day of the outbound transport                                                        |
| MinDays        | The minimum number of days required for the trip                                                   |
| MaxDays        | The maximum number of days allowed for the trip                                                    |
| HomeboundDates | The available return days for homebound transport                                                  |
| Warning        | A collection of warnings that indicate potential problems or issues with the generated transports. |

<figure><img src=".gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

### Define price list

Each transport that is generated will be associated with a specific pricelist, which will be defined for the corresponding agencies and hotels

<figure><img src=".gitbook/assets/image (139).png" alt=""><figcaption></figcaption></figure>
