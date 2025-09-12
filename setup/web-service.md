---
hidden: true
---

# Web service

The web-service purpose would be to select information inserted from office – defined for a certain agency or company – to be displayed on web booking. The information will regard departures/arrivals gateways, hotels, products, etc.

The v3.0 release of the Tourpaq included a new feature, a new popup in booking page that supports a more complex offers search in the system. This feature could be better done by consuming the web-service (GetHotels), which has already provided this type of functionality. However, some changes have been done in order to support all the requirements for this feature (filtering by multiple hotels, departures, countries, surcharges, prices etc).

### Security <a href="#security" id="security"></a>

Regarding the security, each API consumer is given a username and password they have to use in order to have access to the methods. This user has to be set as “Web User” from back-office application. Another important thing, the user is able to make requests only using its assigned agencies to the methods that have in request the AgencyID field. The consumer will use basic authentication when he will call any method from API.

### Methods Description <a href="#methods-description" id="methods-description"></a>

Forward down are explained the web-methods exposed by the web-service.

### GetDepartures <a href="#getdepartures" id="getdepartures"></a>

This method should return all departure gateways for an agency.

The following is an extract from the information that should be available for a departure:

* Name: string
* IATA: string
* Country: string
* CountryCode: string

### GetDeparturesFromResort <a href="#getdeparturesfromresort" id="getdeparturesfromresort"></a>

This method should return all departure gateways for an agency when the client knows the ResortID (a resort is often called destination, but is not the same as Arrival)

### GetDestinations <a href="#getdestinations" id="getdestinations"></a>

A web method for taking all arrival gateways for an agency is also necessary. Information like the following should be available for an arrival:

* Name: string
* IATA: string
* Country: string
* CountryCode: string

### GetCountries <a href="#getcountries" id="getcountries"></a>

Is similar to GetDestinations, but it will return the countries where the transports arrive. It searches for the transports defined in system that have the specified Departure from Request, and returns the transport arrival’s country.

If DepartureID = 0 then it will return all countries for which there are defined transports for that agency.

### GetResorts <a href="#getresorts" id="getresorts"></a>

Returns the resorts depending on the request, and these conditions should be fulfilled:

* existence of a transport for the given agency ID;
* this transport should be enabled for internet sales
* if Country > 0, then we filter the transports to those that arrive in that country
* for all the transports arrivals, the correspondent resorts are put in the response

### GetResortByID <a href="#getresortbyid" id="getresortbyid"></a>

This web-method exposes information about a resort. The following is an extract from the information that should be available for a resort:

* Name: string
* Code: string
* Description: string
* NumberOfRestaurantsAndBars: integer
* Shopping: string
* Attraction: string
* TeaserText: string
* Array of //Picture//(this type will be described in the next chapter: Methods Description)
* MetaDescription: //MetaDescription// (this type will be described in the next chapter: Methods Description)
* GeoLocation: GeoLocation (this type will be described in the next chapter: Methods Description)

### GetTravelLengths <a href="#gettravellengths" id="gettravellengths"></a>

For each transport we take the afferent interval periods, corresponding to the parameters specified in request. The client should have the possibility to filter them by an agency ID, departure, country, resort and departure date. The following is an extract from the information that should be available in response for an interval period(an array):

* Nights: integer (number of nights spent at hotel)
* Days: integer (trip total duration)
* TravelModeID: integer (ID to identify the transport mode: FLY, BUS, TRAIN)
* IntervalID: integer (possible values: 1,2,3,4)
* Name: string

### GetTravelLengthsForTransportAll <a href="#gettravellengthsfortransportall" id="gettravellengthsfortransportall"></a>

This web method should do the same as the previous one, with the only difference that it is used when the requester holds a PriceListTransportAllotment ID (this ID identifies a transport departure for a specific date, a hotel room and a price).

### GetTravelLengthByID <a href="#gettravellengthbyid" id="gettravellengthbyid"></a>

The response from GetTravelLengths/GetTravelLengthsForTransportAll contains also an ID: TravelLengthID. That ID will be useful for this web method to get information about a specific interval period. The response for this method is similar to GetTravelLengths response.

### GetHotelByID <a href="#gethotelbyid" id="gethotelbyid"></a>

Using this web method, the client can get information about a specific hotel when he holds a HotelID. This is an extract from the information available in response:

* HotelID: integer
* Name: string
* Code: string
* ResortID: integer (using this ID, the hotel’s resort can be identified)
* CountryID: integer
* ResortName: string (resort’s name)
* Address: string
* Phone: string
* Email: string
* Description: string
* GoogleDescription: string
* HtmlDescription: string
* Array of Picture
* MetaDescription: MetaDescription
* GeoLocation: GeoLocation
* Distances: Distances (this type will be described in the next chapter: 3.2.39.2)
* Facilities: Facilities (this type will be described in the next chapter: 3.2.39.2)

### GetProducts <a href="#getproducts" id="getproducts"></a>

By using this web-method, a user should be able to get all the products (extras) from the system, based on the filters specified in request. These are the fields that can filter the products:

* AgencyID: integer – return the products for a specific brand
* ArrivalID: integer – return the products available for the arrival with this ID
* ResortID: integer – the products available for the resort with this ID
* HotelID: integer – the products available for the hotel with this ID
* Catering: Boolean – the products of catering type
* Pension: Boolean – the products of pension type

This is an extract from the information available in response (consisting in an array of Product):

* Name: string – product name
* Code: string – product code
* Description: string – product description
* VipProduct: Boolean – the product is of “vip” type
* PartyPackage: Boolean - the product is of “party package” type
* Pension: Boolean – the product is of “pension” type
* Catering: Boolean – the product is of “catering” type
* Array of Price:
  * DateFrom: date –the product is available for bookings that are made starting with this date
  * DateTo: date - the product is available for bookings that are made earlier than this date
  * Price: integer – product price
  * GroupPrice: integer – product group price

