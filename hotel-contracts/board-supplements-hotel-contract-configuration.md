# Board Supplements - Hotel Contract Configuration

### Overview

Use **Board Supplements** to add board-related extras to a hotel contract. These supplements allow different pricing or availability based on the guest’s age, board type, or other custom criteria.

Typical examples are All-Inclusive upgrades and mandatory dinner supplements.

### Purpose

Use this tab to:

* Add extra board charges on top of the default board.
* Control eligibility by age range.
* Link the supplement to an **Extra Category** and optional **Product**.

### Screenshot

<figure><img src="../.gitbook/assets/image (289).png" alt=""><figcaption></figcaption></figure>

***

### Preconditions

Before you start:

1. The hotel contract exists and is open for editing.
2. Board types (AI, HB, etc.) are configured in the system.
3. Periods and room types are set up. This keeps costs consistent.

***

### Board Supplements (extras)

Use this section to create supplement rows.

| Field               | Description                                                             |
| ------------------- | ----------------------------------------------------------------------- |
| **Board**           | Base board type the supplement relates to.                              |
| **From / To (Age)** | Eligible age range. Guests outside the range do not get the supplement. |
| **Extra Category**  | Category used for reporting and grouping.                               |
| **Product**         | Optional. Link the supplement to a product/service.                     |
| **Name**            | Display or internal name. Keep it short and recognizable.               |
| **Code**            | Unique reference code. Used in exports and contract references.         |
| **Clear (×)**       | Clears the row input without deleting anything.                         |
| 🗑️ **Delete**      | Deletes the row.                                                        |
| **Add supplement**  | Saves the row.                                                          |

***

### Board Basis (cost per period)

Use **Board Basis** when you need a supplement cost per **period**.

<figure><img src="../.gitbook/assets/image (295).png" alt=""><figcaption></figcaption></figure>

#### Fields

| Field              | Description                                                        |
| ------------------ | ------------------------------------------------------------------ |
| **Board Type**     | Board the supplement applies to (for example AI, HB).              |
| **From / To Age**  | Age range for this supplement cost.                                |
| **Extra Category** | Category used for grouping and reporting.                          |
| **Product**        | Optional. Link to a product/service.                               |
| **Name**           | Display or internal name.                                          |
| **Code**           | Reference code used for exports and tracking.                      |
| **Period ID**      | Period the cost belongs to. It maps to IDs in the **Periods** tab. |
| **Cost**           | Supplement amount for this board + age + period.                   |
| **Rooms**          | Room codes where the supplement applies.                           |
| **Clear (×)**      | Clears the row input.                                              |

#### How it works

1. Pick a **Board Type** and **age range**.
2. Add a **Cost** for each relevant **Period ID**.
3. Limit the row to specific **Rooms** when needed.

{% hint style="info" %}
If you do not see **Board Basis**, check **System Setup →** [System Setup – Hotel Import](../setup/system-setup/system-setup-hotel-import.md).

If **Do not create extras for board basis** is enabled, the Board Basis menu is hidden.

It also prevents Board Basis extras from being created during hotel contract import.
{% endhint %}

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Gala Dinner

Use **Gala Dinner** for mandatory or optional event supplements.

Common cases are New Year’s Eve and Christmas dinners.

<figure><img src="../.gitbook/assets/image (297).png" alt=""><figcaption></figcaption></figure>

#### Fields

| Field                     | Description                                         |
| ------------------------- | --------------------------------------------------- |
| **Board Type**            | Board type the dinner applies to (for example AIP). |
| **Age From / To**         | Eligible age range.                                 |
| **Extra Category**        | Category used for grouping and reporting.           |
| **Product**               | Optional. Product associated with the dinner.       |
| **Name**                  | Display name of the event.                          |
| **Code**                  | Reference code for exports and contract tracking.   |
| **Start Date / End Date** | Date range for the event. Often a single day.       |
| **Cost**                  | Amount charged to eligible guests.                  |
| **Clear (×)**             | Clears the row input.                               |
| 🗑️ **Delete**            | Deletes the row.                                    |

#### How to add a gala dinner

1. Click **Add Gala Dinner**.
2. Select **Board Type**.
3. Set **Age From / To**.
4. Select **Extra Category** and optional **Product**.
5. Confirm **Name** and **Code** (auto-filled).
6. Set **Start Date / End Date**.
7. Enter **Cost**.
8. Save.

#### Tips

* Use stable **codes**. They show up in exports.
* Add separate rows for different ages or dates.

***

### Related workflows

* [Hotel contract - General](hotel-contract-general.md): Contract header settings and child age ranges.
* [Rooms – Hotel Contract Configuration](rooms-hotel-contract-configuration.md): Room codes referenced by Board Basis.
* [Periods – Hotel Contract Configuration](periods-hotel-contract-configuration.md): Period IDs used for Board Basis costs.
* [Extra Beds Cost – Hotel Contract Configuration](extra-beds-cost-hotel-contract-configuration.md): Often configured alongside board and age rules.

***

### FAQ

**What’s the difference between “Board Supplements” and “Board Basis”?**\
Board Supplements are the supplement definitions (board, age, category, product).\
Board Basis is where you assign costs per **Period ID**.

**Why is the Board Basis menu missing?**\
A system setting can hide it.\
Check **System Setup →** [System Setup – Hotel Import](../setup/system-setup/system-setup-hotel-import.md).

**How does the system evaluate age ranges?**\
It uses the guest’s age in the booking context.\
If the age is outside the range, the row is ignored.

**Can I apply a supplement to only some rooms?**\
Yes. Use the **Rooms** field in Board Basis.\
Limit it when only certain room codes include the board option.

**What’s the difference between Clear and Delete?**\
**Clear (×)** resets the input fields. It does not remove saved rows.\
🗑️ **Delete** removes the row from the contract.

**Can I add multiple supplements for the same board type?**\
Yes. Use separate rows.\
Keep age ranges and codes distinct to avoid conflicts.
