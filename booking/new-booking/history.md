# History

### Overview

The **History** tab provides a detailed log of all changes made to a specific booking. Every modification—manual or automatic—is recorded with the responsible user, date, time, and the values **before** and **after** the change. This ensures complete transparency and traceability across all booking activities.

<figure><img src="../../.gitbook/assets/image (551).png" alt=""><figcaption></figcaption></figure>

***

### Purpose

The History view helps you:

* See **who** made a change and **when**.
* Understand **what** was modified (old and new values).
* Identify **which system component** (engine) triggered the update – for example, a manual user action or an API integration.
* Resolve customer support questions related to **price changes**, **cancellations**, **name corrections**, or other edits.

It is a key tool for **troubleshooting**, **auditing** and reviewing how a booking has evolved over time.

***

### Preconditions

* You must have access to a booking that has been created and, ideally, modified.
* Your user role must include permission to **view booking history**.
* Changes must have been made in the system (by users or by integrations) for entries to appear in the History list.

***

### Using the History tab

#### Access the History tab

1. Open the relevant **booking** from the booking overview or via search.
2. Click the **History** tab in the booking details.
3. Use the expand/collapse controls or search field (if available) to focus on the entries you need.

***

#### Columns in History

Each history entry contains the following columns:

| Field         | Description                                                                                                                           |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **Date**      | The date when the change was saved.                                                                                                   |
| **Time**      | The exact time the modification occurred.                                                                                             |
| **User**      | The name of the user or system that performed the change (for example, `rowebtpq`, `APICore`).                                        |
| **Version**   | Indicates the booking version affected by the change. Useful for tracking major updates.                                              |
| **Change**    | Short description of what was modified (for example, _Status change_, _Passenger name change_, _Room number update_, _Total change_). |
| **Old value** | The value before the modification.                                                                                                    |
| **New value** | The value after the modification.                                                                                                     |
| **Passenger** | Shows which passenger the change relates to, when applicable. Empty if the change is at booking level.                                |
| **Engine**    | Identifies the source system of the change (for example, `APICore`, web booking, office user).                                        |

***

#### Functions and filters

* **Expand / Collapse all**\
  Expands or collapses all history entries, making it easier to scan long histories.
* **Search by text**\
  Allows you to search for specific keywords, passengers, or change types (for example, search for “Total change” to find price modifications).
* **Terms History (sub‑tab)**\
  A dedicated sub‑tab that shows changes related to the **booking’s terms and conditions**, such as payment terms or cancellation rules linked to the booking.

***

#### Example use case: finding a price change

**Scenario**\
A booking shows an unexpected final price, and you need to verify when the change happened and who made it.

1. Open the **History** tab on the booking.
2. Use the text search to look for **“Total change”** or other relevant keywords.
3. Review the **Old value** and **New value** columns to see how the price changed.
4. Check the **User** and **Engine** columns to identify whether the change was made manually by an agent or automatically by the system or an integration.

***

### FAQ

#### 1. Why do I not see any entries in the History tab?

If the History tab is empty:

* The booking may be newly created with no changes yet.
* Your user role may not have permission to **view history**.

Try making a small test change on the booking, save it, and then refresh the History tab. If entries still do not appear, contact your system administrator.

#### 2. Can I edit or delete history entries?

No. History entries are **read‑only** by design and cannot be edited or deleted. This ensures a reliable audit trail. If a mistake was made, correct it by updating the booking; a **new** history line will record the correction.

#### 3. What does the “Engine” column mean?

The **Engine** column shows which system component created the change, for example:

* A logged‑in **user** (office agent).
* The **web booking** engine (customer online changes, if allowed).
* An **API** or integration such as `APICore`.

This helps you distinguish between manual edits and automatic or external updates.

#### 4. How is the “Version” field used?

The **Version** value groups changes by booking version. When significant changes occur (for example, moving the booking, changing core components), the version may be incremented. This allows you to:

* See which changes belong to the same update.
* Compare earlier and later versions when investigating complex edits.
