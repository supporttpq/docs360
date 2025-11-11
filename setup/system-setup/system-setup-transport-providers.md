# System Setup - Transport Providers

### **Overview**

The **Transport Providers** section in **System Setup** allows the system administrator to define and configure global settings related to transport service providers (such as flight, train, or other travel connections). These parameters determine how booking, payment, and ticketing operations are handled when interacting with external transport APIs or providers.

### **Purpose**

This configuration ensures consistent handling of transport-related transactions across all providers. It defines:

* The default currency and payment behavior
* Card and payment credentials used for automated processes
* Rules for selecting and updating transport data
* Timing and restrictions for reservation management

### **Tabs**

The **Transport Providers** section includes several tabs, such as:

* **General** – Core configuration and default rules
* **TravelPort**, **Paxport**, **Amadeus**, **RailHub** – Provider-specific connection and authentication details

The current documentation covers the **General** tab.

***

### **General Tab Fields**

<figure><img src="../../.gitbook/assets/image (466).png" alt=""><figcaption></figcaption></figure>

| **Field**                                      | **Description**                                                                                                                                                                                        |
| ---------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Currency**                                   | Defines the currency used for transport transactions. Example: _EUR_.                                                                                                                                  |
| **Price change margin**                        | The percentage margin applied when a price change occurs (e.g., 50%).                                                                                                                                  |
| **Payment rule**                               | Sets the rule for payment processing (e.g., _Normal deposit + GDS cost_). Determines how deposits and GDS-related fees are applied.                                                                    |
| **Card Owner**                                 | Name of the cardholder used for automated payments or API-based transactions.                                                                                                                          |
| **Card Type**                                  | Type of payment card used (e.g., _VISA_, _MasterCard_).                                                                                                                                                |
| **Card Number**                                | Stores the payment card number used for automated processes. Clicking **Change** allows updating card details.                                                                                         |
| **Expiration Date (Year / Month)**             | Defines the card’s expiration date. Both _Year_ and _Month_ are required.                                                                                                                              |
| **CVC**                                        | The card security code used for transaction validation.                                                                                                                                                |
| **Days number for check PNR**                  | Indicates how many days before departure the system should check PNR (Passenger Name Record) information.                                                                                              |
| **Show TicketNo on Ticket**                    | Display the GDS ticket number on the print ticket                                                                                                                                                      |
| **Time frame before departure**                | The number of minutes before the departure for remove a flight from booking when the Booking Date is the Departure Date.                                                                               |
| **Transport selection rule**                   | Determines the logic for selecting transport offers, e.g., _Cached flight/winning deal_.                                                                                                               |
| **Don’t update DTS on Create GDS Reservation** |  DTS _(Data Transport System)_ is not included when GDS Reservation is created                                                                                                                         |
| **Default Provider**                           | Defines which transport provider is used by default (e.g., _Paxport API_).                                                                                                                             |
| **Early arrival limit**                        | If the arrival time for departure is before the limit, then the guest needs the hotel on the day before the arrival date, adding one extra day (+DAYS) to the stay. This applies only to new bookings. |
| **Late departure limit**                       | If the departure time for the return home is after the limit, then the guest needs the hotel room one day extra (LAND DAYS), adding one extra day to the stay. This applies only to the new bookings   |

### **Providers Settings**

### &#x20;_**TravelPort**_**&#x20;– Configuration Settings**

**Overview**

The **TravelPort** tab under **System Setup → Transport Providers** is used to configure credentials and parameters for integrating with the **TravelPort GDS (Global Distribution System)**. This setup enables communication between your platform and TravelPort for searching, booking, and ticketing transport services (such as flights).

**Purpose**

This configuration ensures secure and accurate connection between the system and the TravelPort API. It defines:

* Authentication credentials and branch details
* Ticketing and queue management rules
* Fare types to be used in searches
* Email communication for confirmation and notifications

**Fields Description**

<figure><img src="../../.gitbook/assets/image (467).png" alt=""><figcaption></figcaption></figure>

