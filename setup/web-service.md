---
noIndex: true
---

# Web service

### Overview

This web service is used to show Tourpaq data in Web Booking.

It returns the information you normally set up in Office, such as:

* departure and arrival airports
* destinations (resorts)
* hotels
* extras (products)
* travel lengths (how many days/nights)

The service can also be used by other parts of Tourpaq that need to search offers, for example advanced search screens.

### Security <a href="#security" id="security"></a>

To use the service, you need a username and password.

That user must be marked as a **Web User** in the back office.

Access is limited:

* The user can only request data for the agencies/brands they are assigned to.
* For calls that include `AgencyID`, the service checks that the user is allowed to use it.

The service uses **Basic Authentication** (username + password sent with the request).

### Methods Description <a href="#methods-description" id="methods-description"></a>

Below is a short description of the methods exposed by the service.

### GetDepartures <a href="#getdepartures" id="getdepartures"></a>

Returns all departure airports (gateways) for the selected agency.

Typical fields returned:

* Name
* IATA code
* Country
* Country code

### GetDeparturesFromResort <a href="#getdeparturesfromresort" id="getdeparturesfromresort"></a>

Returns the possible departure airports for an agency, when you already know the `ResortID`.

Note: A **resort** is often called a destination, but it is not the same as an **arrival airport**.

### GetDestinations <a href="#getdestinations" id="getdestinations"></a>

Returns all arrival airports (gateways) for an agency.

Typical fields returned:

* Name
* IATA code
* Country
* Country code

### GetCountries <a href="#getcountries" id="getcountries"></a>

Similar to **GetDestinations**, but returns only the countries that have arrivals for the selected departure.

It looks at transports set up in the system and returns the arrival country.

If DepartureID = 0 then it will return all countries for which there are defined transports for that agency.

### GetResorts <a href="#getresorts" id="getresorts"></a>

Returns resorts based on the request filters.

These conditions must be met:

* existence of a transport for the given agency ID;
* the transport must be enabled for internet sales
* if `Country > 0`, only arrivals in that country are used
* resorts linked to those arrivals are returned

### GetResortByID <a href="#getresortbyid" id="getresortbyid"></a>

Returns details for one resort (`ResortID`).

Typical fields returned:

* Name
* Code
* Description
* Number of restaurants and bars
* Shopping
* Attractions
* Teaser text
* Pictures
* Meta description
* Geo location

### GetTravelLengths <a href="#gettravellengths" id="gettravellengths"></a>

Returns the available stay lengths for transports that match your filters.

You can filter by agency, departure, country, resort, and departure date.

Typical fields returned for each travel length:

* Nights (hotel nights)
* Days (total trip days)
* Travel mode (for example flight, bus, train)
* Interval ID (typically 1–4)
* Name

### GetTravelLengthsForTransportAll <a href="#gettravellengthsfortransportall" id="gettravellengthsfortransportall"></a>

Same as **GetTravelLengths**, but used when you already have a `PriceListTransportAllotmentID`.

### GetTravelLengthByID <a href="#gettravellengthbyid" id="gettravellengthbyid"></a>

Returns one travel length by `TravelLengthID`.

The response is similar to **GetTravelLengths**.

### GetHotelByID <a href="#gethotelbyid" id="gethotelbyid"></a>

Returns hotel details for one `HotelID`.

Typical fields returned:

* Hotel ID, name, and code
* Resort and country
* Address and contact details
* Descriptions (short and HTML)
* Pictures
* Meta description
* Geo location
* Distances
* Facilities

### GetProducts <a href="#getproducts" id="getproducts"></a>

Returns extras (products) based on filters.

You can filter by:

* Agency/brand
* Arrival, resort, or hotel
* Catering type
* Pension type

Typical fields returned per product:

* Name, code, and description
* Flags such as VIP / party package / pension / catering
* Prices with:
  * booking date from/to
  * price and group price

