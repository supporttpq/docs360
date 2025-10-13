# Allotments per day

### **Overview**

The **Allotment per Day** screen is part of the hotel configuration module. It is used to define and monitor the number of rooms available (allotment) for each room type on a daily basis. This ensures that booking agents and the system know exactly how many rooms can be sold or held on specific dates.

This section is essential for managing availability, avoiding overbookings, and ensuring accurate tracking of room inventory.

### **Purpose**

The purpose of the Allotment per Day functionality is to:

* Allocate a daily number of rooms for each room type.
* Define secured and guaranteed allotments with the hotel.
* Track how many rooms are already booked and how many remain free.
* Adjust daily availability to match contracts, demand, or sales limits.
* Support smooth booking operations by providing clear visibility of inventory.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Field Descriptions**

| Field                   | Description                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- |
| **Room**                | Indicates the room type or category being configured. Example formats: `1/1`, `1/2-SH`.                  |
| **Date**                | The calendar date for which allotment is being defined.                                                  |
| **Day**                 | The day of the week for the selected date                                                                |
| **No.**                 | The number of rooms allocated.                                                                           |
| **Secured**             | Number of rooms secured through a contract with the hotel. These rooms are guaranteed to be available.   |
| **Guaranteed**          | Rooms that are financially guaranteed to the hotel, regardless of sales. Usually part of contracts.      |
| **Book**                | Number of rooms already booked by customers for this date.                                               |
| **Free**                | Remaining available rooms (calculated as allotment minus booked).                                        |
| **Room Above  Book**    | Number of shered rooms booked                                                                            |
| Room Above Free         | Nomber of shered rooms free                                                                              |
| R                       | True (green) if the room is released                                                                     |
| For R                   | Number of rooms available for release                                                                    |
| Max                     | The maximum number of rooms                                                                              |
| Extra                   | Extra rooms number                                                                                       |
| Pax 1, Pax2, Pax3, Pax4 | The maximum number of rooms with a max of  1 - 4 pax                                                     |
| Min                     | The minimum stay                                                                                         |
| Stay length             | Specifies how many rooms are allocated for a charter transport based on the selected number os stay days |

{% hint style="warning" %}
**PAX1, PAX2, PAX3, PAX4** – When you hover over these cells, a tooltip appears showing the number of booked rooms for each corresponding PAX category (PAX1, PAX2, PAX3, PAX4).


{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note: If stop sales are enabled for a hotel on a certain date, a message ( yellow triangle near room) will be visible&#x20;
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



### Search with Allotment Control

#### **Functionality**

When searching with **Allotment Control**:

* The search is based on **departure date**.
* Results display per transport, with columns for:
  * **R (Rooms Allotted)** – The predefined room allotment set for the transport.
  * **B (Rooms Booked)** – The number of rooms already booked for that transport.

The columns together provide a quick overview of remaining availability.

#### **Room Control Status**

Each transport displays a **control status value** that determines how many rooms can be sold:

* **-1** → No room limit (unlimited sales possible).
* **0** → No rooms can be sold on this transport.
* **1+** → The exact maximum number of rooms that can be sold for the specified transport and interval.

#### **Usage Notes**

* This feature is critical for **capacity planning** and ensuring correct allocation of hotel rooms per flight.
* The status values should be monitored regularly, especially during peak booking periods, to avoid overselling.
* Adjustments to allotments must be coordinated with both transport and hotel availability.

### **Instructions for Use**

1. Navigate to **Hotel → Allotment per Day** when setting up or editing a hotel.
2. Select the **Period** (date range), **Room Type**, and optionally filter by **Week Days** to view or adjust availability.
3. Click **Search** to display the daily allotment table.
4. For each **date and room type**:
   * Enter or adjust the number of rooms in **No.**, **Secured**, and **Guaranteed** fields.
   * Verify the number of **Booked** and **Free** rooms (system-calculated).
   * If applicable, set values for **Max**, **Extra**, and **PAX fields**.
5. Use the checkboxes to select days and apply bulk actions if available.
6. After making changes, click **Update** to save.
7. Use **Allotment History** to review previous changes.
8. To cancel changes without saving, click **Cancel**.
