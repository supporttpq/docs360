# Customer Information display on Ticket

### Purpose

Verify that customer information configured at the entity level (Destination, Resort, Hotel, Transport) appears in the correct **Bemærkninger** (Comments) sections across **all three ticket versions**.

### Scope

This test covers the Booking module and Brand configuration screens in the back‑office system.

### Preconditions

* Tester has access to Back‑office with permission to view **All Bookings** and edit **Users → Brands**.
* At least one booking exists that contains customer information set at:
  * Destination
  * Resort
  * Hotel
  * Transport
* Three ticket versions are available for the relevant brand.

### Test Data

| Field              | Value           | Notes                                                |
| ------------------ | --------------- | ---------------------------------------------------- |
| Booking date range | _As needed_     | Use a period that includes the prepared test booking |
| Brand              | _Desired brand_ | The brand whose ticket versions will be switched     |

### Steps & Expected Results

| # | Action                                                                                                                                                                                                | Expected Result                                                                                                                                                                                                                                                                   |
| - | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1 | Navigate to **All Bookings** and filter by the desired dates                                                                                                                                          | Bookings list shows only records within the selected period                                                                                                                                                                                                                       |
| 2 | Select a booking from the list                                                                                                                                                                        | Booking **Edit** page is displayed                                                                                                                                                                                                                                                |
| 3 | Click **Print Ticket**                                                                                                                                                                                | PDF ticket downloads and opens in a new tab                                                                                                                                                                                                                                       |
| 4 | Inspect the ticket PDF                                                                                                                                                                                | Customer information appears:• **Destination / Resort / Hotel** info under the main **Comments (Bemærkninger)** section at the **end** of the ticket.• **Transport** info under the **Comments (Bemærkninger)** section directly **beneath** the **Itinerary (Rejseplan)** block. |
| 5 | Repeat validation for each ticket version:  a. Go to **Users → Brands**.  b. Edit the desired brand.  c. Open the **Ticket** tab and change the **Version** (1, 2, 3).  d. Save and repeat steps 1–4. | Customer information is displayed in the **same locations** for **all three** ticket versions.                                                                                                                                                                                    |

### Pass/Fail Criteria

* **Pass**: Placement of customer information matches the Expected Results table for every ticket version.
* **Fail**: Any deviation in placement or missing information.

### Evidence Collection

Attach the generated PDF from Step 3 for each version and annotate the location of the Bemærkninger sections.&#x20;

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>
