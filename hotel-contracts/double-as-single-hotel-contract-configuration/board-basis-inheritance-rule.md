# Board Basis Inheritance Rule

When you import a hotel contract, **child rooms can inherit board basis**. They inherit it from the **parent room**.

This keeps board basis consistent in the room hierarchy. It also reduces manual edits after import.

### Overview

Some hotel contracts use a room hierarchy. A base room is the **parent room**. Variants, like **Double as Single**, are **child rooms**.

If the contract sets board basis on the parent room, Tourpaq uses it. Tourpaq applies the same value to linked child rooms.

***

### Purpose

Inheritance helps you:

* Keep the **same board basis** across related room types.
* Import faster, with less manual data entry.
* Avoid missing board basis on room variants.
* Get more predictable exports to downstream systems.

This matters most for hierarchical room setups. Examples include family rooms, suites, and room variants.

***

### Preconditions

Inheritance happens when:

1. The contract includes a parent–child room structure.
   * The import template detects the parent room.
   * The child rooms are linked to that parent.
2. The parent room has a board basis.
   * BB (Bed & Breakfast)
   * HB (Half Board)
   * AI (All Inclusive)

***

### Inheritance logic

During import:

1. Tourpaq reads the parent room.
2. If the parent room has a board basis, Tourpaq stores it.
3. Tourpaq checks each child room:
   * If the child room has no board basis, it inherits the parent value.
   * If the child room already has a board basis, it stays unchanged.

#### Result

After import, the parent and child rooms show the same board basis. This only changes if a child room sets its own value.

***

### Example scenario

#### Input contract

A hotel contract defines:

* Several normal rooms (for example Double Room)

<figure><img src="../../.gitbook/assets/image (531).png" alt=""><figcaption></figcaption></figure>

* One Double as Single room (child room)

<figure><img src="../../.gitbook/assets/image (532).png" alt=""><figcaption></figcaption></figure>

The supplier only provides board basis on the parent room. The Double as Single room has no board basis.

**Parent room**

* Double Room
* Board: All Inclusive

<figure><img src="../../.gitbook/assets/image (533).png" alt=""><figcaption></figcaption></figure>

**Child room**

* Double as Single
* Board: _(empty)_

#### System action

Upon import:

* Tourpaq detects the child room.
* It copies the board basis from the parent.
* After import, both rooms show the same board basis.

<figure><img src="../../.gitbook/assets/image (534).png" alt=""><figcaption></figcaption></figure>

#### Final result in the system

| Room Type        | Level  | Board Basis               |
| ---------------- | ------ | ------------------------- |
| Double Room      | Parent | All Inclusive             |
| Double as Single | Child  | All Inclusive (inherited) |

This prevents missing or inconsistent board basis after import.

***

### Related workflows

* [Hotel contract - General](../hotel-contract-general.md)
* [Rooms – Hotel Contract Configuration](../rooms-hotel-contract-configuration.md)
* [Double as Single – Hotel Contract Configuration](./)
* [Board Type](../../board-type/)

***

### FAQ

**Will a child room’s board basis be overwritten on import?**\
No. If the child already has a board basis, it stays unchanged.

**What happens if the parent room has no board basis?**\
Nothing is inherited. Child rooms keep their own value (or stay empty).

**Does this change pricing?**\
It updates the board basis field on the room.\
Pricing impact depends on your pricing logic and exports.

**Where do I verify the inherited board basis after import?**\
Open the imported hotel contract.\
Check the board basis shown on parent and child rooms.

**Why didn’t a child room inherit the board basis?**\
Most cases are missing room hierarchy detection.\
Verify the child room is linked to the correct parent.

***

### Summary

If a parent room has board basis in the contract, Tourpaq applies it on import. Child rooms inherit the same value across the hierarchy.
