# GDPR (General Data Protection Regulation)

GDPR is a regulation in EU law on data protection and privacy for all individuals within the European Union (EU) and the European Economic Area (EEA). It also addresses the export of personal data. The Tourpaq system complies with this regulation, and the procedure of storing personal data is no longer valid. In the context of the Tourpaq system, this is done with a focus on customers **which had returned home from a trip since several days, which is configurable in the system**, \*\*if they do not have other bookings planned \*\* and also if **the customer has the newsletter option unchecked** in the Customer details window.

So, for a certain customer which fulfills those conditions, the anonymisation can be performed automatically by running the service. Customers can be anonymized also instantly, in "Customer Center" by hitting the "Anonymize" button if **customer does not have active bookings in the future**. For using the anonymization functionality, an user with sysadmin role must be used.

### Continuous deletion <a href="#continuous-deletion" id="continuous-deletion"></a>

This service can be used by a user with sysadmin rights. When this type of user is logged into Tourpaq, the **GDPR** Continuous Deletion settings can be accessed from the **Setup** menu:

<figure><img src=".gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

GDPR- Continuous Deletion service settings allows to be activated in different ways depending on which information related to customer is needed to be anonymized. Settings below are relevant only when continuous deletion is choosed.

#### **Activate continous deletion for customers that had returned home for more than the number of days set**

Customers that had returned home and do not have other bookings in the future will be anonymized automatically by the service. This setting can be used also individually, as other settings below GDPR. When customer is anonymized, relevant data linked to him is removed or replaced with predefined text to suggest that he was anonymized. Related to a booking of a customer anonymized, following data will be affected:

* **Customer details** name, address (country and zip code are not replaced), e-mail, phone, secondary data from a customer is removed, customer details in customer center are changed also.
* **Passenger details** name, passport no., nationality, insurance company, insurance police no., country, zipcode, city, address, transport comments, early startdate Gouda insurance, emergency contacts. Names are changed also in the booking overview.
* **Emails or SMS** shown on the booking, in E-mails or SMS tab are deleted. The e-mail addresses are anonymized, this meaning that real e-mail addresses are replaced with addresses containg "Anonymized" word in it.
* **Comments** shown on the booking are are deleted. In the comment boxes "Anonymized" word is placed in order to inform the user that this part was also anonymized.
* **SSR** codes shown on the booking, if are selected, are removed after anonymization
* **Profit** details are affected and the passenger names for which profit and cost is detailed are not displayed anymore.
* **Transport seating** is also affected for a booking, the passenger real names are not shown when hovering with mouse over. Anonymized names are displayed.
* **Tee times** is affected for a booking and it will not display the passenger real names. Anonymized names are shown.
* **Payment type** for a booking of an anonymized customer will replace the payment type wity "GDPR Sensitive" text for users logged with other account than "Administrator" or "Financial". Before anonymization, the Payment type should be marked as GDPR Sensitive from "Method of Payment":

<figure><img src=".gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

* **Extras, discounts or supplements marked as highly sensitive** are also anonymized. For extras:

<figure><img src=".gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

* for discounts and supplements

<figure><img src=".gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

When extras marked as highly sensitive are assigned to a passenger, after customer anonymization, in the booking overview new category called "GDPR Sensitive" will be created and will include the products marked are sensitive which were assigned for passengers.

When discounts or supplements marked as highly sensitive are assigned to a passenger anonymized, those are shown are GDPR Sensitive in the passengers grid over a booking.

Please note than when anonimyzing a customer, all related bookings to this customer are affected.

#### **Activate deletion for SSR codes**

&#x20;By activating this option, service will delete automatically SSR codes which are selected per passenger in the bookings. If only this option is selected together with the option for continuous deletion, then only SSR codes are deleted from the bookings in the range.

#### **Activate deletion for booking comments**&#x20;

By activating this option, service will delete automatically booking comments added over the bookings in the range. The attachments added in the "Comments" tab are also removed.

#### **Activate deletion for bonus codes only**&#x20;

By activating this option, service will delete automatically bonus codes which were added for all bookings in the range.

#### **Activate continuous deletion for excursion guest customer - that are older than the number of days set**

This option will anonymize the excursion guest customers (customers with bookings in Destination App and Visit Sun).

#### **Activate deletion for highly sensitive extras or discounts**

This option will anonymize discounts, supplements and extras marked as GDPR sensitive for all bookings of anonymized customer (see details above).

**Delete transport reporting files for departure dates that are older than the number of days set** By activating this option, transport reporting files will be automatically deleted, when departure date is older than the number of day set.

**Delete extra reporting files and extra category reporting files that are older than the number of days set**

By activating this option, the extra reporting files are deleted.

**Delete hotel reporting files that are older than the number of days set**

Automatic hotel lists can be set to be deleted by activating this option.

Information about all anonymized users is available under the Setup/GDPR, Log tab (when logged in with sysadmin account):

<figure><img src=".gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

### The right to be forgotten for customers and passengers <a href="#the-right-to-be-forgotten-for-customers-and-passengers" id="the-right-to-be-forgotten-for-customers-and-passengers"></a>

The right to be forgotten can be applied to a customer or can be applied for a passenger, so anonymization can be triggered individually. For a **customer**, this can be done by using "Anonymize" button in the "Manage Customer" page when logged with an user with system administrator rights.

<figure><img src=".gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

If the customer is already anonymized, the request date and time, the user who perform it and the report of the anonymization (date, time, anonymized customer id and corresponding bookings) can be seen under the "Anonymize" buton:

<figure><img src=".gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

Data anonymized is data described also for service anonymization (customer and passenger names, address, email address, phone number, emails and sms sent, SSR codes, booking comments and passenger details like nationality, passport number, insurance, address, emergency contacts, sensitive data). Also, the customer or data linked to it will appear in transport reporting files, hotel reporting files or extra reporting files or category reporting files as being anonymized.

Anonymisation can be triggered also for one **passenger** from a booking. Data for this particular passenger is anonymized: passengers, address, email address, phone, email, phone found in customer details and passenger details like nationality, passport no., insurance, address, emails, sms and tickets.

<mark style="color:red;">**Important note: if a customer/passenger is anonymized, personal data cannot be recovered anymore.**</mark>
