# Hotel release - automation

#### Overview

The **Hotel Release Automation** service in Tourpaq Office is designed to automatically manage hotel room releases based on rules configured by company administrators. The service runs **daily** for each company in the system and ensures that available hotel rooms are properly flagged and communicated to suppliers.

#### Purpose

The main goals of the Hotel Release Automation are to:

* Automatically determine and release hotel rooms that are available for booking according to predefined **release rules**.
* Update the status of hotel allotments to **“suitable for release”** so suppliers can manage them in the Tourpaq system.
* Notify suppliers via email when rooms have been released, including a list of affected rooms.
* Maintain an internal log of all release activities for administrative review and tracking.

#### Actions Performed by the Service

1. **Identify Applicable Release Rules**
   * For each hotel of a given company, the system determines which release rules apply based on the current date.
   * Retrieves hotel allotments that fall under these rules.
2. **Compute and Release Rooms**
   *   For each eligible hotel allotment, the service calculates the number of rooms to release:

       ```
       Number of rooms to release = Allocated rooms – Booked rooms
       ```
   * Updates the room allotment status to **“suitable for release”**.
   * Records the details of all released rooms for logging purposes.
3. **Notify Suppliers**
   * Sends an email to each hotel supplier who had at least one room released.
   * The email includes a list of all rooms released during that service run.
   * The supplier email used is taken from the release rule that triggered the room release.
4. **Maintain Logs**
   * Creates a log file recording all rooms released during the service run, including dates and hotel allotments.
   * Provides a historical record for administrative review.

#### Notes

* The automation runs daily for each company in the system.
* Detailed examples and scenarios can be found in the **Hotel Release Rules** section of the hotel specification.
* The service ensures that released rooms are visible and manageable by hotel suppliers, enabling dynamic inventory control and efficient allotment management.
