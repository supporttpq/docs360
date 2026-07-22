---
description: Filter and analyze scheduled transports, seat usage, and costs.
---

# All Transports

<figure><img src="../.gitbook/assets/image (18) (2).png" alt=""><figcaption></figcaption></figure>

### Overview

The **All Transports** page gives you an overview of scheduled transports. You can filter, review, and analyze departures, arrivals, seat usage, and costs.

### Typical workflow

{% stepper %}
{% step %}
**Set your date range**

Use **Transport Date (Start – End)** first. It usually reduces the result set the most.
{% endstep %}

{% step %}
**Narrow down the list**

Add filters like **Departure / Arrival**, **Transport Type**, and **Weekdays**.
{% endstep %}

{% step %}
**Review and adjust columns**

Sort by column headers and add extra columns if needed.
{% endstep %}

{% step %}
**Export selected transports**

Use the left-side checkboxes to select rows, then run your export action.
{% endstep %}
{% endstepper %}

### Filters & Controls

* **Transport:** Filter by transport code.
* **Transport Date (Start – End):** Select a date range.
* **Departure / Arrival:** Filter by departure and arrival points.
* **Flight No:** Search by flight or transport number.
* **Weekdays:** Limit results to specific weekdays.
* **Arrival Country:** Filter by arrival country.
* **Transport Type:** Filter by how the transport is generated and priced.
  * **Charter transports:** Use **Fix Quotas** to define flights.
  * **Dynamic transports:** Use dynamic itineraries. Legs can use real transports and/or external providers (GDS).
  * **Sys-real transports:** Generated from a transport rule. Both legs use real transports.
  * **System transports:** Generated from a transport rule. At least one leg uses an external provider (GDS).
* **Transport Mode:** Filter by category (Boat, Bus, Car, Flight/Train).
* **Direction:** Travel Home, Travel Out, or Both Ways.
* **More Filters:** Open advanced filters.
* **Clear:** Reset all filters.
*   **Use Real Transports:** Show only real transports.

    <figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>
* **Save View:** Save the current filters as a reusable custom view.

### Table Columns

| Column        | Description                                                           |
| ------------- | --------------------------------------------------------------------- |
| **Date**      | The scheduled date of the transport.                                  |
| **Transport** | The transport code.                                                   |
| **Dep. Time** | Departure time.                                                       |
| **Arr. Time** | Arrival time.                                                         |
| **Seats**     | Total number of available seats for the transport.                    |
| **GES**       | Guaranteed empty seats.                                               |
| **AOT**       | Allotment seats total.                                                |
| **BOT**       | Booked seats total – total passengers with reservations.              |
| **Cost**      | Cost of the transport, shown in the local currency (e.g., DKK (kr.)). |

* Click column headers to **sort** (for example, Date or Cost).
*   Click the three dots on the right to add columns.

    <figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>
*   Use the left-side **checkboxes** to select transports for export.

    <figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

Cost is shown in the transport’s local currency.

Example: `DKK (kr.)`.

### Related pages

* [Transport](transport/)
* [Transport Definition](transport/transport-definition.md)
* [Transport Matrix](transport/transport-matrix.md)
