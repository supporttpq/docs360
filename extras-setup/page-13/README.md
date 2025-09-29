# Extras

Applies to Administrator

Extras are optional services/products that a customer can book; like transfer, catering, pension, rental car, etc. This page allows users to create and configure various extras that can be associated with bookings or transport options.

Brands

<figure><img src="../../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure>

Allow the user to assign an extra to an agency. An extra can be assigned as follow:

* not assigned
* for sale - the extra can be booked only on office;
* internet sale - the extra can be booked only on WB
* for sale + internet sale - can be booked both, office and WB
* guide sale - can be booked only by a guide agent
* hotel sale - can be sel only by a hotel agent
* guide sale + internet sale + for sale - can be booked by a admin, guide or a WB

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

### **Overview:**

| Field                       | Description                                                                                                                                                                                                                                                                                                                                                            |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**                    | The public name of the extra, visible to customers. This is required.                                                                                                                                                                                                                                                                                                  |
| **List Name**               | Internal name used for lists or back-office reference.                                                                                                                                                                                                                                                                                                                 |
| **Code**                    | Unique identifier for the extra. Used for backend reference or integration.                                                                                                                                                                                                                                                                                            |
| **Status**                  | Visibility status. Set to `visible` to allow the extra to appear in search and bookings.                                                                                                                                                                                                                                                                               |
| **Stop Sales Hours**        | Time before departure when this extra will no longer be available for booking.                                                                                                                                                                                                                                                                                         |
| **Minimum Length**          | Minimum number of days a trip must be to allow this extra.                                                                                                                                                                                                                                                                                                             |
| **Contract Type**           | Specify the contract type (Allotment, Guarantee, Request, etc.).                                                                                                                                                                                                                                                                                                       |
| **Days Prices Option**      | <p>Allows limiting the prices per day options presented to the web user. Default is <code>0</code> if no variation. Only works for prices declared with days!!!!!! If no Days are declared, the product will be removed!<br>Ex: stay days = 14<br>days price option = 1<br>price days = 7,14,21</p><p>price days >= stay days - X</p><p>7,14,21 >= 14 - 1 => 14,21</p> |
| **Allotment Type**          | Is used to control the number of products available and the time they are available in. The choices are **Manual, Generic** and **Linked to transport**                                                                                                                                                                                                                |
| **Extras Category**         | Categorize the extra (e.g., Meal, Transfer, Tour). This is required.                                                                                                                                                                                                                                                                                                   |
| **Age**                     | Define the applicable age group (e.g., Adult, Child, Infant).                                                                                                                                                                                                                                                                                                          |
| **Period/Trip Length**      | Limit availability by trip length interval.                                                                                                                                                                                                                                                                                                                            |
| **SSR Codes**               | Assigns a SSR code to the extra and when chosen in a booking, the SSR code is reported to the transport company, thus keeping an evidence of passengers                                                                                                                                                                                                                |
| **Select Supplier**         | Assign a supplier responsible for fulfilling the extra.                                                                                                                                                                                                                                                                                                                |
| R**ound Rule**              | Set rounding logic for pricing                                                                                                                                                                                                                                                                                                                                         |
| **One-Way (only)**          | Tick this box if the extra applies to one-way trips only.                                                                                                                                                                                                                                                                                                              |
| **Currency**                | Choose the currency for pricing.                                                                                                                                                                                                                                                                                                                                       |
| **Maximum Length**          | Specify max trip duration for which the extra is valid.                                                                                                                                                                                                                                                                                                                |
| **Currency Prices**         | Enable this to input separate prices per currency.                                                                                                                                                                                                                                                                                                                     |
| **Show Supplier on Ticket** | Toggle if supplier details should appear on customer tickets.                                                                                                                                                                                                                                                                                                          |

### Custom Text

Used to customize the appearance and description of the extra in booking flows or documentation.

| Field           | Description                                                                                                                |
| --------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Name**        | Custom label to override the default extra name.                                                                           |
| **Description** | Rich text editor for detailed descriptions, highlights, or disclaimers. This text can be found in Guest APP and Guide APP. |

### Automatic Billing

Allows integration with internal billing and accounting systems for accurate cost tracking and supplier payouts.

| Field                    | Description                                                                                    |
| ------------------------ | ---------------------------------------------------------------------------------------------- |
| **Department Code**      | Accounting department code for internal tracking.                                              |
| **Account Debit**        | Account to be debited for this extra.                                                          |
| **Account Deposit**      | Account to receive the deposit related to the extra.                                           |
| **Add Own Schedule**     | Eneable will add the extra to it's creditor extra schedules which genarates a separate invoice |
| **Schedule**             | Define one or more billing schedules (Daily, Weekly, Monthly and Annualy).                     |
| **Select Creditor**      | Choose the supplier to be paid for the extra.                                                  |
| **Creditor Currency**    | Set the currency for the creditor’s payout.                                                    |
| **Automatic Billing**    | Enable automated billing upon booking.                                                         |
| **Schedule in the Past** | Allows scheduling billing for past dates (use with caution).                                   |

### Behaviour Settings

These settings control how the extra behaves in the booking process and what logic or restrictions apply to its use.

| Setting                                 | Description                                                                                                                 |
| --------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| **Autoselect in booking & offer**       | Automatically selects this extra during booking and in special offers. Useful for mandatory or strongly recommended extras. |
| **Unremovable On WebBooking**           | Prevents customers from removing the extra themselves during online booking. Ideal for required services.                   |
| **Unremovable On Customer Center**      | Prevents removal by users in the customer self-service portal.                                                              |
| **Auto Select in 'Select offer' popup** | If an offer selection popup appears, this extra is automatically pre-selected.                                              |
| **Add price to deposit**                | Includes the price of this extra in the booking deposit calculation.                                                        |
| **Add On All Pax**                      | Applies the extra to every passenger in the booking (e.g., insurance, meals).                                               |
| **Add only one per room**               | Limits the extra to one per room regardless of the number of passengers.                                                    |
| **Available to book (API)**             | Makes this extra accessible for bookings via external systems or integrations using the API.                                |

***

### &#x20;Other Settings

These settings influence how the extra interacts with billing, privacy regulations, and system integrations.

| Setting                      | Description                                                                                                                                |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **Issue Voucher**            | Enables the generation of a voucher for the extra.                                                                                         |
| **GDPR Sensitive**           | Flags the extra as containing GDPR-relevant data. Triggers data protection measures.                                                       |
| **Content Type**             | Used to classify the extra as a specific content asset, useful in API or content-driven environments.                                      |
| **Package Type**             | Treats the extra as a package rather than a standalone item. May impact how it's displayed or billed.                                      |
| **Use Stay Dates in Prices** | Prices are calculated based on the customer’s actual stay dates rather than fixed pricing. Helpful for seasonal or dynamic pricing models. |
