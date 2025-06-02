# Customer Information on WebBooking

This documentation outlines the steps for creating a new booking and editing an existing booking in the DooBooking system, focusing on how customer information is set, confirmed, and validated.

### **New Booking (Doo Booking)**

This section describes the steps to create a new booking using the DooBooking system.

#### **Steps and Explanations**

| Step | Description                                                                                                                                             | Expected Results                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | Go to the “Do booking” section. Begin in WB "Rejsedeltagere" using a PLTA with customer information pre-filled (including departure and booking dates). | The DooBooking page is displayed.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 2    | Insert required data: - Customer details - Passenger details                                                                                            | Data is correctly inserted into the system.                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 3    | Click on the "Fortsæt" button.                                                                                                                          | The page redirects to the second step/page titled **"Tillæg"**.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 4    | Complete the necessary data in the "Tillæg" step/page. Choose any extras (ensure one extra has a customer info set).                                    | The data is selected successfully.                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 5    | Click "Fortsæt".                                                                                                                                        | The page redirects to the third step/page titled **"Opsummering"**. Under the Confirmation section **"Godkend oplysningerne og bestil rejsen"**, a new **"Passenger Informations"** section appears listing all customer info set on each entity: Hotel (room)ResortDestinationExtra Each information line is displayed with a checkbox. **Important:** All checkboxes must be checked (mandatory) for the **"Bestil Rejse"** (Book Trip) button to be enabled. Otherwise, the button remains disabled. |
| 6    | Click "Bestil Rejse".                                                                                                                                   | The page redirects to the **"ThankYouForBooking"** page. Booking is successfully created.                                                                                                                                                                                                                                                                                                                                                                                                               |

***

### **Edit Booking (Customer Center / Booking Confirmation)**

This section outlines how to edit a booking from the Customer Center.\
**Important:** This only applies to **extras**. You **cannot** edit transport or hotel details via the Customer Center.

#### **Steps and Explanations**

| Step | Description                                       | Expected Results                                                                                                                                                                                                                                                                                                                                    |
| ---- | ------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | Navigate to the second page **"Tillæg"**.         | The **Tillæg** page is displayed.                                                                                                                                                                                                                                                                                                                   |
| 2    | Edit an extra that contains customer information. | The desired extra is selected.                                                                                                                                                                                                                                                                                                                      |
| 3    | Click on "Gem" (Save).                            | A new **"Passenger Information"** popup appears, displaying all customer info related to the selected extra(s). Each line of info has a checkbox. **Important:** All checkboxes must be checked for the popup to disappear and for the changes to be saved. Once confirmed: The extra is added to the booking.The page redirects to the first step. |

***

### **Key Notes**

* All information lines in confirmation steps are **mandatory** to be checked.
* Editing is **limited to extras** only; changes to transport or hotel bookings are **not allowed** in the Customer Center.
* The booking workflow has **three primary steps**:
  1. **Data Entry**
  2. **Extras Selection (Tillæg)**
  3. **Summary & Confirmation (Opsummering)**&#x20;
