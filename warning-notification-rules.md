# Warning notification rules

Can be accessed from **E-mail Setup / Warning Notification Rules**

This features allows the sending of warning emails or sms to a certain user according to a series of rules.

There are 3 tabs for the Feature:

* Warning Notification Rules
* Warning Contacts
* Warning Sent from E-mail

#### Warning Contacts <a href="#warning-contacts" id="warning-contacts"></a>

In here a user can be created that will receive the warning e-mails or SMS.

<figure><img src=".gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

#### Warning sent from e-mail <a href="#warning-sent-from-e-mail" id="warning-sent-from-e-mail"></a>

In here the sending e-mail address can be personalized. All e-mails will appear as sent from the address inserted.

<figure><img src=".gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

#### Warning Notification Rules <a href="#warning-notification-rules" id="warning-notification-rules"></a>

In here rules can be set for each user regarding what notification types he can receive.

<figure><img src=".gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>

The warnings are:

* Informational ->
* HotelReporting Service - Smtp Error -> Warns the user about an issue that has occured when sending an e-mail from Hotel Communication
* HotelReporting Service - Other Errors ->
* ExtraReporting Service - Smtp Error -> Warns the user about an issue that has occured when sending an e-mail from Extra Communication
* ExtraReporting Service - Other Errors ->
* TransportReporting Service - Ftp Error ->
* TransportReporting Service - Smtp Error -> Warns the user about an issue that has occured when sending an e-mail from Transport Communication
* TransportReporting Service - Other Errors ->
* Mailer Helper - Error ->
* Services Watcher - Warning ->
* Update GDS status from TKQ to TKOK Service -> Lets the user know that a GDS booking status has been changed from TKQ to TKOK
* Unable to configure GDS flight -> Warns about issues to a certain GDS transport when configuring flights
* Unable to check PNR -> Warns when the reservation to Travelport isn't found for the booking or something is wrong with the flights from Travelport
* Unable to change Time Changes -> Warns when flight changes weren't performed in Tourpaq for GDS bookings when flight times have been changed by Travelport
* ExtraSupplierReporting Service - Smtp Error -> Warns the user about an issue that has occured when sending an e-mail from Extra Supplier Communication
* ExtraSupplierReporting Service - Other Errors ->
* No Running GDS flights Service -> Warns about issues that prevented the Flight Configuration service from running the previous night for GDS transports
* Unable to submit WebBooking to Travelport -> Warns about issues when submitting GDS bookings created on webbooking to Traveport
* FewerGDSFlight -> When a Dynamic Transport has 10% less flights then the previous day, a warning is sent to inform the user that changes may have been made to the settings of the transport
* QueuemanagementGDS -> Lets the user know that there are GDS bookings that require attention due to time changes from Travelport
* Success to change Time Changes - Lets the user know that Flight Changes have been made by Travelport and they have been also made in Tourpaq
* Failed to sent email due to missing attachment -> Warns about emails containing tickets not beeing sent to guests due to missing files either from Ticket Attachments, extras, hotels or transports
* Unable to Generate Price List Per Day -> Warns about pricelists used for ALC settings not being created
* Success to submit WebBooking to Travelport ->Lets the user know that GDS bookings created from webbooking have been submitted to Travelport
* Bookings in Error Status -> Sends an e-mail containing bookings in error status if the bookings are in that status for more than 1 hour.
* Connected Hotel Error -> Sends an email if to contact assigned, if Error is thrown due to no response from D-Edge API. Every 6 hours, if no request is received from D-Edge and D-Edge API doesn't respond. Will be displayed also on Dashboard/Notification/Warnings
