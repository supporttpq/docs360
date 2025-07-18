# Print Tickets

### Send Ticket

<figure><img src="../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

### 📌 Overview

The **Print Tickets** interface allows users to **generate and send travel tickets** for a specific reservation. It is designed to offer flexible options for printing, emailing, or re-sending electronic tickets (E-tickets).

***

### 🎯 Purpose

This module facilitates:

* Quick generation of printable tickets for travelers.
* Sending E-tickets to customers via email.
* Reprinting tickets per transport when needed (via the tab at the top).

It is primarily used in back-office workflows by customer support, reservation agents, or ticketing coordinators.

***

### ✅ Preconditions

* A valid booking number must exist in the system.
* The booking must be confirmed and contain travel components eligible for ticketing.
* User must have permissions to access and execute ticketing actions.

***

### 🧭 Fields and Options

| Field / Option        | Description                                                                                                                                          |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Booking No**        | Enter the unique booking number for which the ticket is to be printed or sent. The system will auto-fill the customer field if the booking is valid. |
| **Customer**          | Read-only field showing the customer name linked to the booking. Populated automatically based on the Booking No.                                    |
| **Print One Ticket**  | When checked, only one ticket will be printed for the whole booking                                                                                  |
| **Send E-Ticket**     | If checked, the ticket will be sent via email to the customer associated with the booking.                                                           |
| **Copy to e-mail**    | When enabled, the system will also send a copy of the E-ticket to the email address entered in the “Alternative Email” field.                        |
| **Alternative Email** | Optional field to specify an alternative email address for ticket delivery                                                                           |



***

### 🧪 Instructions for Use

1. **Enter a valid Booking No**.
   * The system will auto-populate the customer name.
2. **Choose ticket delivery options**:
   * Check **Print One Ticket** if only one combined ticket is needed.
   * Select **Send E-Ticket** to email the ticket to the customer.
   * Optionally, enable **Copy to e-mail** and enter an **Alternative Email** to CC someone else.

> ✅ Tip: Use the **Reprint Per Transport** tab if tickets are split by transport legs and need to be re-sent individually.

### Reprint Per Transport

<figure><img src="../.gitbook/assets/image (162).png" alt=""><figcaption></figcaption></figure>

### 📌 Overview

The **Reprint Per Transport** module is a specialized tool for batch reprinting tickets based on transport segments. It allows users to filter bookings by transport-related criteria such as travel date, booking date, length of stay, and transport type, and to print all matching tickets in one go.

This feature is particularly useful for preparing grouped ticket printouts for airport or station check-ins, charter operations, or tour departures.

***

### 🎯 Purpose

* To reprint tickets for **multiple bookings tied to specific transports**.
* To enable **bulk printing** based on departure, booking period, or travel duration.
* To support **operational readiness** for outbound/inbound logistics.

***

### ✅ Preconditions

* Transport data must be available and correctly assigned to bookings.
* Tickets must have already been generated (this is a **reprint** tool, not initial issue).
* User must have access rights to print or manage ticketing actions.

***

### 🧭 Fields and Options

| Field                      | Description                                                                                                                                                                                          |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Booking period**         | Filters bookings by the date range when they were created. Useful for reprinting tickets only for recent or specific sales periods. Format: `Start - End`.                                           |
| **Departure period**       | Filters bookings by the actual travel departure date range. Ideal for targeting upcoming or specific departures.                                                                                     |
| **Length**                 | Allows selection of travel duration (in nights/days) to further filter bookings. Dropdown menu with standard travel lengths.                                                                         |
| **Transports**             | Opens a modal to select one or more **transport routes**, such as outbound flights, bus transfers, or return legs. The selected transports will determine which tickets are included for reprinting. |
| **No transports selected** | Placeholder message until a transport is selected. Changes dynamically based on user input.                                                                                                          |
| **Print (button)**         | Executes the print job for all bookings that match the above filters. The result is a batch of tickets prepared for printing or saving as PDF.                                                       |

***

### 🧪 Instructions for Use

1. Open the **Reprint Per Transport** tab from the **Print Tickets** page.
2. Use the **Booking period** and/or **Departure period** filters to narrow down the list of relevant bookings.
3. Optionally, select a **Length** of stay to filter further.
4. Click on **Select transports** and choose the desired transport(s).
5. Once filters are applied, click the **Print** button in the top-right corner.
