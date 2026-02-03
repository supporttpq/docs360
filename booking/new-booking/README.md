# New Booking

### **Overview**

The **New Booking** section in Tourpaq is used to create a **new reservation from scratch** for a customer or group. From here you can search for available **transports**, **hotels**, and **extras**, add **passengers**, and review the **economics** (price, costs, profit) before confirming the booking.

This page is the **landing page** for all documentation related to creating and managing a new booking. Use the sub‑pages in this section for detailed explanations of each area (Economics, Passenger details, E‑mails, Comments, etc.).

***

### **Purpose**

The New Booking functionality is designed to:

* Allow agents to create **new bookings manually** (phone, email, agency, internal sales).
* Support different booking types: **package**, **hotel only**, **transport only**, and bookings with **extras**.
* Provide entry points to detailed views such as **Economics**, **Passenger details**, **History**, and more.
* Ensure bookings are created with complete and correct data before tickets, vouchers, and communications are sent.

***

### **Preconditions**

Before using **New Booking**, make sure:

* You are logged in with a **user role** that has access to create and edit bookings.
* A relevant **Brand** is selected (if required by your setup) so that the correct prices, transports, and hotels are available.
* Core data is configured for the Brand, such as:
  * **Transports** (flights, buses, etc.)
  * **Hotels** and **room types**
  * **Price lists** and **discounts/supplements**
  * **Extras** (transfers, insurances, activities, etc.)

{% hint style="info" %}
If you cannot find any departures, hotels, or prices when searching in **New Booking**, first check that you selected the **correct Brand**, dates, and that valid **price lists** exist for the period.
{% endhint %}

***

### **Quick start**

{% stepper %}
{% step %}
### 1. Open **New Booking**

1. Go to **Booking → New Booking**.
2. If prompted, select the **Brand** you want to book under.
3. Confirm that you are in the correct **sales environment** (e.g. test vs production, if applicable).
{% endstep %}

{% step %}
### 2. Search for travel options

1. Enter the basic search criteria, such as:
   * Departure **gateway** / airport
   * **Destination** / resort or hotel area
   * **Travel dates** (outbound and return)
   * Number of **adults**, **children**, and **infants**
2. Start the search to see available **transports** and **accommodations**.
3. Adjust dates or number of passengers if no suitable options appear.
{% endstep %}

{% step %}
### 3. Select transport and accommodation

1. Choose the desired **outbound** and (if relevant) **return** transport.
2. Select a **hotel**, **room type**, and **board type** according to the customer’s request.
3. Verify that the selected combination is available and that the **price** looks correct.
{% endstep %}

{% step %}
### 4. Add passengers and details

1. Add all **passengers** with names and required personal details (age, date of birth, etc., depending on your rules).
2. Assign passengers to the **rooms** and **seats** where relevant.
3. Open **Passenger details** to add additional information (e.g. contact details or special needs) if needed.
{% endstep %}

{% step %}
### 5. Add extras and review economics

1. Add any **extras** (insurance, transfers, activities, equipment, etc.) requested by the customer.
2. Open **Economics** to review:
   * Total **price** to the customer
   * Underlying **costs**
   * Calculated **profit** / margin
3. Adjust components (hotel, transport, extras, discounts) if the price or profit needs to be changed within your rules.
{% endstep %}

{% step %}
### 6. Confirm and save the booking

1. Check that all required data is entered (passenger details, travel components, payment terms, etc.).
2. Save / confirm the booking.
3. Note the **booking number** and, if needed, proceed to:
   * Send **tickets / confirmations** via the **E‑mails** section.
   * Add **comments** or internal notes.
   * Review **History** for an audit trail.
{% endstep %}
{% endstepper %}

***

### **Key areas in New Booking (sub‑pages)**

Use the following pages for detailed explanations of specific parts of the New Booking flow:

#### Core booking flow

* [**New Booking**](new-booking/) – Main New Booking screen, search, and selection of transports and hotels.
* [**New Booking search support**](new-booking/new-booking-search-support.md) – Details on the search behaviour and options in the New Booking screen.
* [**Edit Passenger**](new-booking/edit-pas.md) – How to update passenger information within a booking.

#### Financials and performance

* [**Economics**](economics.md) – Price, cost, and profit overview for a booking.
* [**Profit**](profit.md) – Detailed profit handling and views per booking.
* [**Individual payments**](individual-payments.md) – Manage payments per passenger or per booking.
* [**Keep automatic discounts prices**](keep-automatic-discounts-prices.md) – Control behaviour when automatic discounts are recalculated.

#### Passenger and booking information

* [**Passenger details**](passenger-details.md) – Detailed personal data and options per passenger.
* [**Customer info / Details on customer card**](customer-info-details-on-customer-card.md) – How customer information is displayed and managed.
* [**History**](history.md) – Log of changes and actions related to the booking.
* [**Comments**](comments.md) – Internal notes on the booking.

