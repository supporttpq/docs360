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
* Support both hotel-wide and room-type rules.
* Keep a log for auditing.

### How “days in advance” is evaluated

Treat **days in advance** as the lead time.

* A value of `0` means “release on the same day.”
* A value of `5` means “release 5 days before the target date.”

### When a release runs

Releases are executed by the daily release automation.

The automation runs **once per day** per company.

Each rule can therefore trigger **at most once per day**.

#### Single-day rule (specific target date)

Use this when you want a release tied to **one target date**.

The rule triggers on:

`target date - days in advance`

Example: target date `20-05-2026` with `5` days in advance triggers on `15-05-2026`.

#### Period rule (runs once per day in a period)

Use this when you want releases evaluated **daily** within a **start/end** period.

On each daily run, Tourpaq releases the target date that matches the rule’s lead time.

Example: a rule with `3` days in advance evaluated on `15-05-2026` targets `18-05-2026`.

### Examples

#### Scenario setup

* Today: **15-05-2026**
* Hotel “Grand Palace” has room types `1S`, `2C`, `3F`
* Inventory period: **01-04-2026** to **01-09-2026**

#### Hotel-wide release rule (all room types)

* Rule: Release date `20-05-2026`, days in advance `5`, email `admin@grandpalacehotel.com`
* Result: On **15-05-2026**, all rooms (`1S`, `2C`, `3F`) are released.
* A log entry is created.
* A report email is sent.

{% hint style="info" %}
If **days in advance** is blank, the system defaults to **0**.
{% endhint %}

#### Room-type release rule (within a period)

* Rule: Start `01-05-2026`, end `01-06-2026`, room `2C`, days in advance `3`, email `admin@grandpalacehotel.com`
* Result: On **15-05-2026**, room type `2C` is released for **18-05-2026**.
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

### Editing releases in Allotment per Day

You can adjust release results per room type and date in **Hotel → Allotment per Day**.

This feature allows releases to be edited directly in **Allotment per Day**, at room and date level, using the same workflow as allotment corrections.

It is designed to handle frequent operational changes such as extending, shortening, executing, or revoking releases after they have already been applied.

See [Allotments per day](../allotments-per-day/).

### Release logic

* When a release is executed, the system stores how many **allotment** and **secured** rooms were released
* When a release is revoked:
  * Rooms are restored by default
  * Allotment room released (AR) and Secured room released (SR) become editable to allow partial restoration
* Allotment per Day values override the release defined in the contract
* Releases can be adjusted quickly at room and day level

### How does the release work (value calculations)

This section documents the system behavior during the "Release" execution, comparing the pre-release state and the post-release state.

<figure><img src="../../../.gitbook/assets/image (598).png" alt=""><figcaption><p>Before Release</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (599).png" alt=""><figcaption><p>After Release</p></figcaption></figure>

<table><thead><tr><th width="148.7777099609375">Field</th><th width="149.77783203125">Before Release</th><th width="140.3333740234375">After Release</th><th>Formula after release</th></tr></thead><tbody><tr><td>NO</td><td>100</td><td>10</td><td>= Max(Book vs Guarantee)</td></tr><tr><td>SECURED</td><td>20</td><td>10</td><td></td></tr><tr><td>GUARANTEED</td><td>0</td><td>0</td><td></td></tr><tr><td>BOOK</td><td>10</td><td>10</td><td></td></tr><tr><td>AR</td><td>0</td><td>90</td><td>= NO Before release - NO After release</td></tr><tr><td>SR</td><td>0</td><td>10 </td><td>= Min(Secured vs NO After release)</td></tr></tbody></table>

### FAQ

#### Who can create or change release rules?

Company administrators.

#### Can I reuse the same rule for multiple hotels?

No. Each rule belongs to one hotel.

#### What’s the difference between a hotel-wide rule and a room-type rule?

* **Hotel-wide** releases all room types for a hotel.
* **Room-type** releases one room type (typically within a period).

#### Can a release run multiple times per day?

No.

The release automation runs **once per day** per company.

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
