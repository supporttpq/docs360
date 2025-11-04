# Flight change

#### **Overview**

The **Flight Change System** automatically detects and manages updates to flight details such as departure times, arrival times, and flight numbers. It ensures passengers are notified about flight modifications and provides tracking for unconfirmed notifications.

***

#### **Automatic Flight Change Generation**

A **flight change** is automatically created when any of the following occur:

* The **departure time** or **arrival time** is edited.
* The **flight number** is changed.

Each flight change is categorized by **magnitude** and **direction** based on the time adjustment.

| **Category**             | **Description**                                                                                                       |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------- |
| **Tiny / Small / Large** | Classification based on configurable time intervals.                                                                  |
| **Sooner / Later**       | <p>Indicates whether the flight was moved earlier or delayed.<br>Example: A 10-minute delay → <em>Tiny Later</em></p> |

***

#### **Queue Management**

* Each flight change is **queued** in the **Flight Change System**.
* Flight changes must be **manually released or dropped** by the user.
* If the **same flight is edited multiple times**, multiple flight changes are queued. The user must manually **delete duplicate entries**.

***

#### **Overview and Filtering**

The system provides a detailed **overview of destinations and flight changes**, with **multiple filtering options** to help users manage and locate specific updates easily.

***

#### **Guest Communication Process**

1. When a flight change is submitted, a **notification email** is sent to the guest.
   * The email contains a **confirmation link** for the guest to acknowledge the change.
2. If the guest **does not confirm receipt**, the system will:
   * **Resend the email** several times.
   * Then, **send an SMS reminder** asking the guest to check their email and confirm the change.
3. Within the system, it is easy to identify guests who **have not yet confirmed** receipt.
4. If no confirmation is received after multiple attempts, the flight change is **forwarded to a service email**, allowing the team to take further action (such as calling the passenger).

***

#### **Customer Outcome**

* Ensures **transparent communication** with passengers regarding flight schedule updates.
* Reduces **manual workload** by automating detection, notification, and follow-up processes.
* Enables **efficient tracking and intervention** when guests fail to confirm flight changes.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Filter Section (Top Panel)

| Field Name            | Description                                                                  |
| --------------------- | ---------------------------------------------------------------------------- |
| **Departure Gateway** | Dropdown to filter by the origin airport of the flight.                      |
| **Arrival Gateway**   | Dropdown to filter by the destination airport.                               |
| **Flight No.**        | Text field to search for a specific flight number.                           |
| **Type of Change**    | Dropdown to filter by the nature of the flight change.                       |
| **Status**            | Dropdown to filter by the current status of the change (e.g., Queued, Sent). |
| **Airline**           | Dropdown to filter flights by airline.                                       |
| **Booking**           | Text field to search by booking number.                                      |
| **Transport**         | Dropdown to filter by transport identifier or vehicle.                       |
| **Departure Date**    | Calendar picker to select the flight's departure date.                       |
| **Created Date**      | Calendar picker to select when the change record was created.                |
| **Departure Time**    | Time selector to narrow results by flight departure time.                    |
| **Show confirmed**    | Checkbox to show the confirmed changes.                                      |
| **Show dropped**      | Checkbox to show the dropped changes.                                        |
| **Display**           | Button to apply current filter settings.                                     |
| **Clear**             | Button to reset all filters (with count of active filters).                  |

***

### Table Columns

| Column Name           | Description                                                                                  |
| --------------------- | -------------------------------------------------------------------------------------------- |
| **Created**           | Date when the flight change entry was created.                                               |
| **Booking**           | The booking that is affected by the flight change (link to the booking)                      |
| **Transport**         | The transport that is affected by the flight change (Link to the actual transport)           |
| **Airline**           | Name of the airline operating the flight.                                                    |
| **Flight No.**        | The flight number for the flight that has a flight change.                                   |
| **Departure Gateway** | The airport or location from where the flight departs.                                       |
| **Departure**         | The departure time in the local time of the departure airport                                |
| **Arrival Gateway**   | The destination airport or location of the flight.                                           |
| **Arrival Time**      | Scheduled arrival time at the destination.                                                   |
| **Type**              | Description of the flight change (e.g., “Flight Change Small Later”, “Tiny Later”).          |
| **Status**            | Current status of the flight change process (e.g., **Queued**, **Sent**, **Resend Second**). |

The flight change sent uses different templates depending on the type of change. This allows the company to decide the content based on the type of change.

When Send or Send SMS is selected, the flight change will be sent at once, independently of the Hour to send in the template.
