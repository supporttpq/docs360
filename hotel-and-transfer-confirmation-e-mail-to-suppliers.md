# Hotel and transfer confirmation e-mail to suppliers

This feature allows the sending of confirmation e-mails to suppliers if they need to confirm the reservation of rooms and products for bookings.

It uses [Dynamic E-mail/SMS Center](email-setup/page-14/), as a special e-mail template is required.

E-mails can be sent from the booking, if confirmation is necessary. A button named **Send Confirmation** will appear on the booking if the action is required.

<figure><img src=".gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Setting up Confirmation E-mails <a href="#setting-up-confirmation-e-mails" id="setting-up-confirmation-e-mails"></a>

Confirmation e-mails can be set up from [Dynamic E-mail/SMS Center](email-setup/page-14/) by using one of the two available confirmation e-mail types:

* Confirmation Transfer
* Confirmation Hotel

The template has to be active and a **Subject** and **Body** is required, so the supplier would understand the e-mail.

Other required fields are:

* From name
* From e-mail
* Reply to

<figure><img src=".gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

In the e-mail, a link will be also sent to allow the supplier to confirm or reject the booking. This link is hardcoded and updated in real time.

Ex: If a confirmation e-mail is sent to a booking with 4 pax and one is cancelled before the supplier can confirm, when he will click on the link, only 3 pax will be displayed.

### Hotel Confirmation requirements <a href="#hotel-confirmation-requirements" id="hotel-confirmation-requirements"></a>

Alongside the e-mail template, a Hotel Confirmation e-mail will also need the following in order to work properly:

* **Supplier** selected for the hotel
* **Reservation Dept Email** field filled in the hotel
* **Contract type** of the hotel to be set as either **Allotment** or **Request**

<figure><img src=".gitbook/assets/image (15) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<mark style="color:red;">**!!! If the hotel doesn't have the Reservation Dept Email field filled, the e-mail will be not be sent**</mark>

### Transfer Confirmation requirements <a href="#transfer-confirmation-requirements" id="transfer-confirmation-requirements"></a>

To set up the **Transfer Confirmation email** the required settings are:

* An extra that will act as transfer
* Supplier for the extra
* **Contract type** must be **Allotment** or **Request**
* Category type has to be Transfer

<figure><img src=".gitbook/assets/image (16) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (17) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Suppliers <a href="#suppliers" id="suppliers"></a>

In order for the confirmation e-mails for transfer to be sent, a new field has been created for Suppliers, named **Reservation Dept Email**. This field is required.

<figure><img src=".gitbook/assets/image (18) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
