# Rooms – Hotel Contract Configuration

### Purpose

The **Rooms** tab is where you define the room types included in the contract. These room definitions drive pricing, occupancy rules, and room selection during booking.

***

### Screenshot

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Preconditions

Before you start:

* The hotel contract exists and is open for editing.
* You know the supplier’s room types and occupancy rules.
* You know if room types should be created, imported, or overridden.

***

### Fields

| Field                     | Description                                                                                                                                             |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Room Type Code**        | Internal system code for the room type (for example `2V+1B` = 2 adults + 1 bed). You can create a new code, override an existing code, or import codes. |
| **Parent Room**           | Used to group variations of rooms under a base category. Select the parent room if this is a derivative room type.                                      |
| **List Text Name**        | Label shown in dropdowns and public-facing lists (for example “Dbl room (2–4 pers.)”).                                                                  |
| **Name**                  | Internal reference name, often used in supplier communication.                                                                                          |
| **Minimum** / **Maximum** | Minimum and maximum occupancy allowed for this room type.                                                                                               |
| **Max Extra**             | Maximum number of extra adults allowed.                                                                                                                 |
| **Max Extra Child**       | Maximum number of children allowed in addition to base occupancy.                                                                                       |

***

### Buttons and actions

* **Override existing base room**: Replaces an existing room type in the base configuration.
* **Add new room type from existing**: Creates a new room type based on an existing one.
* **Add new room type from hotel**: Pulls room definitions directly from the hotel record (if available).
* 🗑️ **Delete icon**: Removes a room entry from the current contract.

***

### Tips

{% hint style="info" %}
Set **Minimum / Maximum** early. Period pricing and booking validation depend on it.
{% endhint %}

* Use **Parent Room** to keep reporting and sorting clean.
* Keep **Room Type Code** stable over time. It is used in exports and rules.
* Use **List Text Name** for user-facing clarity. Keep **Name** supplier-friendly.

***

### Related workflows

* [Periods – Hotel Contract Configuration](periods-hotel-contract-configuration.md): Room types must exist before you add period rows.
* [Board Supplements - Hotel Contract Configuration](board-supplements-hotel-contract-configuration.md): Room setup affects where supplements can apply.
* [Extra Beds Cost – Hotel Contract Configuration](extra-beds-cost-hotel-contract-configuration.md): Occupancy and extra limits control allowed extra beds.

***

### FAQ

**What’s the difference between “Room Type Code”, “Name”, and “List Text Name”?**\
**Room Type Code** is the system key used in rules and exports.\
**Name** is an internal label, often supplier-facing.\
**List Text Name** is what users typically see in dropdowns.

**When should I use “Parent Room”?**\
Use it for variants of a base room type.\
Example: “Double Sea View” under parent “Double”.

**What happens if Minimum/Maximum is wrong?**\
Bookings may fail validation or auto-match the wrong room.\
Pricing and extra bed logic can also break.

**Should I import rooms from the hotel or create them manually?**\
Import when the hotel record is already maintained and accurate.\
Create manually when the contract needs a custom room set.

**What does “Override existing base room” actually change?**\
It replaces the base room definition used by this contract.\
Use it when the global definition is wrong for this supplier.

**Can I delete a room type after adding periods?**\
Avoid it. Period rows may still reference the room code.\
Remove period rows first, then delete the room type.
