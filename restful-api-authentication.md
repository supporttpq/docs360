# Restful API authentication

Export \[\[API]] is based on a token authentication.

#### Request token[​](https://docs.tourpaq.com/docs/documentation/restful-api-authentication#request-token) <a href="#request-token" id="request-token"></a>

The Token can be requested by calling /api/token using POST method.

Here is an example of the request token method using Fiddler:

`POST` [`https://api.tourpaq.com/api/token`](https://api.tourpaq.com/api/token) `HTTP/1.1 User-Agent: Fiddler Host: api.tourpaq.com Accept: application/json, text/javascript,`` `_`/`_`; q=0.01 Content-Type: application/x-www-form-urlencoded; charset=UTF-8 Authorization: Basic Ym9va2luZy50b3VycGFxLmRrOjRkMjBlMDVlNDZmNmU0YjhlZGE5NWYzNDRlZGUxMGI1 Content-Length: 75 Origin: nullgrant_type=password&scope=read&username=name&password=password123`

The response would be:

"access\_token":"TM5yqqOSncppNvS0U8y6iH\_tP6u3Zl ... oXIy\_JRnZ2v2dEw", "token\_type":"bearer", "expires\_in":1799, "refresh\_token":"9cfc12729b8f4d85a4a078fdae204387"

The request parameters:

* //grant\_type// - The type of authentication in this case //password// is implemented this indicate that a //username// and //password// is required.
* //scope// - Is not really implemented. There are no restriction on this filed just pass the //read// it might be implemented in the future.
* //username// - The username of the user
* //password// - the password of the user

The Authorization Header must be sent using Basic realm and the value should be a base64 Encoded value which is composed by //client\_id// and //secret// separated by colon (:). Note that the client\_id and secret should not be stored on the client side for other to see. The best approach would be to request the token on the server side.

`booking.tourpaq.dk:5ad20e05e46f6e4b8eda95f344eca10b5`

The response is containing the following fields:

* //access\_token// - Is the token that will be used to authorize the other calls to the api
* //token\_type// - Is the realm of the Authorization.
* //expires\_in// - the Token expires in 1799 seconds.
* //refresh\_token// - since the token it expires so fast this token can be used to get a new access token without passing the username and password every 30 minutes. This token must be held secured on the server side.

#### Make an api request[​](https://docs.tourpaq.com/docs/documentation/restful-api-authentication#make-an-api-request) <a href="#make-an-api-request" id="make-an-api-request"></a>

Now that the access token is obtained API calls can be made like this:

`GET` [`https://api.tourpaq.com/api/HotelListExport/2013499853`](https://api.tourpaq.com/api/HotelListExport/2013499853) `HTTP/1.1 Host: api.tourpaq.com Accept: application/json, text/javascript,`` `_`/`_`; q=0.01 Accept-Language: en-US,en;q=0.5 Accept-Encoding: gzip, deflate Authorization: Bearer vtbwcg-TmHnA- ... _HqJ5bJ965iB0EVC_TEcjGNkRZ3OOOVKAGw`

The Authorization header is sent with Bearer realm and access token. the access token can be held on the client side.

#### Refresh Token[​](https://docs.tourpaq.com/docs/documentation/restful-api-authentication#refresh-token) <a href="#refresh-token" id="refresh-token"></a>

When the Access Token is expired you will receive and 401 unauthorized response. In this case a new Access Token should be requested. Here is an example of doing that:

This is the 401 Unauthorized response

`HTTP/1.1 401 Unauthorized Content-Type: application/json; charset=utf-8 Server: Microsoft-IIS/7.5 WWW-Authenticate: Bearer X-Powered-By: ASP.NET Date: Wed, 01 Apr 2015 07:54:55 GMT Content-Length: 163`

In order to get a new access token:

`POST` [`https://api.tourpaq.com/api/token`](https://api.tourpaq.com/api/token) `HTTP/1.1 User-Agent: Fiddler Host: api.tourpaq.com Accept: application/json, text/javascript,`` `_`/`_`; q=0.01 Content-Type: application/x-www-form-urlencoded; charset=UTF-8 Authorization: Basic Ym9va2luZy50b3VycGFxLmRrOjRkMjBlMDVlNDZmNmU0YjhlZGE5NWYzNDRlZGUxMGI1 Content-Length: 75 Origin: nullgrant_type=refresh_token&scope=read&refresh_token=9cfc12729b8f4d85a4a078fdae204387`
