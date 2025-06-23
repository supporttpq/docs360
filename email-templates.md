# Email Templates

Applies for Administrator

The Email Center provides the administrator the means of setting the templates for various emails that can be sent from Tourpaq.

The following is an extract of the information that is available for each email type:

* the email address that sends the email;
* the email from(name) that send the message;
* activation status of the template;
* email subject;
* text editor that composes the content of the email and allows dynamic content to be placed inside through predefined constants.

Most email templates are automatically sent by the system if certain conditions are met.

The //Automated email notifications// service is intended to automatically send the emails defined in E-mail center section to the customers, hotel suppliers, or transport providers.

The service is able to execute the following actions:

* Select the e-mails that should be sent
* Send them

Note: If the customer’s email si not filled in, the email cannot be sent.

**1. Thank you for booking**

This e-mail is sent to the customer after a booking is made. E-ticket is attached. The conditions that must be fulfilled by a booking in order to be sent are:

* The e-mail should have not been sent before to the customer
* The booking’s status must be ok
* The booking must not be a last minute booking
* If the booking is made through the Web Booking component of Tourpaq, the email must be sent with a small delay(as the customers should have time to finish the process of making a booking)
* Departure date must not be in the past

**2. Reservation cancelled**

This e-mail is sent to the customer after a booking is cancelled. E-ticket is attached. The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should have not been sent before to the customer
* The booking’s status must be cancelled
* Departure date must not be in the past

**3. Payment preminder**

This e-mail is sent with 3 days before payment due date and not earlier than day after booking. Hash-key-link to credit card payment is sent – no login is required. The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should have not been sent before to the customer
* The booking’s status is ok
* The booking must not be a last minute booking
* Departure date must not be in the past
* Second payment or Rest of payment rates are not paid

**4. Payment reminder**

This e-mail is sent 3 days after payment due date. The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should have not been sent before to the customer
* The booking’s status must be ok
* The booking must not be a last booking minute
* Departure date must not be in the past
* The rest of money the customer needs to pay for any of the payment rates must be greater than a tolerance amount established from System setup

**5. Booking cancelled in 48 hours**

This e-mail is sent to all bookings with missing payments and outstanding balances on due date + 7. The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should have not been sent before to the customer
* The booking’s status must be ok
* The booking must not be a last booking minute
* Departure date must not be in the past
* Deposit, Second payment or Rest of payment rates are not paid

**6. Deposit received**

This e-mail is sent to all bookings for which the deposit has been paid(Deposit has to be greater than 0). The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should not have been sent before to the customer
* The booking’s status must be ok
* The booking must not be a last minute booking
* Departure date must not be in the past

**7. Insurance information missing**

This e-mail is sent 14 days after booking has been made to all the bookings with no insurance and no insurance information. Hash-key-link to passenger details page must be sent – no login required. The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should not have been sent before to the customer
* The booking’s status is ok
* The booking must not be a last minute booking
* Departure date must not be in the past

**8. Insurance information still missing**

This e-mail should be sent 10 days after Insurance information missing mail has been sent if insurance information is still missing. E-ticket is attached. The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should not have been sent before to the customer
* The booking’s status is ok
* The booking must not be a last minute booking
* Departure date must not be in the past
* Insurance information missing e-mail has been sent

**9. Second payment received**

This e-mail is sent automatically to all bookings for which the second payment rate has been paid(Second payment must be greater than 0). The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should not have been sent before to the customer
* The booking’s status must be ok
* The booking must not be a last minute booking
* Departure date must not be in the past

**10. Full payment received**

This e-mail is sent automatically to all bookings for which the Rest of payment rate has been paid(Rest ofpayment must be greater than 0). The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should not have been sent before to the customer
* The booking’s status must be ok
* The booking must not be a last minute booking
* Departure date must not be in the past

**11. Welcome home**

This e-mail should be sent one day after return day to all passengers. Hash-key-link to questionnaire page must be sent – no login required. The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should not have been sent before to the customer
* The booking’s status must be ok
* Departure date must not be in the past

**12. Reporting Schedule Communication**

This e-mail is sent automatically by Transport passenger automate reporting service(for more details please refer to Transport passenger automate reporting specification)

**13. Thank you for your LMS booking**

This e-mail is sent automatically to the last minute bookings. E-ticket is attached. The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should not have been sent before to the customer
* The booking’s status must be ok
* Departure date must not be in the past

If the booking is not fully paid, payment preminder body text must be added to the e-mail with has-key-link to credit card. If it has been paid, payment confirmation must be added. Insurance information body must be added if necessary.

