# Releases

### Overview

Hotel release rules automate when rooms are released back to the supplier.

Rules are configured by **company administrators**.

Each rule belongs to **one hotel**.

Rules cannot be reused across hotels.

{% hint style="info" %}
Dates in the examples use the format **DD-MM-YYYY**.
{% endhint %}

#### Related pages

* [Hotel release - automation](hotel-release-automation.md)
* [Hotel release - Reporting](hotel-release-reporting.md)

### Purpose

* Release unused room allotments on time.
* Email suppliers a release report.
* Support both hotel-wide and room-specific rules.
* Keep a log for auditing.

### How “days in advance” is evaluated

Treat **days in advance** as the lead time.

* A value of `0` means “release on the same day.”
* A value of `5` means “release 5 days before the target date.”

### Examples

#### Scenario setup

* Today: **15-05-2009**
* Hotel “Grand Palace” has room types `1S`, `2C`, `3F`
* Inventory period: **01-04-2009** to **01-09-2009**

#### General release rule

* Rule: Release date `20-05-2009`, days in advance `5`, email `admin@grandpalacehotel.com`
* Result: On **15-05-2009**, all rooms (`1S`, `2C`, `3F`) are released.
* A log entry is created.
* A report email is sent.

{% hint style="info" %}
If **days in advance** is blank, the system defaults to **0**.
{% endhint %}

#### Specific release rule

* Rule: Start `01-05-2009`, end `01-06-2009`, room `2C`, days in advance `3`, email `admin@grandpalacehotel.com`
* Result: On **15-05-2009**, room type `2C` is released for **18-05-2009**.
* A log entry is created.
* A report email is sent.

### Supplier administration

Suppliers can review and manage released rooms in their Tourpaq supplier login.

They can decide if released rooms should be:

* removed from Tourpaq bookings, or
* reused for other channels.

Common filters:

* hotel
* room type
* time period

### Release logs

Administrators can review release actions in **Releases Log** (Hotel → Tourpaq).

Filters include:

* supplier
* brand
* hotel
* room type
* period

### Rule editing behavior

Edits to an active rule take effect **after the current cycle completes**.

Example:

* Old rule: `10` days in advance
* New rule: `4` days in advance
* Result: `10` continues until it expires, then `4` starts.

### FAQ

#### Who can create or change release rules?

Company administrators.

#### Can I reuse the same rule for multiple hotels?

No. Each rule belongs to one hotel.

#### What’s the difference between a general and a specific rule?

* **General** releases all room types for a hotel.
* **Specific** releases one room type within a period.

#### What does “days in advance” mean?

It’s the lead time.

`3` means the release runs 3 days before the target date.

#### Who receives the release email?

The email address saved on the rule that triggered the release.

#### Where can I see what was released?

Use **Releases Log** (Hotel → Tourpaq).

Filter by hotel and period for quick checks.

#### Do suppliers have to accept the release?

Suppliers can decide how to handle released rooms in their supplier login.
