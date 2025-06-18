# Customer Information on Transport setup

This page documents the procedure for testing the configuration and behavior of **Customer Information** setup within the **Transport module**. This feature allows companies to define important informational messages to be displayed to customers during the booking and ticketing process.

***

### 📌 Purpose

To verify that customer information rules can be:

* Created with the proper data fields
* Validated correctly
* Edited and deleted
* Filtered by brand
* Displayed appropriately during the transport booking flow

***

### 🗺️ Navigation Steps

#### 1. **Access Transport Module**

* Go to **Transport > Transports -** A list of all defined transports for the company is displayed.

#### 2. **Open Destination Configuration**

* Click on the transport destination you wish to configure - The edit page for that destination is shown.

#### 3. **Go to Passenger Information**

* Click on the **Passenger Information** tab.

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

* **Expected Result:**
  * A list of existing customer information rules is displayed (or a message stating _"There are no entries to show"_).
  * Each rule includes **Edit** and **Delete** options.
  * Sorting is enabled (latest entries appear on top).
  * Pagination supports 25 entries per page.
  * A **"Default text"** tab is shown for brands using _Use custom text_.

***

### ➕ Creating a New Rule

#### 4. **Click "Create"**

* Opens a form for defining a new customer information rule.
* Includes **Save** and **Cancel** buttons.

#### 5. **Complete the Form Fields**

| Field                                  | Description                                                                                                        |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **From / To (Departure Interval)**     | Required date fields for when the message applies.                                                                 |
| **From / To (Booking Interval)**       | Optional date fields to restrict the message based on booking date.                                                |
| **Information for Customer on Ticket** | Text field (opens in pop-up) to display information to the customer on the ticket, web, or booking confirmation.   |
| **Acknowledge**                        | Checkbox with info tooltip: “If checked, the guest must acknowledge this info (during checkout and booking flow).” |

**Validation Rules:**

* "To" date must be greater than "From" date.
* Overlapping rules are validated differently based on the presence of a booking interval:
  * Rules without booking intervals are only validated against similar rules.
  * Rules with booking intervals are validated against each other.

***

### 💾 Saving and Cancelling

#### 6. **Click "Save"**

* **Expected Result:**
  * Entry is saved successfully, confirmation message displayed.
  * If validation fails, an error message is shown.

#### 7. **Click "Cancel"**

* **Expected Result:** Form closes, entry is not saved.

***

### ✏️ Editing and Deleting Entries

#### 8. **Edit an Entry**

* **Action:** Click "Edit" on a listed rule.
* **Expected Result:** All fields become editable.

#### 9. **Delete an Entry**

* **Action:** Click "Delete" > Confirm in pop-up.
* **Expected Result:** Entry is removed; success message displayed.

***

### 🏷️ Brand-Specific Customization

#### 10. **Customize for Specific Brand**

* **Action:** Go to the tab labeled with the desired brand name.
  * Click **Edit** on an entry.
  * Modify only the **Information for customer on ticket**.
  * Click **Save**.
* **Expected Result:** Custom message is saved for that specific brand only.

***

### 📎 Notes

* Each rule can be tied to a specific time interval for both departure and booking.
* Acknowledgment ensures that the customer explicitly agrees to the displayed information.
* Default text rules serve as a fallback when custom brand text is not configured.
