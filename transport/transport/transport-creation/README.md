# Transport creation

### Basic Setup

#### Overview

The **Basic Setup** screen is used to configure transport routes between departure and arrival locations. It defines the essential travel details, customer information, operational rules, and system settings that control how transport is managed, reported, and sold.

#### Purpose

The purpose of the Basic Setup configuration is to ensure that each transport is set up correctly for sales, reporting, and operational handling. It allows the system to manage passenger details, supplier connections, seating distribution, and financial rules in a consistent way.

#### Preconditions

* The transport route (departure and arrival airports/codes) must be defined.
* Related master data (suppliers, agencies, reporting rules, payment rules, etc.) must exist in the system.
* User must have sufficient permissions to configure or update transport setups.

***

#### Instructions & Field Explanations

**1. Destination**

Defines the basic route and transport identifiers.

* **Code**: Unique identifier for the transport (e.g., BLL-MLA).
* **Return**: Code for the return route.
* **Departure**: Departure airport/location.
* **Arrival**: Arrival airport/location.
* **Transport Mode**: Type of transport (e.g., Fly, Bus).
* **Cancellation Condition**: Defines the cancellation policy linked to this transport.

***

**2. Customer Information**

**When transport is dynamic, this information needs to be set on the Real Transport entity.**

Controls text and allowances shown to customers.

* **Info Customer 1, 2, 3**: Customizable text fields for passenger information.
* **Text to add on ticket**: Extra text to be printed on tickets.
* **Show Baggage Allowance**: Checkbox to display baggage allowance on customer-facing documents.  If checked, luggage allowance information is shown on the ticket as extra columns in transport itineraries.

***

**3. Transportation**

Manages seat maps, airlines, and key operational rules.

* **Seat map** (only if transport layout is enabled): Link to the seating layout. Allows guest to select their seats
* **Airline** (only if Transport mode is FLY): The Airline operating the transport.
* **Transport Type**: Specifies transport category.
* **Pickup point required**: Marks if pickup point selection is mandatory.
* **Show on dashboard**: Checkbox to display transport on the system dashboard.
* **Travel Length Correction**: Adjusts travel length (in days).
* **Shift check-in date by +/- days**: Allows shifting the check-in date, controls checking days in the hotel.
* **Hotel nights correction +/- days**: Adjusts the number of hotel nights linked to transport.
* **Estimated seats sale percentage**: Forecast of seat sales in %.
* **Free Sell**: Marks transport as available without allotments.

***

**4. Name Change Rule**

Controls passenger name change options. When checked, the system will allow a passenger name change.

* **Do Not Allow Name Change Office**: Restricts name changes in the office. This rule will apply after payment has been made.
* **Do Not Allow Name Change Web**: Restricts name changes in online bookings.
* **Name change deadline (days before departure)**: Defines how many days before departure the system will allow a passenger name change.

***

**5. Automatic Seating**

Manages automatic seat assignment for passengers. When checked, the system will automatically distribute passengers into the airplane.

* **Use Automatic Seating**: Checkbox to enable automatic seat distribution.
* **Hour before departure**: Defines when seats should be automatically assigned. How many hours before departure the system will automatically place the passengers into the airplane.
* **Email address(es)**: Recipients of automatic seating notifications (can add multiple email addresses, separated by a comma).

***

**6. Settings**

Defines operational and financial settings for the transport.

* **Tour operator**: Name of the responsible tour operator.
* **Reporting type**: Defines the reporting category.
* **Transport Supplier**: Supplier providing the transport service.
* **Transport cost currency**: Currency for transport costs.
* **Dynamic Itineraries**: Checkbox to allow dynamic itinerary creation. Setting for Real Transports and GDS
* **Use real transport allotments** (only if Dynamic itineraries are checked): Checkbox to enforce supplier allotments.
* **Status**: Defines if the transport is visible or hidden.
* **Hide as filter on lists**: Prevents transport from being used as a filter in searches.
* **Outbound parent transport** - select a transport from which the created transport can draw seats. (**Example**: Transport1 departs from DepartureA, has a stop in PointB, and then goes to DestinationC. The two transports DepA-DestC and PointB-DestC, indeed, share the same transport seat allotment)The new created transport will share the alltoments and layout with the parent set for the outbound flight.
*   **Homebound parent transport** - select a transport from which the created transport can draw seats. It can be a different transport for the homebound flight. (**Example**: P1: charter transport (7 days) that departs every Wednesday, (01.01.2025 - 31.12.2025), P2: charter transport (7 days) that departs every Saturday, (04.01.2025 - 27.12.2025), C1 - child transport having P1 outbound parent and P2 homebound parent - charter transport (3 days) that departs every Wednesday (homeboud is every Saturday) (01.01.2025 - 27.12.2025), C2 - child transport having P2 outbound parent and P1 homebound parent - charter transport (4 days) that departs every Saturday (homebound is every Wednesday) (04.01.2025 - 31.12.2025) ). Once "outbound parent transport" is set, is mandatory to have also a homebound parent. You cannot set one without the other. So if there are no different parent transports for outbound and homebound, just set the same one on both legs.&#x20;

    <figure><img src="../../../.gitbook/assets/image (394).png" alt=""><figcaption></figcaption></figure>
