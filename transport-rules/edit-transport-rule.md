# Edit Transport Rule

### **Overview**

The **Edit Transport Rule** function allows administrators to modify an existing Transport Rule that controls how transports are generated and named within the system. A Transport Rule defines the structure, logic, and naming convention for the transport legs associated with a specific route or operational configuration.\
Through this interface, users can update the rule name and ensure that all previously generated transports remain consistent with the naming logic.

### **Purpose**

The purpose of editing a Transport Rule is to maintain accurate, consistent, and operationally correct route definitions. Editing is typically required when:

* The original rule name was created incorrectly.
* The naming convention changes and the rule must follow updated internal standards.
* A mistake in the configuration must be corrected.
* Operational changes require renaming existing generated transports.

A key system requirement is **uniqueness**:\
➡️ _Two Transport Rules cannot have the same name._

Additionally, when a rule name is updated:\
➡️ _All transports previously generated based on that rule must be automatically renamed to follow the new naming convention._

This ensures data integrity throughout the operational flow and prevents mismatches between Transport Rule names and underlying transport entries.

### **Preconditions**

Before editing a Transport Rule, ensure that:

1. You have **permission** to manage Transport Rules (usually an admin or configuration-level role).
2. The new Transport Rule name is known and confirmed.
3. You verify that **no other existing rule** already uses the intended new name.
4. The system is not actively generating transports based on the rule at the exact moment of editing.
5. Any teams dependent on the rule (transport, planning, ops) are informed if the rename affects their processes.

#### Editing Transport Rule Names

Transport Rule names can be edited at any time. Renaming a Transport Rule will automatically update the names of all transports generated from it, ensuring they continue to follow the established naming convention.

To maintain data consistency, the system does not allow two Transport Rules to share the same name.

<figure><img src="../.gitbook/assets/image (535).png" alt=""><figcaption></figcaption></figure>

**Example:**\
If a Transport Rule was initially created as **BLLPMI1A**, but the correct naming should be **BLLPMI1A-TR**, updating the rule name will also rename all associated generated transports accordingly.

#### Auto-Selecting Stay Days When Adding New Entries

When a user clicks the **“+”** button to add new stay dates, the system automatically preselects the first available stay day from the drop-down list.

<figure><img src="../.gitbook/assets/image (536).png" alt=""><figcaption></figcaption></figure>

This behavior allows users to repeatedly press **“+”** and quickly add all remaining stay days in sequence, creating a faster and more efficient workflow.

#### Displaying Generated Transport Names in the Stay Days Table

In the Stay Days table, an additional column is introduced to display the name of the generated transport associated with each stay day.

<figure><img src="../.gitbook/assets/image (537).png" alt=""><figcaption></figcaption></figure>

The transport name it is a clickable link. Selecting this link opens the corresponding generated transport in a new browser tab, allowing users to review or manage it without losing their place in the current view.

<figure><img src="../.gitbook/assets/image (538).png" alt=""><figcaption></figcaption></figure>

After the new Stay Days have been added, to generate eligible transports for them, click the "Generate" button at the bottom right of the screen.

<figure><img src="../.gitbook/assets/image (539).png" alt=""><figcaption></figcaption></figure>

#### Editing Dates Before Transport Generation

Users can modify the selected dates after the initial save, provided the transports have not yet been generated.\
This ensures flexibility during setup while still preserving data integrity once the generation process begins.

#### Extending Season Dates

The system allows users to extend the season by adjusting the start or end dates, as needed:

* **Extending the end of the season:** Users can add additional weeks at the end if the season is prolonged.
* **Extending the beginning of the season:** Users can add earlier weeks if the season starts sooner than originally planned.

When extending an existing season by adding only a few additional weeks, the system will **reuse the same fix-quota**.\
However, if a completely new season period is added, the system will **generate a new fix-quota**.
