# Customer Information on Extra setup

### **Overview**

The system allows administrators to define rules for displaying customized passenger information tied to extras. These rules control how and when information appears to the customer based on defined date intervals and brands.

***

### **Step-by-Step Instructions**

#### 1. **Accessing Extras Configuration**

* Navigate to **"Extras Setup" → "Extras"**.
* The **Extras** page is displayed listing all defined extras for the company.

#### 2. **Open Extra for Configuration**

* Click on the extra for which the customer information should be set.
* The **Edit page** of the extra is displayed.
* Select the **"Passengers Information"** tab.

#### 3. **Passenger Information Tab**

* All defined entries are listed.
* If no entries exist: _"There are no entries to show"_ message appears.
* Features:
  * Entries sorted by most recently created.
  * Pagination (25 entries per page).
  * Each entry includes **Edit** and **Delete** buttons.
  * A **"Default text"** tab exists to define rules for each brand using custom text.

***

### **Creating a New Rule**

#### 4. Press **"Create"** button

* A new editable line appears with **"Save"** and **"Cancel"** buttons.

#### 5. Fill in Required Fields

* **From / To (Departure Date Interval)**: Mandatory.
* **Booking Date From / To**: Optional.
* **Information for customer on ticket**: Text field displayed via pop-up.
* **Acknowledge**: Checkbox with info tooltip. Requires guest acknowledgment in checkout and booking flow.

**Validation Rules:**

* “To” date must be later than “From”.
* Overlapping validations apply for both departure and booking date combinations.
* If booking date is not used, only rules with null booking dates are compared.

#### 6. Press **"Save"**

* If validations pass: Entry is saved; success message appears.
* If validations fail: Warning message is shown.

#### 7. Press **"Cancel"** (if needed)

* Entry is discarded and not saved.

***

### **Managing Existing Entries**

#### 8. Press **"Edit"** on Existing Entry

* Entry becomes editable. All fields can be changed.

#### 9. Press **"Delete"**

* Confirmation pop-up appears.
* On confirmation, entry is deleted and a success message is shown.

***

### **Customizing Brand Texts**

#### 10. Go to a Specific Brand Tab

* Each brand with **"Use custom text"** enabled appears in a dedicated tab.

**10.1 Press "Edit"**

* Only the _“Information for customer on ticket”_ is editable.

**10.2 Press "Save"**

* The edited information is saved for that brand.

***

### **Notes**

* Entries apply globally unless a brand-specific rule overrides the default.
* Booking dates are optional but allow more granular control when used.
* Tooltip guidance helps explain the “Acknowledge” option to users and customers.
