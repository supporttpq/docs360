# Create / Edit rule

### Overview

The system allows administrators to define rules that control availability and restrictions based on transport, destination, resort, hotel, or room type. Rules are time-bound and can be enabled or disabled as needed.

This functionality ensures precise control over booking conditions, making it possible to handle seasonal restrictions, transport limitations, or hotel-specific rules.

### Key rules

* **Start Date** and **End Date** are mandatory.
* **End Date** must be later than **Start Date**.
* **Note** is mandatory.
* You must select at least one scope field: **Transport**, **Destination**, **Resort**, or **Hotel**.
* After you save a rule, you typically only change **Enabled**. For other changes, create a new rule and disable the old one.

### Create a rule

1. Open **Hotel → Close Out**.
2. Click **Edit** (new line) to create a new rule.
3. Fill in the fields (see below).
4. Keep **Enabled** checked if the rule should apply immediately.
5. Click **Save**.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

After saving, the rule is shown at the top of the list.

### Fields and dependencies

#### Fields

* **Start Date**: First date the rule applies.
* **End Date**: Last date the rule applies.
* **Transport Type**: Filters the available transports.
* **Transports**: One or more transports.
* **Destination**: One or more destinations.
* **Resort**: One or more resorts.
* **Hotel**: One or more hotels.
* **Room Type**: One or more room types.
* **Note**: Internal description of why the rule exists.
* **Enabled**: Turns the rule on/off (default: enabled).

#### Field filtering (dependency chain)

* **Transport** is filtered by **Transport Type**.
* **Destination** is filtered by **Transport(s)**.
* **Resort** is filtered by **Destination(s)** and **Transport(s)**.
* **Hotel** is filtered by **Resort(s)**.
* **Room Type** is filtered by **Hotel(s)**.

{% hint style="warning" %}
You must select at least one of: **Transport**, **Destination**, **Resort**, **Hotel**.\
Room types cannot stand alone without a hotel.
{% endhint %}

### Validation

You can’t save if:

* Start Date or End Date is empty.
* End Date is not after Start Date.
* Note is empty.
* None of Transport/Destination/Resort/Hotel is selected.

### Edit an existing rule

* Toggle **Enabled**, then click **Save**.
* To change dates or scope, create a new rule and disable the old one.

### Examples

* **Seasonal restriction:** Close a hotel from `01-11-2025` to `01-03-2026`.
* **Transport restriction:** Block hotels only for a specific flight/transport.
* **Room block:** Block a specific room type for peak dates (via Hotel + Room Type).

### Notes / best practices

* Write a clear **Note**. You’ll rely on it later.
* Start with a narrow scope. Expand only when needed.
* Review enabled rules regularly. Disable rules that are no longer relevant.
* Allow up to \~2 minutes for changes to reach price lists.

### FAQ

#### Does Close Out cancel existing bookings?

No. Close Out blocks **new** bookings by cutting FHA to `0`. Existing bookings stay unchanged.

#### Why can’t I save a rule without selecting Transport/Destination/Resort/Hotel?

Because the rule needs a scope. Otherwise it would match “everything” and could block sales globally.

#### Can I create a rule only for a room type?

Not by itself. Room types are tied to a hotel. Select **Hotel** first, then **Room Type**.

#### Can I edit dates or scope after saving?

Usually no. After saving, only **Enabled** is meant to change. Create a new rule for date/scope changes.

#### I enabled a rule, but bookings are still possible. Why?

Common causes:

* The price list update has not finished yet (wait \~2 minutes).
* The rule does not match the booking (transport/destination/resort/hotel/room type).
* Availability is coming from another setup outside FHA (depends on configuration).

### Related tasks

* [Close Out](./)
* [Enable / Disable rule](enable-disable-rule.md)
