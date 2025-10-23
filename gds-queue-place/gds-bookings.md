# GDS Bookings

### Overview

A **GDS booking** refers to a reservation created or synchronized through a **Global Distribution System (GDS)**, such as _Amadeus_ or _Travelport_. These systems provide real-time access to flight schedules, seat availability, and prices from commercial airlines.

When a booking in Tourpaq is connected to a GDS, the system automatically imports and maintains information such as the **PNR (Passenger Name Record)**, **ticket numbers**, and **flight details**. Any updates made in the GDS—such as changes in schedule, fare, or status—are automatically synchronized with the corresponding booking in Tourpaq.

GDS bookings differ from **Charter** or **Own Transport** bookings, as they are governed by the airline’s rules and are managed externally through the GDS, rather than directly controlled by the tour operator. This type of booking is typically used for scheduled flights or complex itineraries where integration with airline systems is required.

### Purpose

The purpose of a **GDS booking** is to integrate Tourpaq with external airline systems through a **Global Distribution System (GDS)**, allowing the operator to manage **scheduled flight reservations** alongside charter and own transports within the same platform.

This connection provides several key benefits:

* **Real-time data exchange:** Flight times, seat availability, and fares are automatically retrieved and kept up to date through the GDS.
* **Accurate pricing and ticketing:** Ensures that ticket prices, taxes, and fees match the airline’s data, reducing the risk of manual errors.
* **Automatic synchronization:** Any change made by the airline (e.g., schedule changes, cancellations, rebookings) is reflected in Tourpaq.
* **Centralized management:** Allows the operator to handle charter, own, and scheduled flight bookings in one system, simplifying reporting and customer handling.
* **Compliance and traceability:** The GDS link ensures that booking data, ticket numbers, and fare rules are stored according to airline and IATA requirements.

In summary, the **GDS booking** acts as the bridge between Tourpaq and the airline’s reservation systems, enabling a seamless and reliable workflow for scheduled flights.

### **New Booking**

Applies for Administrator and Agent

New booking function shall give the possibility to make a new booking. The workflow will be as follows:

* Fill in the number of adults, children and infants
* Choose a transport for the desired destination
  * Preconditions: transports must be inserted into the system and transport allotments must be generated
* Choose a hotel and a room from the chosen destination.
  * Preconditions: hotel and rooms must be inserted in the system and hotel allotments must be generated. Prices must also be inserted in the system for the chosen transport and hotel.
* Fill in the data for the person who orders the booking(customer)
* Fill in the data for the passengers.
* Give the possibility to choose different extra options for the trip as: rent a car, choosing to go on an excursion, opting for a catering product, pay cancellation insurance, etc. These extra options can be chosen for each passenger
* Discounts and/or supplements will be applied when is the case.

A total price of the booking together with the payment deadline will be calculated using the rules established from system setup.

Below is a flowchart that illustrates how other assets from the system are involved in the process.

The double arrowed line indicates that a precise asset (already inserted in the system) has been chosen. For example: a transport from Copenhagen to London has been chosen. This transport had been inserted in the system before making this booking. The extra options must also have been inserted in the system before.

Forward down are detailed explained all the steps that should be made when making a new booking:

**1. Choose the agency.** If the logged-in user has the right to operate on more than one agency, the first step that he must take is to choose the agency.

**2. Fill in the number of passenger(passengers number)** There should be separate fields for filling in adults number, children number, infants number.

**3. Choose a transport.** It must be a link that when pressed should open a new window (transports window) from where the transport allotment can be chosen. If the passenger's number has not been filled in, an error message should be displayed – that will ask the user to fill in the passenger's number. The displayed allotments will come from transports assigned to the chosen agency. In the transports window, some filters and buttons that will help search through the allotments more quickly:

* Departure start date
* Departure end date
* Departure
* Arrival
* Transport code
* A button that will search (Search)
* A button that will clear some of the chosen filters(Clear)
* A button that will display all records(Display all)

This is the information that should be displayed for each transport allotment:

