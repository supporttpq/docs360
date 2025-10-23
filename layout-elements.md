# Layout Elements

## Elements

### Overview

The **Layouts Element** page is used to define and manage individual layout elements for transportation modules (e.g., airplanes) or for hotels. Each element represents a visual and functional component (such as seats, wings, exits, toilets, room, stairs) that can be used when designing a seating or cabin layout or a hotel layout.

By combining these elements, the system can generate accurate seat maps for bookings and passenger visualization, and a clear hotel background of the hotel.

### Purpose

* **Standardization**: Ensure consistent definitions of layout elements across all layouts.
* **Visualization**: Provide clear icons and labels for end users booking seats or viewing layouts.
* **Flexibility**: Allow administrators to create new elements (like special seats, exits, or decor) when needed.
* **Accuracy**: Support seat booking logic by distinguishing between available, reserved, or occupied seats.

### Instructions

#### Fields Overview

<figure><img src=".gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure>

| Field                   | Purpose                                                                                | Instructions                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ----------------------- | -------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**                | The descriptive name of the layout element.                                            | Choose a clear and recognizable name (e.g., _Standard Seat_, _Toilet_, _Exit_, _Reserved_). Use consistent naming conventions to avoid confusion.                                                                                                                                                                                                                                                                                                                                              |
| **For Type**            | Defines the transport type the element belongs to (e.g., Airplane, Bus, Train, Hotel). | Select the correct type when creating a new element.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Image**               | Visual representation (icon) used to display the element in layouts.                   | Each element should have an appropriate icon for easier identification (e.g., a seat icon, WC for toilet, exit arrow, room, stairs etc.).                                                                                                                                                                                                                                                                                                                                                      |
| **Element Type**        | Defines the functional type of the element.                                            | <p>Options include:<br>- <strong>Seat</strong> – passenger seat<br>- <strong>Empty Seat Current Booking</strong> – unoccupied seat in the current booking<br>- <strong>Occupant Seat Current Booking</strong> – occupied seat in the current booking<br>- <strong>Occupant Seat Other Booking</strong> – occupied seat in another booking<br>- <strong>Nose / Tail / Wing</strong> – aircraft structure parts<br>- <strong>Decor</strong> – non-interactive elements like exits or toilets</p> |
| **Delete (trash icon)** | Removes the element definition from the system.                                        | Use with caution, as deleting an element may affect existing layouts.                                                                                                                                                                                                                                                                                                                                                                                                                          |

#### Example Workflow

1. **Creating a New Layout Element**
   * Click **Create** in the top-right corner.
   * Enter a **Name** (e.g., _Extra Legroom Seat_).
   * Choose the **Layout** **Type** (e.g., Airplane).
   * Upload/select an **Image** icon.
   * Assign an **Element Type** (e.g., Seat).
   * Save the new element.
2. **Editing an Existing Element**
   * Select the element by clicking on it.
   * Update fields as needed (e.g., changing the image or element type).
   * Save changes.
3. **Deleting an Element**
   * Click the **trash icon**.
   * Confirm deletion.
   * Be aware: removing an element may break layouts where it is already in use.

#### Notes

* **Seats** are the most common elements and may include variations (standard, infant, reserved).
* **Structural elements** like _Nose_, _Tail_, or _Wing_ are non-interactive and used for design accuracy.
* **Decor elements** (e.g., toilets, exits) help passengers understand the layout but are not bookable.
* **Reserved/Selected seats** support booking logic, showing real-time availability.



## Backgrounds

### Overview

The **Backgrounds** tab in the **Layouts Element** section defines the structural backgrounds for layouts, such as **hotel property maps** or **airplane cabin layouts**. Unlike individual elements (seats, exits, toilets, etc.), backgrounds provide the **base canvas** on which layout elements are placed.

They ensure that layouts are visually accurate and context-specific (e.g., hotel floor plans or airplane seating maps).

### Purpose

* **Visualization**: Provide a clear and accurate background image (floor or aircraft diagram) where layout elements can be positioned.
* **Context**: Help users understand where facilities, rooms, or seats are located.
* **Standardization**: Ensure layouts for each hotel or transport type are built consistently with correct backgrounds.
* **Flexibility**: Allow different backgrounds for different vehicle types (e.g., Airbus A320 vs. Boeing 737) or hotels.

### Instructions

#### Fields Overview

| Field                   | Purpose                                                                               | Instructions                                                                                                                                                                 |
| ----------------------- | ------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**                | Name of the background (e.g., hotel name, aircraft type, or floor reference).         | Enter a clear, descriptive name (e.g., _Airbus A320 – 168_, _737-700_, _PCU31-ground_, _BG Mellieha_). Naming must match its real-world counterpart for easy identification. |
| **For Type**            | Defines whether the background belongs to a **Hotel** or an **Airplane** (transport). | Select **Hotel** for property floorplans, **Airplane** for seat maps.                                                                                                        |
| **Image**               | The visual image representing the background (floorplan, aircraft diagram).           | Upload or select a clear, scaled background image. Ensure proportions are correct so layout elements align properly.                                                         |
| **Delete (trash icon)** | Removes the background from the system.                                               | Use with caution. If a background is deleted, any layouts using it will lose their reference image.                                                                          |

#### Example Workflow

1. **Creating a New Background**
   * Click **Create** (top-right).
   * Enter the **Name** (e.g., _Airbus A321 – 200_ or _Hotel VIL30 – Ground Floor_).
   * Select **Layout Type** (**Hotel,** **Airplane, Bus, Train**).
   * Upload/select the **Image** (e.g., aircraft cabin layout or hotel floorplan).
   * Save the background.
2. **Editing a Background**
   * Click on an existing background entry.
   * Update its **Name** or **Image** if needed.
   * Save changes.
3. **Deleting a Background**
   * Click the **trash icon** next to the background.
   * Confirm deletion.
   * Ensure no active layouts depend on this background before deleting.

***

#### Notes

* **Hotel backgrounds** (e.g., _VIL30-floor_, _BG Mellieha_) are used for property maps or floor plans where rooms/facilities are placed.
* **Airplane backgrounds** (e.g., _Airbus A320 – 168_, _737-700_) are used for seat maps, with seats and other cabin elements added on top.
* Backgrounds should be **high-quality and proportional** to avoid misalignment of elements.
* Always check that the correct **Layout Type** is selected to prevent mixing hotel and transport layouts.
