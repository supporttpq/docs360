# Travel Insurance

## **General Tab**

### **Overview**

The system allows passengers to purchase travel insurance as part of their booking. Each insurance product is configured in Tourpaq Office and is linked to a specific insurance provider. Passengers may also choose to use their own external insurance, in which case only basic information (e.g., insurance company, policy number) is stored.

All travel insurance entries configured in the system are associated with a **travel insurance provider**. These entries are processed daily through the automated reporting service, which sends the corresponding data to the provider.\
(For detailed automation behavior, see _Travel Insurance Automated Reporting_).

### **Travel Insurance Asset Structure**

A travel insurance asset contains the full configuration required for system usage and for automated communication with the insurance provider. The following information must be available:

#### **General Information**

The **General** tab is the main configuration area for setting up an insurance product in the system. From here, you define the basic details, behaviour, availability, commission rules, pricing options, and insurance provider extensions.

The **General** tab contains all mandatory and optional settings that define how an insurance product behaves in the booking system. It covers:

* Basic identification
* Booking rules
* Provider type (Gouda / Europæiske)
* Country availability
* Commission and pricing options
* Provider-specific configuration (extensions)
* Brand assignment

This setup ensures that the insurance product appears correctly during the booking flow and that all calculations and integrations run as expected.

#### **Purpose**

The purpose of the General tab is to:

* Define the core identity and behaviour of an insurance product
* Specify which customers can book it (age, country, resort conditions)
* Assign integration settings for external providers (Gouda, Europæiske)
* Control commission, deposit behaviour, and cancellation options
* Connect the insurance product to selected brands

This ensures the insurance behaves correctly across all booking channels.

### **Field Explanation**&#x20;

<figure><img src="../.gitbook/assets/image (473).png" alt=""><figcaption></figcaption></figure>

#### **Brand Assignment (Top Section)**

| **Field**                                          | **Description**                                                                                        |
| -------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| **Tourpaq DK / SE / Live / Other brand dropdowns** | Assigns this insurance to one or more brands. If “Not assigned,” the brand cannot sell this insurance. |

***

### **General Information**

| **Field**                           | **Description**                                                                                   |
| ----------------------------------- | ------------------------------------------------------------------------------------------------- |
| **Name**\*                          | Display name of the insurance (shown to users).                                                   |
| **Resort**                          | Limits the insurance to specific resorts, or “All Resorts”.                                       |
| **InsuranceID**\*                   | Internal identifier used for API calls and integrations.                                          |
| **Product code**\*                  | Provider product code used in external systems (Gouda/Europæiske).                                |
| **Max no. days**\*                  | Maximum number of travel days allowed for this insurance product.                                 |
| **Price Infant**                    | Price for infant travellers, if applicable.                                                       |
| **Add to deposit**                  | If enabled, the insurance price is added to the deposit calculation instead of the final invoice. |
| **Cancellation insurance included** | If checked, cancellation coverage is included in this insurance.                                  |
| **Annual insurance**                | Indicates whether this is a yearly insurance product rather than per-trip.                        |
| **Priced Infant**                   | If enabled, infants are charged based on the “Price Infant” rule.                                 |
| **Commission**                      | Percentage commission paid to the agency for selling the insurance.                               |
| **Auto Select in Booking Window**   | Automatically selects this insurance by default in the booking flow.                              |
| **Currency**                        | The currency used for this insurance product.                                                     |
| **Types**                           | Selects the provider: **Europæiske** or **Gouda**. Determines which extensions become active.     |
| **Country**                         | Defines which customer nationalities are allowed to book this insurance.                          |

***

### **Description Section**

| **Field**                          | **Description**                                                                            |
| ---------------------------------- | ------------------------------------------------------------------------------------------ |
| **Description (Rich text editor)** | Text shown in customer-facing systems describing coverage, terms, and general information. |

***

### **Gouda Extensions**

| **Field**            | **Description**                                                                                                                                                                                                            |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Cover**            | <p>Indicates whether the insurance applies to:</p><ul><li>A <strong>single person</strong>, or</li><li>A <strong>group</strong> (codes: <em>6, 10, 18</em>) — these group values are not sent directly to Gouda.</li></ul> |
| **Tax**              | <p>The fee charged by Gouda for their services.<br>Default: <strong>1.1%</strong> of the insurance price.</p>                                                                                                              |
| **Optionals**        | <p>Extra configuration field for Gouda integrations. </p><p>Additional cover options:</p><ol><li>Personal Property</li><li>Ski</li><li>Excess</li><li>Accident</li><li>Accident + Personal Property</li></ol>              |
| **Product version**  | Indicates which Gouda product version is used.                                                                                                                                                                             |
| **1 year available** | Enables 1-year coverage options if offered by Gouda.                                                                                                                                                                       |

