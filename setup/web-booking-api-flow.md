# Web Booking API flow

### Overview

This page lists the usual API calls behind a web booking flow.

Follow the steps in order.

{% hint style="warning" %}
Never expose your API **client secret** in a browser or mobile app.

Keep it on your server.
{% endhint %}

### Flow in short

1. Request a token (log in).
2. Request an offer (price and availability).
3. Get the passenger list (and set names).
4. Load postal codes (required to save).
5. Load products and supplements.
6. Save the booking.

#### Request token <a href="#request-token" id="request-token"></a>

Request a token by calling `/api/token` with `POST`.

You will use the returned `access_token` in later calls.

For more details about authentication, see [Restful API authentication](../restful-api-authentication.md).

Example request (placeholders):

```
POST https://api.tourpaq.com/api/token
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
Authorization: Basic <base64(client_id:secret)>

grant_type=password&scope=read&username=<username>&password=<password>
```

Example response:

```json
{
  "access_token": "<access_token>",
  "token_type": "bearer",
  "expires_in": 1799,
  "refresh_token": "<refresh_token>"
}
```

Request parameters:

* **grant\_type** - Authentication type. `password` requires username and password.
* **scope** - Not currently enforced. Use `read`.
* **username** - The user name.
* **password** - The password.

The Authorization header uses Basic authentication.

It is a Base64-encoded value built from `client_id:secret`.

Do not store the client secret on the client side.

Example format:

`client_id:secret`

Response fields:

* **access\_token** - Token used to authorize other API calls.
* **token\_type** - Authorization scheme (usually `bearer`).
* **expires\_in** - Token lifetime in seconds.
* **refresh\_token** - Used to request a new access token. Store it securely.

#### Refresh token <a href="#refresh-token" id="refresh-token"></a>

The access token expires after a short time.

When it expires, the API returns `401 Unauthorized`.

Use the `refresh_token` to request a new access token.

Store refresh tokens securely.

This is the `401 Unauthorized` response:

`HTTP/1.1 401 Unauthorized Content-Type: application/json; charset=utf-8 Server: Microsoft-IIS/7.5 WWW-Authenticate: Bearer X-Powered-By: ASP.NET Date: Wed, 01 Apr 2015 07:54:55 GMT Content-Length: 163`

In order to get a new access token:

```
POST https://api.tourpaq.com/api/token
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
Authorization: Basic <base64(client_id:secret)>

grant_type=refresh_token&scope=read&refresh_token=<refresh_token>
```

#### Request offer <a href="#request-offer" id="request-offer"></a>

The offer call returns general information about the trip package.

Example offer request:

