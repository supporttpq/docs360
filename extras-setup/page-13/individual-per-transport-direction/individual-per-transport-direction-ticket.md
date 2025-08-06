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

### **Steps & Expected Results**

<table data-header-hidden><thead><tr><th width="69"></th><th></th><th></th></tr></thead><tbody><tr><td><strong>Step</strong></td><td><strong>Action</strong></td><td><strong>Expected Result</strong></td></tr><tr><td>1</td><td>Open an <strong>existing booking</strong> with transport extras set for both directions.</td><td>The <strong>DooBooking page</strong> for the first step of the WB process is displayed.</td></tr><tr><td>2</td><td>Click <strong>“Print Ticket”</strong> from the internal booking page.</td><td>The <strong>ticket is downloaded</strong> (usually as a PDF file).</td></tr><tr><td>3</td><td>Open the <strong>downloaded ticket</strong> and review the content.</td><td>✅ Under <strong>"Specifikation af rejsebestilling"</strong>:<br>– Extras are listed under their <strong>category name</strong><br>– Information is split into <strong>two columns</strong>: outbound and homebound<br>– <strong>Prices</strong> for each direction are shown along with correct <strong>totals</strong><br><br>✅ Under <strong>"Forklaringer"</strong>:<br>– Extras appear under the same <strong>extra category name</strong><br>– The section is split into <strong>two paragraphs</strong> (one for outbound, one for homebound)<br>– Each shows the <strong>total number of extras booked</strong> per direction</td></tr><tr><td>4</td><td>Now go to the <strong>customer-facing WebBooking (WB) center</strong> and click <strong>“Print Ticket”</strong> from there.</td><td>✅ Under <strong>"Specifikation af rejsebestilling"</strong>:<br>– Extras are again shown under the <strong>correct category</strong><br>– Split into <strong>outbound/homebound</strong> columns<br>– <strong>Prices and totals</strong> match selections<br><br>✅ Under <strong>"Forklaringer"</strong>:<br>– Directional breakdown is respected<br>– Paragraphs and quantities match system selections</td></tr></tbody></table>

***

### **Field and Section Explanations**

<figure><img src="../../../.gitbook/assets/image (314).png" alt=""><figcaption></figcaption></figure>

| **Section**                           | **Description**                                                                                                                                                                                                            |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Specifikation af rejsebestilling**  | The main details area of the printed ticket. It lists selected extras, organized by category, with per-direction columns for outbound and homebound journeys, including their respective prices and the total.             |
| **Forklaringer**                      | The explanation section of the ticket. It shows a written summary of each selected extra. For transport extras, it includes one paragraph for outbound and one for homebound, each specifying the **total number booked**. |
| **Print Ticket (Backoffice)**         | Admin-accessible button used to generate and download the ticket from the internal DooBooking interface.                                                                                                                   |
| **Print Ticket (WB Customer Center)** | Customer-facing ticket print functionality. The layout and data must match what is seen in backoffice.                                                                                                                     |