***

### **Europæiske Extensions**&#x20;

| **Field**               | **Description**                                                                         |
| ----------------------- | --------------------------------------------------------------------------------------- |
| **1–5 (option fields)** | Provider-specific values used by Europæiske for risk categories or benefit definitions. |
| **Trip type**           | Identifies the trip category used by Europæiske (e.g., Single Trip, Multi-Trip).        |

***

### **Pricing Structure**

Insurance prices are inserted according to:

* Insurance area (Extended Europe, Europe, World)
* Age (adult/child/senior)
* Type of price (basic price or daily price)

Each insurance must contain the following price inputs, per area:

#### **Extended Europe**

* Adult basic price
* Adult price per day
* Child basic price
* Child price per day
* Basic Price Senior
* Senior day price

#### **Europe**

* Adult basic price
* Adult price per day
* Child basic price
* Child price per day
* Basic Price Senior
* Senior day price

#### **World**

* Adult basic price
* Adult price per day
* Child basic price
* Child price per day
* Basic Price Senior
* Senior day price

***

### **Price Calculation**

The total insurance price for a passenger is calculated as:

**Total Price = Basic Price + (Trip Length × Price per Day)**

This applies to both adults and children, based on the values defined for their age group and insurance area.

***

### **Passenger Using Personal Insurance**

Passengers may choose to use their own travel insurance instead of purchasing one offered in the system.

For this scenario:

* The **Product Code** does _not_ correspond to a provider’s product
* **Europæiske** and **Gouda extensions** do **not** need to be filled
* Only the manually provided details (e.g., insurance company, policy number) are stored

This ensures the booking remains fully compliant while allowing passengers to travel with external coverage.

Example:

| Travel insurance name               | Travel insurance code | Product code | Max days cover number | Description | Countries |
| ----------------------------------- | --------------------- | ------------ | --------------------- | ----------- | --------- |
| Årsrejsef.EU(Husst.)m.gratis  Total | ÅEH                   | AREU         | 365                   | Bulgary     | Kreta     |

Let’s suppose that this travel insurance corresponds to a product provided by Gouda, so Gouda extensions should be filled in:

| Cover | Optionals | Product version |
| ----- | --------- | --------------- |
| 6     | 0         | 4.0             |

The correspondent prices:

| Bkg start date | Bkg end date | Sc. basic price adult | Sc. basid price child | Sc. adult price per day | Sc. child price per day | Eur. basic price adult | Eur. basic price child | Eur. adult price per day | Eur. child price per day | W. basic price adult | W. basic price child | W. adult price per day | W. child price per day |
| -------------- | ------------ | --------------------- | --------------------- | ----------------------- | ----------------------- | ---------------------- | ---------------------- | ------------------------ | ------------------------ | -------------------- | -------------------- | ---------------------- | ---------------------- |
| 01-12-2009     | 01-12-2011   | 0                     | 0                     | 0                       | 0                       | 350                    | 0                      | 350                      | 0                        | 0                    | 0                    | 0                      | 0                      |

### **How It Works**

#### **1. Define the Insurance Identity**

You start by entering the core details (name, ID, product code). These fields tell the system and external providers what product this is.

#### **2. Select Provider Type**

Choosing **Gouda** or **Europæiske** determines which integration fields appear.\
Each provider requires specific codes and settings.

#### **3. Assign Brands**

The insurance product must be assigned to one or more brands before it can be sold under those brands.

#### **4. Configure Booking Behaviour**

Options such as:

* Auto-select in booking
* Deposit behaviour
* Cancellation included\
  control how the product behaves in the customer-facing booking flow.

#### **5. Set Age and Duration Rules**

Fields like:

* Max no. days
* Price Infant
* Infant handling\
  ensure the product applies correctly to each traveller.

#### **6. Set Commission Rules**

Enter the commission percentage to define agency earnings.

#### **7. Provider Integration Setup**

Depending on provider:

