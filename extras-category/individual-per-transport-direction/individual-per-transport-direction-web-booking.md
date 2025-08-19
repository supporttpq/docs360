# Individual per transport direction Web Booking

### **WB - Do Booking**

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

#### &#x20;**Steps & Field Descriptions**

<table data-header-hidden><thead><tr><th width="84.5555419921875"></th><th></th><th></th></tr></thead><tbody><tr><td><strong>Step</strong></td><td><strong>Action</strong></td><td><strong>Expected Result</strong></td></tr><tr><td>1</td><td><strong>Go to DooBooking page</strong> from a price list or presentation site, and <strong>complete the passenger data</strong> (e.g. name, age, contact info).</td><td>The DooBooking page for the <strong>first step</strong> of the WB (web booking) process is displayed.</td></tr><tr><td>2</td><td>Proceed to <strong>second step (TILLAEG)</strong> where extras are selected.</td><td>All <strong>extra categories</strong> available for the current booking are displayed.</td></tr><tr><td>3</td><td>Locate and check the <strong>extra category for individual transport</strong>.</td><td>Each <strong>passenger</strong> will have <strong>two columns</strong> under this category:<br>- One for <strong>outbound</strong> direction<br>- One for <strong>homebound</strong> direction<br>Only the extras available for the relevant direction will appear under each.</td></tr><tr><td>4</td><td><strong>Select transport extras</strong> for one or more passengers, only in the direction(s) needed.</td><td>The selected extras are correctly <strong>saved</strong> for the corresponding passenger(s) and direction(s).</td></tr><tr><td>5</td><td>In case there are <strong>no products configured</strong> for a direction (e.g., no outbound transport available), or the extra is <strong>not eligible</strong> (due to passenger type, date, etc.):</td><td>The <strong>extra category for that direction will not be shown</strong> at all in the interface.</td></tr><tr><td>6</td><td><strong>Finish the booking</strong> and reach the <strong>ThankYouForBooking</strong> page.</td><td>The <strong>summary</strong> correctly shows the selected extras per passenger and direction. Totals are accurately calculated and displayed.</td></tr></tbody></table>

<figure><img src="../../../.gitbook/assets/image (312).png" alt=""><figcaption></figcaption></figure>

***

#### **Field Explanation**

| **Field**                             | **Description**                                                                                                            |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Passenger Data**                    | Information such as name, age, and other details required to initiate the booking.                                         |
| **TILLAEG Step**                      | The step in the booking flow where all optional **extras** (such as transport, insurance, etc.) can be added.              |
| **Individual Transport Extra**        | An optional service allowing transport to be added per passenger for outbound and/or homebound direction.                  |
| **Outbound / Homebound Columns**      | Visual representation per passenger to manage extras independently for each direction.                                     |
| **Eligibility**                       | System logic determines whether an extra is visible/applicable based on availability, configuration, or passenger details. |
| **Summary Page (ThankYouForBooking)** | Final confirmation screen displaying selected extras and calculated total costs for verification.                          |

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

#### **Steps & Expected Results**

<table data-header-hidden><thead><tr><th width="72.33331298828125"></th><th></th><th></th></tr></thead><tbody><tr><td><strong>Step</strong></td><td><strong>Action</strong></td><td><strong>Expected Result</strong></td></tr><tr><td>1</td><td>Open an <strong>existing booking</strong> that has extras set for <strong>both outbound and homebound</strong> directions.</td><td>The <strong>Edit Booking page</strong> is displayed.</td></tr><tr><td>2</td><td>Navigate to the <strong>"Economics" tab → WebBooking</strong> section.</td><td>The <strong>Booking Confirmation</strong> page is opened.</td></tr><tr><td>3</td><td>Proceed to the <strong>second page: “Tillaeg”</strong>, where optional extras are listed.</td><td>All extras categories configured for this booking are displayed.</td></tr><tr><td>4</td><td>Locate the <strong>extra category for Individual Transport</strong>.</td><td>Each <strong>passenger</strong> has two columns under this category:<br>- One for <strong>outbound</strong><br>- One for <strong>homebound</strong>.<br>Only the extras relevant for each direction are shown.</td></tr><tr><td>5</td><td>Modify or reselect transport extras as needed for the desired direction.</td><td>Selected extras are correctly <strong>saved</strong> to the booking.</td></tr><tr><td>6</td><td>If no extras are configured or valid for a specific direction:</td><td>That direction’s <strong>column/category is hidden</strong> entirely (not shown in the UI).</td></tr><tr><td>7</td><td>Check the <strong>summary and totals</strong> after changes are made.</td><td>All selected extras are <strong>listed</strong> in the summary and the <strong>totals</strong> reflect the updated selections accurately.</td></tr></tbody></table>

<figure><img src="../../../.gitbook/assets/image (313).png" alt=""><figcaption></figcaption></figure>

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
