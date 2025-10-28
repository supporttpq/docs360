# History

### **Overview**

The **Booking History** tab provides a detailed log of all changes made to a specific booking.\
Every modification—manual or automatic—is recorded with the responsible user, date, time, and the values before and after the change.\
This ensures complete transparency and traceability across all booking activities.

***

### **Purpose**

The purpose of the **History** view is to help users track:

* Who made a change and when.
* What data was modified (old and new values).
* Which system component (engine) triggered the update — for example, API Core or a manual user action.

It is a key tool for troubleshooting, auditing, and reviewing booking evolution over time.

* Resolving customer support questions related to changes, payments, or cancellations.

***

### **Preconditions**

* You must have access to a booking that has been created and possibly modified.
* Permissions to view booking history are required.
* Bookings must have been created or altered within the system to generate a visible history.

***

### **Instructions**

**Accessing the History Tab**

1. Open a booking from the booking overview or search results.
2. Select the **History** tab at the top of the booking details screen.
3. Use the search or expand/collapse options to view or filter the desired history entries.

***

**Available Columns**

| **Field**     | **Description**                                                                                     |
| ------------- | --------------------------------------------------------------------------------------------------- |
| **Date**      | The date when the change was made.                                                                  |
| **Time**      | The exact time the modification occurred.                                                           |
| **User**      | The name of the user or system that performed the change (e.g., _rowebtpq_, _APICore_).             |
| **Version**   | Indicates the booking version affected by the change.                                               |
| **Change**    | Describes what was modified (e.g., _Status change_, _Passenger name change_, _Room number update_). |
| **Old Value** | The value before the modification.                                                                  |
| **New Value** | The value after the modification.                                                                   |
| **Passenger** | Displays which passenger the change relates to, when applicable.                                    |
| **Engine**    | Identifies the source system of the change (for example, _APICore_).                                |

***

**Functions and Filters**

* **Expand / Collapse all:**\
  Expands or collapses all history entries for easier browsing.
* **Search by text:**\
  Allows searching for specific keywords, passengers, or change types.
* **Terms History (sub-tab):**\
  Shows all updates made to the booking’s terms and conditions.

***

#### **Example Use Case**

**Scenario:**\
A booking has an incorrect final price, and the user needs to verify when the change occurred.

1. Open the **History** tab.
2. Search for “Total change”.
3. Review the **Old Value** and **New Value** columns to identify when the price was updated and by which user or system.
