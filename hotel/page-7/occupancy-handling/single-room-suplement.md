# Single Room Suplement

This feature can be found in Hotel -> Single Room Supplement.

A single room supplement is an additional charge imposed when one guest occupies a room designated for more than one occupant (e.g., a double room).

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

### 📌 Interface Overview

| **Column**          | **Description**                                                                                                                                                                                          |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Actions**         | Edit or manage the record (pencil icon opens the editing interface).                                                                                                                                     |
| **From Age**        | Minimum age of the guest to whom this supplement applies.                                                                                                                                                |
| **To Age**          | Maximum age of the guest to whom this supplement applies.                                                                                                                                                |
| **Start Date**      | Start date of the supplement's validity.                                                                                                                                                                 |
| **End Date**        | End date of the supplement's validity.                                                                                                                                                                   |
| **Supplement Code** | Identifies the type of supplement. In this case, "SINGLE".                                                                                                                                               |
| **Price**           | Flat amount (in monetary units) to be charged as the supplement.                                                                                                                                         |
| **Percent**         | Indicates if the supplement is applied as a percentage (Checked: The supplement is a percentage on top of the Single room supplement cost. Unchecked: The supplement is a cost on top of the room cost). |
| **PD**              | Per Day: Is per day - If checked, this makes the value be applied per day not per interval                                                                                                               |
| **Hotel Room**      | Specific room type the supplement is applied to (e.g., "Double Room Standard").                                                                                                                          |
| **Period**          | Period reference, typically linked to predefined booking periods.                                                                                                                                        |

### ➕ Actions

* **Create**: Opens a new form to define a different supplement configuration.
* **Edit (✏️)**: Modify the details of an existing supplement record.

When you insert for the first time a rule to the hotel, if is not already created:

* The system will create a new supplement category named "single-room", code SINGLE.
* The system will create a new supplement; code=SINGLE; name="Single room supplement (automatically added)", linked to the SINGLE category.

When a room listed in ROOMS is booked for a single person, the supplement must be applied.

<figure><img src="../../../.gitbook/assets/image (181).png" alt=""><figcaption></figcaption></figure>
