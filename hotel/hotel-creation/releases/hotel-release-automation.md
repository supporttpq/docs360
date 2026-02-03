# Hotel release - automation

### Overview

Hotel Release Automation releases unused room allotments based on configured release rules.

The service runs **daily** per company.

It flags allotments as **Suitable for release** and emails a release report to suppliers.

#### Related pages

* [Releases](./)
* [Hotel release - Reporting](hotel-release-reporting.md)

### Purpose

The main goals are:

* Automatically identify unused allotments and release them based on **release rules**.
* Update the status of hotel allotments to **Suitable for release**.
* Email suppliers a release report with the affected dates and room types.
* Keep an internal log for auditing and troubleshooting.

### Actions performed by the service

1. **Identify applicable release rules**
   * For each hotel, the system checks which rules apply today.
   * It then retrieves the hotel allotments covered by those rules.
2. **Compute and release rooms**
   *   For each eligible allotment, the service calculates how many rooms can be released:

       ```
       Number of rooms to release = Allocated rooms – Booked rooms
       ```
   * It updates the allotment status to **Suitable for release**.
   * It stores the release details for logging.
3. **Notify suppliers**
   * It emails each supplier with at least one released room.
   * The email includes all rooms released in that run.
   * The recipient is the email address from the rule that triggered the release.
4. **Maintain logs**
   * It writes a log entry for each release action, including dates and allotments.
   * This creates a historical record for admins.

### Notes

* The automation runs daily.
* Release rules are configured in the hotel **Releases** tab.
* Released rooms remain visible for suppliers, who decide how to handle them.

### FAQ

#### What does the automation actually change?

It updates hotel allotments to **Suitable for release** and writes release logs. It does not delete bookings.

#### When does the service run?

It runs **daily** for each company.

#### What decides if a room is released today?

The service evaluates the configured release rules against today’s date. It also uses the rule’s **days in advance** lead time.

#### How many rooms are released?

Only the unused part of the allotment:

```
Allocated rooms – Booked rooms
```

#### Can it release a room that is already booked?

No. Booked rooms are not released.

#### Which email address receives the release report?

The email address saved on the release rule that triggered the release.

#### Do suppliers have to “accept” the release?

Suppliers can decide how to handle released rooms in their supplier login. Typical actions include reusing the inventory on other channels.

#### Where can I see what happened?

Use the **Releases Log** in Tourpaq Office. You can filter by supplier, hotel, room type, and period.

#### I changed a release rule today. Will it affect today’s run?

It depends on timing. If the daily run already completed, changes apply on the next run.
