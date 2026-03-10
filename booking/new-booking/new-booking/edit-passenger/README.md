---
description: >-
  Edit passenger (pax) details in Tourpaq Office bookings. Update names,
  birthdate/age, add or remove passengers, and manage customer contact data and
  email/SMS recipients.
---

# Edit Passenger

## **Passengers Tab**

### **Overview**

The **Edit Passenger** window in **Tourpaq Office** lets you manage **passenger (pax) details** for a booking. Update names, title, birthdate/age, and contact data. This data is used for **tickets and travel documents**, rooming, transport seating, insurance, and reporting.

The window is divided into two tabs:

1. **Passengers** – personal details for each traveler
2. **Customer Data** – contact information for the booking’s main customer (not shown here)

### **Purpose**

The Edit Passenger window serves to:

* Maintain accurate passenger names and personal information
* Ensure the correct **birthdate** and **age** are used for price logic (adult/child/infant)
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

<figure><img src="../../../../.gitbook/assets/image (558).png" alt="Edit button in booking passenger section"><figcaption></figcaption></figure>

After clicking the **Edit** button, a new window will open, allowing you to modify the information for each individual passenger.

<figure><img src="../../../../.gitbook/assets/image (563).png" alt="Edit Passenger window with passenger rows"><figcaption></figcaption></figure>

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

### **Passenger Fields Explained**

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

{% hint style="info" %}
For common questions and troubleshooting, see [Edit Passenger - FAQ](/broken/spaces/ZCqO8EQ5P5Mioq1zbQAc/pages/DwNYivW4VDD9nAP3wVEG).
{% endhint %}

***

## FAQ

#### What’s the difference between a **passenger (pax)** and the **customer**?

* A **passenger (pax)** is an individual traveler on the booking.
* The **customer** is the main contracting/contact person for the booking (typically the person who receives confirmations, invoices, and messages).

You edit traveler information in **Passengers**, and communication/contact selection in **Customer Data**.

#### Why is it important that names match the passport/travel document?

Tickets, airline messages (SSR), and supplier documents can require an exact match. If a name is incorrect, it can cause:

* Document/ticket mismatches
* Failed check-in or manual handling requirements
* Extra work with suppliers to correct passenger details

#### Does changing **Birthdate** or **Age** affect the price?

Yes. Age and birthdate drive price logic such as:

* Adult/Child/Infant categorization
* Child-price rules
* Insurance eligibility
* Some discounts/supplements and supplier rules

If prices look wrong, verify the **birthdate** first.

#### Why does the **Age** not look correct?

Typically, age is calculated from **birthdate**. If age looks wrong:

* Confirm the birthdate is entered correctly (day/month/year).
* Make sure the travel dates are correct (age is usually evaluated “at time of travel”).

#### Can I add passengers after I already started the booking?

Yes.

* Use **Add new** to add another pax.
* Always **Save Changes** when you are done.

If the booking’s allotments (hotel/transport) were already taken, you may need to re-check availability and/or take allotment again (depending on your workflow).

#### What happens when I remove a passenger?

Removing a passenger will normally:

* Remove that pax from the booking’s passenger list
* Trigger recalculation of totals and per-pax services
* Potentially change eligibility for discounts/supplements or pricing rules

If you are removing passengers after services have been allocated (seats, rooms, extras), double-check that allotment and connected services still match the intended passenger count.

### Customer Data tab (contact person + communication)

#### Who receives **Email** and **SMS** messages?

* The passenger marked as **Customer** is typically the primary recipient.
* Additional passengers can be opted in via the **EMAIL** and **SMS** checkboxes (they will receive the same communication as the customer).

#### Can I send confirmations/documents to more than one person?

Yes—enable **EMAIL** (and/or **SMS**) for additional passengers who should receive the same message as the customer.

#### What should I do if the wrong person is receiving messages?

1. Open **Edit Passenger**.
2. Go to **Customer Data**.
3. Set the correct passenger as **Customer**.
4. Adjust **EMAIL** / **SMS** checkboxes for other passengers.
5. **Save Changes**.

### Troubleshooting

#### I updated passenger details but the booking documents still show the old data

* Ensure you clicked **Save Changes** in the Edit Passenger window.
* If documents were already generated/sent, you may need to regenerate or resend them depending on your email/ticket flow.

#### I can’t save changes

Common causes:

* Missing mandatory fields (often title/first name/last name/birthdate)
* Invalid date format in birthdate
* Invalid characters in name fields (depending on ticketing rules)
