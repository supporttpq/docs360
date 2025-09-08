# Export - Scheduled Reports

#### Overview

The **Export** interface is used to generate and schedule automated export jobs for booking data, based on time filters and format preferences. This allows tour operators and system users to generate regular data exports without manual intervention.

***

#### Purpose

To streamline the **periodic export** of booking data filtered by date and customized via user preferences, helping with operational tracking, reporting, and system integration (e.g., accounting, BI, auditing).

***

<figure><img src=".gitbook/assets/image (310).png" alt=""><figcaption></figcaption></figure>

***

#### Preconditions

* The user must have export permissions.
* At least one booking must exist in the system for the given filters.
* Schedules can only be created by users with administrative or reporting roles.

#### Filters and Options

**Date Range Filters**

* **Booking start / Booking end** – Filter based on when the booking was created.
* **Departure start / Departure end** – Filter based on travel dates.
* **More Filters** – Additional filters may be available (e.g., destination, supplier, sales channel).

**Export Options**

* **Export for Mac OS** – Ensures file formatting compatibility with Mac systems.
* **Compress as ZIP** – Delivers output as a `.zip` file.
* **Include Cancelled Bookings and Details** – Adds bookings with status canceled.
* **Include Moved Bookings and Details** – Adds rebooked bookings.
* **Export Lite Version** – Strips out extended info for a simpler export.
* **Export Generic Discounts** – Includes promotional or cross-product discounts.

The data will contain information regarding each booking that corresponds to the given filters:

* **Booking number -** A unique identifier assigned to each booking.
* **Adults number -** The total number of adults included in the booking.
* **Children number -** The number of children included in the booking.
* **Infants number -** The number of infants included in the booking.
* **Seats -** The number of seats reserved for the booking.
* **Booking date -** The date when the booking was created.
* **Booking status -** The current status of the booking (e.g., Confirmed, Cancelled, Pending).
* **Booking total price -** The total price paid for the booking, including all products and services.
* Customer No - The custumer's number.
* Customer name - Name of the customer
* **Customer e-mail -** The primary email address of the customer.
* **Seller -** The individual or platform that made the booking.
* **Agent -** The travel agent or representative involved in the booking, if any.
* **Transport code -** A code identifying the mode or provider of transport.
* **Travel length -** The total duration of the trip in days.
* **Hotel code -** A code representing the booked hotel.
* **Resort code -** A code identifying the resort associated with the hotel.
* **Destination** - The booking destination of the travelers
* **Room code -** A code for the specific room type booked.
* **Room price -** The cost of the room per booking or per night, depending on context.
* **Rooms number -** The number of rooms included in the booking.
* **Gender -** The gender of the passenger.
* **Age -** The age of the passenger at the time of travel.
* **First name -** Passenger’s first name.
* **Last name -** Passenger’s last name.
* **Passenger’s status -** The role or status of the passenger.
* **Customer postcode -** Postal code of the customer’s address.
* **Customer fax -** Fax number provided by the customer.
* **Customer phone number -** Contact phone number of the customer.
* **Customer CPR -** The customer’s CPR (civil registration number or ID, depending on locale).
* **Customer city -** The city in which the customer resides.
* **Customer address -** The full street address of the customer.
* **Has cancellation insurance -** Indicates whether cancellation insurance was purchased (Yes/No).
* **Cancellation insurance price -** The cost of the cancellation insurance.
* **Has transfer -** Indicates whether a transfer service (e.g., airport shuttle) is included.
* **Transfer price -** The price paid for transfer services.
* **Travel insurance type -** The type or tier of travel insurance selected.
* **Travel insurance price -** The price of the travel insurance policy.
* **VIP product—**&#x53;pecifies if a VIP product or service was included.
* **VIP product price -** The cost associated with the VIP product.
* **Party package product -** Indicates if a party package was added to the booking.
* **Party package product price -** The price of the party package product.
* **Pension product -** Describes whether a pension/meal plan product was booked.
* **Pension product price -** The price for the pension product.
* **Catering product -** Shows if a catering or food service product was included.
* **Catering product price -** The cost of the catering product.
* **Car product -** Indicates if a rental car or car-related product was booked.
* **Car product price -** The total price for the car product.
* **Extra bed discount -** Discount applied for an extra bed, if applicable.
* **Cancellation fee -** Any fee charged for cancelling the booking.
* **Passenger total price -** The total price assigned to a specific passenger.
* **Departure date -** The date of departure from the origin location.
* **Arrival home date -** The date the traveler returns home.
* **Discounts/Supplements -** Any discounts or additional charges applied.
* **Other products -** Additional products included in the booking not listed above.
* **Transport costs -** Total costs related to transportation.
* **Transfer cost -** Total cost for transfer services.
* **VIP cost -** Total cost for VIP services.
* **Party package cost -** Total cost for party package.
* **Pension cost -** Total cost for pension/meal plan.
* **Catering cost -** Total cost for catering or food service.
* **Car cost -** Total cost of car rental or car services.
* **Other products cost -** Cumulative cost of all other additional products.
* **Insurance cost -** Total cost of all types of insurance (travel, cancellation, etc.).
* **Discounts/Supplements cost -** Total value of discounts and supplements applied.
* **Hotel cost -** Total cost paid for the hotel accommodation.

### Schedule Export

In the Financial Export Schedule in Finance/ Export a schedule can be saved with a specific filter.&#x20;

#### Export Scheduling Options

<figure><img src=".gitbook/assets/image (311).png" alt=""><figcaption></figcaption></figure>

Using the three buttons located next to the **Export** button, you can:

* **View** all previously scheduled exports
* **Create** new export schedules based on selected filters

#### Schedules Table

| Column            | Description                                                                                                                                                                      |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Enabled**       | Toggle to activate or deactivate an export schedule. Schedules not used in 7 days are automatically disabled! For a schedule to be considered used click on "Get Latest Result!" |
| **Description**   | Name of the export schedule (customizable).                                                                                                                                      |
| **Schedule Type** | Frequency of export (e.g., _Once a day_, _Once a week_).                                                                                                                         |
| **Day**           | For weekly exports, allows selection of day (e.g., Monday, Tuesday).                                                                                                             |

🔘 **Create** – Adds a new schedule.\
🗑️ **Trash Icon** – Deletes the schedule.\
📄 **File Icon** – Get Lates Result and download the export

***

#### Export Button (Top Right)

Initiates a **manual export** using the current filters and options selected, independent of the schedule.

***

#### Notes

* Each schedule can run independently based on its frequency and enabled status.
* Use descriptive names for schedules to avoid confusion (e.g., “Weekly Cancellations Export”).
* Each schedule is generated only once a day (the time is set by the Super Admin and is usually at night). The resulting file can be downloaded manually using the Get Latest Result button.&#x20;

The finance export file is generated each night but the export is dependent on the schedule set, e.g daily, yes, then it is fro this night, but if weekly it will take the export from that specif day scheduled in the schedule. The Super Admin collaborates with the developer to determine the specific hour for scheduling tasks. Additionally, the scheduling of the Finance export file is separate from the time set for the scheduler. It is also worth noting that email addresses for the Finance Export can be configured in Setup / System Setup / General Information / Settings.

* Each user only sees the schedulers defined by him/her (he/she cannot see other schedulers defined by other users).
* The filters set do not affect already created schedulers. They can only be generated with the Export button, or to create a new scheduler using the filters.