| **Field**                           | **Description**                                                                                                                                                                                  |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **User**                            | The TravelPort Universal API username or key used to authenticate requests.                                                                                                                      |
| **Password**                        | The password linked to the TravelPort user. Required for all API communications.                                                                                                                 |
| **Branch**                          | Identifies the specific branch or agency code registered with TravelPort (e.g., _P107659_).                                                                                                      |
| **Days number for ticketing**       | The number of days for ticketing after the reservation is made. Example: _3_ days.                                                                                                               |
| **Max GDS search results**          | Limits the number of results returned by the TravelPort GDS when searching for offers. Example: _3_.                                                                                             |
| **Queue Number**                    | Specifies the TravelPort queue where bookings or messages will be placed (e.g., _55_).                                                                                                           |
| **Pseudo City Code (PCC)**          | The TravelPort location code representing the main agency office (e.g., _TTL_).                                                                                                                  |
| **Own Pseudo City Code**            | Used when a secondary or internal PCC must be defined for specific operations (e.g., _6EE3_).                                                                                                    |
| **Fares Indicator**                 | <p>Defines which fare types are retrieved from the system. Options include: </p><ul><li><em>Public Fares</em></li><li><em>Private Fares</em></li><li><em>Public and Private Fares</em></li></ul> |
| Confirmation Email                  | The email for the confirmations received from TravelPort after booking.                                                                                                                          |
| Submit Customer Email to TravelPort | Send to TravelPort customer email, and not the company email.                                                                                                                                    |

**How to Use**

1. **Access the page**\
   Navigate to: `System Setup → Transport Providers → TravelPort`
2. **Enter authentication data**\
   Fill in your _User_, _Password_, and _Branch_ information provided by TravelPort.
3. **Configure operational parameters**
   * Define ticketing time limits and GDS result limits.
   * Specify queue and pseudo city codes based on your agency setup.
4. **Set fare and email preferences**
   * Choose the _Fares Indicator_ according to your agency’s fare agreements.
   * Add a _Confirmation email_ for internal notifications.
   * Enable _Submit Customer Email to TravelPort_ if direct communication is desired.
5. **Save configuration**\
   After completing all fields, click **Save** to apply the configuration. The connection will then be active for TravelPort-based searches and bookings.

### _**Paxport**_**&#x20;– Configuration Settings**

**Overview**

The **Paxport** tab under **System Setup → Transport Providers** allows configuration of the integration between the platform and the **Paxport API**. This setup enables the system to communicate with Paxport’s services for flight bookings.

**Purpose**

This configuration establishes the technical connection parameters required to authenticate and interact with the Paxport environment. It ensures the system can send requests and retrieve information (such as availability, fares, or booking confirmations) from the Paxport platform.

**Fields Description**

<figure><img src="../../.gitbook/assets/image (468).png" alt=""><figcaption></figcaption></figure>

| **Field**                       | **Description**                                                                                                              |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **Paxport API URL**             | The endpoint address of the Paxport API. This is where the system sends requests. Example: `https://api.paxport.net/`        |
| **Paxport Syndicator ID**       | The unique identifier provided by Paxport to identify your agency or syndicator account.                                     |
| **Paxport Target**              | Defines the operational environment — typically _test_ or _production_. Use _test_ for sandbox validation before going live. |
| **Paxport Version**             | Specifies the version of the Paxport API to be used.                                                                         |
| **Paxport Syndicator Password** | The password or API key associated with the **Paxport Syndicator ID**, used for authentication.                              |

**How to Use**

1. **Access the page**\
   Navigate to: `System Setup → Transport Providers → Paxport`
2. **Enter the API details**
   * Fill in the **Paxport API URL** as provided by Paxport.
   * Add your **Syndicator ID** and **Password** for authentication.
3. **Select the environment**
   * Set **Paxport Target** to _test_ or _production_ depending on your usage.
   * Specify the **API Version** if required by Paxport’s technical team.
4. **Save configuration**\
   After completing all fields, click **Save** to apply the setup. The system will now be able to interact with Paxport services for flight searches, bookings, and ancillary data retrieval.

### _**Amadeus**_**&#x20;– Configuration Settings**

**Overview**

The **Amadeus** tab is used to configure the connection between the Tourpaq platform and the Amadeus GDS (Global Distribution System). These settings allow the system to authenticate, communicate, retrieve flight information, and perform flight searches through the Amadeus API services.

