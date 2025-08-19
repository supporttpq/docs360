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
  * Do Booking&#x20;
  * Web Booking customer center

***

### Ticket Printing with Transport Extras

When a booking includes **transport extras for both outbound and homebound directions**, these details are reflected consistently in the tickets generated from both the **internal booking system** and the **customer-facing Web Booking (WB) center**.

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

Whether the ticket is printed from the **internal booking page** or from the **Web Booking center**, the same structure and information are displayed:

* **Specifikation af rejsebestilling** always shows outbound and homebound extras in separate columns, with accurate pricing and totals.
* **Forklaringer** maintains the outbound/homebound split, ensuring clarity for the traveler.

***

### **Booking flow**

* Open an exiting booking (that has already extras set for both directions)
* Click on "Print ticket"
* Open the downloaded ticket
* Under "Specifikation af rejsebestilling" section, extras are displayed properly under dedicated extra category name split in two columns (one for outbound and one for homebound), with corresponding price (and totals)

<figure><img src="../../.gitbook/assets/image (322).png" alt=""><figcaption></figcaption></figure>

&#x20;     Under "Forklaringer" extras are properly displayed with the total number booked, under dedicated extra category name split in two paragraphs (one for outbound and one for homebound)

<figure><img src="../../.gitbook/assets/image (323).png" alt=""><figcaption></figcaption></figure>



Web Booking flow

* Go to WB customer center
* Click on "Print ticket"

<figure><img src="../../.gitbook/assets/image (324).png" alt=""><figcaption></figcaption></figure>

* Open the ticket
* Under "Specifikation af rejsebestilling" section, extras are displayed properly under dedicated extra category name split in two columns (one for outbound and one for homebound), with corresponding price (and totals)  \
  Under "Forklaringer" extras are properly displayed with the total number booked, under dedicated extra category name split in two paragraphs (one for outbound and one for homebound)
