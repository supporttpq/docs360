# Travel Insurance

## **General Tab**

### **Overview**

The system allows passengers to purchase travel insurance as part of their booking. Each insurance product is configured in Tourpaq Office and is linked to a specific insurance provider. Passengers may also choose to use their own external insurance, in which case only basic information (e.g., insurance company, policy number) is stored.

All travel insurance entries configured in the system are associated with a **travel insurance provider**. These entries are processed daily through the automated reporting service, which sends the corresponding data to the provider.\
(For detailed automation behavior, see _Travel Insurance Automated Reporting_).

### **Travel Insurance Asset Structure**

A travel insurance asset contains the full configuration required for system usage and for automated communication with the insurance provider. The following information must be available:

#### **General Information**

* **Travel insurance name**
* **Travel insurance code**
* **Product code**\* – Used to map the insurance product in Tourpaq to the provider’s corresponding product
* **Maximum number of covered days**
* **Description**
* **1 Year Availability** – Specifies whether the product can be purchased for year-long coverage
* **Countries** – Defines the countries or regions covered by the insurance

#### **Provider Extensions**

Depending on the insurance provider, different extensions are required.

### **Europæiske Extensions**

These fields are completed only when the insurance corresponds to a Europæiske product.

The extensions include:

* Five insurance codes (1 to 5)
* Trip type

***

### **Gouda Extensions**

These fields are required for Gouda travel insurance assets.

#### **- Cover**

Indicates whether the insurance applies to:

* A **single person**, or
* A **group** (codes: _6, 10, 18_) — these group values are not sent directly to Gouda.

#### &#x20;**- Tax**

The fee charged by Gouda for their services.\
Default: **1.1%** of the insurance price.

#### **- Optionals**

Additional cover options:

1. Personal Property
2. Ski
3. Excess
4. Accident
5. Accident + Personal Property

#### &#x20;**- Product Version**

Indicates which Gouda product version is used.

***

### **Pricing Structure**

Insurance prices are inserted according to:

* Insurance area (Scandinavia, Europe, World)
* Age (adult/child)
* Type of price (basic price or daily price)

Each insurance must contain the following price inputs, per area:

#### **Scandinavia**

* Adult basic price
* Adult price per day
* Child basic price
* Child price per day

#### **Europe**

* Adult basic price
* Adult price per day
* Child basic price
* Child price per day

#### **World**

* Adult basic price
* Adult price per day
* Child basic price
* Child price per day

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
