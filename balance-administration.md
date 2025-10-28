# Balance Administration

### Overview

The **Balance Administration** feature in Tourpaq is designed to streamline the management of financial transactions related to bookings, ensuring accurate tracking and reconciliation of payments, refunds, and balances.

Applies for Administrator and Financial

This module contains 5 other submodules:

### &#x20;**Unregistered payments**&#x20;

<figure><img src=".gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The unregistered payments are the booking payments with no corresponding booking number. It should be possible to assign an unregistered payment to a certain booking; thus, the modified record won’t appear anymore as unregistered, but it will be found in Payment Registration.

#### **Table Fields Explained**

| Field               | Description                                                                                                                                                                                                                                              |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Payment Date**    | The calendar date the payment was made by the payer. Format: `DD-MM-YYYY`.                                                                                                                                                                               |
| **Accounting Date** | The date the payment is officially recognized in the ledger. May match or lag behind the Payment Date.                                                                                                                                                   |
| **Payment Method**  | <p>How the payment was made. Examples include:<br>- <code>FI</code> (Bank Transfer)<br>- <code>GAVEKORT KOMP</code> (Gift Card Compensation)<br>- <code>GAVEKORT GEVINST</code> (Gift Card Prize)<br>- <code>GAVEKORTFAKT</code> (Gift Card Invoice)</p> |
| **Debit**           | Outflow amount (expenses or disbursements). All values are positive, representing payment amounts.                                                                                                                                                       |
| **Credit**          | Inflow amount. This column remains `0` across all current records, suggesting these are exclusively outgoing transactions.                                                                                                                               |
| **Tracking Code**   | A system-generated or externally supplied reference for tracing or auditing payments.                                                                                                                                                                    |
| **Fee Type**        | Placeholder for any transaction-associated fees (currently unused).                                                                                                                                                                                      |
| **Fee Amount**      | Amount of any transaction fee (currently unused).                                                                                                                                                                                                        |
| **Booking No**      | Reference to a booking if the payment has been or will be linked to one (currently empty).                                                                                                                                                               |

### **Negative balances**&#x20;

<figure><img src=".gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

All the bookings for which money should be returned to the customer will be displayed here. The seller decides if the money must be returned to the customer, and this should be set from the booking page.&#x20;

#### **Functional Options**

* **Seller Filter:** Dropdown to view negative balances linked to specific sellers.
* **Show Release Payment Only:** Checkbox that filters the list to show only records marked for release payment.

#### **Table Fields Explained**

| Field               | Description                                                                                                              |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| **Booking No**      | Unique identifier for a booking. Clickable link for detailed booking view.                                               |
| **Seller**          | Identifier for the agency, travel operator, or partner responsible for the booking.                                      |
| **Creation Date**   | The date the booking was first registered in the system.                                                                 |
| **Departure Date**  | The scheduled start date of the trip or service.                                                                         |
| **Customer**        | The name or anonymized identifier of the customer linked to the booking.                                                 |
| **Booking Total**   | The original total amount expected for the booking.                                                                      |
| **Paid Amount**     | The actual amount received from the customer. May exceed the booking total.                                              |
| **Balance**         | The calculated discrepancy: `Paid Amount - Booking Total`. A negative value indicates overpayment.                       |
| **Release Payment** | Indicates whether the overpaid amount is approved for refund or manual adjustment. Status is visualized with a red icon  |
| **Financed**        | May denote if the balance was covered by financing or external source.                                                   |
| **Comments**        | Manual notes or system-generated explanations, often anonymized for data privacy.                                        |
| **Branch**          |  Internal branch code or identifier                                                                                      |
| **Account**         | May refer to the financial ledger account to which this balance belongs                                                  |

### **Unpaid bookings**&#x20;

<figure><img src=".gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Here should appear all the bookings that haven’t been paid until today. It should be possible to filter the data by departure dates and payment due dates. The following is an extract of the information that could be displayed:

* Booking number
* Seller - Seller ID
* D.Due.Date - Departure due date
* SP.Due Date - Second payment due date&#x20;
* RP due Date - Rest payment due date
* Departure date - Day of the departure
* Customer - Booking customer name
* Booking total - Total sum of the booking
* Paid amount - The amount that was paid
* Balance - How was remeain to be paid
* Due amount It should be possible to sort the data from all 3 submodules by agency and seller.

### **GDS payments**

The **GdsPayments** section allows users to track and manage payments related to Global Distribution System (GDS) bookings, including ticket costs, airline details, and passenger information.

<figure><img src=".gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

1. **Filter the Data:**
   * Use **Departure Period** and **Booking Period** filters to narrow down transactions.
   * Select a **Seller** to view specific payment records.
   * Click **+ More filters** for additional filtering options.
2. **Review Payment Records:**
   * Check the **booking number** to identify a specific transaction.
   * Review **customer, phone number, and passenger details** for accuracy.
   * Verify **PNR codes, airlines, and cost prices** to confirm payment details.
   * Cross-check **departure & arrival airports** for route confirmation.
3. **Manage Comments & Notes:**
   * Review **payment comments** for any transaction-specific notes.
   * Check **Admin Comments** for additional insights or follow-ups.
4. **Edit or Update Payments:**
   * Click on the **Edit (Pencil) Icon** next to a record to modify details.
   * Ensure all updates align with booking and financial records.

**Key Fields Explained:**

* **Booking No.:** Unique reference number for the transaction.
* **Customer & Phone:** Identifies the traveler and contact details.
* **Passengers No.:** Number of passengers for the booking.
* **Departure & Arrival Dates:** Flight schedule details.
* **PNR Codes & Airlines:** Booking reference and airline information.
* **Cost Price:** Total ticket price in the designated currency.
* **Departure & Arrival Airports:** Flight route details.
* **Payment & Admin Comments:** Notes related to transaction status.

**Additional Actions:**

* Use the **filters** to refine searches for specific time frames, sellers, or bookings.
* Ensure **cost prices** match expected payments to avoid discrepancies.

### Refund payments

The refund process allows users to return payments to customers when there is a negative balance in the system.

<figure><img src=".gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

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

* &#x20;**Booking No.:** the booking number for the transaction.
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
