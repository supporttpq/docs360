---
hidden: true
---

# Edit Passenger

## **Passengers Tab**

### **Overview**

The **Edit Passenger** window allows users to view, add, modify, and manage passenger information for a booking. Each passenger (Pax) represents one traveler attached to the booking, and their details are essential for tickets, documents, rooming, transport, and reporting.

The window is divided into two tabs:

1. **Passengers** – personal details for each traveler
2. **Customer Data** – contact information for the booking’s main customer (not shown here)

### **Purpose**

The Edit Passenger window serves to:

* Maintain accurate passenger names and personal information
* Ensure the correct age and birthdate are used for price calculations (child, infant, senior, etc.)
* Add or remove passengers as needed
* Update contact details when required
* Support booking modifications during or after the sales process

Accurate passenger data is essential for:

* Tickets and travel documents
* Golf courses, transport seating, and SSR details
* Room allocation
* Airline requirements
* Insurance, and customer communication

### **How to Use**

In the booking interface, in the passenger section, to be able to edit the information of each passenger in the booking, you must click the Edit button.

<figure><img src="../../../.gitbook/assets/image (558).png" alt=""><figcaption></figcaption></figure>

After clicking the **Edit** button, a new window will open, allowing you to modify the information for each individual passenger.

<figure><img src="../../../.gitbook/assets/image (559).png" alt=""><figcaption></figcaption></figure>

#### **1. Editing an Existing Passenger**

Each row represents one passenger (Pax 1, Pax 2, Pax 3, etc.).\
You can update any field directly by typing or selecting from dropdown menus.

#### **2. Adding a New Passenger**

Click **“Add new”** at the bottom of the list.

#### **3. Removing a Passenger**

Click the **trash icon** on the far right of the passenger row.

#### **4. Saving Changes**

When all updates are completed:

* Click **Save Changes** to apply the modifications to the booking.

### **Passenger Fields Explained**&#x20;

| **Field Name** | **Description**                                                                                                                   |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **TITLE**      | Select the passenger’s title (Mr., Mrs., Chd, Inf, etc.). Determines how the name appears on tickets.                             |
| **F. NAME**    | First name of the passenger. Must match travel documents for flights and tickets.                                                 |
| **L. NAME**    | Last name/surname. Should match travel documents exactly.                                                                         |
| **AGE**        | Age of the passenger at the time of travel. Used for price categories (Adult/Child/Infant). Auto-fills when birthdate is entered. |
| **BIRTHDATE**  | Passenger’s date of birth. Determines age-based pricing and airline category.                                                     |
| **E-MAIL**     | Passenger email (optional). Usually used only for main traveler.                                                                  |
| **PHONE**      | Passenger phone number (optional). Usually filled only for main traveler.                                                         |
| **ADDRESS**    | Passenger address (optional). Typically stored for the main customer, not each pax.                                               |

### **Summary**

The Edit Passenger window is where you manage all traveler-related details in a booking. Always ensure names, ages, and birthdates are correct to avoid issues with:

* Ticket issuance
* Transport bookings
* Insurance

***

## **Customer Data**&#x20;

### **Overview**

The **Customer Data** tab provides an overview of all passengers included in the booking and allows the user to specify which traveler is the _main customer/contact person_ and who should receive notifications (SMS and Email).

While the **Passengers** tab focuses on personal details (names, birthdates, ages), the **Customer Data** tab defines **customer-level communication and identification attributes**.

This view is available within the Edit Passenger modal window opened from the booking details page.

### **Purpose**

The Customer Data tab supports the following objectives:

* Assign which passenger(s) should receive **SMS notifications** and **email communication**.
* Ensure correct contact details for the primary customer.
* Provide a centralized overview of travelers’ communication preferences.

This is essential because invoices, confirmations, travel documents, and operational messages are generally sent only to the selected primary customer and/or travelers opted in for communication.

### **Field Description Table**

<figure><img src="../../../.gitbook/assets/image (560).png" alt=""><figcaption></figcaption></figure>

| **Field Name** | **Description**                                                                                                                          |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **TITLE**      | Passenger's title (Mr., Mrs., Chd, Inf, etc.). Display only; not editable here.                                                          |
| **F. NAME**    | Passenger first name. Synced from passenger list; read-only in this tab.                                                                 |
| **L. NAME**    | Passenger last name. Read-only; matches booking passenger data.                                                                          |
| **AGE**        | Passenger age used for pricing and category logic. Read-only.                                                                            |
| **BIRTHDATE**  | Passenger birthdate. Read-only; ensures correct traveler classification.                                                                 |
| **E-MAIL**     | Email address for the selected passenger. Used for communication and ticket delivery.                                                    |
| **PHONE**      | Passenger phone number. Used for SMS and contact purposes.                                                                               |
| **ADDRESS**    | Passenger address. Usually filled for the main customer only.                                                                            |
| **CUSTOMER**   | Marks the passenger as the **contracting customer**. For a passenger with an email and phone number, a customer will be created.         |
| **SMS**        | When checked, the passenger will receive SMS notifications for the booking. Passenger agreement to receive the same SMS as the customer. |
| **EMAIL**      | When checked, the passenger will receive email communication (documents, confirmation, updates) same as the customer.                    |

### Summary

The **Customer Data** tab centralizes control of booking communications and customer identification. It is essential to:

* Ensure email/phone details are correct
* Select who receives **SMS** and **Email** notifications same as the customer
* Maintain clean and accurate communication settings for each booking