* **For A La Carte**: Makes transport available as a standalone option.
* **Source Agency**: Defines the responsible sales agency.
* **Payment rule**: Sets payment conditions for this transport.
* **Use Change Rule Service**: Enforces system change rules for bookings.

***

**7. Dynamic Transport Supplement**

Adds pricing flexibility by handling supplements dynamically.

* **Dynamic Supplement**: when checked, the transport price will be added as a supplement to guests in the booking (needs DTS supplement)

### Brands <a href="#brands" id="brands"></a>

Select a brand for the transport

<figure><img src="../../../.gitbook/assets/image (395).png" alt=""><figcaption></figcaption></figure>

### Infant <a href="#interval-def" id="interval-def"></a>

<figure><img src="../../../.gitbook/assets/image (396).png" alt=""><figcaption></figcaption></figure>

#### **Overview**

The _Infant_ section is used to configure pricing and allotments for infant passengers in relation to specific departure and booking periods. This ensures proper management of infant availability, pricing, and rules across bookings.

#### **Purpose**

* To define infant pricing based on travel and booking periods.
* To set allotments (maximum availability) for infants on a given departure period.
* To determine whether infant allotments should be actively checked against availability rules.

This setup helps the booking system manage reservations efficiently and ensures accurate pricing and capacity control for infants.

#### **Fields Explanation**

#### **1. Departure From -** The start date of the travel period for which the rule applies.

* **Usage**: Only bookings with departure dates on or after this date will be affected.
* **Example**: _01-09-2025_ → Rules apply starting from September 1, 2025.

#### **2. Departure To -** The last date of the travel period for which the rule applies.

* **Usage**: Ensures the configuration is valid only up to this date.
* **Example**: _30-09-2025_ → Rules apply until September 30, 2025.

#### **3. Booking Date From -** The earliest date when bookings for infants can be made.

* **Usage**: Prevents the rule from applying to earlier bookings.
* **Example**: _01-07-2025_ → Infant bookings are valid starting from July 1, 2025.

#### **4. Booking Date To -** The last date when bookings for infants can be made.

* **Usage**: Blocks infant pricing/allotment after this date.
* **Example**: _31-08-2025_ → Infant bookings must be made before or on August 31, 2025.

#### **5. Infant Price -** The price charged for an infant passenger (usually under 2 years old).

* **Usage**: Defines how much the customer pays for adding an infant to the booking.
* **Example**: _300_ → Infant price is 300 (currency depends on system setup).

#### **,6. Check Infant Allotment -** Maximum infant allotment that can be booked on each departure. Setting it to 0 will not allow infant seats to be booked

* **Values**:
  * ✅ (Enabled) → Infant bookings are limited to available allotments.
  * ❌ (Disabled) → No allotment restrictions; any number of infants can be booked.
* **Example**: _❌_ → Infant allotment is not enforced.

#### **7. Infant Total Allotment -** Maximum number of infants allowed within the defined departure and booking period.

* **Usage**: Controls capacity to prevent overbooking of infants.
* **Example**: _5_ → Only 5 infants can be booked for this period.

#### **Instructions for Use**

1. **Click “Create”** to define a new infant rule.
2. **Fill in all required fields**: departure dates, booking dates, infant price, and allotments.
3. **Enable or disable allotment checking** depending on business rules.
4. **Save** the configuration to activate it for bookings.
5. **Edit or delete** existing rules as needed using the edit (pencil) or delete (bin) icons.



### **Passenger Information**

#### **Overview**