### GetHotelDiscounts <a href="#gethoteldiscounts" id="gethoteldiscounts"></a>

In Tourpaq System, in the Hotel section are defined the extra beds discounts. The user should be able to get all the discounts for a given hotel starting from a given departure date.

Typical fields returned:

* Discount value
* Age group
* Interval ID
* Percent flag (whether the discount is a percentage)

### GetAvailableDays <a href="#getavailabledays" id="getavailabledays"></a>

Returns the dates where trips/excursions are available.

This is useful for calendars, so customers only see dates that can be booked.

If the search selection changes (for example departure airport), the returned dates change too.

Typical request fields include:

* Departure, country, resort
* Start date and end date
* Adults, children, and child ages
* Agency/brand
* Interval ID
* Transport-hotel flag

### GetTransportAllotments <a href="#gettransportallotments" id="gettransportallotments"></a>

Returns transport departures that match your filters and date range.

If there is no allotment returned, it will return the transport allotment with the lowest departure date from future that matches those filters for a wider period.

Typical request filters:

* AgencyID: integer
* DepartureID: integer
* CountryID: integer (if = 0, this filter is not taken in consideration)
* ResortID: integer (can be 0)
* DepartureDate: date
* TravelLengthID: integer (can be 0; this ID is often taken using GetTravelLengths web-method)
* AdultsNumber: integer
* ChildrenNumber: integer
* ChildrenAges: array of integer

Typical response fields:

* Earliest departure date (the next matching departure, if none are found in the requested range)
* A list of transport allotments (departures), including:
  * departure date
  * departure and arrival names
  * airline (if relevant)
  * intervals and number of nights

### GetHotelsByAllotment <a href="#gethotelsbyallotment" id="gethotelsbyallotment"></a>

After you call **GetTransportAllotments**, you can use this method to list hotels with available rooms for a specific departure.

* AgencyID: integer
* ResortID: integer
* TransportAllotmentID: integer (taken from GetTransportAllotments response)
* IntervalID: integer (taken from GetTransportAllotment response)
* AdultsNumber: integer
* ChildrenNumber: integer
* DepartureDate: date

The response contains a list of hotels, including a limited set of price/departure options (often 3 departures per hotel).

### GetHotels <a href="#gethotels" id="gethotels"></a>

Similar to **GetHotelsByAllotment**, but designed for broader search.

The response includes:

* hotel information
* prices and availability for a limited number of departures (often 3)

> 💡 **Remarks:**

* Some filters are provided as a list of IDs in one field (comma-separated).
* If such a field is empty, the service treats it as “no filter”.
* Required fields depend on your setup and use case.

Common request fields:

