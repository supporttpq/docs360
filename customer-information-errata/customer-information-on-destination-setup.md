# Customer Information on Destination setup

### Overview

This documentation explains how to configure and manage customer-specific information that appears on tickets and other booking-related outputs, based on the **destination** selected. It provides detailed explanations of the setup process, validation rules, and brand-specific customization.

### Purpose

To ensure that destination-based customer information is accurately displayed across customer-facing outputs and acknowledged by the end-user when required.

### Preconditions

* The user has administrative access to the back-office.
* Destinations are already defined within the system.
* Brands have "Use custom text" enabled if brand-specific text is required.

### Navigation Path

**Setup → Destinations → Passenger Information tab**

***

### Step-by-Step Instructions

#### Step 1: Access Destinations

* Navigate to **Setup → Destinations -** The system displays a list of all destinations defined for the company.

#### Step 2: Select a Destination

* Click on the destination you wish to configure - The destination edit page is displayed.

#### Step 3: Go to "Passenger Information" Tab

* All existing rules are listed.
* If no rules exist, the message **"There are no entries to show"** appears.
* The tab includes a **pagination system** (25 entries per page) and is sorted with the latest entry on top.
* Each entry includes **Edit** and **Delete** options.
* A **Default Text** tab is available to define global rules.
* Brands with **"Use custom text"** enabled will have a dedicated tab for rule customization.

#### Step 4: Press "Create"

* A form appears to define a new customer information rule, with **Save** and **Cancel** options.

#### Step 5: Fill in Rule Data

| Field                                  | Type            | Description                                                                                                       |
| -------------------------------------- | --------------- | ----------------------------------------------------------------------------------------------------------------- |
| From (departure date)                  | Date (required) | Start interval for departure date.                                                                                |
| To (departure date)                    | Date (required) | End interval for departure date.                                                                                  |
| Booking date from                      | Date (optional) | Start of the booking date interval.                                                                               |
| Booking date to                        | Date (optional) | End of the booking date interval.                                                                                 |
| Information for the customer on ticket | Text            | Info displayed on the ticket, WB, and booking page. Opens in separate pop-up.                                     |
| Acknowledge                            | Checkbox        | If enabled, the user must acknowledge the message during checkout and booking flow. Tooltip explains its purpose. |

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Validation Notes:**

* **Date Interval Rules**:
  * "To" must be later than "From".
  * Booking dates are optional, but rules using them are validated differently.
* **Overlapping Validation**:
  * Prevents multiple overlapping rules.
  * Rules with NULL booking dates are compared only to other NULL booking date rules.
  * Rules with set booking dates are only compared against other rules with set booking dates.

#### Step 6: Press "Save"

* Entry is saved.
* A success message confirms the action.
* If validations fail, an explicit **warning message** appears.

#### Step 7: Press "Cancel" (after Step 5)

* Entry is discarded.
* No data is saved.

#### Step 8: Press "Edit" on an Entry  - The rule is opened in **edit mode,** and all fields are editable.

#### Step 9: Press "Delete" on an Entry

* A confirmation dialog appears.
* Upon confirmation, the entry is removed and a success message is displayed.

#### Step 10: Brand-Specific Configuration

1. Navigate to a specific brand tab.
2. Press "Edit" on an entry.

* All entries defined on "Default text" tab are displayed
* Only "Information for customer on ticket" is enabled and can be edited. The information can be customized on each brand.

3. Press "Save - Value is saved on that specific brand
