# Customer Data

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

<figure><img src="../../../../.gitbook/assets/image (564).png" alt="Customer Data tab showing email and SMS recipients"><figcaption></figcaption></figure>

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
