# Seat Types

**Overview**

The **Seat Types** page defines the different seat categories used across all aircraft or transport layouts.\
Each seat type can have specific characteristics, icons, and passenger restrictions (e.g., “Extra Legroom,” “Exit Row,” “Standard,” or “No Infant Seat”).

These seat types are later used in the **Assign Seats** page to visually distinguish seat categories and apply restrictions or pricing logic in the booking process.

***

**Purpose**

The purpose of seat types is to:

* Standardize the definitions for various seat categories across the system.
* Control passenger eligibility (e.g., prevent infants from being assigned exit-row seats).
* Provide clear visual distinction between seat types for internal users and guests.
* Support price differentiation for premium or restricted seating options.

***

**Instructions**

1. **Open the Seat Types Page**\
   Navigate to **Transport → Seat List → Edit Seat Types**.
2. **View or Edit Existing Seat Types**
   * Each row represents a predefined seat type.
   * You can click the **pencil icon** to edit or update details.
3. **Create a New Seat Type**\
   Click **Create**, then fill in the fields described below.
4. **Save Changes**\
   After defining or editing a seat type, click **Save** to make it available for seat assignment.

***

**Field Descriptions**

| **Field / Column**     | **Description**                                                                                                            |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Name**               | The seat type name displayed in the system (e.g., _Extra Legroom Seat_, _Standard Seat_, _No Lean Seat_).                  |
| **Description**        | Additional explanation of the seat’s location or characteristics. This is often visible internally or to agents.           |
| **Icon**               | A small visual indicator used to differentiate seat types in seat maps                                                     |
| **Code**               | An internal identifier used for technical mapping or integrations. Usually a single character such as “X.”                 |
| **Don’t Allow Infant** | Checkbox defining whether infants are restricted from sitting in this seat type (e.g., for safety in exit rows).           |
| **Minimum Age**        | Defines the minimum passenger age allowed to occupy this seat. Common for exit-row seats (e.g., 16 or 18 years).           |
| **Maximum Age**        | Defines the maximum passenger age allowed to occupy this seat (e.g., to exclude elderly passengers from exit-row seating). |
| **Delete (🗑)**        | Removes the seat type from the list. Seat types already assigned in active seat maps cannot be deleted.                    |

***

**Example Use Cases**

| **Scenario**                      | **Seat Type Configuration**                                                |
| --------------------------------- | -------------------------------------------------------------------------- |
| Exit-row seats with extra legroom | “Extra Legroom” with **Minimum Age = 16** and **Don’t Allow Infant = Yes** |
| Standard economy seat             | “Standard” seat type with no restrictions                                  |
| Seats in front rows               | “Front Cabin” seat type, optional restriction for infants                  |
| Infant-accommodating seat         | “INF” seat type, with **Don’t Allow Infant = No**                          |

***

**Result**

Once seat types are defined:

* They become selectable in **Assign Seats** when configuring layouts.
* The system uses them to control seat availability and eligibility.
* The icons and restrictions appear in the seat selection view, ensuring passengers and agents see correct options during booking.
