# Add Transport Modes and Transport Types to Extras Resources

### Overview

You can link an **Extra** to a transport resource. This controls when the extra is shown during booking.

Extras Resources support two filters:

* **Transport Modes**
* **Transport Types**

Use these filters to limit an extra.

Only show it for certain kinds of transport.

### Access

* Open **Extras Setup → Extras**.
* Open your extra.
* Go to **Resources**.

### Purpose

Transport Mode and Transport Type allow you to control **when an extra is available**, based on the transport used in the booking.

This is useful when selling extras such as golf bags, infant prices, or seat selection on Dynamic Packages, while ensuring that these extras are not handled as ancillaries in Amadeus.

### Transport filters screenshot

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/image (603).png" alt="Transport Mode and Transport Type filters in Resources."><figcaption></figcaption></figure></div>

### Transport Modes

Transport Mode allows you to restrict results to specific modes of transportation, such as FLY (Flight) or Bus.

If a booking does not match the selected Transport Mode, the extra will not be displayed.

| **Transport Mode** | **Used for**             |
| ------------------ | ------------------------ |
| FLY (flight)       | Filtering Transport Type |
| CAR                | Self-traveling by car    |
| BUS                | Travel by bus            |
| TRAIN              | Travel by train          |

### Transport Type

Transport Type restricts an extra to bookings that use a specific type of transport. If a booking does not match the selected Transport Type, the extra will not be displayed.

| **Transport Type** | **Used for**                                      |
| ------------------ | ------------------------------------------------- |
| Charter            | Charter with fixed out and return flights         |
| Dynamic            | GDS transports                                    |
| Sys-real           | Charter using real transport based on single legs |
| System             | GDS transports                                    |

If both Transport Mode and Transport Type are selected, the combination must correspond to the Transport Mode and Type of the booking, else the extra will not be displayed.

### How to set Transport Mode and Transport Type

1. In Tourpaq Office, go to **Extras Setup → Extras**.
2. Open the extra you want to change.
3. Go to **Resources**.
4. Select one or more **Transport Mode** values.
5. Optional: select one or more **Transport Type** values.
6. Click **Save**.

### Using excluded values

Both filters support **Use as Excluded**.

Turn it on to exclude what you selected. The extra will be available for everything **except** those values.

#### Example

* You do not want an extra to show for flights.
  * Transport Mode = FLY
  * Use as Excluded = enabled

### Important notes

* Both filters support multiple selections.
* If you leave **Transport Type** empty, the extra can be used with all transport types.
* **Transport Mode** does nothing unless the selected Transport Type supports it.
* These filters can help avoid sending extras to Amadeus.

### Related pages

* [Extras](../extras.md)
* [Resources](./)
