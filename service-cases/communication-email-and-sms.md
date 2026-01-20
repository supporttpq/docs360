# Communication (Email & SMS)

#### **Overview**

Communication between the agency and the customer regarding service cases can be conducted via **Email** or **SMS**.\
Dedicated buttons on the **service case editing page** provide direct access to these tools, allowing messages to be sent and received while maintaining a full history in the service case.

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **SMS Communication**

**Requirements:**

* **SMS integration** must be enabled for the company via **Feature Access** by a super admin.
* Complete the required configuration in the **SMS Configuration** tab under **System Setup**.
* The **SMS Service** must be activated by a super admin.

**Functionality:**

* The SMS tool opens a **chat-style dialog**, where users can:
  * Send messages directly to the customer using the phone number saved in the service case.
  * View customer replies in the same chat interface.
* All messages exchanged via SMS are automatically linked to the service case.

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Email Communication**

**Requirements:**

* A **MailBee license key** must be purchased from: [MailBee Email Components](https://afterlogic.com/mailbee-net/email-components).
* The **MailBee Platform service** must be activated by a super admin for each brand.
* Complete the setup by going to: **Users → Brands → Edit → Service Case Tab**, and fill in the required information.

<figure><img src="../.gitbook/assets/image (236).png" alt=""><figcaption></figcaption></figure>

“Send Mail” button will open the E-mail overview dialog. From here, the user can send an email directly to the customer, as from the agency’s dedicated email address, set in Brands / Service case tab.

<figure><img src="../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Replies from customer will be automatically displayed in the same dialog.

If you need to get a certain email, to this email overview, just copy the service case key and include it in the email that you will forward to the agency’s email set for service case.

<figure><img src="../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

All files that the customer will attach to an email sent, will be saved in the attachments section of the service case.

<figure><img src="../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Usage Notes**

* SMS and Email communications are fully integrated into the service case, providing a complete history for tracking and reporting.
* Ensure all required setup steps are completed for SMS or Email functionality before attempting to send messages.
* Attachments sent via email are automatically saved, eliminating the need for separate uploads.
