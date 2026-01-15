# Extras

Applies to Administrator

Extras are optional services/products that a customer can book; like transfer, catering, pension, rental car, etc. This page allows users to create and configure various extras that can be associated with bookings or transport options.

#### Brands

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Allow the user to assign an extra to an agency. An extra can be assigned as follow:

* not assigned
* for sale - the extra can be booked only on office;
* internet sale - the extra can be booked only on WB
* for sale + internet sale - can be booked both, office and WB
* guide sale - can be booked only by a guide agent
* hotel sale - can be set only by a hotel agent
* guide sale + internet sale + for sale - can be booked by a admin, guide or a WB

<figure><img src="../../.gitbook/assets/image (571).png" alt=""><figcaption></figcaption></figure>

### **Overview:**

| Field                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**                    | The public name of the extra, visible to customers. This is required.                                                                                                                                                                                                                                                                                                                                                                         |
| **List Name**               | Internal name used for lists or back-office reference.                                                                                                                                                                                                                                                                                                                                                                                        |
| **Code**                    | Unique identifier for the extra. Used for backend reference or integration.                                                                                                                                                                                                                                                                                                                                                                   |
| **Status**                  | Visibility status. Set to `visible` to allow the extra to appear in search and bookings.                                                                                                                                                                                                                                                                                                                                                      |
| **Stop Sales Hours**        | Time before departure when this extra will no longer be available for booking.                                                                                                                                                                                                                                                                                                                                                                |
| **Minimum Length**          | Minimum number of days a trip must be to allow this extra.                                                                                                                                                                                                                                                                                                                                                                                    |
| **Contract Type**           | Specify the contract type (Allotment, Guarantee, Request, FreeSell).                                                                                                                                                                                                                                                                                                                                                                          |
| **Days Prices Option**      | <p>Allows limiting the prices per day options presented to the web user. Default is <code>0</code> if no variation. Only works for prices declared with days!!!!!! If no Days are declared, the product will be removed!<br>Ex: stay days = 14<br>days price option = 1<br>price days = 7,14,21</p><p>price days >= stay days - X</p><p>7,14,21 >= 14 - 1 => 14,21</p>                                                                        |
| **Allotment Type**          | Is used to control the number of products available and the time they are available in. The choices are **Manual, Generic** and **Linked to transport**                                                                                                                                                                                                                                                                                       |
| **Extras Category**         | Categorize the extra (e.g., Meal, Transfer, Tour). This is required.                                                                                                                                                                                                                                                                                                                                                                          |
| **Age**                     | Define the applicable age group (e.g., Adult, Child, Infant).                                                                                                                                                                                                                                                                                                                                                                                 |
| **Period/Trip Length**      | Limit availability by trip length interval.                                                                                                                                                                                                                                                                                                                                                                                                   |
| **SSR Codes**               | Assigns a SSR code to the extra and when chosen in a booking, the SSR code is reported to the transport company, thus keeping an evidence of passengers                                                                                                                                                                                                                                                                                       |
| **Select Supplier**         | Assign a supplier responsible for fulfilling the extra.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Round Rule**              | Set rounding logic for pricing                                                                                                                                                                                                                                                                                                                                                                                                                |
| **One-Way (only)**          | Tick this box if the extra applies to one-way trips only.                                                                                                                                                                                                                                                                                                                                                                                     |
| **Currency**                | Choose the currency for pricing.                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Maximum Length**          | Specify max trip duration for which the extra is valid.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Currency Prices**         | Enable this to input separate prices per currency. If selected, the sales price for each brand will be calculated from the default price, using the relevant currencies. The sales prices are not updated for existing bookings. **Example:** The company currency is EUR, and the brand currency is SEK. The currency rate has changed from 11,55 to 11,3. This update will trigger the service to run an automatic update of the pricelist. |
| **Show Supplier on Ticket** | Toggle if supplier details should appear on customer tickets.                                                                                                                                                                                                                                                                                                                                                                                 |

### Custom Text

Used to customize the appearance and description of the extra in booking flows or documentation.

<figure><img src="../../.gitbook/assets/image (442).png" alt=""><figcaption></figcaption></figure>

| Field           | Description                                                                                                                |
| --------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Name**        | Custom label to override the default extra name.                                                                           |
| **Description** | Rich text editor for detailed descriptions, highlights, or disclaimers. This text can be found in Guest APP and Guide APP. |

### Automatic Billing

Allows integration with internal billing and accounting systems for accurate cost tracking and supplier payouts.

<figure><img src="../../.gitbook/assets/image (443).png" alt=""><figcaption></figcaption></figure>

