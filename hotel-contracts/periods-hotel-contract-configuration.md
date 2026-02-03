# Periods – Hotel Contract Configuration

### Overview

Use the **Periods** tab to define seasonal contract periods.

Each period contains rows for room/board combinations.

Rows control allotment, release, minimum stay, and cost.

***

### Screenshot

<figure><img src="../.gitbook/assets/image (441).png" alt=""><figcaption></figcaption></figure>

***

### Preconditions

* Room types must be defined in the **Rooms** tab.
* Board types (AI, BB, etc.) should be configured in advance.
* Have the supplier’s release rules, guarantees, and minimum-stay terms ready.

***

### Fields

| Field                          | Description                                                                                  |
| ------------------------------ | -------------------------------------------------------------------------------------------- |
| **Start Date / End Date**      | Defines the date range for a contract period. Add multiple periods for seasonal pricing.     |
| **R (Release days)**           | Realease day                                                                                 |
| **CD (Cut-down allotment)**    | Enables cut-down behavior for allotments in this period (if used by your setup).             |
| ➕ **Add Interval**             | Adds a new interval for the selected period.                                                 |
| 🗑️ **Trash Icon (on period)** | Deletes the entire period.                                                                   |
| 🗑️ **Trash Icon (on row)**    | Deletes a specific interval.                                                                 |
| **Room Code**                  | Room reference from the **Rooms** tab. Each row applies to one room code.                    |
| **Board**                      | Board basis for this row (for example BB, HB, AI).                                           |
| **Allotments**                 | Number of rooms available for sale in this period.                                           |
| **Guarantee**                  | Number of guaranteed rooms you commit to sell (if applicable).                               |
| **Secured**                    | Number of secured rooms (if applicable).                                                     |
| **Min Stay**                   | Minimum number of nights required for bookings in this period.                               |
| **Cost**                       | Supplier cost for the room and board in this period.                                         |
| **Single Cost**                | Single-occupancy supplement on top of **Cost**.                                              |
| **SP%**                        | Marks **Single Cost** as a percentage on top of **Cost** (instead of an amount).             |
| **Stay Type**                  | How cost is applied. Typical values are **Per Pax**, **Per Room**, or **Per Pax Per Night**. |
| **Tr. Length**                 | Transport-length reference used by some setups (for example `5d` = 5 days).                  |

### Buttons and actions

* **Add new period**: Creates a new date range (period).
* **Add interval**: Adds a new row for room/board within the selected period.
* 🗑️ **Delete (period)**: Deletes the entire period and all rows.
* 🗑️ **Delete (row)**: Deletes a single row in the period grid.

***

### How it works

{% stepper %}
{% step %}
### Create the date range

Add a period with **Start Date** and **End Date**.
{% endstep %}

{% step %}
### Add rows for rooms and boards

Use **Add interval** to add rows for each room/board combination.
{% endstep %}

{% step %}
### Set availability rules

Fill **Allotments**, **R**, **Min Stay**, and any guarantee fields you use.
{% endstep %}

{% step %}
### Set costs

Enter **Cost**, plus optional **Single Cost** and **Stay Type**.
{% endstep %}
{% endstepper %}

### Notes (for internal use)

#### Overview

Use **Notes** to store internal comments for the period.

Notes are only visible in Tourpaq Office.

They are **not shared with suppliers**.

#### Purpose

Use Notes to:

* Provide internal context or reminders regarding specific contract periods.
* Help colleagues and administrators track changes and maintain consistency in contract management.

#### Field Explanation

* **Notes (Internal Use Only)** – A free-text field where the administrator can enter comments, clarifications, or reminders related to the hotel contract period.
  * **Visibility**: Notes are strictly internal.
  * **Format**: Free text, no character limit (though concise entries are recommended).

#### Instructions for Use

1. Go to **Hotel Contract → Periods**.
2. Open the relevant period.
3. Enter your comment in **Notes (Internal Use Only)**.
4. Save the contract.

{% hint style="info" %}
Keep notes short. Write what changed and why.
{% endhint %}

***

### Tips

* Align period dates with the supplier’s season definitions.
* Add periods in chronological order. It makes audits easier.
* Avoid overlaps unless your setup explicitly supports it.
* Set **Min Stay** early. It affects booking validation.

***

### Related workflows

* [Rooms – Hotel Contract Configuration](rooms-hotel-contract-configuration.md): Room codes must exist before you add period rows.
* [Board Supplements - Hotel Contract Configuration](board-supplements-hotel-contract-configuration.md): Supplements often reference period logic and room codes.
* [Hotel contract - General](hotel-contract-general.md): Contract header settings can impact period behavior.

***

### FAQ

**Can I create multiple periods for the same contract?**\
Yes. Use one period per season or pricing strategy.

**What happens if periods overlap?**\
It depends on your configuration. Overlaps can cause pricing conflicts. Avoid them.

**Do I need a row for every room and board?**\
Usually, yes. Missing combinations may not price correctly.

**What is “Release days (R)”?**\
It’s the deadline for releasing unsold allotment back to the supplier.

**What’s the difference between Allotment, Guarantee, and Secured?**\
Allotment is availability for sale. Guarantee and Secured are commitment fields, when used.

**When should I use “Single Cost” and “SP%”?**\
Use **Single Cost** for single-occupancy supplements. Use **SP%** if it’s percentage-based.
