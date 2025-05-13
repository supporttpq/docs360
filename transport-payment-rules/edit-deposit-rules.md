# Edit Deposit Rules

<figure><img src="../.gitbook/assets/image (180).png" alt=""><figcaption></figcaption></figure>

The **Deposit Rules** tab allows administrators to configure custom deposit and payment rule entries based on booking and departure date ranges. This enables flexible financial planning for specific travel periods.

### **1. Overview Table Columns**

| Field                    | Description                                                                                                          |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------- |
| **Booking From**         | Start date of the booking period the rule applies to. Only bookings made on or after this date will follow the rule. |
| **Booking To**           | End date of the booking period the rule applies to. Only bookings made on or before this date will follow the rule.  |
| **Departure From**       | Start date of the departure period this rule applies to. Only trips departing on or after this date are affected.    |
| **Departure To**         | End date of the departure period this rule applies to. Only trips departing on or before this date are affected.     |
| **Deposit Value**        | Fixed deposit amount to be collected during the specified period.                                                    |
| **Deposit Percentage**   | Deposit calculated as a percentage of the total booking value.                                                       |
| **Second Payment Value** | Value for the optional second payment (if not disabled).                                                             |
| **Disabled**             | Checkbox to disable this particular rule entry. When checked, the rule is ignored.                                   |
| **Deposit Due**          | Number of days after booking when the deposit payment is due.                                                        |
| **Second Payment Due**   | Number of days before departure when the second payment is due.                                                      |
| **Last Payment Due**     | Number of days before departure when the final payment is due.                                                       |
| **Delete (🗑️ icon)**    | Removes the rule entry from the list.                                                                                |

### **2. Actions**

* **Create Button**: Adds a new row to define a custom deposit rule.
* **Pagination**: Allows navigation through multiple rule entries.
* **Company Tabs**: Deposit rules can be configured globally (_Entire Company_) or for specific travel brands/agencies (e.g., Primo Tours, Bravo Tours, etc.).

### **3. Rule Application Logic**

* Rules are applied based on **booking and departure date range matches**.
* When multiple rules overlap, priority may be determined by specificity (more exact match of both ranges).
* Disabled rules are **not** considered in the payment schedule.

⚠️Note: If a specific deposit rule is set per brand, it will override any rule set in the payment rule.