| Field                    | Description                                                                                  |
| ------------------------ | -------------------------------------------------------------------------------------------- |
| **Department Code**      | Accounting department code for internal tracking.                                            |
| **Account Debit**        | Account to be debited for this extra.                                                        |
| **Account Deposit**      | Account to receive the deposit related to the extra.                                         |
| **Add Own Schedule**     | Enable to add the extra to its creditor extra schedules, which generates a separate invoice. |
| **Schedule**             | Define one or more billing schedules (Daily, Weekly, Monthly and Annually).                  |
| **Select Creditor**      | Choose the supplier to be paid for the extra.                                                |
| **Creditor Currency**    | Set the currency for the creditor’s payout.                                                  |
| **Automatic Billing**    | Enable automated billing upon booking.                                                       |
| **Schedule in the Past** | Allows scheduling billing for past dates (use with caution).                                 |

### Behaviour Settings

These settings control how the extra behaves in the booking process and what logic or restrictions apply to its use.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="307.3333740234375">Setting</th><th>Description</th></tr></thead><tbody><tr><td><strong>Autoselect in booking &#x26; offer</strong></td><td>Automatically selects this extra during booking and in special offers. Useful for mandatory or strongly recommended extras. The product will already be selected by default in a new booking. When using this feature, please make sure the product does not have a discount linked to it.</td></tr><tr><td><strong>Unremovable On Web Booking</strong></td><td>Prevents customers from removing the extra themselves during online booking. Ideal for required services.</td></tr><tr><td><strong>Unremovable On Customer Center</strong></td><td>Prevents removal by users in the customer self-service portal.</td></tr><tr><td><strong>Add price to deposit</strong></td><td>Includes the price of this extra in the booking deposit calculation.</td></tr><tr><td><strong>Include in basic price</strong></td><td>If checked, this will hide the extras from the view of the customer in Web Booking and Customer Centre. It will, however, increase the base price and affect the booking total.</td></tr><tr><td><strong>Add On All Pax</strong></td><td>If selected for one passenger in webbooking, the product will be automatically selected for all eligible pax of the booking; If removed, will be removed from all.</td></tr><tr><td><strong>Add only one per room</strong></td><td>Limits the extra to one per room regardless of the number of passengers.</td></tr><tr><td><strong>Available to book (API)</strong></td><td>Check whether a product should be shown as available to book in the Offer API, without adding it to the total.</td></tr></tbody></table>

***

### Other Settings

These settings influence how the extra interacts with billing, privacy regulations, and system integrations.

<figure><img src="../../.gitbook/assets/image (445).png" alt=""><figcaption></figcaption></figure>

| Setting                      | Description                                                                                                                                |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **Issue Voucher**            | Enables the generation of a voucher for the extra.                                                                                         |
| **GDPR Sensitive**           | Flags the extra as containing GDPR-relevant data. Triggers data protection measures.                                                       |
| **Content Type**             | Used to classify the extra as a specific content asset, useful in API or content-driven environments.                                      |
| **Package Type**             | Treats the extra as a package rather than a standalone item. May impact how it's displayed or billed.                                      |
| **Use Stay Dates in Prices** | Prices are calculated based on the customer’s actual stay dates rather than fixed pricing. Helpful for seasonal or dynamic pricing models. |

***

### FAQ

#### 1. Why can’t I see the extra when I try to book it?

**Q:** The extra exists, but it doesn’t show up in Office/Web Booking. Why?\
**A:** Check `Status = visible`, and check the `Brands` channel setup (for sale / internet sale / etc.). Also confirm it’s in the right `Extras Category` and matches any `Minimum Length`, `Maximum Length`, and `Period/Trip Length` limits.

#### 2. What’s the difference between “for sale” and “internet sale” in Brands?

**Q:** Which one should I use?\
**A:** `for sale` means Office only. `internet sale` means Web Booking only. Use `for sale + internet sale` if it should be bookable in both channels.

#### 3. Why does the product disappear when using Days Prices Option?

**Q:** I set a `Days Prices Option`, and now the extra gets removed.\
**A:** `Days Prices Option` only works for prices that have `days` defined. If none of the prices have `days`, the product is removed from the selection.

#### 4. How do I make an extra mandatory?

**Q:** I want it selected by default, and customers shouldn’t remove it.\
**A:** Enable `Autoselect in booking & offer`. Then enable `Unremovable On Web Booking` and/or `Unremovable On Customer Center`, depending on where it must be locked.

#### 5. What does “Include in basic price” actually do?

**Q:** Does it hide the extra or remove it?\
**A:** It hides the extra from the customer view in Web Booking and Customer Centre. It still increases the base price. It affects booking totals.

#### 6. Will “Currency Prices” update existing bookings?

**Q:** We changed currency rates. Will old bookings get updated?\
**A:** No. Currency price calculation affects new pricing logic. It does not update sales prices for existing bookings.

#### 7. Where does “Custom Text” appear?

**Q:** Who will see the name/description entered here?\
**A:** The `Description` text can be shown in Guest App and Guide App. It can also be used to control how the extra is presented in booking flows.

#### 8. What are SSR Codes used for?

**Q:** Why should I add an SSR code to an extra?\
**A:** If the extra is selected in a booking, the SSR code can be reported to the transport company. This creates an evidence trail for passenger requests.
