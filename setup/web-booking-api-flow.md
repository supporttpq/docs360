# Web Booking API flow

Bellow is described the flow that should be used to implement the **Web Booking** page using API

#### Request token[​](https://docs.tourpaq.com/docs/documentation/web-booking-api-flow#request-token) <a href="#request-token" id="request-token"></a>

The Token can be requested by calling /api/token using POST method.

Here is an example of the request token method using Fiddler:

`POST` [`https://api.tourpaq.com/api/token`](https://api.tourpaq.com/api/token) `HTTP/1.1 User-Agent: Fiddler Host: api.tourpaq.com Accept: application/json, text/javascript,`` `_`/`_`; q=0.01 Content-Type: application/x-www-form-urlencoded; charset=UTF-8 Authorization: Basic Ym9va2luZy50b3VycGFxLmRrOjRkMjBlMDVlNDZmNmU0YjhlZGE5NWYzNDRlZGUxMGI1 Content-Length: 75 Origin: nullgrant_type=password&scope=read&username=myUsername&password=password123`

The response would be:

"access\_token":"TM5yqqOSncppNvS0U8y6iH\_tP6u3Zl ... oXIy\_JRnZ2v2dEw", "token\_type":"bearer", "expires\_in":1799, "refresh\_token":"9cfc12729b8f4d85a4a078fdae204387"

The request parameters:

* **grant\_type** - The type of authentication in this case **password** is implemented this indicate that a **username** and **password** is required.
* **scope** - Is not really implemented. There are no restriction on this filed just pass the **read** it might be implemented in the future.
* **username** - The username of the user
* **password** - the password of the user

The Authorization Header must be sent using Basic realm and the value should be a base64 Encoded value which is composed by **client\_id** and **secret** separated by colon (:). Note that the client\_id and secret should not be stored on the client side for other to see. The best approach would be to request the token on the server side.

`booking.tourpaq.dk:5ad20e05e46f6e4b8eda95f344eca10b5`

The response is containing the following fields:

* **access\_token** - Is the token that will be used to authorize the other calls to the api
* **token\_type** - Is the realm of the Authorization.
* **expires\_in** - the Token expires in 1799 seconds.
* **refresh\_token** - since the token it expires so fast this token can be used to get a new access token without passing the username and password every 30 minutes. This token must be held secured on the server side.

#### Refresh Token[​](https://docs.tourpaq.com/docs/documentation/web-booking-api-flow#refresh-token) <a href="#refresh-token" id="refresh-token"></a>

The access token expires every 20 minutes and is not sliding expiration. the best practice would be to save the refresh token obtained from request token call on the client session an use that to authenticate the user again . After login retry the call. This way the user will not have to type the user and password again. When the Access Token is expired you will receive and 401 unauthorized response. In this case a new Access Token should be requested. Here is an example of doing that:

This is the 401 Unauthorized response

`HTTP/1.1 401 Unauthorized Content-Type: application/json; charset=utf-8 Server: Microsoft-IIS/7.5 WWW-Authenticate: Bearer X-Powered-By: ASP.NET Date: Wed, 01 Apr 2015 07:54:55 GMT Content-Length: 163`

In order to get a new access token:

`POST` [`https://api.tourpaq.com/api/token`](https://api.tourpaq.com/api/token) `HTTP/1.1 User-Agent: Fiddler Host: api.tourpaq.com Accept: application/json, text/javascript,`` `_`/`_`; q=0.01 Content-Type: application/x-www-form-urlencoded; charset=UTF-8 Authorization: Basic Ym9va2luZy50b3VycGFxLmRrOjRkMjBlMDVlNDZmNmU0YjhlZGE5NWYzNDRlZGUxMGI1 Content-Length: 75 Origin: nullgrant_type=refresh_token&scope=read&refresh_token=9cfc12729b8f4d85a4a078fdae204387`

#### Request offer[​](https://docs.tourpaq.com/docs/documentation/web-booking-api-flow#request-offer) <a href="#request-offer" id="request-offer"></a>

The offer request will provide with general information about the trip package.

This ordinary call to request offer:

`GET` [`https://api.tourpaq.com/api/offers?pltaIDs=1241703&roomNo=1&priceType=1&periodID=1&adultNo=1&childNo=2&infantNo=1&childrenAges=9`](https://api.tourpaq.com/api/offers?pltaIDs=1241703\&roomNo=1\&priceType=1\&periodID=1\&adultNo=1\&childNo=2\&infantNo=1\&childrenAges=9) `HTTP/1.1 User-Agent: Fiddler AbsoluteLinks: true Accept: application/hal+json Authorization: Bearer mWHMYrMnLW ... U-GUVneEDsxYLUgWCYdcw Host: api.tourpaq.com`

You can found more information about this call [https://api.tourpaq.com/help/api/offers](https://api.tourpaq.com/help/api/offers)

1. pltaIDs is offer unique identifier. This can be a single integer or a list of integers separated by comma. In case the pltaIDs is a single integer value the following parameters will be a single integer value: roomNo, priceType, adultNo, childNo, infantNo. In case the pltaIDs has a list of integers (ex. 23,26 ) then the parameters roomNo, priceType, adultNo, childNo, infantNo will have a list of integers with the same length as pltaIDs parameter.

Ex. a. pltaIDs=1241703,1241783\&roomNo=1,1\&priceType=1,1\&periodID=1\&adultNo=2,2\&childNo=0,1\&infantNo=1,0& childrenAges=9,1 b. pltaIDs=1241703,1241784\&roomNo=1,1\&priceType=1,1\&periodID=1\&adultNo=1,2\&childNo=2,1\&infantNo=1,0\&childrenAges=4,3,1|9

In the example a. there are two room types one room each type (roomNo=1,1), each room has two adults (adultNo=2,2), only the second room has a child (childNo=0,1) and only the first room has one infant(infantNo=1,0) since there is just one child.

In the example b. the childrenAges are split by a pipe to point out the room where the children will stay. The call will respond with a notificationStatus witch will be success, warning or error. The call will provide information about transport int filed help:transportavailability and for the hotel room in help:priceavailability.

#### Passenger distribution in rooms[​](https://docs.tourpaq.com/docs/documentation/web-booking-api-flow#passenger-distribution-in-rooms) <a href="#passenger-distribution-in-rooms" id="passenger-distribution-in-rooms"></a>

This call can be made asynchronous with offer call and it provides a list of passengers distributed in rooms based on query string. This list can be modified with real names. Products and supplements can be added or removed form individual passenger afterward the booking can be saved.

`GET` [`https://api.tourpaq.com/api/passengers?pltaIDs=1241703&roomNo=1&priceType=1&periodID=1&adultNo=1&childNo=2&infantNo=1&childrenAges=9,1&distribute=Manual`](https://api.tourpaq.com/api/passengers?pltaIDs=1241703\&roomNo=1\&priceType=1\&periodID=1\&adultNo=1\&childNo=2\&infantNo=1\&childrenAges=9,1\&distribute=Manual) `HTTP/1.1 User-Agent: Fiddler Host: api.tourpaq.com AbsoluteLinks: true Accept: application/hal+json Authorization: Bearer CS0V03QVH8 ... yNCFCUcZEbG8DL4U9qFXS`

More information about this call can be found at: [https://api.tourpaq.com/help/api/wb-passengers](https://api.tourpaq.com/help/api/wb-passengers)

#### Postal codes[​](https://docs.tourpaq.com/docs/documentation/web-booking-api-flow#postal-codes) <a href="#postal-codes" id="postal-codes"></a>

In order to save the booking postal code is mandatory. This call provide a list of postal codes. This call can be cached.

`GET` [`https://api.tourpaq.com/api/postcode/countries`](https://api.tourpaq.com/api/postcode/countries) `HTTP/1.1 User-Agent: Fiddler AbsoluteLinks: true Accept: application/hal+json Authorization: Bearer CS0V03QVH8HBeECL ... CUcZEbG8DL4U9qFXS Host: api.tourpaq.com`

More information about this call can be found at: [https://api.tourpaq.com/help/api/postalcode-countries](https://api.tourpaq.com/help/api/postalcode-countries)

#### Products[​](https://docs.tourpaq.com/docs/documentation/web-booking-api-flow#products) <a href="#products" id="products"></a>

Available product for current booking configuration

`GET` [`https://api.tourpaq.com/api/relevantProduct?pltaIDs=1241703&roomNo=1&priceType=1&periodID=1&adultNo=1&childNo=2&infantNo=1&childrenAges=9,1`](https://api.tourpaq.com/api/relevantProduct?pltaIDs=1241703\&roomNo=1\&priceType=1\&periodID=1\&adultNo=1\&childNo=2\&infantNo=1\&childrenAges=9,1) `HTTP/1.1 User-Agent: Fiddler AbsoluteLinks: true Accept: application/hal+json Authorization: Bearer 4L6-8EyfvS ... ZNOW4-L4 Host: api.tourpaq.com`

More information about this call can be found at: [https://api.tourpaq.com/help/api/wbrelevantproduct](https://api.tourpaq.com/help/api/wbrelevantproduct)

#### Supplements[​](https://docs.tourpaq.com/docs/documentation/web-booking-api-flow#supplements) <a href="#supplements" id="supplements"></a>

Available supplement for current booking configuration

`GET` [`https://api.tourpaq.com/api/relevantSupplement?pltaIDs=1241703&roomNo=1&priceType=1&periodID=1&adultNo=1&childNo=2&infantNo=1&childrenAges=9,1`](https://api.tourpaq.com/api/relevantSupplement?pltaIDs=1241703\&roomNo=1\&priceType=1\&periodID=1\&adultNo=1\&childNo=2\&infantNo=1\&childrenAges=9,1) `HTTP/1.1 User-Agent: Fiddler AbsoluteLinks: true Accept: application/hal+json Authorization: Bearer 4L6-8EyfvSkhsF9M ... OW4-L4 Host: api.tourpaq.com`

More information about this call can be found at: [https://api.tourpaq.com/help/api/svrelevantsupplement](https://api.tourpaq.com/help/api/svrelevantsupplement)

#### Save booking with no payment[​](https://docs.tourpaq.com/docs/documentation/web-booking-api-flow#save-booking-with-no-payment) <a href="#save-booking-with-no-payment" id="save-booking-with-no-payment"></a>

Save the booking or pending the booking to be saved after payment confirmation. In this case no payment is required so the booking will be saved on the spot.

More information about this call can be found at: [https://api.tourpaq.com/help/api/attemptToSaveBooking](https://api.tourpaq.com/help/api/attemptToSaveBooking) Information about how the filed RawBookingJson can be constructed can be found here [https://api.tourpaq.com/Help/ResourceModel?modelName=BookingInformationRequestBody](https://api.tourpaq.com/Help/ResourceModel?modelName=BookingInformationRequestBody) The passenger filed can be filled from the response of the api/passengers call

`POST` [`https://api.tourpaq.com/api/attemptToSaveBooking/`](https://api.tourpaq.com/api/attemptToSaveBooking/) `HTTP/1.1 Connection: keep-alive Content-Length: 17542 Content-Type: application/json; charset=UTF-8 Accept: application/hal+json Accept-Language: da-DK,da;q=0.9,en-US;q=0.8,en;q=0.7 Authorization: Bearer VREXm6eXsq8DU0weM77w ... nSVsJh5ipvTe1FWbA Host: api.tourpaq.com{ \"SaveTemporaryJson": true, "RawBookingJson": "{ "booking\" : \{ \"isLoaded\" : true, \"isSuccessfulyGenerated\" : true, \"adults\" : 2, \"children\" : 0, \"infants\" : 0, \"outboundTrAllId\" : 62199, \"homeboundTrAllId\" : 62200, \"periodId\" : 1, \"pltaID\" : [{ \"pltaId\" : 1422223, \"roomName\" : \"1-værelses lejlighed (2 personer)\", // truncated ... \} ], \"customer\" : { \"firstName\" : \"Olav\", \"lastName\" : \"Nygaard\", // truncated ... }, \"bonusCode\" : \"\", \"giftCardCode\" : \"\", \"passengers\" : [{ \"uniquePaxHash\" : \"NThlZTM3NGItZjU5OS00ZGVmLTlkZjEtOWI2MTE3NGRhMWU4\", \"ID\" : 0, \"index\" : 0, // truncated ... \"roomDetails\" : { \"isLocked\" : false, \"departureDate\" : \"2018-01-27T00:00:00\", // truncated ... }, \"extraBed\" : { \"discount\" : 0, // truncated ... }, \"transfer\" : { \"hasTransfer\" : false, // truncated ... }, \"pickupPoint\" : { \"nameWithPrice\" : \"undefined (NaN:NaN) - kr. \" }, \"selectedGenericAllotmentBindIDs\" : [], \"travelInsurance\" : { \"ID\" : 57, \"price\" : 0, // truncated ... }, \"cancellationInsurance\" : { \"hasCancelInsurance\" : false, // truncated ... }, \"travelAndCancellationInsurancesTotal\" : 0, \"selectedProducts\" : [{ \"isVisible\" : true, \"bindID\" : \"MzI5MzoyMDUxMDo=\", // truncated ... } ], \"selectedSupplements\" : [{ \"name\" : \"Olie- og Valutajusteringer\", // truncated ... } ], \"selectedDiscounts\" : [{ \"ID\" : 5017, // truncated ... } ], \"passengerRoomDiscount\" : { \"quantity\" : 1, // truncated ... }, \"additionalStuffPriceAccumulated\" : 199, \"totalIncludedInBasePriceProducts\" : 0, \"autoSelectedSupplementTotal\" : 181, \"total\" : 6499, \"selectedSeats\" : [], \"selectedAllotments\" : [], \"campaignDefinitionProductArray\" : [] }, { // truncated - passenger 2 ... } ], // truncated - passenger 2 ... \"saveBookingLink\" : \"/api/bookings/139\", \"waitListApproval\" : false, \"selectedCreditCardForPaymentForLogPurposes\" : \"\", }, \"payment\" : \"\" }" }`

Flow on a single page Application

![!](https://docs.tourpaq.com/assets/images/webbooingload-db98adb0698c6da3281a8372d9919df9.png)