All fields must be filled with valid credentials provided by Amadeus or by the agency’s Amadeus administrator.

**Field Descriptions**

<figure><img src="../../.gitbook/assets/image (469).png" alt=""><figcaption></figcaption></figure>

| **Field**              | **Description**                                                                                                                     |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| **API Key**            | The authentication key provided by Amadeus. Required to authorize all API requests.                                                 |
| **API Secret**         | The secret token paired with the API Key. Used to generate secure authentication tokens. Must remain confidential.                  |
| **Target**             | Identifier for the Amadeus environment (test or production). Determines which Amadeus system the platform communicates with.        |
| **URL**                | The endpoint address for the Amadeus API services. Defines where requests are sent (e.g., test or live environment).                |
| **Office ID**          | The Amadeus office identifier assigned to your agency. Required for creating PNRs and other booking-related actions.                |
| **Duty Code**          | Code defining the agent’s permission level within Amadeus. Often matches the Office ID.                                             |
| **Use Instant Search** | Enables the Amadeus Instant Search method for faster flight availability responses. When disabled, standard search is used instead. |

**Usage Notes**

* All fields must be valid for the system to perform Amadeus flight searches or booking actions.
* Credentials differ between **TEST** and **PRODUCTION** environments — ensure correct values before switching.
* Any change in API Key or Secret requires saving the configuration and re-authenticating.

### _**RailHub -**_**&#x20;Configuration Settings**

**Overview**

The **RailHub** configuration page allows you to connect the system to the RailHub platform, enabling the retrieval and processing of rail transport services. This integration makes it possible for the system to search, book, and manage rail segments using RailHub’s API.

All fields on this page represent authentication and identification values required for secure communication with the RailHub system.

**Purpose**

The purpose of the RailHub configuration module is to:

* Establish a secure connection between Tourpaq and RailHub.
* Authenticate API requests using RailHub credentials.
* Ensure that rail searches, bookings, and rate checks are correctly linked to your agency’s account.
* Allow the system to operate using real-time data from RailHub’s backend services.

By configuring these fields correctly, the system can communicate with RailHub to offer rail travel options to customers.

**Field Explanation**

<figure><img src="../../.gitbook/assets/image (470).png" alt=""><figcaption></figcaption></figure>

| **Field**                | **Description**                                                                                                                                                                                     |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **RailHub URL**          | The base API endpoint for the RailHub service. All API requests (search, booking, availability) are sent to this URL. Must match the environment provided by RailHub (e.g., staging or production). |
| **RailHub Username**     | The username assigned to your organization. Used for authenticating all API requests.                                                                                                               |
| **RailHub Password**     | The password associated with the username. Required for secure login to the RailHub API.                                                                                                            |
| **RailHub Partner Code** | A unique partner identifier provided by RailHub. This code tells the system which agency account is being used.                                                                                     |
| **RailHub Agent Code**   | Identifies the specific agent or office performing operations within RailHub. Used for access control and auditing.                                                                                 |

**How It Works**

1. **Authentication**\
   When the system sends a request to RailHub (e.g., search for rail connections), it uses the **Username**, **Password**, and **Partner Code** to authenticate.
   * These values are included in the request headers or authentication payload.
   * RailHub verifies them before allowing further actions.
2.  **Service Requests**\
    After successful authentication, the system interacts with RailHub through the **RailHub URL**, which defines the API environment:

    * Staging (test)
    * Production (live)

    All communication—search requests, pricing checks, and booking operations—uses this endpoint.
3. **Agent Identification**\
   The **RailHub Agent Code** ensures that the correct office or department is recorded in RailHub.\
   This helps with:
   * Usage tracking
   * Access control
   * Reporting
4. **Data Flow**
   * Tourpaq sends a request (e.g., search for rail tickets).
   * RailHub validates the credentials.
   * RailHub returns available rail connections, prices, and other details.
   * Tourpaq displays the results so the user can select and book them.
5. **Error Handling**\
   If any credential is incorrect (URL, Username, Password, Partner Code, Agent Code), RailHub will reject the request.\
   The system will show errors such as “Authentication failed” or “Access denied.”