`GET` [`https://api.tourpaq.com/api/offers?pltaIDs=1241703&roomNo=1&priceType=1&periodID=1&adultNo=1&childNo=2&infantNo=1&childrenAges=9`](https://api.tourpaq.com/api/offers?pltaIDs=1241703\&roomNo=1\&priceType=1\&periodID=1\&adultNo=1\&childNo=2\&infantNo=1\&childrenAges=9) `HTTP/1.1 User-Agent: Fiddler AbsoluteLinks: true Accept: application/hal+json Authorization: Bearer mWHMYrMnLW ... U-GUVneEDsxYLUgWCYdcw Host: api.tourpaq.com`

You can find more information about this call here:

https://api.tourpaq.com/help/api/offers

`pltaIDs` is the offer identifier.

It can be one value or a list of values separated by commas.

If `pltaIDs` is a list (for example `23,26`), these parameters must also be lists with the same number of values:

* `roomNo`
* `priceType`
* `adultNo`
* `childNo`
* `infantNo`

Examples:

*   Example A (two offers, one child in room 2):

    ```
    pltaIDs=1241703,1241783&roomNo=1,1&priceType=1,1&periodID=1&adultNo=2,2&childNo=0,1&infantNo=1,0&childrenAges=9,1
    ```
*   Example B (children split by room using `|`):

    ```
    pltaIDs=1241703,1241784&roomNo=1,1&priceType=1,1&periodID=1&adultNo=1,2&childNo=2,1&infantNo=1,0&childrenAges=4,3,1|9
    ```

In example (a), there are two room types.

Each room has two adults.

Only the second room has a child.

Only the first room has an infant.

In example (b), `childrenAges` uses `|` to separate children by room.

The response includes a `notificationStatus` field that can be `success`, `warning`, or `error`.

#### Passenger distribution in rooms <a href="#passenger-distribution-in-rooms" id="passenger-distribution-in-rooms"></a>

This call returns a list of passengers distributed into rooms.

You can call it at the same time as the offer call.

You can then:

* replace placeholder passenger names with real names
* add or remove products and supplements per passenger
* save the booking

`GET` [`https://api.tourpaq.com/api/passengers?pltaIDs=1241703&roomNo=1&priceType=1&periodID=1&adultNo=1&childNo=2&infantNo=1&childrenAges=9,1&distribute=Manual`](https://api.tourpaq.com/api/passengers?pltaIDs=1241703\&roomNo=1\&priceType=1\&periodID=1\&adultNo=1\&childNo=2\&infantNo=1\&childrenAges=9,1\&distribute=Manual) `HTTP/1.1 User-Agent: Fiddler Host: api.tourpaq.com AbsoluteLinks: true Accept: application/hal+json Authorization: Bearer CS0V03QVH8 ... yNCFCUcZEbG8DL4U9qFXS`

More information:

https://api.tourpaq.com/help/api/wb-passengers

#### Postal codes <a href="#postal-codes" id="postal-codes"></a>

Postal code is required to save a booking.

This call provides a list of postal codes.

You can usually cache this response.

`GET` [`https://api.tourpaq.com/api/postcode/countries`](https://api.tourpaq.com/api/postcode/countries) `HTTP/1.1 User-Agent: Fiddler AbsoluteLinks: true Accept: application/hal+json Authorization: Bearer CS0V03QVH8HBeECL ... CUcZEbG8DL4U9qFXS Host: api.tourpaq.com`

More information:

https://api.tourpaq.com/help/api/postalcode-countries

#### Products <a href="#products" id="products"></a>

Available products for the current booking configuration.

`GET` [`https://api.tourpaq.com/api/relevantProduct?pltaIDs=1241703&roomNo=1&priceType=1&periodID=1&adultNo=1&childNo=2&infantNo=1&childrenAges=9,1`](https://api.tourpaq.com/api/relevantProduct?pltaIDs=1241703\&roomNo=1\&priceType=1\&periodID=1\&adultNo=1\&childNo=2\&infantNo=1\&childrenAges=9,1) `HTTP/1.1 User-Agent: Fiddler AbsoluteLinks: true Accept: application/hal+json Authorization: Bearer 4L6-8EyfvS ... ZNOW4-L4 Host: api.tourpaq.com`

More information:

https://api.tourpaq.com/help/api/wbrelevantproduct

#### Supplements <a href="#supplements" id="supplements"></a>

Available supplements for the current booking configuration.

`GET` [`https://api.tourpaq.com/api/relevantSupplement?pltaIDs=1241703&roomNo=1&priceType=1&periodID=1&adultNo=1&childNo=2&infantNo=1&childrenAges=9,1`](https://api.tourpaq.com/api/relevantSupplement?pltaIDs=1241703\&roomNo=1\&priceType=1\&periodID=1\&adultNo=1\&childNo=2\&infantNo=1\&childrenAges=9,1) `HTTP/1.1 User-Agent: Fiddler AbsoluteLinks: true Accept: application/hal+json Authorization: Bearer 4L6-8EyfvSkhsF9M ... OW4-L4 Host: api.tourpaq.com`

More information:

https://api.tourpaq.com/help/api/svrelevantsupplement

#### Save booking with no payment <a href="#save-booking-with-no-payment" id="save-booking-with-no-payment"></a>

Use this call to save the booking right away when no payment is needed.

More information:

* https://api.tourpaq.com/help/api/attemptToSaveBooking
* https://api.tourpaq.com/Help/ResourceModel?modelName=BookingInformationRequestBody

The passenger data can be filled from the `/api/passengers` response.

Example request (headers only):

```
POST https://api.tourpaq.com/api/attemptToSaveBooking
Content-Type: application/json; charset=UTF-8
Authorization: Bearer <access_token>
```

{% hint style="warning" %}
This call includes personal data (names, contact details, etc.).

Avoid logging request bodies in plain text.
{% endhint %}

Flow on a single page Application

![!](https://docs.tourpaq.com/assets/images/webbooingload-db98adb0698c6da3281a8372d9919df9.png)

### Related pages

* [Restful API authentication](../restful-api-authentication.md)

### FAQ

<details>

<summary><strong>Why do I get <code>401 Unauthorized</code>?</strong></summary>

Most often, the access token expired.

Refresh the token, then retry the call.

</details>

<details>

<summary><strong>What is <code>pltaIDs</code>?</strong></summary>

It is the offer identifier used to request pricing and availability.

</details>

<details>

<summary><strong>Why do I need postal codes?</strong></summary>

Postal code is required when you save a booking.

Load postal codes before saving.

</details>

<details>

<summary><strong>How do I handle multiple rooms in one call?</strong></summary>

Use comma-separated lists for parameters like `pltaIDs`, `roomNo`, and passenger counts.

Use `|` in `childrenAges` to split children by room.

</details>

<details>

<summary><strong>Is it safe to store the client secret in a web app?</strong></summary>

No.

Keep the client secret on your server.

</details>

<details>

<summary><strong>Where can I see all parameters and response fields for an endpoint?</strong></summary>

Use the API help pages linked under each section.

They list the full input and output for each endpoint.

</details>
