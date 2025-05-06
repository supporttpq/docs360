# Company Setup

A company can be created only by a Superadministrator user. Those who wish to create a new company are advised to contact Tourpaq Support. A company can be created in two ways:

### Manual Setup <a href="#manual-setup" id="manual-setup"></a>

Details of a company can be edited by an Administrator user. These are the fields that can be modified:

* Name of the company
* Address of the company
* Country
* Postcode
* IBAN
* CVR
* Phone
* Fax

After this, a Brand and an Admin user type are required. These can be firstly created by the Superadministrator. But after the first Brand and Admin user have been created, any Admin user can create Brands and users for the company.

#### **Brand Creation**

The following fields are necessary for the brand to work properly:

* General Tab
  * Brand name
  * Brand code
  * Contact email address
  * Booking IDs start from (this must be different from other brands) - number from which the bookings begin to be counted
  * Booking IDs ends to (this must be different from other brands) - number at which the booking count ends
  * Offer ID's start - number from which the offers begin to be counted
  * Offer ID's ends - number at which the offers count ends
  * Gift Card ID's start - number at which thegift cards count start
  * Gift Card ID's end - number at which the gift cards count ends
  * WebBooking link - link for the webbooking page
  * Allow Cancel. Ins. changes - guests cannot make any more changes to insurances, x days after the booking has been created
  * Stop Web changes - guests cannot make any changes to the bookings, x days before the departure
* Ticket Tab
  * Brand name
  * Country
  * Postcode
  * Address
  * CVR
  * Phone
  * Fax
  * Bank
  * Creditor number
* Insurance Tab
  * Insurance type
  * Insurance agent username
  * Insurance agent password
  * Insurance agent code
  * Insurance agency code
  * Days no before/after departure - insurances are reported to the company x days before the departure
  * Creditor number

Note!!! Information for Insurance Tab is taken from the insurance company.

Other fields:

* General Tab
  * Bcc e-mail address
  * Website reset cache link - link to the presentation site that uses the Tourpaq API, used to reset the system cache
  * Terms and Conditions page link
  * Voucher IDs start from - number from which the voucher count starts
  * Voucher IDs ends to - number at which the voucher count ends
  * Hide included extras prices - hides the price of the extras "Add to basic price"; when active, it will disregard multiple selection categories
  * Uses custom text - when a company has more brands, this allows each brand to have a different name for a product
  * Currency
  * Autocomplete passenger names from last booking - loads the names of passengers from the previous booking made by the same customer
*   Ticket Tab

    * IBAN number
    * Bic Code Swift Address
    * Hide Payment Plan
    * Customized Star – the text that replaces the default "Stars" header. This replacement occurs only when the Customized Stars field for the respective hotel is filled.&#x20;

    <figure><img src="../.gitbook/assets/customized-stars-header-122824a932809b8c5272a49b5b95b3cf.png" alt=""><figcaption></figcaption></figure>

#### **User creation**

Mandatory fields:

* UserName
* Password
* First Name
* Last name
* Seller ID in booking
* User role

Other fields:

* Status
* Enable password valability days - enables the usage of "Password valability days"
* Password valability days - the user cannot use the password after a number of days
* Phone - is used for 2FA
* Email - where the user will receive emails and also used for 2FA
* Use 'One Time Password' feature
* Web user - necessary for companies that use the webbooking feature, allows for bookings to be used from internet by guests
* VistSun User
* Select Offer - Profile Picture - you can select profile picture for the user when an offer is sent
* Exclude personal contact data from Select Offer - Agency contact data will be used instead!
* Disable Two Factor - enable/disable the 2FA per user

Additional settings - allows and give some additional permission to the user depending on his role:

* Allow to book stop sale transport
* Allow to merge customers
* Allow financial Export
* Show personal details in financial export
* Show personal details in hotel lists
* Show personal details in extras lists
* Show personal details in TeeTime lists
* Show personal details in Flight Transfer lists
* Allow to view Personal Data on Booking and VAB \[This also affects if you can view the Customer and Phone columns in VAB]
* Allow to add special offers
* Allow to add special cost
* Allow to overbook transports
* Allow to overbook hotels
* Allow to show Profit Tab
* Allow to login on multiple PCs
* Allow to set LMS limit
* Allow to overbook Generic Product
* Allow to override Seating Rules
* Allow to see all unpaid bookings
* Hide as filter on lists: \[Hide this user in the lists throughout the system]
* Ignore export departure date limit
* Allow to view Internal Logs
* Allow User To UnApprove ExtraOrder Refunds

<figure><img src="../.gitbook/assets/image (28) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Automated Setup <a href="#automated-setup" id="automated-setup"></a>

USERS -> Company -> New API

For Automated New Company creation, the user will only have to complete the following informations:

<figure><img src="../.gitbook/assets/image (29) (1).png" alt=""><figcaption></figcaption></figure>

* Company Information
  * Company Name
  * Company Type
  * Country
  * Currency
  * PostCode
* User details
  * First Name
  * Last Name
  * User Name
  * Email
  * Password

After the Company details are completed, at least one agency should be created.

<figure><img src="../.gitbook/assets/image (30) (1).png" alt=""><figcaption></figcaption></figure>

In order to add a new Agency,the following informations should be completed:

* Agency Name
* Phone
* Email
* Address
* Theme - the website theme
* Add WebSite/Details
  * Staging WebBooking & Web - This option will create a webbooking and presentation site
  * Staging WebBooking - This option will create only a webbooking site

After the settings are completed, a WEBUSER and a WINDOWS SERVICE user will be automatically created.