* Departure date
* Departure - Departure airport
* Arrival - Arrival airport
* Transport code
* AO1 - Allotment out for interval 1
* AO2 -  Allotment out for interval 2
* AO3 -  Allotment out for interval 3
* AO4 -  Allotment out for interval 4
* Flight number

Departure start date should have as a default value today’s date and Departure end date today’s date plus 3 weeks. If the logged in user makes other choices for these filters, these new values should be restored next time he makes a booking and opens the transports window.

When making the search, the transports allotments with no seats for selling(AOUT = 0) or seats number lower than passengers number should not be displayed. These allotments should appear only when Display all button will be pressed.

When Display all button is pressed, Departure start date and Departure end date should be cleared, as none of the filters is taken into account; but when opening again the transports window, Departure start date and Departure end date will not be unfilled, but will have the values they had before Display all button was pressed.

Arrival filter should have an autocomplete functionality. Thus, when entering a letter, all the arrivals from the current company beginning with the inserted letter should appear. Departure and Transport code will have the same functionality.

Arrival, Departure and Transport code filters should not be remembered for the next time the transport window is opened.

In the user interface, when a transport allotment is selected there should automatically be filled in the possible values for the trip length; thus, if the selected allotment has available seats for only one week, the agent shouldn’t be able to select any other value for the excursion duration.

**4. Choose a hotel** It must be a link that when pressed it should open a new window (hotels window) from where the hotel can be chosen. This link should be visible only after a transport allotment has been chosen.

The displayed hotels must be located in resorts from the transport’s arrival. That’s the reason why it mustn’t be possible to choose a hotel before transport. This is the information that should be displayed for each hotel:

* Hotel
* Resort
* Standard room
* Standard room’s beds number
* Available rooms number
* Normal prices
* Discount prices
* Group prices

Normal, discount and group prices come from the price lists defined for the already chosen agency and transport, the found hotel and its standard room. It mustn’t be possible to choose a hotel (and implicitly a room) if the correspondent price is 0, and it mustn’t be possible to choose a group price if the passengers number is not greater or equal to the value defined from System setup group(for a better understanding, please refer to System setup group section).

In the hotel's window should also appear some filters and buttons that will help finding the hotels more quickly:

* Resort name
* Hotel code
* A button that will make the search(Search)
* A button that will clear the chosen filters(Clear)
* A button that will display all records(Show all room types)

The possibility to opt for displaying all the rooms of the hotel (by default, only the standard rooms are shown)

The Search button will return all the hotels that match the given filters (Resort name, Hotel code and Display all rooms).

Clear button should clear the filters, except for the Display all rooms option (for this option, should exist a checkbox in the user interface that will be checked/unchecked only manually).

When Show all room types button is pressed, Resort name and Hotel code filters should be cleared, as none of the filters is taken into account.

The choice made for Display all rooms should be remembered for the next time the logged-in user makes a booking and opens the hotels window.

It must be possible to choose more than one room for the trip, but the chosen rooms must be from the same hotel.

**5. Choose the room**

It must be a link that when pressed it should open a new window (rooms window) from where the room/rooms can be chosen.

This step shouldn’t be made in most of the cases, as the room can be selected from hotels window. But if the logged in user wants to change the selection, he can press this link and find only the rooms from the already selected hotel.

Once a room is selected, it will be displayed in a table; the default number of selected rooms is 1, but it should be possible to change this number from the table. If the inserted number is zero, the room will be automatically removed from the list.

**6. Choose/Insert the customer**

The customer is the person that owns the booking. He is the one that makes the payments, receives the e-mails, can make changes or cancel the booking.

It should be possible to create a new customer or choose one for which the information has already been inserted in the system.

The following is an extract of the information that must be available for each customer:

* Phone number
* First name
* Last name
* Address
* Company
* Country
  * It will be chosen from the countries inserted in the system by the super administrator
* Postcode
  * It will be chosen from the postcodes inserted in the system by the super administrator
* Evening phone
* Mobile
* Fax
* E-mail address

A customer must be identified by his phone number – meaning that if his information has already been inserted in the system, by filling in the phone number his data must be displayed automatically. If by mistake there is more than one customer with the same phone number, it should appear a window (customers window) where the customers with that phone number will be displayed and the desired one can be chosen.