**14. Booking updated**

This e-mail is sent when a change is made to a booking. \ Especially the changes that imply a booking total value update, adding a product, changing the passenger distribution in rooms etc. (For instance, if only editing passengers and updating their age/Date of birth, without having impact on product selection, the email will not be sent, even if the booking version also increases.)\ The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should have not been sent before
* The booking’s status must be ok
* Departure date must not be in the past

**15. Hotel release**

This e-mail is sent automatically by Hotel release automation service(for more details please refer to Hotel release automation specification)

**16. Flight Changes**

This e-mail is sent to the customer when a flight change is made. The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should have not been sent before
* The booking’s status must be ok
* Departure date must not be in the past

**17. Welcome Home Reminder**

This e-mail is sent one week after return day if at least one passenger from the booking hasn’t filled in the questionnaire. Hash-key-link to questionnaire page is sent – no login required. The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail should not have been sent before to the customer
* The booking’s status must be ok
* Departure date must not be in the past

**18. Seat Email Reminder**

This e-mail is sent to the customer with 60 days before departure to announce him that the seats can be reserved from the transport. If there are less than 60 days and more than 1 day to departure, e-mail should be sent 12 hours after booking is made. The conditions that must be fulfilled by a booking in order to be selected are:

* The e-mail has not been sent before
* The booking’s status must be ok
* Departure date must not be in the past

**19. Financial Export**

This email is sent according to settings made for each agency of the company and contains information about bookings made in a specific interval.

**20. Questionnaire After Deposit Paid**

This email is sent after the customer has paid the deposit. The conditions that must be fulfilled by a booking in order to be selected are:

* booking is departing in future
* booking is OK
* e-mail has not been sent yet
* //Thank you for booking// email sent
* deposit has been FULLY paid in the last 24hrs

**21. Wait list booking**

This e-mail is sent when the allotment has been fully booked, but the company/agency allows more bookings to be made on it without allotment in the hope of getting more allotment from the hotel. The conditions that must be fulfilled by a booking in order to be selected are:

* booking departs in the future
* email has not been already sent
* booking is WaitList
* booking update is older than 20 minutes (for webbooking)

**22. Vouchers Generated**

This email is sent after the Vouchers for a booking have been generated. The conditions that must be fulfilled by a booking in order to be selected are:

* booking departs in the future
* this kind of mail is not already sent
* booking is OK
* date is close to departure (set in system setup)
* product attributes have been set

**23. Attributes are missing**

This email is sent when the guest haven't filled in all attributes required by a booked product. The conditions that must be fulfilled by a booking in order to be selected are:

* booking departs in future
* such email has not been sent
* booking is fully paid
* there are less than 30 days left till departure

**24. Creditor Invoice**

This e-mail is sent to creditors and contains financial information regarding hotels and products assigned to the creditor.

**25. Hotel Reporting**

This e-mail is send based on intervals set in the Communication tab of the hotel, information in the file is filtered based on the selected options.

**26. Extras Reporting**

This e-mail is send based on intervals set in the Communication tab of the extra, information in the file is filtered based on the selected options.

**27. Supplier Extras Reporting**

This e-mail is send based on intervals set in the supplier, information in the file is filtered based on the selected options.

**28. Documents Uploaded**

This e-mail is sent to all eligible bookings when a document is uploaded for a transport, hotel or product. The conditions that must be fulfilled by a booking in order to be selected are:

* booking departs in the future

**29. Email sent from view all bookings**

This email can be sent by an admin or seller from View all Bookings tab of the system to the bookings displayed according to the filters set. It is mostly used to inform customers of changes or promotions.

**30. Email sent from Customer Export**

This email can be sent by an admin or seller from Customer Export part of the system to all bookings displayed according to the filters set. It is mostly used to inform customers of promotions.

**31. Request more rooms**

This e-mail can be sent from **Dashboard** to hotels when more rooms are required. It becomes available to be sent when there are no more free rooms of a type in the hotel.

**32. Early booking rooming list**

There are 2 e-mails sent in this case according to the settings made by the user in the hotel:

* an e-mail containing a rooming list to the supplier
* an invoice with financial to the creditor

**33. Extras Category Reporting**

This e-mail is send based on intervals set in the Communication tab of the extra category, information in the file is filtered based on the selected options.

**34. Pending payment notification**

Sometimes DIBS needs more time to analyse the transaction and decide upon a status (\~2-24-72 hours). The customer will receive this email informing that we must wait for a status on the payment.

**35. Captured money but no allotment**

