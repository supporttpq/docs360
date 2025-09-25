# Create / Edit rule

### **Overview / Purpose**

The system allows administrators to define rules that control availability and restrictions based on transport, destination, resort, hotel, or room type. Rules are time-bound and can be enabled or disabled as needed.

This functionality ensures precise control over booking conditions, making it possible to handle seasonal restrictions, transport limitations, or hotel-specific rules.

### **How It Works**

A new rule is created by defining a set of criteria (such as start date, end date, and applicable transports or destinations). The system validates the input before saving the rule. Once saved, the rule is displayed at the top of the list and can later be activated or deactivated through the **Enabled** checkbox.

***

### **Key Features / Functions**

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Rule Creation**

* **Start Date** (mandatory): The beginning date of the rule.
* **End Date** (mandatory): The ending date of the rule. Must be later than the start date.
* **Transport Type**: Selection field listing all available transport types.
* **Transports**: Multiple selection field with all available transports.
* **Destination**: Multiple selection field with available destinations.
* **Resort**: Multiple selection field with resorts from the selected destination(s) or transports.
* **Hotel**: Multiple selection field with hotels from the selected resort(s).
* **Room Type**: Multiple selection field with rooms from the selected hotel(s).
* **Note**: Free text description for the rule.
* **Enabled**: Checkbox to activate the rule immediately (default: checked).

**Dependencies between fields:**

* Transport is filtered by selected Transport Type.
* Destination is filtered by selected Transport(s).
* Resort is filtered by Destination(s) and Transport(s).
* Hotel is filtered by Resort(s).
* Room Type is filtered by Hotel(s).

⚠️ At least one of the following fields must be defined: **Transport, Destination, Resort, Hotel.**

***

#### **Validation Rules**

* **Mandatory fields** must be completed (Start Date, End Date, Note, and at least one of Transport/Destination/Resort/Hotel).
* **End Date must be greater than Start Date**.
* If validation fails, a warning is displayed, and the rule cannot be saved.

***

#### **Rule Editing**

* Once created, the only editable field is the **Enabled** checkbox.
* When checked, the rule is active.
* When unchecked, the rule is inactive.
* Saving updates the status, and a success message is displayed.

***

#### **Rule Cancellation**

* If you cancel while creating a rule, no data is saved and the editable line is removed.

***

### **Examples / Scenarios**

* **Seasonal Restriction:** A hotel is unavailable from 01-11-2025 to 01-03-2026. A rule can be created for that hotel with those dates, leaving Enabled checked.
* **Transport-Specific Restriction:** A flight route is temporarily closed. A rule can be applied to the affected transport.
* **Room Block:** Specific room types are blocked for bookings during peak dates.

***

### **Notes / Best Practices**

* Always add a clear **Note** for every rule to make future reviews easier.
* Use **specific selections** (e.g., resort + hotel) to avoid overly broad restrictions.
* Regularly review active rules to ensure outdated ones are disabled.
* Start and End Dates should be planned in advance to minimize manual changes.