The _Passenger Information_ section is used to define informational notes or errata that apply to bookings for specific stay periods. These messages typically provide additional details for customers or internal staff (e.g., special conditions, restrictions, or exceptions).

#### **Purpose**

* To communicate relevant information related to bookings and stays (e.g., transport notes, exceptions, overlapping rules).
* To ensure passengers and staff are aware of important details connected to their travel.
* To manage conditions within specific booking and stay periods.

#### **Fields Explanation**

<figure><img src="../../../.gitbook/assets/image (399).png" alt=""><figcaption></figcaption></figure>

#### **1. Stay From -** The start date of the hotel or travel stay period for which this information applies.

* **Usage**: Notes will only apply if the passenger’s stay begins on or after this date.
* **Example**: _29-10-2025_ → Information applies starting October 29, 2025.

#### **2. Stay To -** The end date of the hotel or travel stay period for which this information applies.

* **Usage**: Ensures the message is only relevant until this date.
* **Example**: _29-10-2025_ → Information is valid up to October 29, 2025.

#### **3. Booking Date From -** The earliest date when bookings must be made for the passenger's information to apply.

* **Usage**: Prevents the rule from applying to earlier bookings.
* **Example**: _04-06-2025_ → Only bookings made on or after June 4, 2025, are affected.

#### **4. Booking Date To -** The latest date when bookings can be made for the information to apply.

* **Usage**: Ensures the rule is limited to a certain booking period.
* **Example**: _04-06-2025_ → Only bookings made up to June 4, 2025, are affected.

#### **5. Information -** The actual message or note that will be displayed/associated with the booking.

* **Usage**: Describes transport notes, errata, or booking conditions.
* **Example values**:
  * _Transport test_ → internal test note.
  * _Transport errata def overlapping_ → indicates overlapping transport information.

#### **6. Acknowledge -** Indicates whether this information must be confirmed (acknowledged) by the user or system.

* **Values**:
  * ✅ (Enabled) → Acknowledgement required; ensures the message is seen.
  * ❌ (Disabled) → Acknowledgement not required.
*   **Example**:&#x20;

    <figure><img src="../../../.gitbook/assets/image (400).png" alt=""><figcaption></figcaption></figure>

#### **Instructions for Use**

1. **Click “Create”** to define a new passenger information entry.
2. **Fill in stay and booking dates** to specify the valid period.
3. **Enter the information text** with clear and concise notes (e.g., transport conditions, exceptions).
4. **Enable or disable acknowledgment** depending on whether users must confirm having seen the information.
5. **Save** the configuration to apply it to the system.
6. **Edit (pencil)** to update or **delete (bin)** to remove an entry when it is no longer relevant.

### Interval Definition <a href="#interval-def" id="interval-def"></a>

Set the interval between flights.

* Interval - from 1-4
* Date From - start date
* Date To - end date
* Days - days between the flights
* API Text - It's used in setting the fix quota. Multiple intervals can be set.

<figure><img src="../../../.gitbook/assets/image (397).png" alt=""><figcaption></figcaption></figure>

### Timetable <a href="#timetable" id="timetable"></a>

Used to set the date and time of the flights.

