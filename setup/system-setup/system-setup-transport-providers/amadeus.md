# Amadeus

**Overview**

The **Amadeus** tab is used to configure the connection between the Tourpaq platform and the Amadeus GDS (Global Distribution System). These settings allow the system to authenticate, communicate, retrieve flight information, and perform flight searches through the Amadeus API services.

All fields must be filled with valid credentials provided by Amadeus or by the agency’s Amadeus administrator.

**Fields**

<figure><img src="../../../.gitbook/assets/image (661).png" alt=""><figcaption></figcaption></figure>

| **Field**                    | **Description**                                                                                                                     |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| **API Key**                  | The authentication key provided by Amadeus. Required to authorize all API requests.                                                 |
| **API Secret**               | The secret token paired with the API Key. Used to generate secure authentication tokens. Must remain confidential.                  |
| **Target**                   | Identifier for the Amadeus environment (test or production). Determines which Amadeus system the platform communicates with.        |
| **URL**                      | The endpoint address for the Amadeus API services. Defines where requests are sent (e.g., test or live environment).                |
| **Office ID**                | The Amadeus office identifier assigned to your agency. Required for creating PNRs and other booking-related actions.                |
| **Duty Code**                | Code defining the agent’s permission level within Amadeus. Often matches the Office ID.                                             |
| **Use Instant Search**       | Enables the Amadeus Instant Search method for faster flight availability responses. When disabled, standard search is used instead. |
| **Automatic ticket issuing** | Enables automated issuing of e-tickets for GDS bookings handled through Amadeus.                                                    |

**Usage notes**

* All fields must be valid for the system to perform Amadeus flight searches or booking actions.
* Credentials differ between **test** and **production** environments. Verify values before switching.
* Any change in API Key or Secret requires saving the configuration and re-authenticating.
