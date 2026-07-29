# Giftcards

## Giftcards

Giftcards let customers use a code to receive a booking discount.

### Overview

The **Giftcards** page provides an overview and management of all giftcards across brands.\
Each card contains key information related to its creation, usage, payment status, and visibility.

#### Filter options

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (10) (2).png" alt="Giftcards filter options"><figcaption></figcaption></figure></div>

| **Field**           | **Description**                                                                              |
| ------------------- | -------------------------------------------------------------------------------------------- |
| **Giftcard number** | Enter a specific card number to search for a particular gift card.                           |
| **Create user**     | Filters results by the user who created the gift card.                                       |
| **Create period**   | Defines the date range when the gift card was created.                                       |
| **Expire period**   | Defines the validity period of the gift card—cards expiring within this range will be shown. |
| **Show Hidden**     | When enabled, displays cards that are marked as hidden or inactive.                          |
| **Display**         | Adjusts the number of visible columns or data shown.                                         |
| **+ More Filters**  | Expands advanced filtering options                                                           |
| **Clear**           | Resets all applied filters.                                                                  |

#### Table columns

| **Column**              | **Description**                                                                                                                                                     |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Card No.**            | Unique number automatically assigned to each gift card.                                                                                                             |
| **Brand**               | Indicates which brand the card belongs to (e.g., _Tourpaq DK_).                                                                                                     |
| **Payer Email**         | Email address of the person who purchased or received the gift card.                                                                                                |
| **Payer Phone**         | Contact phone number of the payer.                                                                                                                                  |
| **Gift Receiver Email** | Email of the person receiving the gift card. The card and related details are sent to this address.                                                                 |
| **Create User**         | The user (usually an internal staff member) who created the gift card.                                                                                              |
| **Create Date**         | Date and time when the gift card was generated.                                                                                                                     |
| **Exp. Date**           | Expiration date—after this date, the card cannot be redeemed.                                                                                                       |
| **Code**                | Unique alphanumeric code used to redeem the gift card during booking or payment.                                                                                    |
| **Total Amount**        | Initial value of the gift card at creation.                                                                                                                         |
| **Remaining Amount**    | Current balance still available for use.                                                                                                                            |
| **Status**              | Indicates if the card is _Visible_ (available for use) or hidden.                                                                                                   |
| **Use on All Brands**   | Shows whether the card can be used across multiple brands. A red icon (✗) means it’s restricted to one brand; a green check (✓) means multi-brand usage is enabled. |
| **Is Paid**             | Indicates whether the payment for the gift card has been processed. Green check (✓) = paid; red cross (✗) = unpaid.                                                 |

#### Buttons and actions

| **Button** | **Description**                                                 |
| ---------- | --------------------------------------------------------------- |
| **Create** | Opens the form to create a new gift card.                       |
| **Export** | Exports the list of visible gift cards to a file (e.g., Excel). |

#### System behavior

* Only **paid and visible** gift cards can be used by customers.
* Once redeemed, the **remaining amount** automatically updates.
* Expired gift cards will no longer appear as _Visible_ unless “Show Hidden” is selected.

### Requirements

* Super Administrator access activates Giftcards.
* A brand needs a configured Giftcard ID interval.

### Feature activation <a href="#feature-activation" id="feature-activation"></a>

Activate Giftcards with Super Administrator access.

In **Users → Brands → Edit Brand**, complete the Giftcard ID interval.

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (21) (1) (1) (1).png" alt="Edit Brand Giftcard ID interval"><figcaption></figcaption></figure></div>

### Create a Giftcard <a href="#giftcard-creation" id="giftcard-creation"></a>

Giftcards are available under the **Extras** menu.

Click **Create** to add a giftcard.

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (14) (1) (1) (1) (1) (1).png" alt="Create Giftcard page"><figcaption></figcaption></figure></div>

#### Field descriptions

* **Brand** - Select the brand for the Giftcard.
* **Payer Email** - Enter the address that receives the Giftcard email.
* **Payer Phone** - Optionally record the payer's phone number. This field supports internal information only.
* **Gift Receiver Email** - Optionally enter the recipient's email address. The email template can use the `[CustomerName]` variable.
* **Expiration Date** - Set the date when the Giftcard expires. Expired Giftcards cannot be used.
* **Status** - Select **Visible** or **Hidden**.
* **Amount** - Enter the Giftcard amount.
* **Used on all brands** - Allow the Giftcard to be used across brands.
* **Used Amount** - Shows the amount already used from the Giftcard.
* **Created Date** - Shows when the Giftcard was created.
* **Is Paid** - Shows the Giftcard payment status.
* **Message** - Enter the public message displayed on the Giftcard.
* **Internal comment** - Enter a comment visible only to Tourpaq administrators.

Click **Save**.

An unpaid giftcard cannot be used or sent to the receiver. The payment flag shows this status.

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (16) (1) (1) (1) (1) (1).png" alt="Unpaid Giftcard status"><figcaption></figcaption></figure></div>

#### Record payment

In the **Payments** tab, record the giftcard payment.

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (15) (1) (1) (1) (1) (1).png" alt="Giftcard Payments tab"><figcaption></figcaption></figure></div>

Use one of these payment methods:

* Bank payment.
* Cash payment.
* Credit card.

The paid giftcard can be used for Office and Web Booking reservations.

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (57).png" alt="Paid Giftcard status"><figcaption></figcaption></figure></div>

#### Preview Giftcard

Click **Card preview** to open the giftcard PDF. The PDF includes the giftcard details, amount, informative text, and custom text.

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Giftcard PDF preview"><figcaption></figcaption></figure></div>