* Departures: String (int IDs separated by comma)
* Countries: (int IDs separated by comma)
* Resorts: (int IDs separated by comma)
* Hotels: (int IDs separated by comma). If empty, the API searches for all the hotels that conforms to the other filters
* Surcharges. This filter has 3 attributes: Products (of type IntArrayAsString), Transfers (IntArrayAsString), Insurances (IntArrayAsString). This field is not actually a filter. It only asks for the specified surcharges, if they are available and applicable, to be included in response (along with some information about them). This field is used in the booking popup from office.
* Categories, with 2 attributes of type IntArrayAsString: Hotels and Resorts (filtering by hotels and resorts categories). Also this field is used in the booking popup from office
* AgencyID: integer
* IntervalID: integer (1,2,3,4)
* IntervalDays: integer (take only the trips with this total duration, in days)
* DepartureDate: date (search offers that depart starting with this date)
* MaxDepartureDate: date (optional; if not specified, it will be set as DepartureDate + 12 months)
* AdultsNumber: integer
* ChildrenNumber: integer
* ChildrenAges: IntArrayAsString
* AdultsAges: IntArrayAsString
* RoomsPax: allows to specify a custom passengers distribution in rooms
* StaticFilters, with two inner elements: \_ TransportHotel (Boolean): the API will return the trips that represent only a flight reservation \_ Stars (string): filter the hotels by stars, that are at least equal to that value (eg: “1”, “2+”)
* DynamicFilters, an array of DynamicFilter. This filter is used for hotel facilities filtering. You have the possibility to use comparison operators (eq = equal, ne = not equal, lt = lower than, le = lower or equal, ge = greater or equal, gt = greater than, bt=between). A dynamic filter requires an ID (the facility ID), an operator, and a “Value” (we will compare the hotel facility’s value to this field). If you use the “bt” operator, “ValueTo” should be also provided (eg: HotelFacility between Value AND ValueTo)
* SortBy: integer (possible values: 1 – Local Center, 2 – Beach, 3 – Construction Year, 4 – Resort Name, other values – Contract Type)
* ShowAllHotels: Boolean - if true, the API will search for a larger period(2 years), so that all the hotels that have free rooms (enough for the number of passengers given in request) will be returned
* NotOnlyInternetSale (Boolean, default value = false). By default, this method returns only the entities that are published on the web. If you want to get ALL of them, you have to set this field to true (for example, a hotel may be assigned to an agency only for office access, as the agency doesn’t want to sell the offers from the public website, that consumes our API; in this case, if you want to get ALL the offers, even those that are not published on web, set this field to true)
* GetLinkedToProductDiscounts: Boolean - if true, the API will search for promotion discounts (or discounts linked to products) available that applies for passengers selection
* PriceFilter is valuable when you want to get only the offers filtered by a price range. It has three attributes: \_ ByTotalPrice (Boolean): filter by price/person if false or by total price (if adultsNumber+ChildrenNumber>1) when true \_ PriceFrom and PriceTo: get only the offers with prices in this range
* NumberOfDeparturesPerHotel. By default, this method returns only three departures per hotel. Using this field you are able to get a custom number of departures. If equal to 0, then all departures are returned, not only three of them
* PageNumber and PageSize are used for pagination

### GetHotelPrices <a href="#gethotelprices" id="gethotelprices"></a>

Returns prices for one hotel (`HotelID`).

Unlike **GetHotels**, this method can return all departures for the hotel (paged).

The request is similar to **GetHotels**, but also includes `HotelID`.

### GetHotDeals <a href="#gethotdeals" id="gethotdeals"></a>

This method provides information from the system about the hot deals for an agency. This is an extract of the fields that should be specified in request in order to retrieve the hot deals:

* AgencyID: integer (agency’s ID)
* AdultsNumber: integer
* ChildrenNumber: integer
* ChildrenAges: array of integer
* GetPriceInformation: Boolean - if true, the response will provide information about the allotment (price, flight changes etc.); see chapter 3.2.39.2
* GetLinkedToProductDiscounts: Boolean – if true, the API will search for promotion discounts (or discounts linked to products) available that applies for passengers selection
* Order: Boolean – if true the results are ordered by departure date, price and hotel name

The response that will be returned after calling this web-method should contain an array of HotDeals. This is an extract from the information that a HotDeal should contain:

* DaysNo: integer – the total number of days the passengers will spend the trip
* Departure: string – the departure name (e.g. Billund)
* DepartureDate: date
* HotelID: integer
* Name: string – the name of the hotel
* Resort: string – the name of the resort
* PhotoID: integer
* Price: integer - the price per passenger
* DiscountPrice: integer - another type of the price for this offer
* PriceListTransportAllotmentID: integer - is the ID of the offer
* CountryName: string
* ShortDescription: string – a short description of the hotel
* TransportType: string – e.g. FLY
* RoomTypes: array of RoomType (see chapter 3.2.39.2)

### GetXmlFeedOffers <a href="#getxmlfeedoffers" id="getxmlfeedoffers"></a>

This web-method returns an agency’s offers starting with a given departure date. It is intended to be called by an XML feed application that generates an XML at a particular time.

This is an extract of the information returned by this method:

