# System Setup Groups

### **Overview**

The **System Setup Groups** module allows administrators to define and manage group categories for bookings. Each group is linked to a specific **destination** and **agency/brand**, enabling the system to apply special offers or conditions for groups traveling to a particular resort.

### **Purpose**

* Standardize group configurations across agencies and brands.
* Apply minimum passenger requirements and special offers for group bookings.
* Centralize management of group rules to prevent duplication and ensure consistency.

### **Administrator Permissions**

Administrators can:

1. **View** all system setup groups that belong to their company.
2. **Edit** existing system setup groups.
3. **Insert** new system setup groups.
4. **Delete** system setup groups.

### **Behavior Rules**

* Each system setup group is uniquely tied to a **destination** and **agency/brand**.
* If an administrator attempts to add a group rule that already exists, the module will **update the existing rule** instead of creating a duplicate.

### **System Setup Group Fields**

| **Field**                        | **Description**                                                                      |
| -------------------------------- | ------------------------------------------------------------------------------------ |
| **Brand**                        | The brand to which the group belongs.                                                |
| **Destination**                  | The resort or destination associated with the group.                                 |
| **Minimum Number of Passengers** | The minimum number of passengers required to qualify for the group’s special offers. |
