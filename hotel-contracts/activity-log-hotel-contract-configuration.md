# Activity Log - Hotel Contract Configuration

### **Overview**

The **Activity Log** screen in the _Hotel Contract_ module displays a comprehensive audit trail of changes made to a hotel contract. It captures every modification, including inserts, updates, and deletions, along with metadata such as the user who made the change, the date and time of the action, and details about what was changed.

This tool is primarily used for **transparency**, **troubleshooting**, and **tracking changes** for contract compliance and operational accuracy.

***

### **Purpose**

The purpose of the **Activity Log** is to:

* Monitor changes made to hotel contracts.
* Provide accountability by showing which user made specific changes.
* Help identify data discrepancies or errors.
* Enable agencies and internal teams to audit past modifications.

***

### **Preconditions**

Before accessing the Activity Log:

* You must have the necessary **permissions** to view hotel contracts and audit logs.
* At least one **hotel contract must exist** with changes logged.
* You should know the **date range** and optionally the **user** for which you want to view activity.

***

### **Instructions for Use**

#### **Accessing the Activity Log**

1. Navigate to the **Hotel Contract** module.
2. Click on the **Activity Log** tab in the top menu.
3. Select the **date period** using the calendar controls (top-left).
4. Optionally, choose a specific **user** from the dropdown.
5. Click **Display** to view logs for the selected criteria.
6. Click **Clear** to reset filters.

***

### **Field Descriptions**

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

| Field Name         | Description                                                                                           |
| ------------------ | ----------------------------------------------------------------------------------------------------- |
| **KEYID**          | A unique identifier for the contract entry. All rows with the same KEYID belong to the same contract. |
| **ACTION**         | The type of change performed. Example: `Insert`, `Update`, `Delete`.                                  |
| **ENTITY NAME**    | The object or entity that was changed. Here, it is consistently `HotelContract`.                      |
| **PROPERTY NAME**  | The specific attribute/property of the entity that was modified.                                      |
| **ORIGINAL VALUE** | The previous value before the change. For `Insert` actions, this may be empty.                        |
| **NEW VALUE**      | The new value after the change was made.                                                              |
| **AGENCY**         | Indicates which agency made the change. `All brands` means the change is global across all brands.    |
| **DESCRIPTION**    | A brief text summarizing or categorizing the change                                                   |
