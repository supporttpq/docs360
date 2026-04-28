# Releases/Stop Sales Log

### Overview

The **Stop Sales Log** provides a complete audit trail of all changes made to allotments where availability has been reduced or stopped.

It tracks when and how room availability was modified, including manual actions and automated processes such as Stop Sale services.

This page is primarily used for troubleshooting, auditing, and operational monitoring.

### Purpose

* Track all stop sale and release actions
* Identify who made changes and when
* Verify system or supplier driven updates
* Support investigation of availability issues
* Ensure transparency in allotment management

### Navigation

Hotel → Releases / Stop Sales Log

<figure><img src=".gitbook/assets/image (738).png" alt=""><figcaption></figcaption></figure>

***

### Filters and Search Options

The filter section allows narrowing down the log entries.

|                                |                                                                                                                                                                                           |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <h4>Supplier</h4>              | <p>Dropdown used to filter log entries by <strong>supplier</strong>.</p><p>This corresponds to the supplier linked to the hotel contract.</p>                                             |
| <h4>Allotment From / To</h4>   | <p>Defines the date range of the allotment being analyzed.<br>Only changes affecting this period will be shown.</p>                                                                       |
| <h4>Change Date From / To</h4> | <p>Filters based on when the change was made.<br>Useful for tracking recent updates or historical actions.</p>                                                                            |
| <h4>Hotels</h4>                | <p>Field used to select one or more <strong>hotels</strong>.</p><ul><li>Clicking <strong>Edit</strong> opens a selection dialog</li><li>Filters log entries for specific hotels</li></ul> |
| <h4>Room</h4>                  | Filter by specific room type.                                                                                                                                                             |
| <h4>Show Hidden</h4>           | <p>Checkbox that includes <strong>hidden or system-level entries</strong> in the results.</p><p>When enabled, additional technical records may be displayed.</p>                          |
| <h4>Display</h4>               | Button used to apply the selected filters and refresh the log results.                                                                                                                    |
| **More Filters**               | Expands the filter section to include additional criteria.                                                                                                                                |
| **Clear**                      | Resets all filters to default values.                                                                                                                                                     |
| **Display names**              | Checkbox that toggles between **codes and readable names** for hotels and rooms.                                                                                                          |

### Table Fields Explanation

Each row represents a **single allotment change event**.

**Change Date/Time -** Date when the modification was made. Represents when the stop sale or release action occurred.

**Supplier** - Supplier associated with the allotment.

**User** - Name of the user that performed the action.

**All Date** - The specific date of the allotment affected.

**Hotel** - Hotel where the change was applied.

**Room** - Room type affected by the change.

**Initial R.No** - Initial number of available rooms before the change.

**Final R.No** - Final number of available rooms after the change.

&#x20;        Example: 100 → 0 indicates a full stop sale.

**Source** - Indicates how the change was triggered.

### Expected Behavior

* All stop sale and release actions are logged
* Data reflects both manual and automated updates
* Logs are immutable (read-only)
* Filters dynamically control visible data
* Pagination is applied for large datasets

***

## Behavior and Interpretation

### Stop Sale

When:

* **INITIAL R.NO > 0**
* **FINAL R.NO = 0**

This indicates that availability was **closed (stop sale)**.

***

### Release

When:

* **FINAL R.NO > INITIAL R.NO**

This indicates that rooms were **released back into availability**.

***

### No Availability Change

If values are equal, the log may represent:

* A system check
* A non-impacting update

***

## Practical Use Cases

Investigating Overbooking - Check whether allotment was reduced after bookings were made.

Investigating Closed Availability - Identify when and why rooms became unavailable.

Supplier or System Issues - Determine whether changes came from:

* Internal users
* Automated services
* External integrations

***

## Key Notes

* The log is **read-only** and cannot be modified.
* It reflects **historical actions**, not current availability.
* Always correlate **ALL DATE** (stay date) with **CHANGE DATE/TIME** when analyzing issues.
* The **SOURCE** field is critical for debugging system behavior.