* HotelID: integer – the ID of the hotel
* Name: string – hotel’s name
* LinkAlias: string – this is an alias for the hotel name; it will be used to form the URL where we can see the hotel offers
* ResortLinkAlias: string – similar to the previous; an alias for the resort name
* Code: string – hotel’s code name
* Description: string – a short description of the hotel
* LongDescription: string – a html description of the hotel
* Pictures: array of Picture (see chapter 3.2.39.2)
* IsTransportHotel: Boolean – if true, then this offer is only a flight (not with accommodation)
* Facilities: HotelFacilities (see chapter 3.2.39.2)
* Distances: Distances (see chapter 3.2.39.2)
* GeoLocation: GeoLocation (see chapter 3.2.39.2)
* Prices: array of PriceInformation (see chapter 3.2.39.2)

### GetAgencyHotels <a href="#getagencyhotels" id="getagencyhotels"></a>

For a given agency, returns minimal information of all active hotels, like: hotel ID, name, alias, code and whether it is published on web.

### GetFacilities <a href="#getfacilities" id="getfacilities"></a>

Returns information about all the facilities for a given agency: facility ID, category ID, facility name, facility data type, default value (as Value).

### GetSuppliers <a href="#getsuppliers" id="getsuppliers"></a>

For a given agency, returns information about all the suppliers, like: supplier ID, name and geo location (latitude and longitude).

### LogAllotmentsSearch <a href="#logallotmentssearch" id="logallotmentssearch"></a>

Using this method you are able to log in the system the visits for an array of transport allotments (actually ID of departures). In general, this ID is taken from PriceInformation, the field TransportAllotmentID.

### Methods Responses <a href="#methods-responses" id="methods-responses"></a>

This section lists the main data types returned by the service.

### Picture <a href="#picture" id="picture"></a>

* PictureID: integer
* Description: string

### Meta description <a href="#meta-description" id="meta-description"></a>

* Title: string
* Keywords: string
* Description: string

### GeoLocation <a href="#geolocation" id="geolocation"></a>

Location details:

* Latitude: decimal
* Longitude: decimal
* MapKeywords: string

### Distances <a href="#distances" id="distances"></a>

Distances from the hotel (values depend on setup):

* Center: integer
* Pool: integer
* Beach: integer
* Airport: integer
* Pub: integer

### Hotel facilities <a href="#hotelfacilites" id="hotelfacilites"></a>

These facilities will be used for describing a hotel.

* Restaurant: Boolean
* Bar: Boolean
* Lunch: Boolean
* SwimmingPool: Boolean
* Internet: Boolean
* WiFi: Boolean
* TV: Boolean
* SailorVacation: Boolean
* Golf: Boolean
* Wellness: Boolean
* AllInclusive: Boolean
* Refrigerator: Boolean
* Breakfast: Boolean

### HotelInfo <a href="#hotelinfo" id="hotelinfo"></a>

This type is used to store information about a hotel. The fields returned here are almost the same as those returned using GetHotelByID, but it contains only the information absolutely necessary.

* Name: string
* LinkAlias: string – this is an alias for the hotel name; it will be used to form the URL where we can see the hotel offers
* Code: string
* ResortID: integer
* CountryID: integer
* ResortName: string
* Country: string
* Stars: string
* ConstructionYear: integer
* NumberOfRooms: integer – the number of rooms in hotel
* Pictures: array of Picture (see 3.1)
* Prices: array of PriceInformation (see 3.7)
* IsTransportHotel: Boolean – this is a hotel made only to show that the offer is a flight only
* Facilities: HotelFacilities – (see 3.5)
* Distances: Distances – (see 3.4)
* GeoLocation: GeoLocation – (see 3.3)

### PriceInformation <a href="#priceinformation" id="priceinformation"></a>

This custom type will store information about the offers, as: prices, discounts and supplements, flight information (if the transport is FLIGHT), the number of available rooms, etc.

This is an extract of the stored information:

