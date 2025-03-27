---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Balance Administration

Applies for Administrator and Financial

This module contains 5 other sub modules:

### &#x20;**Unregistered payments**&#x20;

<figure><img src=".gitbook/assets/image (9) (1) (1).png" alt=""><figcaption></figcaption></figure>

The unregistered payments are the booking payments with no correspondent booking number. It should be possible to assign an unregistered payment to a certain booking; thus, the modified record won’t appear anymore as unregistered, but it will be found in Payment registration.

### &#x20;**Negative balances**&#x20;

<figure><img src=".gitbook/assets/image (10) (1) (1).png" alt=""><figcaption></figcaption></figure>

All the bookings for which money should be returned to the customer will be displayed here. The seller decides if the money must be returned to the customer and this should be set from booking page. The following is an extract of the information that could be displayed:

* Booking number
* Seller
* Booking creation date
* Booking customer name
* Booking total
* Paid amount
* Balance
* Release payment - checkbox set from economics tab of the booking, informs if the money can be sent to the customer
* Financed
* Comments - taken from Comments tab of the booking, Economics section
* Branch - taken from Economics tab of the booking, Other Information Section
* Account - taken from Economics tab of the booking, Other Information Section

### **Unpaid bookings**&#x20;

<figure><img src=".gitbook/assets/image (11) (1) (1).png" alt=""><figcaption></figcaption></figure>

Here should appear all the bookings that haven’t been paid until today. It should be possible to filter the data by departure dates and payment due dates. The following is an extract of the information that could be displayed:

* Booking number
* Seller
* Payment due date
* Departure date
* Booking customer name
* Booking total
* Paid amount
* Balance
* Due amount It should be possible to sort the data from all 3 sub modules by agency and seller.

### **GDS payments**

The **GdsPayments** section allows users to track and manage payments related to Global Distribution System (GDS) bookings, including ticket costs, airline details, and passenger information.

<figure><img src=".gitbook/assets/image (12) (1) (1).png" alt=""><figcaption></figcaption></figure>

1. **Filter the Data:**
   * Use **Departure Period** and **Booking Period** filters to narrow down transactions.
   * Select a **Seller** to view specific payment records.
   * Click **+ More filters** for additional filtering options.
2. **Review Payment Records:**
   * Check the **Booking No** to identify a specific transaction.
   * Review **Customer, Phone Number, and Passenger Details** for accuracy.
   * Verify **PNR Codes, Airlines, and Cost Prices** to confirm payment details.
   * Cross-check **Departure & Arrival Airports** for route confirmation.
3. **Manage Comments & Notes:**
   * Review **Payment Comments** for any transaction-specific notes.
   * Check **Admin Comments** for additional insights or follow-ups.
4. **Edit or Update Payments:**
   * Click on the **Edit (Pencil) Icon** next to a record to modify details.
   * Ensure all updates align with booking and financial records.

**Key Fields Explained:**

* **Booking No:** Unique reference number for the transaction.
* **Customer & Phone:** Identifies the traveler and contact details.
* **Passengers No:** Number of passengers for the booking.
* **Departure & Arrival Dates:** Flight schedule details.
* **PNR Codes & Airlines:** Booking reference and airline information.
* **Cost Price:** Total ticket price in the designated currency.
* **Departure & Arrival Airports:** Flight route details.
* **Payment & Admin Comments:** Notes related to transaction status.

**Additional Actions:**

* Use the **filters** to refine searches for specific time frames, sellers, or bookings.
* Ensure **cost prices** match expected payments to avoid discrepancies.

### Refound payments

The refund process allows users to return payments to customers when there is a negative balance in the system.

<figure><img src=".gitbook/assets/image (8) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Filter and Select the Seller (Optional):**

* Use the dropdown menu to filter refunds by seller.
* Check "Show release payment only" if applicable.

**Review Refundable Transactions:**

* Look at the list of transactions with negative balances.
* Identify the customer and transaction details.

**Initiate the Refund:**

* Click the **"Refund"** button in the **Account** column.
* Confirm the refund process as prompted.

**Verification:**

* Ensure the **Balance** column updates accordingly.
* Verify if the refund status is marked as completed.

**Key Fields Explained:**

* **Booking No:** Unique reference number for the transaction.
* **Seller:** The party responsible for the booking.
* **Creation Date:** Date the transaction was recorded.
* **Customer:** Name of the customer requesting the refund.
* **Booking Total & Paid Amount:** Original transaction value.
* **Balance:** Negative amount indicating a refund is needed.
* **Released Payment & Financed:** Indicators for processed payments.
* **Comments:** Additional notes related to the refund.
* **Account:** The action button to trigger a refund.

**Additional Actions:**

* Use the **Print** button to generate reports of pending refunds.
* Check financing and released payments before issuing refunds.