It must also be possible for the customers window to be opened by pressing a link where all the customers (that belong to the agent’s company) will be displayed.

When making a new booking, there will be 2 ways to choose the customer: either by inserting the information for a new one (the fields will be empty by default) or by choosing one from customers window.

When inserting the data for a new customer, the following fields must be required (meaning that if the fields are not filled in, the customer mustn’t be saved):

* First name
* Last name
* Phone number
* Address
* Postcode
* Country

In the customers window should exist some filters and buttons that will help finding the customers more quickly:

* Customer name
* Phone number
* A button that will make the search(Search)
* A button that will display all records(Display all)

Customer name filter should have an autocomplete functionality. Thus, when entering a letter, all the customers’ names from the agent’s company beginning with the inserted letter should appear.

If a customer has been chosen for a booking, he can be changed later – either by choosing a new customer from the customers window or by inserting a new one. For the insertion of a new customer, it must exist a button that will clear all the fields, so new information could be inserted.

Once the agency, transport, hotel, room type and customer have been chosen, the booking can be saved. Even if the booking is saved, the process is not finished yet. A new stage should follow – when data regarding passengers and their options will be saved.

But this stage will not be reached if the booking hasn’t first been saved. And in order to be saved, there are some conditions that must be fulfilled:

* The chosen transport allotment must have enough available places for the selected length of trip and number of passengers. If not, an error message must be displayed.
* For the selected hotel and room must exist allotments that cover all the period of the trip (allotments that are not released and for which the booked rooms number is lower than the rooms number). If not, an error message must be displayed.
* The selected room should have enough beds for the number of passengers. If no, an error message should be displayed.

If any of these conditions is not fulfilled, the booking mustn’t be saved.

The following should happen when a booking is saved for the first time:

* The booking status will be Error – this status will illustrate that the process is not finished yet
* The seats will be taken from the transport allotment
* The selected room/rooms will be booked and this will be illustrated in the correspondent hotel rooms allotments

After the allotments are taken, the next step must be done:

**7. Fill in the passengers information.** This is the data that must be inserted for each of the passengers:

* Gender
* Age
* First name
* Last name
* Room
  * If more than one room have been selected in the previous step, it must be specified which of the rooms is selected
* Cancellation insurance
  * It must be specified if the passenger opts to pay a cancellation insurance or not
* Transfer cost
  * It must be specified if the passenger opts for transfer cost or not
* Travel insurance
* Discount or Supplement
  * It must be possible to choose a discount or a supplement for a passenger. There are also discounts/supplements that will be added automatically(for a better understanding, please refer to D**iscount or Supplement** section)
* Extra bed
  * Extra bed discount must automatically be added to the passenger’s information
* Catering extras – this field will appear only if there are available catering extras for the departure and booking date
  * It must be possible to select a catering product for the passengers – from the list of available products(for more details please refer to Extras section)
* VIP extras – same as catering extras
* Party package extras – same as catering extras
* Pension extras – same as catering extras
* Car extras – same as catering extras
* Hotel extras – same as catering extras
* Pickup point – this field will appear only if the selected transport requires a pickup point

The following information must be required for each passenger (meaning that if the fields are not filled in, an error message must be displayed and the passengers mustn’t be saved):

* Age
* First name
* Last name
* Room
* Travel insurance

For the infants, only the age, first name and last name must be filled in. The values for room and travel insurance will be automatically selected (no room or travel insurance is needed for an infant).

Besides the fields that must be filled in in order to save the passengers, there are other conditions that must be fulfilled:

* The inserted genders must match the adults number, children number and infants number that were filled in at the beginning of the process.
  * When filling in the passengers details, there will be some predefined genders: M(Male), F (Female), C (Child), I (Infant)
* The passengers must match the room’s beds distribution.
  * When a room is inserted in the system, ordinary beds number, minimum beds number, extra beds for adults, extra beds for children are filled in. Minimum beds number will define the minimum number of passengers that will be accepted in the room. These would be the conditions that must be fulfilled:
    * The total number of passengers(adults number + children number) must be greater than the minimum number of beds from the room
    * Extra beds for adults can be occupied by adults or children
    * Extra beds for children can be occupied only by children

