# System Setup

Applies for Administrator

The system setup should contain general settings for the Tourpaq system. The administrator only will be allowed to edit the current values of the settings. The delete of the rules will be made programmatically.

### General Information <a href="#general-information" id="general-information"></a>

* Payment Dashboard Overdue - number of days before a payment overdue booking is displayed on dashboard
* Upsale Days Before Departure - number of days before departure, the upsale tab is displayed on dashboard
* Payment reminder tolerance -
* Questionnaire percentage - minimum percentage of questionnaire respondants to consider the listed results reliable
* Questionnaire value
* Offer reminder days
* Hide prices - hides prices older than the inserted days period
* Hide filters - automatically hides transports, hotels and users that have allotments and information older than x days
* Locked bookings departure date - bookings made before this date will not be editable
* Show allotment control - Shows/hides the "All. per day" tab in Edit Hotel page
* Input payments type
* Export text format: this affects the format of the Payment registration export. Current options to choose from: C5(text) and NAV(CSV/Excel)
* Vouchers generation (number of days before departure)
* Retrive age from - the way pax age is set
* Financial Export e-mail address - address where the finacial export is sent (For the first activation of this feature, please contact us at [tourpaq.support@roweb.ro](mailto:tourpaq.support@roweb.ro). Also please set an Email template for Financial Export Email for at least one agency in your company)
* Default currency - used for the entire company
* PriceList GoUpPrice limit - the maximum number of times that the service is allowed to increase the price until the permission is required
* PriceList GoDownPrice limit - the maximum number of times that the service is allowed to decrease the price until the permission is required
* Photo upload notification URL
* Max. budget select offer
* Average hotel costs day numbers - the number of days used to calculate the average hotel costs value; this value will be compared with today's value
* Cost margin - difference used on dashboard
* Stop sale email - a new email will be sent to this address when a new stop sale is done
* Disable Room Edit Days - behavior available for web! Set to 0 to disable. Sets how many days before departure, the customer cannot edit the room choice anymore. Ex: If booking leave on 20.03 and this is set to 10, the customer can edit the room choice up to 10.03
* Ignore Transport Cost - ignore Transport Cost in Profit columns from Price List
* Reset Newsletter choice -the "Asked about the newsletter" option will be reset after X number of days
* Enable Checkbox on VAB - A Checkbox will appear on View All Bookings - they will be used to send email/SMS only towards the bookings that are checked
* Web Hook URL - A URL that is used for Web Hook Configurations that are enabled, set by the user on company, if this is empty Web Hooks will not work!

### Payment rate rules <a href="#payment-rate-rules" id="payment-rate-rules"></a>

These settings allow having a specific rate structure of existing booking orders. We can have a single rate payment for the entire booking amount, or up to three individual rates: deposit, second payment and rest of payment to allow the users a more relaxed payment plan.

Please see details on [Payment rate rules](https://docs.tourpaq.com/docs/documentation/payment-rate-rules)

### Radix Data <a href="#radix-data" id="radix-data"></a>

* Username
* Password
* TravelPortalName
* TravelPortalIATANumber
* TravelPortalBookingAgent
* TravelPortalBookingAgentPWD

Required for Radixx transport reporting.

### Currency <a href="#currency" id="currency"></a>

This is the currency conversion rate that will be set in the system. Set the currency of the system.

### Sms Configuration <a href="#sms-configuration" id="sms-configuration"></a>

#### **Twilio**

* Twilio Acccount Number
* Twilio Account Token
* Twilio Phone Number (E.164 Format)

#### **Mail Platform**

* Use Mail Platform
* User Name
* User Token
* Mail (Ex: @mail2sms.mailmailmail.net)
* Mail From (the mirror mail)

### Auto Europe <a href="#auto-europe" id="auto-europe"></a>

Autoeurope is a service provider for rent a car services.&#x20;

Tourpaq is integrated with this service in a way that it makes sense for Tourpaq application flow. The way this service is integrated with Tourpaq is via extras.&#x20;

To have access to Auto Europe provider, you need to contact Auto Europe to give you the credentials for login in the system.&#x20;

After you receive the credentials, you need to insert the username and the password into the fields and then contact the Tourpaq Support to activate the feature.&#x20;

### Hotel Providers

**Hotel Beds** is a bed bank provider.&#x20;

In order to start using this fture a company must set up hotel beds credentials in system setup, Hotel Beds tab. You need to contact the Hotel Beds to obtain the login details:&#x20;

* API Endpoint&#x20;
* Cache Endpoint&#x20;
* Image Endpoint&#x20;
* Small image Endpoint - this is used to display images on hotel import page.&#x20;
* API Key - this is provided by the Hotel Beds&#x20;
* API Secret - this is provided by the Hotel Beds&#x20;
* Facilities template - this is the template used by tourpaq.&#x20;

**Availpro** is a service provider for D-EDGE.&#x20;

To have acces to D-EDGE, you need first to contact Availpro for login credentials, then insert the username and password in Tourpaq System Setup menu, under Availpro tab.&#x20;

### **GDS Data**

* Currency
* User
* Password
* Branch
* Days number for ticketing (The number of days for ticketing after the reservation is made.)
* Max GDS search results (The maximum number of result return by the GDS search for the services.)
* Queue Number (The number of queue where we move the GDS bookings for ticketing.)
* Pseudo City Code
* Own Pseudo City Code
* Price change margin
* Fares Indicator
* Payment rule
* Card owner
* Card type
* Card number
* Expiration Data: Year and Month
* CVC
* Confirmation email (The email for the confirmations recieved from Travelport after booking.)
* Days number for check PNR (The number of days before departure for check PNR.)
* Show TicketNo on Ticket (Display the GDS ticketNumbers on the print ticket.)
* Time frame before departure (The number of minutes before the departure for remove a flight from booking.)
* Transport selection rule
* Use division PNR by classes (Use the division by classes for an optimal price)
* Don't update DTS on Create GDS Reservation (DTS is not included when GDS Reservation is created) - when reservations are created, DTS won't change it's amount.

### Inflight Service <a href="#inflight-service" id="inflight-service"></a>

* Username
* Password
* Host Adress
* File Prefix (This field indicates the name of the file before the date is added to the end. If left blank 'PassengerData\_' will be set by default. Full name example: PassengerData\_20140815)
* Folder (If the destination folder is not in the root directory you can specify an adress. Please use "/ /" as directory separators Ex Dir1 / / Dir2 / / Dir3 IMPORTANT:The folder structure must exist on the FTP Server)
* Port (If the FTP port is left blank, the default port number (21) will be autocompleted)
* Enabled (Check to enable Inflight Service. If disabled the files will not be generated nor sent)

Required for transport reporting.

### Firebase Config

To make the Firebase configuration from system setup menu, please contact Tourpaq Support to do the right settings for Firebase.

### Travel Lenghts

Travel length is used for Charter travel details, in select offer page.&#x20;

If the fields are left empty in system setup menu, by default the travel length is set to 7 days.&#x20;

In System setup menu / Travel length tab, you can set customizes trip intervals, inserting days from and days to.&#x20;

Click save to save the new interval.&#x20;

Now go to select offer page, reload the page. New travel length is available.&#x20;

Also if you want to add another travel interval

* &#x20;Click add
* Insert the new interval and&#x20;
* click save.&#x20;

Go again to select offer page , reload the page and now both intervals are shown.