* Out/Home - flight type
* Start period
* End period
* Departure time (hour) – hour when the departure is
* Arrival time (hours) - hour when the transport arrives at destinatio.n
* Airline - Airline name
* Flight number - flight number
* Days - the transport arrives at the destination with a delay of x days from the departure date (eg: departure 01-05-2025 00:00, arrival 02-05-2025 00:00)
* Land days (should be disabled for travel out)
* Extra day out - controls hotel check-in days
* FL - flinght changes (After changing time and date of a flight, check this and update; an e-mail will be sent to all bookings made on this flight that the flight hours have been changed. Requires **Flight change e-mail** template
* Alternative Airport - this can be set for both Travel Out and Travel home lines and can change the returning airport. It will be shown on booking and ticket. (Example: Flight leaves from Billund to Antalya and returns to Billund, but the departure home airport will be Istanbul instead of Antalya).

<figure><img src="../../../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure>

### Fix quota <a href="#fix-quota" id="fix-quota"></a>

Used to generate and divide the places on the transport between flights and intervals.

* Start Date - is the date of the first departure, and next departures will be generated every number of days defined by the value selected in Period (or interval) dropdown
* End Date
* Place Number - number of seats in the transport (Place number = I1 + I2 + I3 + I4 + One way out)
* Period - sets trip length
* Override Period - is used to generate departure dates using the same interval, but with a gap of x days between departures
* Simple cost - is used to calculate transport cost per passenger (superadmin setting; when active removes Transport All Price, Guaranteed Seats, Tax and ProRate columns)
* Transport All. Price - is the cost for guarantee seats. The value should be the total cost of the guaranteed seats. In this case, you also fill the Guarantee seats field.
* Guaranteed seats - the number of seats that will be paid whether they are booked or not
* Tax - is an additional cost you pay per seat sold
* ProRate1
* ProRate2
* ProRate3
* ProRate4
* I1 - number of seats for interval 1
* I2 - number of seats for interval 2
* I3 - number of seats for interval 3
* I4 - number of seats for interval 4

When using Pro Rate allotment, which means you pay for seat sold you fill the pro rate cost for each interval. If you are not using 4 intervals, fill only what is needed. I1, I2, I3 and I4 is allotment available for each interval. In case you want to sell one-ways fill allotment for one-way out and one-way home. Note that sum of values from this 6 fields must equal value from place number field.

The guarantee empty seats fields are linked to Empty seats feature, which you will be presented in a different video. If you use it, here you can define how many seats will the system block to be sold only as empty seats. You can do this for each interval including for one way.

* One way out - number of seats for one way out
* One way home - number of seats for one way home

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

To finish click on Insert and then Generate. The end result is:

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

or

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

This depends on the simple cost being active or not. In fix quota you can control the number of seats to be sold, costs, etc. For more information please check [Transport](../) and [Transport dashboard](../../../transport-dashboard.md).

In case of a **child transport** creation (that has one or two different transports set as outbound and homebound parent transport) fix quota definitionThatThatends on the fixquotas ,of the parent transports. The start and end date must be included in the corresponding dates from the parent transports. Otherwise, fix quota will not be generated.

<figure><img src="../../../.gitbook/assets/ChildTransportFixQuota-90a88a655e66bee5d547c3cb9be26636.png" alt=""><figcaption></figcaption></figure>

To view departure in a fix quota, click the view button. Here you can view the generated departures. You can change values for each departure.&#x20;

You have allotment in the green columns, the booked seats in yellow columns, free seats in red colored columns and costs in blue columns. On each departure, the sum of allotment out total must be equal to the sum of allotment for intervals 1, 2,3,4, one way out, and guarantee empty seats for intervals 1,2,3, and 4.&#x20;

Allotment home total is calculated as the sum of allotment home charter, one-way home, and guarantee empty seats home. You can view booked seats: total booked seats outbound and of each interval, including one-way out and also booked seats on return, total,layoutr, and one-way home.&#x20;

Free seats are shown in red columns: total free seats on outbound and for each interval, including one-way out and also free seats on return: total, charter, and one-way home.&#x20;

The empty seats –definition. That ends is a check to ensure that you do not allocate more seats on outbound than the number of seats available on return.&#x20;

The column displays the difference between the Allotment Home Charter column and the sum of Allotment Out for interval 1 from one week before, Allotment Out for interval 2 from two weeks before, Allotment Out for interval 3 from three weeks before, and Allotment Out for interval 4 from 4 weeks before.&#x20;

Insert the allotment for each interval and for each departure day.&#x20;

The price column is the total cost price for guarantee seats.&#x20;

The pro rate fields are the costs for each interval.&#x20;

You also have a tax per seat sold and a passenger handling cost.&#x20;

In case you have a reserved PNR, you can use the PNR field to store it. You can set a PNR for each interval where you have allotment.&#x20;

If you do not use one way's fill out 0 one allotment total.

### Layout <a href="#layout" id="layout"></a>

Used for seating passengers in bookings. Available only if the agency transport layout service is activated.

This is done in the Transport from the Layout tab. Click on the layout tab.&#x20;

Select a fix quota. Click, display.&#x20;

Seat layouts can be assigned for each departure and arrival flight in part. Seat layouts can be different from flight to flight, depending on the transport type used. We can assign for each departure date different layout type.&#x20;

Click on the dropdown list and choose the desired layout.&#x20;

Click save, and we see the seat type price. We do the same thing for the next departure date, and we can select another Layout type, different from the previously chosen one. Click save, and we can continue for the next departure date with a different layout type. Layouts can be changed, but the new layout needs to have the same or a higher number of seats than the existing layout.&#x20;
