# HubSpot

### Overview

The HubSpot section in **Brand settings** connects Tourpaq to a HubSpot account.

It syncs customers and bookings to HubSpot for marketing and reporting.

### What you can do here

* Connect Tourpaq to HubSpot using a **license key**.
* Define which HubSpot **subscriptions** Tourpaq can manage.

If it’s set up correctly, Tourpaq updates HubSpot automatically.

### Access

1. Navigate to **Users → Brands → Select an agency → HubSpot**.
2. Open the **HubSpot** tab.

You will find it next to other brand integrations.

### Field reference

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### License Key

Enter the HubSpot key/token Tourpaq should use for API calls.

🔹 _Format_: A long alphanumeric string (e.g., `f9d3e4b2-xxxx-xxxx-xxxx-9c14c62e1a10`).&#x20;

🔹 _Required_: Yes — the integration won’t work without it.

#### Subscriptions

Enter HubSpot subscription names separated by `;` (semicolon).

Tourpaq uses these to decide which customers it may subscribe.

Example:

`Customer Creation;Booking Update`

{% hint style="info" %}
Some HubSpot portals no longer support legacy API keys. If that’s your case, use a Private App token instead (if Tourpaq is configured to accept it).
{% endhint %}

### Setup

{% stepper %}
{% step %}
### Add Brand Code

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Set a **Brand Code** for each brand.

Tourpaq uses this code as a prefix in HubSpot booking data.
{% endstep %}

{% step %}
### Add HubSpot credentials and subscriptions

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Add the **License Key** and **Subscriptions** for the brand.
{% endstep %}
{% endstepper %}

### Subscription lookup and subscribe calls (example)

Tourpaq make a request to HubSpot to retrieve all eligible subscriptions for a given email address:

Example request:

`https://api.hubapi.com/communication-preferences/v3/status/email/<email>`

Example response:

{% file src="../.gitbook/assets/hubspot all Subscription by email .txt" %}

Next, the system checks if any subscriptions listed under the **HubSpot** tab in Brand match the subscriptions returned by HubSpot.

If a match is found, the system verifies whether the customer should be subscribed, and if so, it makes the following request:

`https://api.hubapi.com/communication-preferences/v3/subscribe`

Example request body:

{% file src="../.gitbook/assets/hubspot subscribe customer.txt" %}

Once connected, data synchronization will occur automatically according to the system’s scheduled sync jobs or configured triggers.

### Data sync behavior

#### What Tourpaq sends per booking

Tourpaq sends booking data to HubSpot.

This typically includes:

* Booking identifiers and status
* Main customer details (name, email, phone)
* Travel details (dates, destination, hotel, transport)
* Financial totals (amounts, discounts, currency)
* Metadata (brand, sales channel)

The exact mapping depends on your HubSpot setup.

#### When Tourpaq creates or updates bookings in HubSpot

**Creates** a new HubSpot booking/deal when:

* the booking is completed in Office or Web Booking
* the booking is in a valid state (not a draft)

**Updates** an existing booking/deal when key data changes, for example:

* status changes (confirmed, cancelled)
* passenger details change
* travel details change (dates, hotel, transport)
* price or discount changes
* payment values change (if synced)

#### Sync frequency

The sync typically runs on a schedule.

It commonly runs **hourly**, per agency configuration.

### Implementation notes (advanced)

<details>

<summary>Customer details mapping</summary>

Tourpaq maps customer contact details from the booking into a HubSpot contact.

It also applies brand-specific flags and sets the HubSpot owner.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

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

For example:

* AgencyID 163 marks the user as a Nortlander DK contact and sets NortlanderDKOwner
* AgencyID 58 marks the user as a Primo Tours contact and sets PrimoToursOwner

Each case represents a different brand or agency, and only one case is applied.

3. Result\
   After the method runs, the crtUser object is fully prepared:

* it contains the customer’s booking data
* it is linked to exactly one agency brand
* it has the correct HubSpot owner assigned for that brand

</details>

<details>

<summary>Booking/deal details mapping</summary>

Tourpaq creates or updates a HubSpot deal/custom object with financial and travel data.

It also sets transport flags and flight details (when available).

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

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

</details>

### Tips

* Keep the **License Key** private.
* If sync fails, rotate the key/token in HubSpot first.
* Validate subscriptions exist in HubSpot before adding them in Tourpaq.
* Use consistent Brand Codes. Avoid changing them mid-season.

### FAQ

#### Where do I get the License Key?

Create it in HubSpot, then paste it into the brand’s HubSpot tab in Tourpaq.

The exact location depends on whether you use legacy API keys or Private Apps.

#### How do I enter multiple subscriptions?

Separate them with `;` (semicolon).

Example: `Customer Creation;Booking Update`.

#### What happens if Subscriptions is empty?

Tourpaq cannot match subscriptions for the customer.

That often means it will skip subscribing the customer.

#### Why are some bookings not created in HubSpot?

Common causes:

* missing/invalid key
* missing Brand Code
* booking is still a draft or not in a valid state
* sync job has not run yet

#### Does Tourpaq create new contacts, or update existing ones?

It typically reuses an existing contact when email matches.

Otherwise it creates a new contact.

#### How often does the sync run?

Many setups run hourly.

Your agency can configure the interval.