Sometimes two customers compete for a last allotment, both in DIBS payment pages, one faster taking it and the slower one also successfully paying but no allotment being available anymore. This email informs on what has happened and that, most probbably, a refund will occur soon.

**36. Individual Payment Email**

This e-mail is sent from the booking page to all passengers that have their email submited. A link is sent in the email, directing the customers to a separate customer center where they can pay their passenger total.

**37. Destination Email**

This e-mail is used to define a template for the Destination or Guest app mobile app. It can be used in the app in multiple ways:

* Order - type of e-mail or SMS message sent after the customer books an excursion
* Excursion - type of e-mail or SMS message sent to the customers that booked a specific excursion
* Arrival - type of e-mail or SMS messages sent to the customers that arrived / will arrive at the hotel on a specific date
* Hotel - type of e-mail or SMS messages sent to the customers that are staying at a specific hotel

**38. Hotel Contract**

This e-mail is sent to the suppliers e-mail adress or other e-mail adresses with the contact attached and a link through which the contract can be aproved or rejected

**Email template with ticket attachment:**

\*Thank you for booking \*Reservation canceled \*Insurance information still missing \*Full payment received \*Thank you for your LMS booking \*Booking updated \*Flight Changes Email \*Wait list booking

**39. Product Reservation Email**

This e-mail is sent to the passenger that bought a parking extra.

**When should it be sent?**

* Booking is fully paid
* Must be successfully reported to APCOA
* Latest report to APCOA is made more than 20 min
* Parking extra to be booked
* VRN to be completed
* 30 days before departure

40. **Special Offer Rejected** &#x20;

This email is sent when a hotel's special offer is rejected, from the Notifications menu.

41. **Quotation list**

A quotation list email is a message containing a detailed list of products or services with their respective prices, quantities, and terms, sent to a potential customer. It's used to provide a comprehensive overview of the pricing and details of a potential purchase, helping the customer make an informed decisio

42. **Stop sales introduction**&#x20;

This email is sent when a new stop sale is created.

43. **Mail Platform for SmS**
44. **Dynamic Email / SMS**&#x20;

It can be used to notify the guests of their departure date, to welcome them to the trip location, to welcome them home, to make them aware of certain products they can book etc.

45. **Confirmation Hotel**&#x20;

&#x20;A hotel confirmation email acknowledges a reservation, providing essential details like dates, room type, and booking number. It also includes the hotel's address, contact information, payment status, and any relevant policies.&#x20;

Alongside the e-mail template, a Hotel Confirmation e-mail will also need the following in order to work properly:

* **Supplier** selected for the hotel
* **Reservation Dept Email** field filled in the hotel
* **Contract type** of the hotel to be set as either **Allotment** or **Request**

**!!! If the hotel doesn't have the Reservation Dept Email field filled, the e-mail will be not be sent**

46. **Confirmation Transfer**

&#x20;An email sent to verify and confirm the details of a scheduled transfer, such as the movement of a person, item, or service from one location to another. It typically includes information like the date, time, locations, names involved, and any relevant logistical or contact details. This type of email serves to ensure mutual understanding and agreement between the involved parties.

To set up the **Transfer Confirmation email** the required settings are:

* An extra that will act as transfer
* Supplier for the extra
* **Contract type** must be **Allotment** or **Request**
* Category type has to be Transfer

47. **Seats vs. Beds Reporting**

This email is sent according to a scheduler set on communication. Attached to this email is a Seats vs beds report.

48. **Giftcard Email**

This email is sent automatically after the Giftcard is paid.

49. **Time Share fee created notification**

<mark style="color:red;">No longer used.</mark>

50. **Select offer SMS**

This SMS is sent to inform  the customer about the offer that he requested. It is sent manually, and can contain a personalized message set in in the Brands menu / Select Offer.

51. **Time share fee reminder**

<mark style="color:red;">No longer used</mark>

52. **Time share fee preminder**

<mark style="color:red;">No longer used</mark>

53. **Car Registration**

This email is sent to passengers who have a product with the attribute "car registration"

54. **Full Individual Payment Received**

**This email is sent when the passengr made a full ammount paid by "Individual payment"**

55. **Deposit received per passenger**

**This email is sent when the deposit is paid by "Individual payment"**

**New Variables that work ONLY on this template.**

* \[ConfirmationCode] - Confirmation code from APCOA
* \[CarRegistration] - Car licence plate
* \[Product] - Product name
* \[EntryDateTime] - Entry date will be calculated as Departure date - 2h
* \[ExitDateTime] - Exit date will be calculated as Departure date + 1h
