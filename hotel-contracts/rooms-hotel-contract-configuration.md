# Rooms – Hotel Contract Configuration

#### Purpose

The **Rooms** tab allows you to define and configure the room types included in the contract. This step is crucial for ensuring correct price application, occupancy handling, and room categorization during booking.

***

#### Screenshot

<figure><img src="../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

***

#### Instructions – Fields and Actions

| Field                     | Description                                                                                                                                                |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Room Type Code**        | Internal system code for the room type (e.g., `2V+1B` for 2 adults + 1 bed). Options include creating new, overriding existing, or importing from a hotel. |
| **Parent Room**           | Used to group variations of rooms under a base category. Select the parent room if this is a derivative room type.                                         |
| **List Text Name**        | Name displayed in dropdowns and public-facing lists (e.g., "Dbl room (2-4 Pers.)").                                                                        |
| **Name**                  | Internal reference name, often used in supplier communication.                                                                                             |
| **Minimum** / **Maximum** | Minimum and maximum occupancy allowed for this room type.                                                                                                  |
| **Max Extra**             | Maximum number of extra adults allowed.                                                                                                                    |
| **Max Extra Child**       | Maximum number of children allowed in addition to base occupancy.                                                                                          |

***

#### Buttons and Actions

* **Override existing base room**: Replaces an existing room type in the base configuration.
* **Add new room type from existing**: Add a room type from one that are already exist.
* **Add new room type from hotel**: Pulls room definitions directly from the hotel record (if available).
* 🗑️ **Delete icon**: Removes a room entry from the current contract.

***

#### Related Workflows

* **Contract Periods Tab**: Room types defined here are required before applying period-based pricing.
* **Board Supplements / Extra Beds**: Room configuration impacts which supplements apply and how many beds can be added.
* **Booking Process**: Room types and constraints (min/max) directly affect room availability, auto-matching with passenger count during booking.
