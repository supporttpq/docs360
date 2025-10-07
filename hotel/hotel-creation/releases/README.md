# Releases

#### Overview

The **Hotel Release Rules** feature in Tourpaq Office enables administrators to automate the release of hotel rooms back to the supplier when they are no longer needed. The release process depends entirely on rules configured at the **company administrator level**.

Each rule applies only to a **single hotel**. Rules cannot be shared across multiple hotels. They can be set to trigger on a specific date or relative to a given number of days before that date.

#### Purpose

Hotel Release Rules serve the following objectives:

* Automate the release of unused hotel room allotments.
* Notify hotel suppliers of released rooms through email reports.
* Allow flexible configuration at both **general hotel level** and **room-specific level**.
* Provide administrators and suppliers with reporting and log access for full transparency.

***

#### Types of Release Rules

Two types of rules can be created in the **Hotel Releases** tab. Each type is listed under its own subtab:

**1. General Release Rule**

* Applies to **all room types** of a hotel.
* Triggers on a specific date or a set number of days before that date.
* Automatically generates a release report and sends it via email to the supplier.

**Required Fields:**

* **Release Date** – the fixed date when the release occurs.
* **Number of Days in Advance** – defines how many days before the release date the action should occur.
* **Email Address** – the supplier’s email address to receive the release report.

**2. Specific Release Rule**

* Applies to **a single room type** of a hotel.
* Functions within a defined period (start date and end date).
* Can release the specified room type repeatedly during the rule’s active period.

**Required Fields:**

* **Start Date** – date from which the rule becomes active.
* **End Date** – date until which the rule remains active.
* **Room Type** – the specific room category (e.g., 1S, 2C, 3F).
* **Number of Days in Advance** – days prior to the booking date when the release will occur.
* **Email Address** – supplier’s email address to receive the release report.

***

#### Examples

**Scenario Setup:**

* Today’s date: **15-05-2009**.
* Hotel “Grand Palace” has three room types (1S, 2C, 3F) available from **01-04-2009 to 01-09-2009**.

**General Release Rule**

* Rule: Release Date = 20-05-2009, Days in Advance = 5, Email = admin@grandpalacehotel.com.
* Result: On 15-05-2009, all hotel rooms (1S, 2C, 3F) are released. A log file is created, and an email report is sent to the supplier.

Notes:

* If no start date is provided, the rule executes daily, releasing rooms for dates X days ahead.
* If no number of days is provided, the system defaults to **0 days** in advance.

**Specific Release Rule**

* Rule: Start Date = 01-05-2009, End Date = 01-06-2009, Room Type = 2C, Days in Advance = 3, Email = admin@grandpalacehotel.com.
* Result: On 15-05-2009, the 2C room type is released for 18-05-2009. A log file is created, and a supplier email is sent.

Notes:

* On **27-05-2009**, the general release rule does not apply because the 5-day offset does not match 20-05-2009.
* On **30-05-2009**, the specific rule does not apply because the release date (3 days later) falls outside the defined period.

***

#### Supplier Administration

Hotel suppliers can log into their dedicated **Tourpaq Office supplier account** to manage rooms available for release. This allows them to decide whether released rooms should be:

* Removed from the Tourpaq Booking System, or
* Reused for other distribution channels.

The supplier interface provides filters for:

* Hotel
* Room Type
* Time Period

***

#### Release Logs

Company administrators can review all release actions in the **Releases Log** submenu (under Hotel → Tourpaq). Logs may be filtered by:

* Supplier
* Brand
* Hotel
* Room Type
* Period

***

#### Rule Editing Behavior

If a release rule is modified while still in effect, the changes only take effect **after the previous configuration finishes its cycle**.

**Example:**

* Original rule: 10 days in advance.
* Updated rule: 4 days in advance.
* Result: The 10-day rule continues until its effect expires, after which the 4-day rule becomes active.
