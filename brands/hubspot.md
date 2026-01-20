# Hubspot

### **Overview**

The **HubSpot** section under _Brands Settings_ is used to connect Tourpaq with a company’s HubSpot account.\
This integration allows automatic synchronization of customer and booking data between the Tourpaq system and HubSpot CRM for marketing, reporting, or customer management purposes.

***

### **Purpose**

The purpose of this page is to:

* Establish the link between Tourpaq and HubSpot using an **API License Key**.
* Manage HubSpot **subscriptions** related to specific data sync processes (e.g., contact updates, booking imports, or campaign tracking).

A correct setup ensures that all customer information from Tourpaq is accessible and updated in HubSpot without manual export/import work.

***

### **Instructions**

#### **Access**

1. Navigate to **Users → Brands → Select an agency -> HubSpot**.
2. The HubSpot tab appears next to other configuration areas (e.g., _GDS, XML Feed, Business Central_).

***

#### **Fields Description**

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

| **Field**         | **Description**                                                                                                                                                                                                                                                                                                                              |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **License Key**   | <p>Enter the API key provided by HubSpot. This key authorizes Tourpaq to send and receive data securely.<br>🔹 <em>Format</em>: A long alphanumeric string (e.g., <code>f9d3e4b2-xxxx-xxxx-xxxx-9c14c62e1a10</code>).<br>🔹 <em>Required</em>: Yes — the integration won’t work without it.</p>                                              |
| **Subscriptions** | <p>HubSpot subscription name splitted by ; where the customer will be added.                             Enter the specific HubSpot subscription(s) used for synchronization.<br>These define which events or data sets will be synced (for example: <em>Customer Creation</em>, <em>Booking Update</em>, or <em>Lead Conversion</em>). </p> |
|                   |                                                                                                                                                                                                                                                                                                                                              |

***

#### **How to Set Up**

For the Hubspot integration to start working, you need to add "Brand Code" on each Brand in Tourpaq:

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Brand Code will be the prefix for bookings added to Hubspot using the integration.

Then, add the License Key and Subscriptions for each brand in Tourpaq (in Hubspot-tab).

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

First, we make a request to HubSpot to retrieve all eligible subscriptions for a given email address:

`https://api.hubapi.com/communication-preferences/v3/status/email/tcaspilot@gmail.com`\
Response JSON: _"hubspot all Subscription by email.txt"_

{% file src="../.gitbook/assets/hubspot all Subscription by email .txt" %}

Next, the system checks if any subscriptions listed under the **HubSpot** tab in Brand match the subscriptions returned by HubSpot.

If a match is found, the system verifies whether the customer should be subscribed, and if so, it makes the following request:

`https://api.hubapi.com/communication-preferences/v3/subscribe`\
Request body: _"hubspot subscribe customer.txt"_

{% file src="../.gitbook/assets/hubspot subscribe customer.txt" %}

Once connected, data synchronization will occur automatically according to the system’s scheduled sync jobs or configured triggers.

***

### **How it work**

#### 1. What information is sent to HubSpot per booking

For each booking, the system sends a structured set of booking-related data to HubSpot. This typically includes:

**Booking identification**

* Booking number
* Booking status
* Booking creation date
* Brand / owner

**Customer information**

* Main customer name
* Email address
* Phone number (if available)
* Customer ID (internal reference)

**Booking content**

* Travel period (departure and return dates)
* Destination
* Hotel name and room type
* Number of passengers (adults, children, infants)
* Transport details (if applicable)

**Financial data**

* Total booking amount
* Discounts
* Paid amount / outstanding amount (if supported)
* Currency

**Operational metadata**

* Sales channel (Office / Web booking)
* Booking source
* Assigned user or agency (if applicable)

The exact field mapping depends on the HubSpot object configuration (Deal, Contact, or Custom Object).

***

#### 2. When bookings are created or updated in HubSpot

#### Booking creation

A booking is **created in HubSpot** when:

* A new booking is successfully completed in the Booking Engine (Office or Web)
* The booking reaches a valid, confirmed state (not a draft)

At this point:

* A Deal (or booking object) is created
* The booking is linked to the customer contact (created or reused)

***

#### Booking updates

A booking is **updated in HubSpot** when one of the following events occurs:

* Booking status changes (for example confirmed, cancelled)
* Passenger data is modified
* Travel details are changed (dates, hotel, transport)
* Total price or discount changes
* Payment-related values are updated (if synced)

Updates are event-driven and only triggered when relevant booking data changes.

The service runs hourly (each agency can set this period as they wish), for all bookings created/updated during that hour. Tourpaq sends the following details to Hubspot for each booking:

* customer details;

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

This method populates a HubSpotUser object with data from a booking and sets brand-specific flags based on the agency.

Here is what details are sent, step by step.

1. Copies customer details\
   The first part maps personal and contact information from the booking object to the HubSpotUser:

* first and last name
* phone and mobile phone
* zip code, city, address, and country
* business unit, taken from the agency code

This ensures the HubSpot contact is created with the same data as the booking customer.

2. Handles agency specific logic\
   The switch statement checks booking.AgencyID and applies brand specific fields:

* sets a contact flag to "true" for the matching brand
* assigns the HubSpot owner (ownerID) to the corresponding brand owner field

3. Result\
   After the method runs, the crtUser object is fully prepared:

* it contains the customer’s booking data
* it is linked to exactly one agency brand
* it has the correct HubSpot owner assigned for that brand

The method does not return anything. It mutates the crtUser object in place so it can be saved or sent to HubSpot afterward.

* booking details:

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

The booking details that are sent to hubspot are:&#x20;

1. Create and populate the deal\
   A new CustomDeal instance is created and most fields are filled directly from the booking object:

* financial data like total amount, deposit, balance, and paid amounts
* booking identifiers such as booking number, agency code, and booking ID
* customer data like participant name and email
* travel data like destination, hotel, dates, duration, pension type
* metadata such as business unit, owner, and booking links

Dates are converted to UTC using DateTimeToUTC. Optional dates are checked with HasValue and default to 0 if missing.

2. Deal status and associations

* Stage is set to "closedwon" when booking.Status is 0, otherwise "closedlost"
* The deal is associated with a HubSpot contact using hubSpotUserID
* OwnerId assigns the deal owner in HubSpot

3. Aggregated passenger data

* NumberOfPax is calculated by summing adults and children across all bookings
* NumberOfChildren sums only children

This ensures passenger counts reflect the full booking group.

4. Transport type flags\
   After the object is created, transport flags are set based on booking.TransportMode:

* Flighttransport, Cartransport, Bustransport, Traintransport\
  Each is set to "yes" or "no" depending on the transport mode.

5. Flight details\
   Outbound and return flight information is added:

* airports are formatted as Name (Code)
* flight numbers are taken directly from the booking

6. Default extras\
   Several extras are explicitly set to "0":

* SkiTransports
* SkiRentals
* SkiSchools
* Transfer

This likely indicates that these services are not booked or not applicable by default.

7. Result\
   The method returns a fully initialized CustomDeal object that:

* represents one booking as a HubSpot deal
* is linked to a contact and owner
* contains complete financial, travel, and customer data

### **Tips**

* Keep your **License Key** private — it grants full API access to your HubSpot account.
* If you encounter sync issues, verify that the key has not expired or been revoked in HubSpot.
* Each booking sends identification, customer, travel, and financial data to HubSpot
* Bookings are created in HubSpot when they are completed and confirmed
* Bookings are updated whenever key booking data changes
* The sync is automatic and event-based, not manual