#### Communication

* [**E‑mails**](e-mails.md) – Sending and tracking booking‑related emails.
* [**SMS**](sms.md) – Sending and managing SMS messages linked to the booking.
* [**QR code for vouchers**](qr-code-for-vouchers.md) – Configuration and use of QR codes on vouchers.

#### Services and allocation

* [**Hotel Room**](hotel-room.md) – Managing hotel room allocation within a booking.
* [**Transport Seating**](transport-seating.md) – Assign and manage seats for transports.
* [**Tee Times**](tee-times/) – Handle tee time bookings and related modules.
* [**Golf Courses**](golf-courses.md) – Manage golf course information related to bookings.
* [**Extra Orders**](extra-orders.md) – Manage additional extras ordered through or after the booking.

#### Special booking behaviours

* [**Waitting list**](waitting-list.md) – How waiting lists work in bookings.
* [**Moved Booking**](moved-booking.md) – Moving a booking to another departure, hotel, etc.
* [**Copy Booking**](copy-booking.md) – Copying an existing booking.
* [**Circuit Bookings**](circuit-bookings.md) – Handling circuit or round‑trip bookings.
* [**Booking for 2 One Ways**](booking-for-2-one-ways.md) – Creating bookings that consist of two separate one‑way transports.
* [**Multiple one way flights bookings**](multiple-one-way-flights-bookings.md) – Handling bookings with more complex one‑way combinations.
* [**Multiple transports one room bookings**](multiple-transports-one-room-bookings.md) – Bookings where passengers use different transports but stay in the same room.
* [**Hotel Only Bookings**](hotel-only-bookings.md) – Create bookings without transport.
* [**Transport only Booking**](transport-only-booking.md) – Create bookings with transport but no hotel.
* [**Child Price**](child-price/) – Behaviour of child pricing in bookings.
* [**A la Carte**](a-la-carte/) – A la carte booking options and packages.
* [**Remove pax on outbound or homebound only**](remove-pax-on-outbound-or-homebound-only/) – Special handling when a passenger travels only one way.

#### Other booking‑related tools

* [**Conversation**](conversation.md) – Conversation/history related to a booking.
* [**Don't sent ticket option**](/broken/spaces/ZCqzVJEAfJB0xT0ODRb) – Configuration and usage of the "do not send ticket" option.
* [**Coded discount booking**](coded-discount-booking.md) – Using coded discounts when creating a booking.

***

### **FAQ**

#### **1. When should I use New Booking instead of WebBooking?**

Use **New Booking** when an **agent** or **internal user** is creating or adjusting a booking manually (e.g. phone or email requests, partner agency sales, special cases). Use **WebBooking** when the **customer books themselves** through your online booking engine.

***

#### **2. Why do I see no available departures or hotels for the dates I search?**

Common reasons:

* The selected **Brand** has no valid **price lists** or **allotments** for the chosen period.
* The **dates** fall outside configured **travel lengths** or allowed stay durations.
* The **gateway**, **destination**, or **hotel** filters are too restrictive.

Try widening the search (dates, destination, or number of passengers). If nothing appears, check your **Transport**, **Hotel**, and **Price list** setup or contact your administrator.

***

#### **3. The price looks wrong or is 0 – what should I check?**

* Confirm the correct **Brand** is selected.
* Verify that there is a valid **price list** and **room/transport price** for the chosen period and configuration.
* Check whether **discounts/supplements** or **special rules** affect the final price.
* Open **Economics** to see how the price is calculated and which components are missing or zero.

If prices still look incorrect, contact your internal support or pricing team.

***

#### **4. Can I use New Booking to edit an existing booking?**

No. Use [**All bookings**](../all-bookings/) to:

1. Search for the booking by booking number, customer, or filters.
2. Open the **booking details**.
3. Edit transports, hotels, passengers, extras, etc., using the relevant sub‑pages (Economics, Passenger details, Hotel Room, Transport Seating, etc.).

***

#### **5. How do I handle group bookings with many passengers?**

For larger groups:

* Carefully define the **number of passengers** and **room distribution** from the start.
* Use **Passenger details** to maintain clear information for each traveller.
* Consider using **Copy Booking** for similar group configurations.
* Use **Economics** to check overall profitability of the group booking.

Your organisation may also have specific procedures or products for group bookings—follow those internal guidelines where applicable.

***

#### **6. What is the best way to document special requests or internal notes?**

Use the **Comments** sub‑page on the booking to:

* Add **internal notes** that are not visible to the customer.
* Document **special agreements** or exceptions.
* Leave information for colleagues who might handle the booking later.

For requests that must appear to suppliers or customers, use the relevant fields in **Passenger details**, **Hotel Room**, **Transport Seating**, or dedicated **SSR (Special Service Requests)** pages.
