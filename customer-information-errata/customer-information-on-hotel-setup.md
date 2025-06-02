# Customer Information on Hotel setup

### Overview

This document outlines managing customer-specific information on hotel setups via a back-office interface. It includes step-by-step instructions, expected results, validation rules, and guidance on interacting with the “Passengers Information” tab.

***

### 📘 Purpose

To verify that customer information for tickets, booking dates, and room types can be added, edited, and managed per hotel, including default and brand-specific configurations.

***

### 🧭 Test Case Steps and Descriptions

#### 1. Navigate to Hotel Setup

* Go to the **"Hotel" menu → "Hotels" -** A list of all hotels configured in the system is displayed.

***

#### 2. Select a Specific Hotel

* Click on the hotel for which customer info should be defined. - The hotel’s **edit page** is shown and  the **"Passengers Information"** tab becomes visible.

***

#### 3. Open the “Passengers Information” Tab

* Displays a paginated list (25 entries per page) of all existing customer information rules.
* If there are no rules, a message **"There are no entries to show"** is shown.
* Sorting is available, showing the newest entry on top.
* Each row includes an **edit** and **delete** button.
* A **"Default text"** tab and additional tabs for each brand with custom text enabled are available.

***

#### 4. Add a New Rule

* Click the **"Create"** button.&#x20;
* A form opens for defining a new rule.

***

#### 5. Fill in Customer Rule Data

**Required Fields**:

* **From / To (Departure Dates)**: Define the range for departure.
* **Booking Date From / To**: Optional date fields to limit based on booking date.
* **Information for Customer**: Text field displayed on ticket, WB, or booking page (input via pop-up).
* **Acknowledge Checkbox**: Requires customer confirmation; has an info tooltip.
* **Room Type**: Drop-down list showing all room types defined for the hotel.

**Validation Notes**:

* “To” must be greater than “From”.
* Date validation is based on combinations of departure date, booking date, and room type.
* Overlapping rules with identical parameters are restricted.
* Two rules may exist for the same period if they apply to **different room types**.

***

#### 6. Save the Rule

* Click the **"Save"** button.
* Entry is saved and a confirmation message appears.
* If validation fails, a warning message is displayed.

***

#### 7. Cancel Creation

**Action**:

* After editing, click **"Cancel" -** The entry is not saved and is removed from the list.

***

#### 8. Edit Existing Rule

* Click the **"Edit"** button on a specific rule. - Fields become editable. You can update all values.

***

#### 9. Delete a Rule

* Click the **"Delete"** button.
* Confirm in the pop-up dialog.\
  **Expected Result**:
* Rule is deleted upon confirmation.

***

### 🔁 Brand-Specific Configuration

#### 10. Managing Brand Tabs

Each hotel may have:

* **"Default text"**: Shared rule across all brands.
* **Brand-specific tabs**: For hotels where **“Use custom text”** is enabled per brand.

**Actions**:

* Select a brand tab.
* Click **Edit** on the existing entry.
* Save after editing.

**Expected Result**:

* Customized rules are applied and saved per brand.

***

### 🔍 Notes on Edge Cases

* **Booking Dates Null**: If booking dates are left null, the system compares only departure date rules.
* **No Booking Date Set**: Allows broader application of rules without constraints on when the booking was made.
* **Multiple Room Types**: Allows flexibility by separating rules for each room category.

***

### ✅ Summary of Validations

| Field            | Mandatory | Notes                                                   |
| ---------------- | --------- | ------------------------------------------------------- |
| From/To (Depart) | Yes       | "To" must be after "From"                               |
| Booking Dates    | Optional  | Valid only against same rule set                        |
| Info for Ticket  | Yes       | Opens pop-up to enter multi-line text                   |
| Acknowledge      | Yes       | User must check to proceed; tooltip provided            |
| Room Type        | Yes       | Allows differentiating rules per accommodation category |