* Fill Gouda fields to enable Gouda risk and product mapping
* Fill Europæiske fields for their product structure

These values must match the provider’s documentation.

#### **8. Country Availability**

Choose which nationalities are allowed to book the product.\
Example: Denmark, Bulgaria, Spain, Mallorca.

***

### **Notes**

* Required fields (\*) must be filled before saving.
* Changing provider type resets provider-specific fields.
* Country selection must match legal coverage rules.
* Brand assignment controls visibility across booking channels.

## **Date Period**&#x20;

### **Overview**

The **Date Period** tab allows administrators to define booking periods and configure age rules and pricing models for insurance or additional services. A “Date Period” groups together validity dates, maximum age rules, and all pricing options that apply within the selected period.

This section ensures that correct price calculations are applied based on:

* Booking dates
* Traveller age groups (adult, child, senior, infant)
* Selected travel zones (Europe, Extended Europe, Worldwide)
* Duration ranges (e.g., 1–4 days, 5–9 days)

***

### **Purpose**

The purpose of the Date Period configuration is to:

* Control which prices apply during a specific booking timeframe
* Define age boundaries for children, infants, and seniors
* Set base and daily prices for different travel zones
* Apply duration-based pricing rules
* Manage insurance or service price variations depending on trip length

This ensures that the system always calculates the correct final price based on the traveller’s age, destination, and trip duration.

***

### **Field Explanation**

<figure><img src="../.gitbook/assets/image (471).png" alt=""><figcaption></figcaption></figure>

#### **General Fields (Left Panel)**

| **Field**           | **Description**                                                                                                                 |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Period**          | The name or label of the defined booking period (e.g., _Period 1_, _Winter Season_).                                            |
| **Booking start**   | The date from which the period becomes valid. Prices and rules under this period apply for bookings made on or after this date. |
| **Booking end**     | The last date on which the period is valid.                                                                                     |
| **Max age child**   | The maximum age considered a child. Travellers older than this age fall into the adult category.                                |
| **Infant**          | Checkbox indicating whether infant pricing applies during this period.                                                          |
| **For Senior Only** | Restricts this pricing period to senior travellers only (e.g., senior insurance).                                               |

***

#### **Extended Europe (Right Panel – Section 1)**

Pricing fields for the **Extended Europe** region.

| **Field**              | **Description**                                 |
| ---------------------- | ----------------------------------------------- |
| **Basic price adult**  | Base premium for adults within Extended Europe. |
| **Day price adult**    | Additional price per day for adults.            |
| **Basic price child**  | Base premium for children.                      |
| **Child day price**    | Daily rate applied to child travellers.         |
| **Basic price Senior** | Base price for senior travellers.               |
| **Senior day price**   | Daily surcharge for seniors.                    |

***

#### **Europe / World Sections**

This sections (Europe, World) contain the same structure as Extended Europe:

* Adult base and day prices
* Child base and day prices
* Senior base and day prices

***

#### **Europe – Fast Pris (Fixed Price) Section**

Fixed-price insurance scheme based on trip duration.

| **Duration Range** | **Field Meaning**                   |
| ------------------ | ----------------------------------- |
| **1–4 dagar**      | Price for trips lasting 1–4 days.   |
| **5–9 dagar**      | Price for trips lasting 5–9 days.   |
| **10–16 dagar**    | Price for trips lasting 10–16 days. |
| **17–23 dagar**    | Price for trips lasting 17–23 days. |
| **24–31 dagar**    | Price for trips lasting 24–31 days. |

#### **World – Fast Pris (Fixed Price)**

Same structure as Europe Fast Pris but applies to worldwide destinations.

***

### **How It Works**

1. **Select or Create a Date Period**\
   Each period contains its own pricing rules. When a booking falls inside the period’s start–end range, the system applies the rules from that period.
2. **Age Calculation**
   * Children are recognized based on **Max age child**.
   * Senior pricing is applied when the senior category is enabled and the traveller meets senior age criteria.
   * Infants are priced separately when the **Infant** checkbox is checked.
3. **Price Determination**\
   The system calculates price based on:
   * Travel zone (Europe, Extended Europe, World)
   * Age category (child, adult, senior)
   * Trip duration (days)

## **Photos**

The system allows add images related to the travel insurance asset.&#x20;

<figure><img src="../.gitbook/assets/image (472).png" alt=""><figcaption></figcaption></figure>
