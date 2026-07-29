# Overview

Applies to Administrator

Extras are optional services/products that a customer can book; like transfer, catering, pension, rental car, etc. This page allows users to create and configure various extras that can be associated with bookings or transport options.

### Brands

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Brands settings for an Extra."><figcaption></figcaption></figure></div>

Allow the user to assign an extra to an agency. An extra can be assigned as follow:

* not assigned
* for sale - the extra can be booked only on office;
* internet sale - the extra can be booked only on WB
* for sale + internet sale - can be booked both, office and WB
* guide sale - can be booked only by a guide agent
* hotel sale - can be set only by a hotel agent
* guide sale + internet sale + for sale - can be booked by a admin, guide or a WB

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (571).png" alt="Brand assignment settings for an Extra."><figcaption></figcaption></figure></div>

### Overview

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
| **Extras Category**         | Categorize the extra (e.g., Meal, Transfer, Tour). The user can choose from the dropdown one of the categories created in the Extras Category. This is required.                                                                                                                                                                                                                                                                              |
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

### Custom text

Used to customize the appearance and description of the extra in booking flows or documentation.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (442).png" alt="Custom Text settings for an Extra."><figcaption></figcaption></figure></div>

| Field           | Description                                                                                                                |
| --------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Name**        | Custom label to override the default extra name.                                                                           |
| **Description** | Rich text editor for detailed descriptions, highlights, or disclaimers. This text can be found in Guest APP and Guide APP. |

### Automatic billing

Allows integration with internal billing and accounting systems for accurate cost tracking and supplier payouts.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (443).png" alt="Automatic Billing settings for an Extra."><figcaption></figcaption></figure></div>

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

### Golf course

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (602).png" alt="Golf course settings for an Extra."><figcaption></figcaption></figure></div>

This section is shown **only when an Extra is configured with the type&#x20;**_**Golf**_.\
If the Extra has a different type, this section is not displayed.

#### Rounds

Defines how many golf rounds are included in this extra.

* Numeric value
* Represents the maximum number of rounds for one booking. Valid number are 1 to 99
* Used by the system when calculating and validating the golf product in the booking

Example:\
If **Rounds = 5**, the guest is entitled to five rounds of golf.

#### Product Parent ID

Internal identifier that links this golf extra to its parent product in Tourpaq.

* Used internally by the system to connect related products
* Fill Product ID when you want to use genarated allotment from another Product.

#### Important

These fields are **only relevant for Extras of type Golf** and are ignored for all other Extra types.

### Behaviour settings

These settings control how the extra behaves in the booking process and what logic or restrictions apply to its use.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Behaviour settings for an Extra."><figcaption></figcaption></figure></div>

<table><thead><tr><th width="307.3333740234375">Setting</th><th>Description</th></tr></thead><tbody><tr><td><strong>Autoselect in booking &#x26; offer</strong></td><td>Automatically selects this extra during booking and in special offers. Useful for mandatory or strongly recommended extras. The product will already be selected by default in a new booking. When using this feature, please make sure the product does not have a discount linked to it.</td></tr><tr><td><strong>Unremovable On Web Booking</strong></td><td>Prevents customers from removing the extra themselves during online booking. Ideal for required services.</td></tr><tr><td><strong>Unremovable On Customer Center</strong></td><td>Prevents removal by users in the customer self-service portal.</td></tr><tr><td><strong>Add price to deposit</strong></td><td>Includes the price of this extra in the booking deposit calculation.</td></tr><tr><td><strong>Include in basic price</strong></td><td>If checked, this will include the price of the extra in the basic prices of the booking.<br>This is often used in combination with "Autoselect in booking &#x26; offer.</td></tr><tr><td><strong>Add On All Pax</strong></td><td>If selected for one passenger in webbooking, the product will be automatically selected for all eligible pax of the booking; If removed, will be removed from all.</td></tr><tr><td><strong>Add only one per room</strong></td><td>Limits the extra to one per room regardless of the number of passengers.</td></tr><tr><td><strong>Available to book (API)</strong></td><td>Check whether a product should be shown as available to book in the Offer API, without adding it to the total.</td></tr></tbody></table>

***

### Other settings

These settings influence how the extra interacts with billing, privacy regulations, and system integrations.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (445).png" alt="Other settings for an Extra."><figcaption></figcaption></figure></div>

