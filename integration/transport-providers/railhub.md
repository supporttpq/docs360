# RailHub

## **Overview**

The **RailHub** configuration page allows you to connect the system to the RailHub platform, enabling the retrieval and processing of rail transport services. This integration makes it possible for the system to search, book, and manage rail segments using RailHub’s API.

All fields on this page represent authentication and identification values required for secure communication with the RailHub system.

## **Purpose**

The purpose of the RailHub configuration module is to:

* Establish a secure connection between Tourpaq and RailHub.
* Authenticate API requests using RailHub credentials.
* Ensure that rail searches, bookings, and rate checks are correctly linked to your agency’s account.
* Allow the system to operate using real-time data from RailHub’s backend services.

By configuring these fields correctly, the system can communicate with RailHub to offer rail travel options to customers.

## **Fields**

<figure><img src="../../../.gitbook/assets/image (470).png" alt=""><figcaption></figcaption></figure>

| **Field**                | **Description**                                                                                                                                                                                     |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **RailHub URL**          | The base API endpoint for the RailHub service. All API requests (search, booking, availability) are sent to this URL. Must match the environment provided by RailHub (e.g., staging or production). |
| **RailHub Username**     | The username assigned to your organization. Used for authenticating all API requests.                                                                                                               |
| **RailHub Password**     | The password associated with the username. Required for secure login to the RailHub API.                                                                                                            |
| **RailHub Partner Code** | A unique partner identifier provided by RailHub. This code tells the system which agency account is being used.                                                                                     |
| **RailHub Agent Code**   | Identifies the specific agent or office performing operations within RailHub. Used for access control and auditing.                                                                                 |

## **How it works**

1. **Authentication**\
   When the system sends a request to RailHub (e.g., search for rail connections), it uses the **Username**, **Password**, and **Partner Code** to authenticate.
   * These values are included in the request headers or authentication payload.
   * RailHub verifies them before allowing further actions.
2.  **Service requests**\
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
