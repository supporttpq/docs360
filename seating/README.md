# Seating

### Seat List

#### **Overview**

The **Seat List** page is used to define and manage seat layouts for different aircraft types. Each seat layout represents the configuration of seats used for a specific plane model, including the seat distribution per row and layout type.

This setup ensures that correct seat maps can be assigned to flights or transport departures, enabling accurate seat reservations and passenger placement.

***

#### **Purpose**

The **Seat List** allows system administrators to:

* Maintain an overview of all available seat layouts.
* Define new seat configurations for different aircraft models or transport types.
* Assign or edit seat positions for each layout.
* Hide unused or outdated layouts to keep the list organized.

Seat layouts defined here are later used when configuring transport departures.

***

#### **Preconditions**

Before configuring seat layouts:

1. Ensure the aircraft or transport type exists in the system and has a corresponding capacity setup.
2. You must have user permissions to access and edit the **Seat List** module.
3. If the layout should be used in a specific transport (e.g., a charter flight), make sure the corresponding contract or transport record is already created.

***

#### **Instructions**

1. **Show Unused** – Toggle this option to display layouts that are no longer in active use.
2. **Create** – Click to create a new seat layout. When creating, you must define:
   * **Name** – The name of the aircraft or transport model (e.g., _B737 – 168 Pax A7 2023_).
   * **Column Distribution** – Defines how seats are arranged in each row (e.g., _3x3_ for an airplane with six seats per row).
   * **Layout Type** – Defines the transport category, such as _Airplane_.
   * **Rows** - Defines the numer of rows in seat list
   * **Columns** - defines the numer of columns
   * **Default Seat Type** - Select wich seat tpe will be set as default
3. **Edit (✏️)** – Click to edit the name or configuration of an existing seat layout.
4. **Hide** – Temporarily removes a layout from the visible list without deleting it.
5. **Assign Seats** – Opens the seat assignment view where individual seats can be positioned and numbered according to the aircraft’s configuration.
6. **🗑️ (Delete)** – Permanently removes the seat layout from the system. This action cannot be undone.

***

**Column Descriptions**

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (3) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

| **Column**              | **Description**                                                                                |
| ----------------------- | ---------------------------------------------------------------------------------------------- |
| **Name**                | The aircraft or seat layout name, typically indicating the plane type and total seat capacity. |
| **Column Distribution** | Defines how seats are arranged in each column (e.g., 3x3 = six columns).                       |
| **Layout Type**         | The type of transport the layout applies to (e.g., Airplane).                                  |
| **Assign Seats**        | Opens the seat map editor to define and assign seat numbers.                                   |
| **🗑️**                 | Deletes the layout entry.                                                                      |

### Assign Seats

#### **Overview**

The **Assign Seats** page is used to configure the detailed seat map for a specific aircraft or transport layout.\
Here, you define the exact seat numbering, row structure, and position of each seat within the plane, ensuring that the seat map matches the real-world configuration used by the airline or transport provider.

Once seats are assigned, this layout is used in **Transport → Departures** to allow passengers to select or be automatically assigned a seat.

***

#### **Purpose**

The purpose of this feature is to:

* Create an accurate seat map reflecting the actual layout of the transport vehicle.
* Define individual seat numbers and their row/column positions.
* Mark specific seats as unavailable or extra-charge (e.g., exit row or premium seats).
* Support the booking system by displaying correct seat availability for each departure.

***

#### **Preconditions**

Before assigning seats:

1. A seat layout must already exist in the **Seat List** (with _Column Distribution_ and _Layout Type_ defined).
2. The aircraft or transport type must have a known capacity and configuration.
3. You must have the required permissions to edit layouts.
4. The layout should not be assigned to an active departure in operation (to avoid conflicts).

***

#### **Instructions**

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (3) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

1. **Open the Assign Seats view**\
   From the **Seat List**, click **Assign Seats** next to the layout you want to configure.
2. **Seat Map Area**\
   A grid will appear, divided into rows and columns based on the _Column Distribution_ (e.g., 3x3). Each cell represents a potential seat position.
3. **Add or Remove Seats**
   * To **add a seat**, click an empty cell and assign a seat number (e.g., _1A_, _1B_, _1C_).
   * To **remove a seat**, click on it and select **Delete**.
4. **Set Seat Properties**\
   Each seat include:
   * **Seat Name** – Unique identifier for the seat (e.g., _12F_).
   * **Row Number** – Indicate the row.
   * **Type** – Standard, exit row, extra legroom, etc.
   * **Seat Number** – Defines the seat numer in a row.
5. **Reorder or Adjust Rows**\
   Rows can be inserted, duplicated, or deleted to match the aircraft’s physical layout.
6. **Save Changes**\
   After completing the configuration, click **Save** to finalize the seat map.\
   The updated layout becomes available in all transports using this configuration.

***

**Result**

When the seat layout is correctly configured:

* It becomes selectable in **Transport Layouts**
* Passengers can view and choose seats according to the defined structure.