| Setting                      | Description                                                                                                                                |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **Issue Voucher**            | Enables the generation of a voucher for the extra.                                                                                         |
| **GDPR Sensitive**           | Flags the extra as containing GDPR-relevant data. Triggers data protection measures.                                                       |
| **Content Type**             | Used to classify the extra as a specific content asset, useful in API or content-driven environments.                                      |
| **Package Type**             | Treats the extra as a package rather than a standalone item. May impact how it's displayed or billed. Activate the Package Content tab     |
| **Use Stay Dates in Prices** | Prices are calculated based on the customer’s actual stay dates rather than fixed pricing. Helpful for seasonal or dynamic pricing models. |

***

### Board supplement

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (10) (3).png" alt="Board Supplement settings for an Extra."><figcaption></figcaption></figure></div>

{% hint style="info" %}
The Board Supplement section is displayed only for Extras that belong to an Extras Category of type _Pension_. If the selected Extras Category has any other type, this section is hidden.
{% endhint %}

#### Field descriptions

**Board type**

Dropdown field that defines the target board for this supplement.

Example:

* HB – Half Board

The Board type is used by Tourpaq to determine the Board type of the Extra. This is used to match the extra to the relevant Board type on the web and when it is necessary to upgrade a Board basis (when the Board basis is not available for the full stay).

{% hint style="warning" %}
It is recommended to set the Board type for all Board Basis and Board Supplement extras.
{% endhint %}

**Board basis filter**

The Board basis filter is used to limit the Extras eligibility to rooms that have the specified Board Type as the Board basis.

Example for a Board basis Extra:

A hotel offers different Board Basis options depending on the season:

* **Low season:** Breakfast
* **High season:** Half Board

These meal plans are configured as separate **Board Basis Extras**.

The **Board Basis Filter** determines when each Extra is eligible. For example, the **Breakfast** Board Basis Extra has the **Board Basis Filter** set to **Breakfast**, making it available only during periods where the room's Board Basis is configured as **Breakfast**. During periods where the room's Board Basis is **Half Board**, the Breakfast Extra is not offered.

This ensures that customers are only presented with the Board Basis that matches the room configuration for the selected travel period.

Example with Board supplement:

A hotel offers two different Board Basis options during the same travel period:

* **Breakfast**
* **Half Board**

Customers can upgrade either option to **All Inclusive**, but the upgrade price differs depending on the room's included Board Basis.

To support this scenario, create two separate **Board Supplement Extras**:

* The first Board Supplement will set the _Board basis filter_ to Breakfast to limit it to rooms with Breakfast as their board basis.
* The second Board supplement will have the _Board basis filter_ set to Half board, to limit it to rooms with Half board as their Board basis.

Using separate Board Supplement Extras with different **Board Basis Filters** ensures that Tourpaq displays the correct upgrade option and price based on the room's configured Board Basis.

### Clone extras

The **Clone** functionality allows you to duplicate an existing extra configuration and reuse it for another product, period, or brand.

Instead of creating a new extra from scratch, cloning copies:

* Core configuration (Overview, Basic Setup)
* Prices
* Allotment
* Resources

This reduces manual work and ensures consistency across products.

{% hint style="info" %}
After cloning has been done, the new extra must be reassigned to a Brand and the rest of the settings that were not cloned must be redone.
{% endhint %}

The Clone Extras feature is used to:

* Create similar extras quickly
* Reuse seasonal configurations
* Copy extras to another accommodation
* Duplicate pricing structures
* Maintain standardized setup across brands

#### How to clone an Extra

1\. Locate the Existing Extra - Navigate to: Extras → Search → Open the extra you want to duplicate.

2.  Click “Clone” - Select the **Clone** option

    <div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Clone option for an Extra."><figcaption></figcaption></figure></div>
3.  Select the code for the new Extras

    <div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Code selection for a cloned Extra."><figcaption></figcaption></figure></div>
4.  Define Clone Settings

    <div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Clone settings for an Extra."><figcaption></figcaption></figure></div>

You need to:

* Enter a new Name
* Assign to another category
* Adjust validity dates
* Update brand assignment
* Modify price if needed

4. Save - Confirm creation of the cloned extra.
5. Review Configuration

Important:

* Verify pricing
* Check validity dates
* Confirm category
* Test booking flow
* Review communication rules
