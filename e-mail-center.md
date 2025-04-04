# E-mail center

Redundance with [Email Templates](email-templates.md)

Applies for Administrator

The Email Center should provide to the administrator the means of setting the templates for various emails that are sent by the Automated email notifications. A method of testing the email sending with a certain email template must be implemented.

The following is an extract of the information that should be available for each email type:

* the email address that sends the email;
* the email from(name) that send the message;
* activation status of the template;
* email subject;
* text editor that composes the content of the email and allows dynamic content to be placed inside through predefined constants.

**Here is a short description of each automatic email that the platform sends**

* **Thank you for booking**:
* **Reservation canceled**:
* **Payment preminder**:
* **Payment reminder**:
* **Booking canceled in 48 hours**:
* **Deposit received**
* **Insurance information missing**
* **Insurance information still missing**
* **Second payment received**
* **Full payment received**
* **Welcome home**
* **Reporting Schedule Communication**
* **Thank you for your LMS booking**
* **Booking updated**
* **Hotel release**
* **Flight Changes Email**
* **Welcome Home Reminder**
* **Seat Email Reminder**
* **Financial Export Email**
* **Questionnaire After Deposit Paid**
* **Wait list booking**
* **Vouchers Generated**
* **Attributes are missing**
* **Creditor Invoice**
* **Special offer Rejected**
* **Hotel Reporting**
* **Extras Reporting**
* **Supplier Extras Reporting**
* **Documents Uploaded**
* **Email sent from view all bookings**
* **Email sent from Customer Export**
* **Request more rooms**
* **Early booking rooming list**
* **Quotation list**
* **Stop sales introduction**
* **Extras Category Reporting**
* **Pending payment notification**: Sometimes DIBS needs more time to analyse the transaction and decide upon a status (\~2-24-72 hours). The customer will receive this email informing that we must wait for a status on the payment.
* **Captured money but no allotment**: Sometimes two customers compete for a last allotment, both in DIBS payment pages, one faster taking it and the slower one also successfully paying but no allotment being available anymore. This email informs on what has happened and that, most probbably, a refund will occur soon.