* PriceListTransportAllotmentID: integer – the ID of the offer
* InfantPrice: integer – the price for an infant
* Price1...Price4: integer – base prices for intervals 1...4
* DiscountPrice1…DiscountPrice4: integer – discount prices for intervals 1..4
* Discount1…Discount4: integer – discounts for intervals 1…4
* Supplement1…Supplement4: integer – supplements for intervals 1..4
* DiscountsInfo and SupplementsInfo are arrays of DiscountOrSupp that give more detailed information about Discount1..4 and Supplement1..4, information like the interval for which it applies, the amount, the name of the disc/sup, the room number for which it applies, availability date etc
* FreeRoomsCount1…FreeRoomsCount4: integer –the number of available rooms (for each interval period)
* ExtraBedDiscounts: ExtraBedDiscount – a custom type where will be stored information about this discount, if there will be passengers that will occupy extra beds
* BaseRoomTypeID: integer – ID of the room type for this offer
* HotDeal: Boolean –this offer is a hot deal if it’s value is true
* TotalPrice: integer – total price calculated for this offer (with discounts/supplements, extra bed discounts, surcharges)
* DiscountsLinkedToProducts: array of Discount – a custom type that displays information about a discount like the amount of the discount, the passenger age period interval for which it applies and how long it is applied
* Surcharges: this field contains three arrays of Surcharge: Products, Insurances and Transfers. If a web method’s request asks for any surcharge of these types, they are returned right here, with information like: ID, name, price, interval, room number, age from and age to
* ProductsAddedToBasicPrice: an array of ProductBasicInfo. These products are included in a room’s basic price. An element of type ProductBasicInfo gives the same information about a product like a Surcharge (see previous)
* TransportInformation: TransportInformation – a custom type that will store information about the transport, like: departure gateway, arrival gateway, transport type (e.g. FLIGHT, BUS), departure date, arrival date, flight number, and for each period interval, information about return: flight number, departure date, segments (if the flight is taken from GDS), flags that specifies if the flight is from GDS etc.

### RoomType <a href="#roomtype" id="roomtype"></a>

This type contains information regarding a room type from a hotel. This is an extract from the information that will be available:

* Name: string – room name
* RoomTypeID: integer
* OrdinaryBedNumber: integer – the number of beds from a room
* MinimumBedNumber: integer – minimum number of bed that should be occupied by passengers
* ExtraAdultBedNumber: integer – the number of extra beds for adults
* ExtraChildBedNumber: integer – the number of extra beds for children
* RoomsCount: integer – the number of available rooms for the given type
* PaxDistribution (an array of RoomPax): this field gives information about the distribution of passengers in rooms. This distribution is automatically done if it is not already specified in request (this is possible in GetHotels). A RoomPax specifies for a room number how many adults and the ages of the children that stay in it

***

### FAQ

<details>

<summary><strong>Who is this web service for?</strong></summary>

It is for systems that need to show Tourpaq offers and content outside Office.

The most common case is Web Booking.

</details>

<details>

<summary><strong>How do I get access?</strong></summary>

You need a service user (username + password).

The user must be set as a **Web User** and assigned to the right agencies/brands.

</details>

<details>

<summary><strong>What is the difference between arrival, destination, and resort?</strong></summary>

* **Arrival** usually means the arrival airport.
* **Resort** is the destination area where hotels are located.
* A resort is often called a “destination” in everyday language.

</details>

<details>

<summary><strong>Why do I get empty results?</strong></summary>

Common reasons:

* You are using an `AgencyID` the user is not assigned to.
* There are no transports/offers that match the filters.
* Internet sales is not enabled for the relevant transports/hotels.
* Your date range is too narrow.

</details>

<details>

<summary><strong>Which method should I start with?</strong></summary>

Most flows start with departures/countries/resorts, then transport departures, then hotels.

If you already know the departure you want, start with **GetTransportAllotments**.

</details>
