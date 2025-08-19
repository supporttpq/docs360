# Individual per transport direction - Ticket

### **Overview**

This page focuses on verifying how **individual transport extras** are displayed in printed tickets generated from both the **backoffice booking system** and the **WebBooking customer center**. It ensures that selected extras are presented correctly, split by **direction** (outbound/homebound), with accurate pricing and explanatory notes.

### **Purpose**

The purpose of this is to:

* Ensure that transport extras are properly **listed** in the printed ticket.
* Confirm that **directional information (outbound/homebound)** is clearly separated.
* Validate that **prices and totals** are accurate.
* Verify that **explanations (“Forklaringer”)** reflect the correct total quantities and directional breakdown.

### **Preconditions**

* You must have access to an **existing booking** with:
  * At least one passenger
  * **Transport extras configured and selected** for both outbound and homebound directions
* Booking must be in a state where ticket printing is allowed
* You must have access to:
  * DooBooking (internal tool)
  * WebBooking customer center

***

### Ticket Printing with Transport Extras

When a booking includes **transport extras for both outbound and homebound directions**, these details are reflected consistently in the tickets generated from both the **internal booking system** and the **customer-facing WebBooking (WB) center**.

#### Ticket Content

The ticket displays transport extras in two main sections:

**1. Specifikation af rejsebestilling**

* Extras are grouped under their **respective category name**.
* Information is organized into **two columns**: one for **outbound** and one for **homebound**.
* Each column shows the **price per direction**, and the correct **totals** are calculated.

**2. Forklaringer**

* Extras appear again, grouped under the same category name.
* The section is split into **two paragraphs**, one for outbound and one for homebound.
* Each paragraph displays the **total number of extras** booked for that direction.

#### Consistency Between Internal and Customer-Facing Tickets

Whether the ticket is printed from the **internal booking page** or from the **WB center**, the same structure and information are displayed:

* **Specifikation af rejsebestilling** always shows outbound and homebound extras in separate columns with accurate pricing and totals.
* **Forklaringer** maintains the outbound/homebound split, ensuring clarity for the traveler.

***

### **Field and Section Explanations**

<figure><img src="../../.gitbook/assets/image (314).png" alt=""><figcaption></figcaption></figure>

| **Section**                           | **Description**                                                                                                                                                                                                            |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Specifikation af rejsebestilling**  | The main details area of the printed ticket. It lists selected extras, organized by category, with per-direction columns for outbound and homebound journeys, including their respective prices and the total.             |
| **Forklaringer**                      | The explanation section of the ticket. It shows a written summary of each selected extra. For transport extras, it includes one paragraph for outbound and one for homebound, each specifying the **total number booked**. |
| **Print Ticket (Backoffice)**         | Admin-accessible button used to generate and download the ticket from the internal DooBooking interface.                                                                                                                   |
| **Print Ticket (WB Customer Center)** | Customer-facing ticket print functionality. The layout and data must match what is seen in backoffice.                                                                                                                     |
