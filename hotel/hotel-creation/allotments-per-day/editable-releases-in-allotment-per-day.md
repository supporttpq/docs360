# Editable releases in Allotment per Day

### **Overview** <a href="#overview" id="overview"></a>

The **Allotment per Day** screen is part of the hotel configuration module. It is used to define and monitor the number of rooms available (allotment) for each room type on a daily basis. This ensures that booking agents and the system know exactly how many rooms can be sold or held on specific dates.

This section is essential for managing availability, avoiding overbookings, and ensuring accurate tracking of room inventory.

### **Purpose** <a href="#purpose" id="purpose"></a>

The purpose of the Allotment per Day functionality is to:

* View and adjust room availability per day and room type
* Define secured and guaranteed allotments with the hotel.
* Track how many rooms are already booked and how many remain free.
* Execute, undo or correct releases on a daily basis
* Override contract-level release rules when needed
* Restore released rooms if a release is revoked
* Support smooth booking operations by providing clear visibility of inventory.

Release handling here is especially important because release changes often happen late and need immediate correction without changing the original contract.

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### Screen structure

The screen is divided into three main areas:

1. Search and control area (top)
2. Allotment table (center)
3. Release columns (grouped inside the table)

### 1. Search and control area

Period - Defines the date range shown in the table. Only days within this range are displayed.

Room Type - Filters the view to a specific room type. Leave empty to see all room types.

Week Days - Optional filter to show only selected weekdays.

Search - Loads the allotment data based on the selected filters.

Search with Stay Length - Searches based on stay length logic. This search does **not** include transports.

Search with Allotment Control - Searches using full allotment control logic and **includes transports**.

Display Names - Toggles between internal codes and readable names.

Save - Saves all changes made in the table.

Cancel - Discards unsaved changes.

Allotment History - Opens the change log for this hotel and period.

### 2. Allotment table – common columns

Room Type - The room category this row belongs to.

Date - The specific arrival date.

Day - Day of the week for the date.

NO. - Total number of rooms defined for this room type and date.

Secured - Rooms that are secured and not automatically released.

Guaranteed - Rooms guaranteed to the hotel, regardless of sales.

Book - Number of rooms already booked.

Free - Available rooms that can still be sold.

### 3. RELEASE section

The **RELEASE** headline groups all release-related columns. These columns always have a grey background to separate them from availability data.

Release handling here applies to **daily releases only**.

DAYS - The number of days before arrival when the release is executed.

* Initial value comes from the Release rule in the contract
* Editable if a release rule exists
* Empty and not editable if no release rule is defined
* Can be changed to extend or shorten the release deadline

R - Indicates whether the release has been executed.

* Checked: the release is executed
* Unchecked: the release is not executed or has been undone
* Removing the checkmark **undoes the release** and makes AR and SR editable

AR (Allotment Released) - Number of **allotment rooms** that were released.

* Filled automatically when a release is executed
* Editable only when undoing a release
* Used to control how many allotment rooms are restored

SR (Secured Released) - Number of **secured rooms** that were released.

* Filled automatically when a release is executed
* Editable only when undoing a release
* Used to control how many secured rooms are restored

Pax columns (PAX1, PAX2, PAX3, PAX4) - The maximum number of rooms with a max of 1 - 4 pax

* Used for pax-based control and limits per room.

MIN - The minimum stay

### How to work with releases

#### Execute a release

1. Ensure DAYS has the correct value
2. Wait until the system executes the release automatically (supported for Daily" releases only). Please see [hotel-release-reporting.md](../releases/hotel-release-reporting.md "mention")
3. The R checkbox becomes checked
4. AR and SR are filled with released numbers

### Release logic

* When a release is executed, the system stores how many **allotment** and **secured** rooms were released
* When a release is revoked:
  * Rooms are restored by default
  * AR and SR become editable to allow partial restoration
* Allotment per Day values override the release defined in the contract

#### Undo a release

1. Uncheck the R checkbox
2. Edit DAYS if a new release deadline is needed
3. Adjust AR and SR to define how many rooms are restored
4. Save changes

By default, undoing a release restores all released rooms unless adjusted.

***

### Bulk updates (Change Value tool)

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

The Change Value tool can be used to:

* Edit DAYS for multiple rows
* Uncheck R for multiple rows
* Adjust AR and SR for multiple rows

This is useful when correcting releases across many dates or room types.

***

### Activity log

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

All changes made to release data in Allotment per Day are logged.

* Activity name: **Release update**
* Includes changes to DAYS, R, AR and SR
* Used for auditing and troubleshooting

***

### Permissions

Release columns are visible and editable only if the user or supplier has:

* Access to Allotment per Day
* Access to Release management

Without both rights, release data is hidden or read-only.
