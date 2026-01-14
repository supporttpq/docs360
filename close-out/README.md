# Close Out

### Overview

**Close Out** restricts availability for selected transports, destinations, resorts, hotels, and room types within a date range.

When a Close Out rule is enabled, the system sets **Free Hotel Allotment (FHA)** to `0` for the matching hotels/rooms. This blocks new bookings for those combinations.

### Purpose

This feature is used by **travel coordinators, back-office staff, and product managers** to:

* Define and review **Close Out rules** that affect sales and availability.
* Filter and identify rules by date range, transport, destination, hotel, or room type.
* Confirm when and by whom rules were created.
* Enable/disable rules, or adjust them when needed.

### Preconditions

* The user must have access rights to the **Hotel → Close Out** menu.
* Create rules carefully. They can block sales across many products.
* The relevant transport/hotel/room types must exist in the system.

### Step-by-step

#### Step 1: Open Close Out

* Navigate to the **Hotel menu**.
* Select **Close Out** (below **Stop Sales**).

#### Step 2: Understand what you see

The list shows existing rules.

Each rule has an **Edit** action.

Rules are created on **company level** (not per brand).

#### Step 3: Filter the list

<figure><img src="../.gitbook/assets/image (11) (1) (3).png" alt=""><figcaption></figcaption></figure>

Fill in filters, then click **Display**.

Common filters:

* **Start date** (default today)
* **End date** (default one year ahead)
* **Transport type** (multi-select)
* **Transports** (multi-select)
  * Options include _Select all_, _Show hidden_, and _Show code_.
* **Destination** (multi-select)
* **Resort** (multi-select)
* **Hotel** (multi-select)
* **Room type** (multi-select)

#### Step 4: Results table columns

| **Field/Option**          | **Description**                                                            |
| ------------------------- | -------------------------------------------------------------------------- |
| **Start Date / End Date** | Date interval for rule validity (departure date range).                    |
| **Transport Type**        | Filters rules by type of transport (e.g., charter, dynamic).               |
| **Transports**            | Specific transports where the rule applies.                                |
| **Destination**           | Destination filter.                                                        |
| **Resorts**               | Resort filter.                                                             |
| **Hotels**                | Hotel filter.                                                              |
| **Room Type**             | Room type filter.                                                          |
| **Note**                  | Additional description set on the rule (truncated, full text on hover).    |
| **Enabled**               | Shows whether the rule is active.                                          |
| **Created / Created By**  | Date, time, and user who created the rule. Username links to user details. |
| **Display Button**        | Executes the filter search.                                                |
| **Clear Button**          | Removes all applied filters and reloads full list.                         |
| **Pagination**            | Navigates results (25 rules per page by default).                          |

#### Step 5: Sort and paginate (optional)

* Navigate through multiple pages using **pagination**.
* Sort results by **Start Date** or **End Date** (ascending/descending).

#### Step 6: Clear filters

* Click **Clear** to reset all filter inputs.

### Notes

* Filtering by **brand** is not available. Close Outs are created on company level.
* Changes can take up to \~2 minutes to reach price lists.

### Related tasks

* [Create / Edit rule](create-edit-rule.md)
* [Enable / Disable rule](enable-disable-rule.md)

### FAQ

#### Does Close Out cancel existing bookings?

No. Close Out blocks **new** bookings by cutting FHA to `0`. Existing bookings stay unchanged.

#### How long does it take for a rule to apply?

Usually \~2 minutes. It depends on background processing and price list updates.

#### What’s the difference between Close Out and Stop Sales?

Close Out blocks sales by setting **FHA to `0`** for the matched scope.

Stop Sales reduces day-by-day availability in the hotel allotment flow. It can also be brand-specific.

#### Why can’t I filter or create Close Out rules per brand?

Close Out rules are stored and applied at **company level** only.

#### I enabled a rule, but bookings are still possible. Why?

Common causes:

* The price list update has not finished yet (wait \~2 minutes).
* The rule scope does not match the booking (transport/resort/hotel/room type).
* Availability is coming from another setup outside FHA (depends on configuration).

#### Can I create a rule only for a room type?

Not by itself. Room types are tied to a hotel, so the rule must include at least one of:

* Transport, destination, resort, or hotel

Start with a narrow scope first. Expand only if needed.