### GetHotelDiscounts <a href="#gethoteldiscounts" id="gethoteldiscounts"></a>

In Tourpaq System, in the Hotel section are defined the extra beds discounts. The user should be able to get all the discounts for a given hotel starting from a given departure date.

This is an extract from the information available in response:

* Discount: integer – this is the value of the discount
* Age: integer – the discount is available only for this category of age
* IntervalID: integer – the discount is available only if the trip has this duration
* Percent: Boolean – if this field’s value is “true”, then the “Discount” value is a percent

### GetAvailableDays <a href="#getavailabledays" id="getavailabledays"></a>

By using this web-method, the user will be able to get the dates for which excursions are available (being given a start date and a maximum end date) – there are more filters that will be taken into account. This can be useful to highlight these days in a calendar, so the customers can make a better selection in the search form. If the selection from the search form changes, the returned dates will also change. If for example the end-user changes the departure, the method should return only those dates for which trips are available from the new selected departure.

* These are the fields that can be specified in the request:
* DepartureID: integer
* CountryID: integer
* ResortID: integer
* DepartureDate: date
* MaxDepartureDate: date
* AdultsNumber: integer
* ChildrenNumber: integer
* ChildrenAges: array of integer
* AgencyID: integer
* IntervalID: integer
* TransportHotel: Boolean

### GetTransportAllotments <a href="#gettransportallotments" id="gettransportallotments"></a>

This web-method should return all the transport allotments that correspond to the given filters; these transport allotments should have the departure date greater than a given date and lower than another given date.

If there is no allotment returned, it will return the transport allotment with the lowest departure date from future that matches those filters for a wider period.

These are the filters that the user can specify in request:

* AgencyID: integer
* DepartureID: integer
* CountryID: integer (if = 0, this filter is not taken in consideration)
* ResortID: integer (can be 0)
* DepartureDate: date
* TravelLengthID: integer (can be 0; this ID is often taken using GetTravelLengths web-method)
* AdultsNumber: integer
* ChildrenNumber: integer
* ChildrenAges: array of integer

This is an extract from the information that will be available in response:

* EarliestDepartureDate: date (if not allotments is returned, this will be the first departure date that matches the request; if the user will re-call the web-method with this date as DepartureDate, then it should return no allotments)
* TransportAllotments: TransportAllotment \_ TransportAllotment: integer \_ DepartureDate: date \_ Departure: string (departure name) \_ Arrival: string (arrival name) \_ Airline: string \_ Array of Interval: \_ IntervalID(period interval): integer \_ Nights: integer(the number of nights spent by the passengers at the hotel)

### GetHotelsByAllotment <a href="#gethotelsbyallotment" id="gethotelsbyallotment"></a>

After getting information from the system using GetTransportAllotments web-method, the user can call this method in order to take information about the hotels with available rooms. The most important filters the user should specify in the request are:

* AgencyID: integer
* ResortID: integer
* TransportAllotmentID: integer (taken from GetTransportAllotments response)
* IntervalID: integer (taken from GetTransportAllotment response)
* AdultsNumber: integer
* ChildrenNumber: integer
* DepartureDate: date

The response will contain an array of “Hotel” (custom type). More information about this type will be described in the next chapter (3.2.39.2). This type will also contain information (prices, rooms, flight information, discounts etc.) about a predetermined number of allotments (e.g. 3 allotments). This information will be stored in an object - Prices of type PriceInformation. Please refer to chapter 3.2.39.2 in order to see more details about this custom type.

### GetHotels <a href="#gethotels" id="gethotels"></a>

This method is similar to the previous one because the response is the same, as structure (not as values). In other words, the response contains an array of “HotelInfo” - a custom type that will be described next chapter (3.2.39.2). This type will also contain information (prices, rooms, flight information, discounts etc.) about a predetermined number of allotments (e.g. 3 allotments). This information will be stored in an object - Prices of type PriceInformation. To see more details about this custom type, please refer to chapter 3.2.39.2.

> 💡 **Remarks:**

* **IntArrayAsString** is actually the string type, this notation is a convention in this document, for simplicity, to highlight that it should be an array of integers separated by comma
* If a field of type IntArrayAsString is empty or null, then by convention we consider that this filter is ignored (an empty array)
* Only the underlined fields are mandatory.

The followings are the most important fields that will be taken in consideration for a request:

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

This method gets prices information about a given hotel (when the caller has a HotelID). It is similar to GetHotels, excepting that GetHotels returns information regarding only the first 3 allotments (and about the hotel), while GetHotelPrices returns all the allotments (paged).

In other words, after calling this method, the response will contain an array of PriceInformation, a custom type where is stored information (prices, rooms, flight information, discounts etc.) about each of the allotments. To see more details about this custom type, please refer to chapter 3.2.39.2. The request is similar to that of GetHotels. In addition, a new field should be given, HotelID. Also, here we don’t have the OptionalFilters field.

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

In this chapter will be enumerated the custom types that are used in some of the methods reponses.

### Picture <a href="#picture" id="picture"></a>

* PictureID: integer
* Description: string

### Meta description <a href="#meta-description" id="meta-description"></a>

* Title: string
* Keywords: string
* Description: string

### GeoLocation <a href="#geolocation" id="geolocation"></a>

This type contains information about geo location:

* Latitude: decimal
* Longitude: decimal
* MapKeywords: string

### Distances <a href="#distances" id="distances"></a>

This type contains information about distances from hotel:

* Center: integer
* Pool: integer
* Beach: integer
* Airport: integer
* Pub: integer

### HotelFacilites <a href="#hotelfacilites" id="hotelfacilites"></a>

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
