# Transport

### Overview

The **Transport** page is the master list of your transport routes.

Use it to create, edit, and maintain transport codes for flights, buses, and more.

{% hint style="info" %}
Need departures, seat totals, and cost analysis for a date range? Use [**All Transports**](../all-transports.md).
{% endhint %}

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Transport list showing codes, departure/arrival, airline, and reporting type."><figcaption></figcaption></figure>

### Typical workflow

{% stepper %}
{% step %}
### Filter the list

Use **Code**, **Departure**, and **Arrival** to narrow results fast.
{% endstep %}

{% step %}
### Open a transport

Click a **Code** to open the transport for editing.
{% endstep %}

{% step %}
### Create a new transport

Use **Create** for manual setup, or **Create using wizard** for guided setup.
{% endstep %}
{% endstepper %}

### Filters & controls

At the top of the page, filters help refine the list:

| Filter             | Description                                            |
| ------------------ | ------------------------------------------------------ |
| **Code**           | Search or filter by transport code.                    |
| **Departure**      | Filter by departure location (e.g., Billund, Kastrup). |
| **Arrival**        | Filter by destination/arrival location.                |
| **All Transports** | Filter by transport category or type.                  |
| **Show Visible**   | Show visible or hidden transports.                     |
| **Clear**          | Reset all filters.                                     |

Buttons:

* **Create** – Adds a new transport entry manually.
* **Create using wizard** – Launches a step-by-step creation tool for guided setup.

### List columns

| Column                  | Description                                                                |
| ----------------------- | -------------------------------------------------------------------------- |
| **Code**                | Unique identifier for the transport, flight code.                          |
| **Return**              | Associated return transport code.                                          |
| **Departure**           | City or location where the transport originates.                           |
| **Arrival**             | Destination city/location.                                                 |
| **Dynamic Itineraries** | Shows whether dynamic itinerary support is enabled (✔ = Yes, ✖ = No).      |
| **Airline**             | Name of the carrier (e.g., Airseven, KLM, Turkish Airlines).               |
| **Reporting Type**      | The platform used for reporting passenger and flight data (e.g., Paxport). |
| **Flight Number**       | Official flight number used by the carrier.                                |
| **Trash**               | Delete the transport record.                                               |

### Tips

* Click a transport **Code** to open edit mode.
* Sort by column headers (for example, **Airline** or **Code**).

### FAQ

<details>

<summary>What’s the difference between <strong>Transport</strong> and <strong>All Transports</strong>?</summary>

* **Transport** is your route master data (codes, default settings, reporting type).
* **All Transports** is the operational list for a date range (departures, seats, costs).

</details>

<details>

<summary>How do I show transports that are hidden?</summary>

Use the **Show Visible** filter to switch between visible and hidden transports.

</details>

<details>

<summary>When should I use <strong>Create</strong> vs <strong>Create using wizard</strong>?</summary>

* Use **Create** when you already know the fields you need.
* Use **Create using wizard** when you want a guided setup flow.

</details>

<details>

<summary>What does <strong>Dynamic Itineraries</strong> mean?</summary>

It indicates whether the transport uses dynamic itinerary logic.

When enabled, pricing and settings can be driven by legs and real transports.

</details>

<details>

<summary>Why do I see no transports in the list?</summary>

Most common causes:

* **Departure** / **Arrival** filters don’t match any records.
* You are only showing **Visible** transports, but the ones you need are hidden.
* The **All Transports** filter is set to a category/type that excludes your routes.

</details>

<details>

<summary>Why can’t I edit or delete a transport?</summary>

You usually don’t have the required permissions.

If you should have access, ask an admin to check your role for transport setup.

</details>

<details>

<summary>What’s the difference between <strong>Hidden</strong> and <strong>Deleted</strong>?</summary>

* **Hidden** transports still exist. You can show them and re-enable later.
* **Deleted** transports are removed from the list.

If you’re unsure, hide first. Delete only when you’re certain.

</details>

<details>

<summary>Why is <strong>Airline</strong> or <strong>Flight Number</strong> empty?</summary>

Those fields are often only set when the transport is a flight.

They can also be configured later during transport setup and scheduling.

</details>

<details>

<summary>Where do I set seats, departures, and costs?</summary>

This page is the route list.

Operational data like departures, seats, and cost analysis lives in [**All Transports**](../all-transports.md).

</details>

### Related pages

* [All Transports](../all-transports.md)
* [Transport creation](transport-creation/)
* [Transport Definition](transport-definition.md)
* [Transport Matrix](transport-matrix.md)
* [Transport Dashboard](../../transport-dashboard.md)
