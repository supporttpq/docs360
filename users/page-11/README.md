# Users

Tourpaq manages users access to it's functions and permitted actions by user user roles. Below you can find what this roles are and what a user with that role can do.

### Super administrator user type <a href="#super-administrator-user-type" id="super-administrator-user-type"></a>

The Super Administrator can make general settings that apply to the whole Tourpaq System and are allowed to manage all the user types.

The person with a super administrator role can do the following:

* Insert a new company in the system
* Insert a new agency in the system and assign it to a certain company
* Insert a new user in the system. These would be the steps that are made when inserting a new user
* Assign the user to a certain company. From now on, this will be named the user’s company / the company of the user;
* Insert a username and password that will be used to access the application. The username has to be unique in the application;
* Choose a role for the user. A super administrator can choose any role, except for super administrator. It can be only one super administrator in the system;
* Assign the user to agency/agencies that belong to the already selected company. If the chosen role is administrator, he will have the right to operate on all the agencies.
* Enable or disable certain features for companies
* Add Countries in the system
* Add post codes in the system
* Add SSR codes in the system
* Manage services for each company and agency
* Post internal messages
* Can Block or Unblock all users of a company from accessing the system

### System Administrator user type <a href="#system-administrator-user-type" id="system-administrator-user-type"></a>

A system admin is has more limited access than a normal Administrator. This user has access to 3 menus:

* Setup
* Booking

#### **Setup**

* Users - same as the administrator menu, allows to access and modify users under the company.
* System setup - same as the administrator menu, allows modifying of company specific settings.
* GDPR - allows modifications to the GDPR system settings regarding data deletion

#### **Booking**

This menu contains the same items as a normal administrator but with some missing entries

### Administrator user type <a href="#administrator-user-type" id="administrator-user-type"></a>

The administrators are a certain company's staff that manages all the company's related activities in the system such as: booking, payments, automatic emails, hotel, resorts etc. An account with this role can be deleted only if it has not placed a booking in the system.

The person with an administrator role can do the following:

* Insert a new agency in the system. The agency will automatically belong to the company that the administrator belongs to.
* Insert a new user in the system. These would be the steps that are made when inserting a new user:
* Insert a username and password that will be used to access the application. The username has to be unique in the application.
* Choose a role for the user. An administrator can choose any role for the user, except for super administrator. He will be able to insert another administrator in the system.
* Assign the user to agency/agencies. If the chosen role is an administrator, he will have the right to operate on all the agencies of the company.

The administrator user type can have the following additional rights:

* Allow to book stop sale transport
* Allow to add special cost
* Overbook transports|Allow to overbook transports
* Overbook hotels|Allow to overbook hotels
* Allow to report user stories and bugs
* Allow to add special offers
* Allow to add special cost
* Allow to merge customers
* Allow to view Profit Tab of Booking
* Allow to view discount column in VAB
* Allow to set LMS limit
* Allow to login on multiple PCs
* Allow to overbook Generic Product
* Allow to override Seating Rules

### Sales user type <a href="#sales-user-type" id="sales-user-type"></a>

The agent user type manages the selling process. They have access to:

* view the made bookings,
* make new bookings directly in the system,
* manage printed tickets,
* make payments for a certain booking order.

The agent user type can have the following additional rights:

* Allow to post internal messages
* Allow to add special cost
* Overbook transports|Allow to overbook transports
* Overbook hotels|Allow to overbook hotels
* Allow to view pricelist
* Allow to edit hotel web tab
* Allow to merge customers
* Allow to view Profit Tab of Booking
* Allow to view discount column in VAB
* Allow to login on multiple PCs
* Allow to overbook Generic Product
* Allow to override Seating Rules
* Allow to see all unpaid bookings

An account with this role can be deleted only if it has not placed a booking in the system.

### Financial user type <a href="#financial-user-type" id="financial-user-type"></a>

Financial user is an agent type with financial permissions. Besides the agent's permissions, the person with this role is allowed to manage the payment data such as: payment methods, importing payments from a bank export file, manage the successful existing payments or the unregistered ones as well as the unpaid bookings. An account with this role can be deleted only if it has not placed a booking in the system.

The financial user type can have the following additional rights:

* Allow to post internal messages
* Allow to add special cost

### Supplier user type <a href="#supplier-user-type" id="supplier-user-type"></a>

Supplier role are used when a provider of accommodation services needs to login to Tourpaq Office and manage their offer. This is the case especially when the Tourpaq Hotel Release Service sets a certain number of rooms as “available for release” with a certain number of days before the departure and the supplier user will be able to remove all or a part of the releasable rooms.

The supplier user type can have the following additional rights:

* Allowed to see and change release rules
* Allow to control released hotel alloment
* Stop Sale Hotel|Allow to make stop sale
* Allow to change hotel allotment|Allow to always change hotel allotment
* Allow to see transport allotment|Allow to see transport allotment
* Allow to add special offers
* Allow to see departure seats vs beds
* VisitSun supplier
* Allowed to view Hotel Contract
* Allow to merge customers
* Allow to view Profit Tab of Booking
* Allow to login on multiple PCs
* Allow to overbook Generic Product
* Allow to override Seating Rules
* Allow to see all unpaid bookings
* Allowed to view Hotel Room Allotments

### Extra Supplier user type <a href="#extra-supplier-user-type" id="extra-supplier-user-type"></a>

Extra Supplier role is used for a provider of services at a destination needs to login to Tourpaq Office and manage their offers. This is the case especially when allotments are used for certain products or they require a list of guests that have booked their products.

The Extra Supplier user has access to:

* Extras lists
* Tee time extras lists
* Destination lists

Aditional rights:

* Allow to Block Product Allotment

### Guide user type <a href="#guide-user-type" id="guide-user-type"></a>

The guide user type is used in the situations when a guide that manages tours for a certain company and resort destination logs in the system to manage the holiday. He has access to:

* printed tickets,
* sales ledger payments,
* view and search completed bookings made for the resorts he is designated to
* send push notifications for the bookings he has access to; notifications are received in guest app, if logged in with the corresponding booking
* access his/her payments for the services,
* export hotel list data of his interest,
* view various statistics of the relevant company and resorts – similar to Tourpaq dashboard
* Tourpaq Guest app

The guide user type can have the following additional rights:

* Allow to add special cost
* Is destination Admin

### Guide Master user type <a href="#guide-master-user-type" id="guide-master-user-type"></a>

The guide master user type is used as a supervising role for the guides, being able to track their activity. He will have access to:

* printed tickets,
* sales ledger payments,
* view and search completed bookings administrated by the guides
* send push notifications for the bookings he has access to; notifications are received in guest app, if logged in with the corresponding booking
* access to the guide payments,
* export hotel list data of his interest,
* view various statistics of the relevant company and resorts – similar to Tourpaq dashboard
* access to the Service Cases
* access to the destination reports
* access to the guide profiles
* access to the sales statistics of the guides
* access to the extras page as well as being able to book an order in behalf of a specific destination
* access to the GuestApp backoffice menu items(Vocabulary, Insider Tips, Maps, Weekly Activities, Good to know)
