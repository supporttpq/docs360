---
description: >-
  Automate hotel room releases and supplier notifications based on release
  rules, booking status, and travel timing in Tourpaq.
---

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
