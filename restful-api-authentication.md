# Restful API authentication

#### Overview

The **Tourpaq Export API** uses **token-based authentication** to ensure secure access.\
Authentication tokens are issued via the `/api/token` endpoint and are required for all subsequent API calls.

***

### Requesting a Token

The authentication token can be requested by making a **POST** call to:

```
https://api.tourpaq.com/api/token
```

#### Example Request (using Fiddler)

```
POST https://api.tourpaq.com/api/token HTTP/1.1
User-Agent: Fiddler
Host: api.tourpaq.com
Accept: application/json, text/javascript, */*; q=0.01
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
Authorization: Basic Ym9va2luZy50b3VycGFxLmRrOjRkMjBlMDVlNDZmNmU0YjhlZGE5NWYzNDRlZGUxMGI1
Content-Length: 75
Origin: null

grant_type=password&scope=read&username=name&password=password123
```

#### Example Response

```json
{
  "access_token": "TM5yqqOSncppNvS0U8y6iH_tP6u3Zl...oXIy_JRnZ2v2dEw",
  "token_type": "bearer",
  "expires_in": 1799,
  "refresh_token": "9cfc12729b8f4d85a4a078fdae204387"
}
```

***

#### Request Parameters

| Parameter       | Description                                                                                |
| --------------- | ------------------------------------------------------------------------------------------ |
| **grant\_type** | Defines the type of authentication. The value `password` requires a username and password. |
| **scope**       | Currently not implemented (use `read`). Reserved for future functionality.                 |
| **username**    | The Tourpaq username.                                                                      |
| **password**    | The Tourpaq password.                                                                      |

***

#### Authorization Header

The **Authorization** header must use **Basic authentication**.\
The value should be a **Base64-encoded** string containing the **client\_id** and **secret**, separated by a colon `:`.

Example:

```
client_id:secret
```

Encoded as:

```
Authorization: Basic Ym9va2luZy50b3VycGFxLmRrOjRkMjBlMDVlNDZmNmU0YjhlZGE5NWYzNDRlZGUxMGI1
```

> ⚠️ **Important:** The `client_id` and `secret` must never be stored or exposed on the client side.\
> The safest approach is to handle the token request **on the server side**.

Example:

```
client_id: booking.tourpaq.dk  
secret: 5ad20e05e46f6e4b8eda95f344eca10b5
```

***

#### Response Fields

| Field              | Description                                                                                                  |
| ------------------ | ------------------------------------------------------------------------------------------------------------ |
| **access\_token**  | The token used to authorize subsequent API calls.                                                            |
| **token\_type**    | The authorization type (usually `Bearer`).                                                                   |
| **expires\_in**    | Token validity period in seconds (e.g., 1799 seconds ≈ 30 minutes).                                          |
| **refresh\_token** | Used to obtain a new access token without resubmitting credentials. Should be stored securely on the server. |

***

### Making an API Request

Once the access token is obtained, include it in the **Authorization** header for all API calls:

```
GET https://api.tourpaq.com/api/HotelListExport/2013499853 HTTP/1.1
Host: api.tourpaq.com
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Authorization: Bearer vtbwcg-TmHnA-..._HqJ5bJ965iB0EVC_TEcjGNkRZ3OOOVKAGw
```

> The `Authorization` header uses the **Bearer** scheme followed by the access token.\
> The access token can safely be stored on the client side.

***

### Refreshing the Token

When the **Access Token expires**, the API will respond with:

```
HTTP/1.1 401 Unauthorized
Content-Type: application/json; charset=utf-8
WWW-Authenticate: Bearer
```

In this case, a **new Access Token** must be requested using the **Refresh Token**.

#### Example Request

```
POST https://api.tourpaq.com/api/token HTTP/1.1
User-Agent: Fiddler
Host: api.tourpaq.com
Accept: application/json, text/javascript, */*; q=0.01
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
Authorization: Basic Ym9va2luZy50b3VycGFxLmRrOjRkMjBlMDVlNDZmNmU0YjhlZGE5NWYzNDRlZGUxMGI1
Content-Length: 75
Origin: null

grant_type=refresh_token&scope=read&refresh_token=9cfc12729b8f4d85a4a078fdae204387
```

The response will contain a new **access\_token** and **refresh\_token** pair.

***

#### Summary

| Action               | Endpoint                                    | Method | Authentication                   |
| -------------------- | ------------------------------------------- | ------ | -------------------------------- |
| Request Access Token | `/api/token`                                | POST   | Basic Auth (client\_id + secret) |
| Refresh Access Token | `/api/token`                                | POST   | Basic Auth (with refresh\_token) |
| Access Data          | Various (e.g., `/api/HotelListExport/{id}`) | GET    | Bearer Token                     |

***

Would you like me to make a **shorter “developer quick reference”** version too — with just the endpoints, headers, and key examples (for embedding in a dev portal or API guide)?
