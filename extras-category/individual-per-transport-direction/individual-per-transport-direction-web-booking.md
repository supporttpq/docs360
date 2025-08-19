# Individual per transport direction Web Booking

## **WB - Do Booking**

#### **Overview**

This page explains how to test the behavior of the **Individual Transport Extra Category** in the **WebBooking** flow of our travel booking system.&#x20;

#### **Purpose**

The purpose of this test case is to validate that:

* The **individual transport extras** behave correctly for **each direction** (outbound/homebound).
* Data is correctly saved and reflected in the **Thank You** For Booking page summary.

This ensures a smooth and intuitive experience for users selecting transport options during booking.

#### **Preconditions**

* You must have access to the **DooBooking** page.
* A **valid booking flow** (WB process) must be configured and operational.
* At least one **extra category** for **individual transport** should be configured for both outbound and/or homebound directions.
* The booking should support extras and the second step (TILLAEG) should be accessible.

***

### Using Transport Extras in WebBooking (WB)

Transport-related extras can be configured **individually per direction** (outbound and homebound). This ensures that travelers can select and pay only for the services relevant to each part of their journey.

***

### Prerequisites

Before using this functionality, make sure:

* The **extra category** and corresponding **extra items** are properly defined&#x20;
* The extra is correctly configured to be available on bookings (brand, resources, prices, and availability are set).
* A booking has been created with extras defined for **both outbound and homebound directions**&#x20;

***

## Behavior in DooBooking (WB)

When a customer makes a booking through the WebBooking (WB) center, extras behave as follows:

* On the **Extras (TILLAEG)** step, all available extra categories for the booking are displayed.
* For categories linked to **individual transport directions**, each passenger sees **two separate columns**:
  * One for **outbound** extras
  * One for **homebound** extras
* Only the extras that are **eligible for the corresponding direction** are shown.
* Customers can select extras per passenger and per direction. Once selected, the extras are **saved correctly** to the booking.
* If no products are available on one direction, or no extras are eligible, the category for that direction will simply **not be displayed**.

***

### Booking Completion

After the extras are selected and the booking process is completed:

* The **Thank You for Booking** confirmation page displays the selected extras.
* Outbound and homebound selections are clearly separated.
* Totals are calculated correctly, ensuring both the traveler and the agent have full visibility of the chosen extras.

<figure><img src="../../.gitbook/assets/image (312).png" alt=""><figcaption></figcaption></figure>

***

### WB - Customer Center (Booking Confirmation)

#### **Overview**

The folowing informations describes the procedure for editing **individual transport extras** in an **existing booking** using the **WebBooking module**.

#### **Purpose**

* Confirm that previously selected **transport extras** are correctly loaded when editing an existing booking.
* Validate that users can **modify extras** for either travel direction (outbound or homebound).
* Verify that the **summary and totals** reflect the new selections accurately.

This ensures the accuracy and reliability of our booking edit workflow.

#### **Preconditions**

* A **booking must exist** with:
  * At least one **passenger**
  * Transport extras **already set** for both directions (outbound and homebound)
* User must have access to:
  * The **Booking Edit** module
  * The **WebBooking** section under the “Economics” tab
* Transport extras must be correctly configured in the system for visibility

***

## Managing Transport Extras in the Customer Center (Booking Confirmation)

The Customer Center allows users to review and adjust transport-related extras even after a booking has been created. Extras that are defined individually per transport direction (outbound and homebound) are displayed in a way that ensures clarity and flexibility for both the customer and the agent.

***

### Accessing Booking Confirmation

From an existing booking that already has extras configured for both directions, you can open the **Booking Confirmation** page via:

* **Economics → WebBooking** in the booking edit view.

This page mirrors the WebBooking flow and provides the same structure for extras management.

***

### Extras Display in the "Tillaeg" Section

Within the **Extras (Tillaeg)** page:

* All extras categories available for the booking are displayed.
* For categories linked to **transport directions**, each passenger has **two dedicated columns**:
  * One for outbound extras
  * One for homebound extras
* Only extras relevant to each direction are displayed.
* If no products are defined for a given direction (or none are eligible), the category for that direction will **not be shown at all**.

***

### Updating Extras

Users can add or change extras for passengers directly within this section. Once selections are made, the system ensures that:

* Extras are properly saved to the booking.
* The summary section updates automatically to reflect all selected extras.

***

### Booking Summary and Totals

At the end of the confirmation process:

* All selected extras are clearly listed in the **summary section**.
* Outbound and homebound extras are separated for clarity.
* Totals are calculated correctly based on the selections, ensuring pricing accuracy.

<figure><img src="../../.gitbook/assets/image (313).png" alt=""><figcaption></figcaption></figure>

***

### **Field and Page Descriptions**

| **Field/Section**                | **Description**                                                                                                                |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **Edit Booking Page**            | The central interface used to review and modify an existing booking’s data.                                                    |
| **Economics Tab → WebBooking**   | Tab used to access the WebBooking version of the booking, with all relevant data shown as the customer would see it.           |
| **Tillaeg Page**                 | The second step/page in the WebBooking where **extras (tillegg)** are managed and selected.                                    |
| **Individual Transport Extra**   | A category of optional extras allowing for transport to be selected for outbound and/or homebound directions.                  |
| **Outbound / Homebound Columns** | Separate columns displayed per passenger, enabling extra selection by direction.                                               |
| **Eligibility Rules**            | Rules that determine whether an extra is shown or hidden, based on factors like availability, passenger type, and travel date. |
| **Summary Section**              | A panel showing selected extras, quantities, and associated costs after selections are made.                                   |
| **Totals**                       | Financial breakdown of the selected extras, displaye                                                                           |
