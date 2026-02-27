---
description: >-
  Verify that customer information (errata) appears in the correct Comments
  (Bemærkninger) sections on Tourpaq ticket PDFs across ticket versions 1–3.
---

# Customer Information displayed on the Ticket

### Purpose

Verify that customer information (errata) configured at entity level (Destination, Resort, Hotel, Transport) appears in the correct **Bemærkninger** (Comments) sections across **all three ticket versions**.

### Scope

This test covers the Booking module and Brand configuration in Tourpaq Office (back office).

### Preconditions

* Tester has access to the back office with permission to view **All Bookings** and edit **Users → Brands**.
* At least one booking exists that contains customer information set at:
  * Destination
  * Resort
  * Hotel
  * Transport
* Three ticket versions are available for the relevant brand.

### Test Data

<table><thead><tr><th width="173.44439697265625" align="center">Field</th><th width="189.2222900390625" align="center">Value</th><th>Notes</th></tr></thead><tbody><tr><td align="center">Booking date range</td><td align="center"><em>As needed</em></td><td>Use a period that includes the prepared test booking</td></tr><tr><td align="center">Brand</td><td align="center"><em>Desired brand</em></td><td>The brand whose ticket versions will be switched</td></tr></tbody></table>

### Steps & Expected Results

<table><thead><tr><th width="54.5555419921875" align="center">#</th><th width="338.22216796875">Action</th><th>Expected Result</th></tr></thead><tbody><tr><td align="center">1</td><td>Navigate to <strong>All Bookings</strong> and filter by the desired dates</td><td>Bookings list shows only records within the selected period</td></tr><tr><td align="center">2</td><td>Select a booking from the list</td><td>Booking <strong>Edit</strong> page is displayed</td></tr><tr><td align="center">3</td><td>Click <strong>Print Ticket</strong></td><td>PDF ticket downloads and opens in a new tab</td></tr><tr><td align="center">4</td><td>Inspect the ticket PDF</td><td><p>Customer information appears:</p><p>• <strong>Destination / Resort / Hotel</strong> info under the main <strong>Comments (Bemærkninger)</strong> section at the <strong>end</strong> of the ticket.</p><p>• <strong>Transport</strong> info under the <strong>Comments (Bemærkninger)</strong> section directly <strong>beneath</strong> the <strong>Itinerary (Rejseplan)</strong> block.</p></td></tr><tr><td align="center">5</td><td><p>Repeat validation for each ticket version: a. Go to <strong>Users → Brands</strong>. </p><p>b. Edit the desired brand. </p><p>c. Open the <strong>Ticket</strong> tab and change the <strong>Version</strong> (1, 2, 3). </p><p>d. Save and repeat steps 1–4.</p></td><td>Customer information is displayed in the <strong>same locations</strong> for <strong>all three</strong> ticket versions.</td></tr></tbody></table>

### Pass/Fail Criteria

* **Pass**: Placement of customer information matches the Expected Results table for every ticket version.
* **Fail**: Any deviation in placement or missing information.

### Evidence Collection

Attach the generated ticket PDF from Step 3 for each version and annotate the location of the Bemærkninger sections.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (2) (1) (1) (1).png" alt="Ticket PDF example showing where customer information (errata) appears in Comments (Bemærkninger) sections"><figcaption><p>Example ticket PDF: customer information (errata) appears in Comments (Bemærkninger) sections.</p></figcaption></figure>
