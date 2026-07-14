# Board Type

## **Intro**

**Board Type** defines the meal plans available in the system. A board type represents a specific meal arrangement, such as Breakfast, Half Board, or All Inclusive.

At the hotel level, the **Board Basis** defines which meal plan is included in the price.

A **Board Basis Extra** represents the meal plan included in the price of the room.. Each Board Basis Extra is linked to a Board Type, which identifies the meal plan it represents.

A **Board Supplement Extra** represents an upgrade to a different meal plan. Like a Board Basis Extra, it is linked to a Board Type that defines the meal plan being offered.

**Board Supplement Policy** controls how board supplements are handled in the booking process. The policy is configured on the **Extra Category** level and is shared by all hotels linked to that Extra Category.

Board type assignments are subject to change over time. A hotel contract may define one board type for a room in a given year and a different board type for the same room in other contract periods, depending on negotiated terms.

## Board Types Management

The **Board Types** section allows Administrators to configure and maintain the list of board types available in the system. These types are used to define the meal and service options associated with a room booking at a hotel.

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Overview

Board Types represent different service packages offered by hotels. These may include combinations of meals, drinks, and seasonal offerings. Each board type is uniquely identified by a code and can be used across multiple hotel contracts and room configurations.

### UI Elements

| Column                                                                                                       | Description                                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**                                                                                                     | Display name of the board type, shown in system (mandatory)                                                                                                                                    |
| **Code**                                                                                                     | Unique system identifier (mandatory).                                                                                                                                                          |
| **List Name**                                                                                                | Is used in all communication with the hotel (lists) (mandatory)                                                                                                                                |
| **Order** <i class="fa-arrow-up-long">:arrow-up-long:</i><i class="fa-arrow-down-long">:arrow-down-long:</i> | <p>The order of Board types is used when the system must automatically downgrade or upgrade a board type.<br>The topmost board type will be considered the highest order (most expensive).</p> |
| **Trash icon** <i class="fa-trash-can">:trash-can:</i>                                                       | Deletes the selected board from the list.                                                                                                                                                      |

### Actions

* **Create**: Click the `Create` button (top right) to add a new board type. You will need to provide values for at least the `Name, Code and ListName` fields.
* **Delete**: Use the trash icon next to a board type to remove it. Deletion is only possible if the board type is not referenced in existing contracts or configurations.
* **Ordering:** The order of Board types is used when the system automatically downgrades or upgrades a board type.
* **Edit:** Opens the selected Board Basis so you can view or modify its configuration, such as Name, Code, List Name, and Description.

## Edit Board Type

### Use in System

Board Types are used in:

* Hotel / Allotment
* Extras/Extras
* Webbooking
* Booking window
* Ticket
