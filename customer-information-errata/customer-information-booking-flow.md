# Customer Information Booking Flow

### Purpose

This page describes expected system behavior for creating and editing bookings in a system that requires customer information acknowledgment for various components (transport, hotels, resorts, destinations, extras). The focus is on ensuring that all mandatory customer info is acknowledged before finalizing a booking.

***

### **New Booking Flow**

#### Overview

A user creates a new booking and is required to acknowledge all mandatory customer information related to selected services. Booking cannot be completed unless all such information is reviewed and confirmed.

#### Steps & Expected Results

| **Step** | **Action**                                                             | **Expected Result**                                                                                                    |
| -------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 1        | Create a new booking by pressing “New booking”                         | Booking Edit page is displayed                                                                                         |
| 2        | Insert required data (number of passengers, customer details)          | Data is properly saved                                                                                                 |
| 3        | Choose the transport (with customer info that requires acknowledgment) | Transport is selected                                                                                                  |
| 4        | Choose a hotel (with customer info that requires acknowledgment)       | Hotel/room is selected and passengers are auto-allocated                                                               |
| 5        | Press “Take allotment”                                                 | Passenger Info pop-up appears listing customer info (Hotel, Resort, Destination); checkboxes must be marked to proceed |
| 6        | Acknowledge all displayed info                                         | Checkboxes are marked                                                                                                  |
| 6.1      | Press “Save”                                                           | Info is saved and pop-up closed                                                                                        |
| 7        | Select extra service(s) with mandatory info                            | Extra is selected                                                                                                      |
| 7.1      | Press “Save Passengers”                                                | Pop-up with extra-related info appears, checkboxes must be marked                                                      |
| 8        | Acknowledge extra service info                                         | Checkboxes are marked                                                                                                  |
| 8.1      | Press “Save”                                                           | Info saved and pop-up closed                                                                                           |
| 9        | Press final “Save”                                                     | Booking saved with “OK” status                                                                                         |

***

### **Edit Booking Flow**

#### Overview

Modifying an existing booking may retrigger the need to acknowledge any changed or newly required customer information, especially when editing hotels, allocating passengers, or adding extras.

#### Steps & Expected Results

| **Step** | **Action**                                | **Expected Result**                                                                                 |
| -------- | ----------------------------------------- | --------------------------------------------------------------------------------------------------- |
| 1        | Edit an existing booking                  | Booking Edit page is displayed                                                                      |
| 2        | Edit hotel option or allocate passengers  | Data is saved                                                                                       |
| 3        | Press “Take allotment”                    | Passenger Info pop-up appears with updated hotel/resort/destination info; checkboxes must be marked |
| 4        | Acknowledge all displayed info            | Checkboxes are marked                                                                               |
| 4.1      | Press “Save”                              | Info is saved and pop-up closed                                                                     |
| 5        | Press “Edit Passengers” and select extras | Extra is selected                                                                                   |
| 5.1      | Press “Save Passengers”                   | Pop-up with extra-related info appears; checkboxes must be marked                                   |
| 6        | Acknowledge extra service info            | Checkboxes are marked                                                                               |
| 6.1      | Press “Save”                              | Info saved and pop-up closed                                                                        |
| 7        | Press final “Save”                        | Booking saved with “OK” status                                                                      |

***

### Mandatory Acknowledgment Enforcement

* **All customer information requiring acknowledgment is marked as mandatory**.
* Users **cannot save or proceed** with the booking unless all checkboxes are checked.
*   If not acknowledged, a warning message appears:

    > "You must check all mandatory terms before you create the booking!"

***

### Notes

* The **"Passenger Information" pop-up** appears:
  * When allotment is taken.
  * When editing passengers or extras.
* All check-box items in the pop-up represent **mandatory terms** and must be confirmed before proceeding.
