# Giftcards

This feature permits the customer to use a "bonus" code in order to receive a discount for the booking.

### **Giftcards Overview**

The **Giftcards** page provides an overview and management of all giftcards across brands.\
Each card contains key information related to its creation, usage, payment status, and visibility.

***

#### **Filter Options (Top Bar)**

<figure><img src=".gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

| **Field**           | **Description**                                                                                |
| ------------------- | ---------------------------------------------------------------------------------------------- |
| **Giftcard number** | Enter a specific card number to search for a particular gift card.                             |
| **Create user**     | Filters results by the user who created the gift card.                                         |
| **Create period**   | Defines the date range when the gift card was created.                                         |
| **Expire period**   | Defines the validity period of the gift card — cards expiring within this range will be shown. |
| **Show Hidden**     | When enabled, displays cards that are marked as hidden or inactive.                            |
| **Display**         | Adjusts the number of visible columns or data shown.                                           |
| **+ More Filters**  | Expands advanced filtering options                                                             |
|  **Clear**          | Resets all applied filters.                                                                    |

***

#### **Table Columns**

| **Column**              | **Description**                                                                                                                                                     |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Card No.**            | Unique number automatically assigned to each gift card.                                                                                                             |
| **Brand**               | Indicates which brand the card belongs to (e.g., _Tourpaq DK_).                                                                                                     |
| **Payer Email**         | Email address of the person who purchased or received the gift card.                                                                                                |
| **Payer Phone**         | Contact phone number of the payer.                                                                                                                                  |
| **Gift Receiver Email** | Email of the person receiving the gift card. The card and related details are sent to this address.                                                                 |
| **Create User**         | The user (usually an internal staff member) who created the gift card.                                                                                              |
| **Create Date**         | Date and time when the gift card was generated.                                                                                                                     |
| **Exp. Date**           | Expiration date — after this date, the card cannot be redeemed.                                                                                                     |
| **Code**                | Unique alphanumeric code used to redeem the gift card during booking or payment.                                                                                    |
| **Total Amount**        | Initial value of the gift card at creation.                                                                                                                         |
| **Remaining Amount**    | Current balance still available for use.                                                                                                                            |
| **Status**              | Indicates if the card is _Visible_ (available for use) or hidden.                                                                                                   |
| **Use on All Brands**   | Shows whether the card can be used across multiple brands. A red icon (✗) means it’s restricted to one brand; a green check (✓) means multi-brand usage is enabled. |
| **Is Paid**             | Indicates whether the payment for the gift card has been processed. Green check (✓) = paid; red cross (✗) = unpaid.                                                 |

***

#### **Buttons and Actions**

| **Button** | **Description**                                                 |
| ---------- | --------------------------------------------------------------- |
| **Create** | Opens the form to create a new gift card.                       |
| **Export** | Exports the list of visible gift cards to a file (e.g., Excel). |

***

#### **Additional Notes**

* Only **paid and visible** gift cards can be used by customers.
* Once redeemed, the **remaining amount** automatically updates.
* Expired gift cards will no longer appear as _Visible_ unless “Show Hidden” is selected.

### Feature activation <a href="#feature-activation" id="feature-activation"></a>

It can be activated by a Super Administrator.

After the activation, on Users -> Brands -> Edit Brand the Giftcard IDs interval should be completed.

<figure><img src=".gitbook/assets/image (21) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Giftcard creation <a href="#giftcard-creation" id="giftcard-creation"></a>

The giftcards sections are under the "Extras" menu.

Click on Create to create a gift card.&#x20;

<figure><img src=".gitbook/assets/image (14) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Select Brand for which the gift card exists.&#x20;
* Enter the payer email address - this is where the email with the gift card will be sent.&#x20;
* Payer phone - the phone of the customer that pays the giftcard. Optional, for internal information use, has no effect on the Giftcard.
* Gift card receiver email - the name of the customer that pays the giftcard. Optional, the name will appear in the email only if the email template has the \[CustomerName] variable.
* Expiration Date - the date when the giftcard will expire. It will no longer could be usable.
* Select the status of the gift card (visible or hidden).&#x20;
* Insert the amount on the gift card.&#x20;
* Used on all brands - if checked, the giftcard could be used between brands. Eg. A giftcard created on Primo Tours could be used on Arhus.
* Used Amount - the used amount from the giftcard.
* Created Date - the date when the giftcard was created.
* Is Paid - the payment status of the giftcard.
* Message field is the public one that will appear on the gift card. Example: Happy Birthday text.&#x20;
* The internal comment is only visible for Tourpaq admin users.&#x20;

Click on Save button.&#x20;

At this moment the gift card cannot be used even if appears on the system. Also, you cannot send the email to the receiver, because it is not paid yet. This is shown by this flag.&#x20;

<figure><img src=".gitbook/assets/image (16) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Click on Payments tab to pay the gift card.&#x20;

<figure><img src=".gitbook/assets/image (15) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* You can pay via bank payment method.&#x20;
* You can use the cash payment.&#x20;
* You can use the credit card to pay this gift card.&#x20;

The gift card appears as being paid, and it can be used for bookings in the office or web booking.

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Click on card preview, and you can see a PDF file with the card. It contains the gift card information, the amount, an informative text and a custom text.

<figure><img src=".gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
