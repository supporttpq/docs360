# Extra Cost – Hotel Contract Configuration

### Overview

The **Extra Cost** section in the “Edit Hotel Contract” module allows the configuration of additional charges that are not directly included in the base room price—such as cleaning fees, resort fees, or optional services. These costs can be applied per person or per room, and they may vary by age and period.

***

### Purpose

Use this tab to keep pricing complete and consistent.

It helps the system calculate totals correctly.

It also improves invoice and customer-facing transparency.

***

### Preconditions

Before you configure **Extra Cost**:

* The **hotel contract** exists.
* At least one **Period** exists.
* Room types exist in **Rooms**.
* You know the age bands you want to price.

***

### Fields

| Field                    | Description                                                                                                           |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------- |
| **Type**                 | The extra cost type. Example: Final Cleaning or Resort Fee. Selected from a dropdown of predefined types.             |
| **Room**                 | Specifies the room types to which this cost applies. Selecting “All rooms” applies it globally across all room types. |
| **From / To (Age)**      | The age range (in years) for which the extra cost is applicable.                                                      |
| **Period ID**            | Represents a predefined contract period. Each period has its own pricing rules.                                       |
| **Extra Cost/Pax/Night** | Cost applied **per person per night** within the selected age range and period.                                       |
| **Extra Cost/Room**      | Cost applied **per room**, regardless of occupancy. Use it for fixed fees like final cleaning.                        |

***

### How it works

{% stepper %}
{% step %}
### Choose what the cost represents

Select a **Type** that matches the fee.

Use a dedicated type when you need separate reporting.
{% endstep %}

{% step %}
### Scope it to rooms

Pick a specific **Room**.

Use **All rooms** only when the fee is always the same.
{% endstep %}

{% step %}
### Limit it by age (optional)

Set **From / To (Age)** when the fee depends on guest age.

Leave the range broad when it applies to everyone.
{% endstep %}

{% step %}
### Set the amount per period

Use the **Period ID** rows to set the fee by season.

Fill either **Extra Cost/Pax/Night** or **Extra Cost/Room**.
{% endstep %}
{% endstepper %}

***

### Tips

{% hint style="info" %}
Keep age ranges unique per **Type + Room**. Overlaps can create conflicts.
{% endhint %}

* Use **Extra Cost/Pax/Night** for per-person, per-night fees (for example city tax).
* Use **Extra Cost/Room** for fixed charges (for example final cleaning).
* If the cost changes by season, set different values per **Period ID**.

***

### Related workflows

* [Hotel contract - General](hotel-contract-general.md)
* [Rooms – Hotel Contract Configuration](rooms-hotel-contract-configuration.md)
* [Periods – Hotel Contract Configuration](periods-hotel-contract-configuration.md)
* [Extra Beds Cost – Hotel Contract Configuration](extra-beds-cost-hotel-contract-configuration.md)

***

### FAQ

**What’s the difference between “Extra Cost/Pax/Night” and “Extra Cost/Room”?**\
**Pax/Night** scales with number of guests and nights.\
**Room** stays fixed per room, regardless of occupancy.

**Can I use both fields in the same row?**\
Avoid it unless you explicitly need both charges.\
If you do, double-check the total in a test booking.

**Why do I see multiple rows under “Period ID”?**\
Each row maps to one contract period.\
It lets you change the fee by season.

**Should I set an age range if the cost applies to everyone?**\
No. Use a broad range (or the default) only when needed.\
Keep the setup simple unless the supplier demands it.

**What happens if age ranges overlap?**\
Rules can conflict.\
Results may depend on rule order or internal selection logic.

**Why isn’t my extra cost applied in pricing?**\
Check the **Room** scope first.\
Then check **Period ID** and age range.\
Finally, confirm that the amount field is filled.
