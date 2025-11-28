# Board Basis Inheritance Rule

When importing a hotel contract where the **board basis is defined on the parent room**, the **child room automatically inherits the same board basis**. This ensures consistency across room structures and removes the need to manually assign the board basis to each child room during import.

### **Overview**

In the Tourpaq contract import system, hotel room structures often include **parent rooms** and **child rooms**. When a contract defines the **board basis** (e.g., BB, HB, FB, AI) at the parent room level, the system automatically applies this same board basis to all related child rooms.

### **Purpose**

The inheritance logic ensures:

* **Consistency** of board basis across all room types within the same hierarchy.
* **Faster contract loading**, reducing manual data entry.
* **Data accuracy**, preventing situations in which child rooms receive incomplete or mismatched board basis.
* **Predictable behavior** when processing or exporting room data to sales channels, price engines, or partners.

This is particularly important when working with hotels that use hierarchical room structures, such as _Family Rooms_, _Suites_, or _Room Variants_.

### **Preconditions**

For the inheritance to take place, the following conditions must be met:

1. **The contract file contains a parent–child room structure.**
   * Parent room is explicitly marked or logically detected by the import template.
   * Child rooms belong to the parent room via hierarchy.
2. **The parent room has a board basis defined.**\
   Examples:
   * BB (Bed & Breakfast)
   * HB (Half Board)
   * AI (All Inclusive)

### **System Behavior / Inheritance Logic**

During the import process:

1. The system reads the parent room data.
2. If the parent room contains a **Board Basis**, the value is stored.
3. For each child room:
   * If the child room has **no board basis**, it automatically inherits the parent’s value.

#### **Result**

After import is completed, looking at the hotel configuration in the system will show that **both the parent and its child rooms share the same board basis**, unless explicitly overridden.

### **Example Scenario**

#### **Input Contract**

A hotel contract defines:

* Several _normal rooms_ (e.g., Double Room)

<figure><img src="../../.gitbook/assets/image (531).png" alt=""><figcaption></figcaption></figure>

* One _Double as Single_ room (child room)

<figure><img src="../../.gitbook/assets/image (532).png" alt=""><figcaption></figcaption></figure>

The supplier only provided board basis on the **parent room**, not on the _Double as Single_.

**Parent Room:**

* Double Room
* Board: Al - All Inclusive

<figure><img src="../../.gitbook/assets/image (533).png" alt=""><figcaption></figcaption></figure>

**Child Room:**

* Double as Single
* Board: _(empty)_

#### **System Action**

Upon import:

* The system detects the child room.
* It copies the board basis from the parent (Al).
* After import, both rooms now display the same board type.

<figure><img src="../../.gitbook/assets/image (534).png" alt=""><figcaption></figcaption></figure>

#### **Final Result in the System**

| Room Type        | Level  | Board Basis                    |
| ---------------- | ------ | ------------------------------ |
| Double Room      | Parent | Al - All Inclusive             |
| Double as Single | Child  | Al - All Inclusive (inherited) |

This matches the expected business behavior and prevents missing or inconsistent board data.

### **Summary**

When a parent room has a board basis defined in the contract, the system automatically applies that board to all child rooms during import. After the import is complete, both the parent and child rooms display the same board basis in the hotel details, ensuring consistent and accurate contract data.
