# Flight change

### **Overview**

The **Flight Change System** automatically detects and manages updates to flight details such as departure times, arrival times, and flight numbers. It ensures passengers are notified about flight modifications and provides tracking for unconfirmed notifications.

***

### **Purpose**

The main purposes of the _Flight Changes_ page are:

* To provide visibility into **all flight schedule modifications**
* To allow teams to **filter changes** based on criteria like airline, gateway, booking, type, or status
* To help users quickly identify changes that require action (Queued, Resent First, etc.)
* To understand how each change affects downstream systems, customer itineraries, and operational workflows

### **Automatic Flight Change Generation**

A **flight change** is automatically created when any of the following occur:

* The **departure time** or **arrival time** is edited.
* The **flight number** is changed.

Each flight change is categorized by **magnitude** and **direction** based on the time adjustment.

| **Category**             | **Description**                                                                                                       |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------- |
| **Tiny / Small / Large** | Classification based on configurable time intervals.                                                                  |
| **Sooner / Later**       | <p>Indicates whether the flight was moved earlier or delayed.<br>Example: A 10-minute delay → <em>Tiny Later</em></p> |

***

### **Queue Management**

* Each flight change is **queued** in the **Flight Change System**.
* Flight changes must be **manually released or dropped** by the user.
* If the **same flight is edited multiple times**, multiple flight changes are queued. The user must manually **delete duplicate entries**.

***

### **Overview and Filtering**

The system provides a detailed **overview of destinations and flight changes**, with **multiple filtering options** to help users manage and locate specific updates easily.

***

### **Guest Communication Process**

1. When a flight change is submitted, a **notification email** is sent to the guest.
   * The email contains a **confirmation link** for the guest to acknowledge the change.
2. If the guest **does not confirm receipt**, the system will:
   * **Resend the email** several times.
   * Then, **send an SMS reminder** asking the guest to check their email and confirm the change.
3. Within the system, it is easy to identify guests who **have not yet confirmed** receipt.
4. If no confirmation is received after multiple attempts, the flight change is **forwarded to a service email**, allowing the team to take further action (such as calling the passenger).

***

### **Customer Outcome**

* Ensures **transparent communication** with passengers regarding flight schedule updates.
* Reduces **manual workload** by automating detection, notification, and follow-up processes.
* Enables **efficient tracking and intervention** when guests fail to confirm flight changes.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Filter Section (Top Panel)

| **Filter Field**               | **Description**                                                             |
| ------------------------------ | --------------------------------------------------------------------------- |
| **Departure Gateway**          | Filters by the airport where the flight or transport segment departs.       |
| **Arrival Gateway**            | Filters by the airport where the flight arrives.                            |
| **Flight No.**                 | Filters changes related to a specific flight number.                        |
| **Type of Change**             | Filters by the type of schedule change (e.g., later, earlier, large, tiny). |
| **Status**                     | Filters by the system status: _Queued_, _Sent_, _Resent First_, etc.        |
| **Airline**                    | Filters by the airline operating the affected flight.                       |
| **Booking**                    | Filters by booking reference number.                                        |
| **Transport Type**             | Filters by the type of transport (Transport, Real Transport).               |
| **Transport**                  | Filters by the specific transport code (e.g., BCNJPN-A04).                  |
| **Departure Date (Start–End)** | Filters by the date range of the flight’s departure.                        |
| **Created Date**               | Filters by the date the change was created in the system.                   |
| **Departure Time**             | Filters changes by scheduled departure time.                                |
| **Show confirmed**             | Checkbox to include changes marked as _Confirmed_.                          |
| **Show dropped**               | Checkbox to include changes that were _Dropped_.                            |
| **Display**                    | Runs the search and refreshes the table with current filters.               |
| **Clear**                      | Resets all filters to their default values.                                 |

***

### Table Columns

| **Column Name**       | **Description**                                                                        |
| --------------------- | -------------------------------------------------------------------------------------- |
| **Created**           | The date when the change entry was created in the system.                              |
| **Booking**           | The booking ID affected by this flight change.                                         |
| **Transport Type**    | Categorizes the type of transport (usually “Transport” for flights).                   |
| **Transport**         | Transport code representing the operational flight grouping.                           |
| **Airline**           | The airline operating the original or modified flight.                                 |
| **Flight No.**        | The flight number impacted by the schedule change.                                     |
| **Departure Gateway** | Airport from which the flight departs.                                                 |
| **Departure**         | Scheduled departure date and time.                                                     |
| **Arrival Gateway**   | Airport where the flight arrives.                                                      |
| **Arrival Time**      | Scheduled arrival time.                                                                |
| **Type**              | The type of change applied (e.g., Tiny Earlier, Tiny Later, Small Later, Large Later). |
| **Status**            | The internal processing status (Queued, Sent, Resent First, etc.).                     |

The flight change sent uses different templates depending on the type of change. This allows the company to decide the content based on the type of change.

When Send or Send SMS is selected, the flight change will be sent at once, independently of the Hour to send in the template.
