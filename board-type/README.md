# Board Type

Each hotel defines a default board basis per room, as specified in the current hotel contract configuration. Additionally, some hotels support the application of board supplements, which can be optionally added to enhance or modify the default board offering.

Board types are configurable at the company level and may be used for various purposes beyond indicating meal inclusions (e.g., internal categorization, pricing models).

Board supplement policies vary by hotel:

* **Uniform board type per room**: All guests assigned to a room must have the same board type or supplement.
* **Individual board type per guest**: Each guest may independently select a different board type or supplement within the same room.

Board type assignments are subject to change over time. A hotel contract may define one board type for a room in a given year and a different board type for the same room in subsequent contract periods, depending on negotiated terms.

System implementations should accommodate these variations to ensure accurate handling of board type configurations and restrictions across hotels and contract versions.

## Board Types Management

The **Board Types** section allows system administrators or product managers to configure and maintain the list of board types available in the system. These types are used to define the meal and service options associated with a room booking at a hotel.

<figure><img src="../.gitbook/assets/image (16) (2).png" alt=""><figcaption></figcaption></figure>

### Overview

Board Types represent different service packages offered by hotels. These may include combinations of meals, drinks, and seasonal offerings. Each board type is uniquely identified by a code and can be used across multiple hotel contracts and room configurations.

### UI Elements

| Column       | Description                                                  |
| ------------ | ------------------------------------------------------------ |
| **Name**     | Display name of the board type, shown in system  (mandatory) |
| **Code**     | Unique system identifier (mandatory).                        |
| **ListName** | Label displayed in selection lists (mandatory)               |
| **HTMLText** | Optional. Can store HTML-formatted content for rich display. |

### Actions

* **Create**: Click the `Create` button (top right) to add a new board type. You will need to provide values for at least the `Name``, Code and ListName` fields.
* **Delete**: Use the trash icon next to a board type to remove it. Deletion is only possible if the board type is not referenced in existing contracts or configurations.

### Use in System

Board Types are used in:

* Hotel / Allotment
* Extras/Extras
* Webbooking
* Booking window
* Ticket
