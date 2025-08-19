# Individual per transport direction Web Booking

## **Web Booking - Do Booking**

#### **Overview**

This page explains how to test the behaviour of the **Individual Transport Extra Category** in the **Web Booking** flow of our travel booking system.&#x20;

#### **Purpose**

The purpose of this test case is to validate that:

* The **individual transport extras** behave correctly for **each direction** (outbound/homebound).
* Data is correctly saved and reflected in the **Thank You** For Booking page summary.

This ensures a smooth and intuitive experience for users selecting transport options during booking.

#### **Preconditions**

* You must have access to the **Do Booking** page.
* A **valid booking flow** (Web Booking process) must be configured and operational.
* At least one **extra category** for **individual transport** should be configured for both outbound and/or homebound directions.
* The booking should support extras and the second step (TILLAEG) should be accessible.

***

### Using Transport Extras in Web Booking (WB)

Transport-related extras can be configured **individually per direction** (outbound and homebound). This ensures that travellers can select and pay only for the services relevant to each part of their journey.

***

### Prerequisites

Before using this functionality, make sure:

* The **extra category** and corresponding **extra items** are properly defined&#x20;
* The extra is correctly configured to be available on bookings (brand, resources, prices, and availability are set).
* A booking has been created with extras defined for **both outbound and homebound directions**&#x20;

***

## Behaviour in Do Booking (Web Booking)

When a customer makes a booking through the Web Booking, extras behave as follows:

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
* Totals are calculated correctly, ensuring both the traveller and the agent have full visibility of the chosen extras.

<figure><img src="../../.gitbook/assets/image (312).png" alt=""><figcaption></figcaption></figure>

***

### Web Booking - Customer Center (Booking Confirmation)

#### **Overview**

The following information describes the procedure for editing **individual transport extras** in an **existing booking** using the **Web Booking module**.

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
  * The **Web Booking** section under the “Economics” tab
* Transport extras must be correctly configured in the system for visibility

***

## Managing Transport Extras in the Customer Center (Booking Confirmation)

The Customer Center allows users to review and adjust transport-related extras even after a booking has been created. Extras that are defined individually per transport direction (outbound and homebound) are displayed in a way that ensures clarity and flexibility for both the customer and the agent.

***

### Accessing Booking Confirmation

From an existing booking that already has extras configured for both directions, you can open the **Booking Confirmation** page via:

* **Economics → Web Booking** in the booking edit view.

This page mirrors the Web Booking flow and provides the same structure for extras management.

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