Other sections that should be in booking page:

a) Economics

In this section, information regarding payments rates and due dates will be displayed:

* Deposit to pay
* Deposit paid
* Deposit due date
* Second payment to pay
* Second payment paid
* Second payment due date
* Rest of payment to pay
* Rest of payment paid
* Rest of payment due date
* The possibility to allow release payment(this will specify that money should be returned to the customer)

And other information:

* Internet password(this password will be used to login on webbooking)
* Cancellation date(in case of canceled booking)
* Information regarding the last update of the booking:
  * The user that has made the last update
  * Update date
  * Update hour and minute
* Branch
* Account

From this section should also be possible to make payment by card – it should be a link that when pressed is must open a new window from where the payment can be done.

b) Extras

From this section, it should be possible to add extra products for each passenger (besides the ones that are added from passengers details. It should be possible to add a product for all passengers or for a certain one.

There should be displayed only the products that match the booking date, departure date, destination, resort, hotel or transport together with their price.

c) Passengers details

From this section extra information for each passenger will be inserted:

* Insurance company
* Insurance policy number
* Country
* Postcode
* Address
* Transport comments
* Emergency contacts
  * Name
  * Relation
  * Phone number

d) History

In this section will be displayed all the changes and important information regarding a booking, like:

* Seller signature change
* Booking date change
* Booking total change
* Booking number change
* Booking version change
* Adults number change
* Children number change
* Departure date change
* Transport change
* Period interval change
* Customer change
* Hotel change
* Resort change
* Password change
* Booking status change
* Any change that is made for a passenger: room change, cancellation insurance added, product added, total changed, etc.

For each change, this should be the displayed information:

* The date of the change
* The hour of the change
* The user that has made the change
* The booking version
* Old value
* New value

e) Emails From this section will be possible to view all the types of e-mail that have been sent for the current booking.

f) Comments From this section is should be possible to insert the following comments:

* Hotel comments
* Comments for the customer
* Intern comments
* Economy comments
* Destination/Guides comments

g) SSR

### **View all bookings**

Applies for Administrator and Agent

This function must give the possibility to display all the bookings from the system, bookings that belong to the agency/agencies on which the logged-in user has the rights to operate.

Filtering the data will also be possible, and these would be the filters:

* Agency/Agencies
* Booking start date
* Booking end date
* Passengers number
* Departure start date
* Departure end date
* Arrival start date
* Arrival end date
* User/s
* Transport/s
* Hotel/s
* Booking status(ok, cancelled, error, locked)

As a result, the bookings that correspond to the selected filters together with several calculations indicating the following data will be displayed:

* Total number of bookings
* Total number of passengers
* Total number of infants
* Basic prices total
* Travel insurances total price
* Unordered List ItemCancelation insurances total price
* Cancelation fees total price
* Pension products total price
* Catering products total price
* Car products total price
* Transfer costs total price
* Pickup points total price
* Discounts total
* Supplements total
* Total booking prices

The options selected by the user for the filters will be kept and restored next time he will use the View all bookings function. In this way, he won’t need to choose the filters again. Each time he makes a new selection for the filters, the new ones will take the place of the old ones and these new options will be restored next time he will use the function.

It will also be possible to sort the displayed bookings by:

* Booking number
* Transport name
* Unordered List ItemResort name
* Hotel name
* Departure date
* Passengers number

### **Find faster booking**

Applies for Administrator and Agent

This function must give the possibility to find a booking using the following fields:

* Booking number
* Phone
* Booking status
* Pass First name
* First Name
* Last Name
* Address
* Pass Last Name
* Postcode
* Country
* Company
* Order number (finds bookings based on the order number of the payment)
* Place
* E-mail
* Contact
* Pnr Code (finds bookings based on the transport PNR code)
* Ev. phone
* Fax
* Mobile
* Cust. no
* Booking date after

All the bookings that correspond to the inserted filters will be displayed.
