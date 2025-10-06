# Pricelist Setup

This feature is available for the administrator user type.

> More information on the effects can be found in [Broken link](broken-reference "mention") page

### Create/Copy price list <a href="#createcopy-price-list" id="createcopy-price-list"></a>

#### Create price lists <a href="#create-price-lists" id="create-price-lists"></a>

Price lists are created in the **Price List** tab by selecting **Create/Copy Price List**. The creation process involves the following steps:

1. **Select Brand** – Choose the brand for which the price list will be available.
2. **Select Transport** – Choose the transport option for the price list.
3. **Set Fix Quota** – Define the transport’s fixed quota.
4. **Select Hotel** – Choose the hotel that will use the price list.
5. **Select Rooms** – Specify the rooms to include in the price list.

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Not created prices <a href="#not-created-prices" id="not-created-prices"></a>

This feature allows users to identify **price lists that were not created**.

* Common reasons for missing price lists include:
  1. The **fix quota** does not cover the hotel allotment period.
  2. Some required **settings for the transport or hotel** were skipped during price list creation.

<figure><img src="../.gitbook/assets/image (36) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Copy price list <a href="#copy-price-list" id="copy-price-list"></a>

The **Copy Price List** feature allows users to duplicate price lists **within the same brand**.

#### Steps to Copy a Price List

1. **Select Source** – Choose the **Transport**, **Hotel**, **Room**, and **Date** from which the price list will be copied.
2. **Select Destination** – Choose the **Transport**, **Hotel**, **Room**, and **Date** to which the prices will be copied.
3. **Different Days** – Define the difference in days between the source and destination price lists. This is used if:
   * The transport’s fixed quota does not match, or
   * You want to extend the price list by a specific number of days.
4. **Adjust Prices and Discounts** – Use the **Change Discounts for Original Prices** and **PRICE DIFFERENCE** sections to modify values as needed.
5. **Copy Options** – Checkboxes allow copying prices from:
   * A transport to all transports of the brand.
   * A hotel to all hotels assigned to the transport.
   * A room to all rooms of a hotel.
6. **Important:** Before copying, ensure all checkboxes in the **PRICE DIFFERENCE** section are selected, even if values are 0.
7. **Execute Copy** – Click **Copy Prices**.
8. **Save Discounts** – Click **Save Changed Discounts** to finalize.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Field-by-Field Explanation

#### **Filters (Top Section)**

| Field              | Description                                                                                            |
| ------------------ | ------------------------------------------------------------------------------------------------------ |
| **Departure date** | Defines the travel date range for which prices should be displayed. Example: 03-03-2025 to 03-03-2025. |
| **Resorts**        | Filters the results by specific resorts.                                                               |
| **Transports**     | Filters by available transport options (e.g., flights, buses).                                         |
| **Transport type** | Select transport categories (e.g., all seats, specific seat types).                                    |
| **Hotels**         | Filters by hotel(s).                                                                                   |
| **Allotment type** | Defines room allotment conditions (e.g., “All rooms”).                                                 |
| **Room**           | Filters specific room categories.                                                                      |
| **Fix quotas**     | Optionally restricts the view to fixed quota contracts.                                                |
| **Display names**  | Toggles whether to show hotel names.                                                                   |
| **Stay Length**    | Defines the length of stay (number of nights).                                                         |
| **Checkboxes**     |                                                                                                        |

A price list is blank when first created.

<figure><img src="../.gitbook/assets/image (41) (1).png" alt=""><figcaption></figcaption></figure>

The fields must then be filled manually by the user with the amounts calculated or required. Some fields are set to autofill based on a formula that takes into consideration the amounts already inserted. In the end, a price list should look like this:

<figure><img src="../.gitbook/assets/image (40) (1) (1).png" alt=""><figcaption></figcaption></figure>

Fields:

* Optional tools, to be used only when needed
  * Show/Hide History (details the changes that have been made to that price line)
  * Reset this pricelist in API v4.1
  * Recalculate the Free Hotel Allotment value
* Hotel (autofill field)
* Room (autofill field)
* Dept date (autofill field, departure date for bookings made with this room)
* FHA (Free Hotel Allotment, autofill field, if the value is 0, but the hotel has allotments, please use Recalculate the Free Hotel Allotment value)
* FTA (Free Transport Allotment, autofill field)
* P1 - P4 (price fields for intervals, filled by user)
* PP1 - PP4 {basic profit forecast of price per interval for 1 pax, PP1 = P1 - (transport + room costs) autofill field}
* POWO (price for one way out transports, filled by user)
* POWH (price for one way home transports, filled by user)
* D1-D4 (discount price for 1 week, overwrites P1 in webbooking, filled by user)
* PD1-PD4 {basic profit forecast of discount price per interval for 1 pax, PD1 `=` D1 - (transport + room costs), autofill field}
* DPOWO (discount price for one way out transports, autofill field)
* DPOWH (discount price for one way home transports, autofill field)
* G1 - G4 (group price, user filled field)
* PG1 - PG4 {basic profit forecast of group price per interval for 1 pax, PG1 `=` G1 - (transport + hotel cost), autofill field}
* GPOWO (group price for one way out transports, filled by user)
* GPOWH (group price for one way home transports, filled by user)
* CH1-CH4 (child price, acts as an extra bed discount, overrides extra bed discount)
* CH1% - CH4% (calculates the CH based on a percentage from P prices)
* DEBD check box - Disable extra bed discount - if checked, disables extra bed discount for all price types: P1-P4 and D1-D4
* DEBDD check box (Disable extra bed discount for discount price - if checked, disables extra bed discount only for D1-D4 prices)
* CHOWO (child price for one way out)
* CHOWH (child price for one way home)
* M1-M4 (maximum rooms per transport)
* PM1-PM4 (profit margin for P prices)
* PM% (transforms the value from PM in percentage)
* WL checkbox (waitlist behavior)
* HD checkbox (hot deal list)
* NFIS checkbox (not for internet sale)
* P CH check box (used to change - increase/decrease - prices)
* PL. R. RULE check box (if checked, enables price regulation rules)
* PL. REG. RULE. (select between price regulation rules)
* TR R Rule (transport regulation rule)
* LOWP1-LOWP4 (lowest regulation price)
* GR
* TP (transport price)
* TAG CH (tag change)
* TAG
* STATUS

#### Tabs <a href="#tabs" id="tabs"></a>

Below the filters are the following tabs:

**Prices -** Contains the actual pricelist

**Discounts -** Contains discounts from the hotel

<figure><img src="../.gitbook/assets/image (42) (1).png" alt=""><figcaption></figcaption></figure>

**Column filters -** Allows the user to filter among the columns shown in prices. All unchecked filters will be displayed in **PRICES**

<figure><img src="../.gitbook/assets/image (43) (1).png" alt=""><figcaption></figcaption></figure>

Filter categories:

* Price - display prices per intervals, as well as PLTA ID (price list transport allotment ID)
* Profit Price - display profit forecasts for prices per intervals
* Disc price - diplay discount prices per intervals
* Profit disc. price - display profit forecasts for discount prices per intervals
* Gr. prices - display group prices per intervals
* Profit gr. prices - display profit forecasts for group prices per intervals
* Ch. prices - display child prices per intervals
* Max rooms - display max number of rooms per intervals
* Low. reg. prices - lowest value of price regulation rules
*   Generic filters

    * P. Ch. - increase/decrease prices per interval
    * Hide average profit - hides average real profit per pax
    * TP - transport price&#x20;

    ⚠️ **Warning:** Values here change **Extra bed discount** (P1 - TP) \* - TP)\*X%=EBD

    * GR - guarantee rooms
    * GS - guarantee seats
* Regulation rules - display price regulation rule filters
* Other tools
  * Waitlist
  * Hot Deal
  * Facebook
* OW Prices - display one way price filters

#### Children prices as a percentage <a href="#children-prices-as-a-percentage" id="children-prices-as-a-percentage"></a>

Along with fixed children's prices, the system allows the user to calculate these prices based on a percentage of the adult price. This will make price updates much easier. Simply insert a value in the **CH1 %** column, and that value will be converted into a percentage of the amount from **P1**.

<figure><img src="../.gitbook/assets/image (44) (1).png" alt=""><figcaption></figcaption></figure>

> A passenger will get the Child Price ONLY if:

* Passenger title is CHD
* Passenger's age is validated against the Child Price age under the Hotel
* Passenger occupies an extra bed

#### Alternative hotel name <a href="#alternative-hotel-name" id="alternative-hotel-name"></a>

A handy improvement is being able to customize hotel name for specific departures.

<figure><img src="../.gitbook/assets/image (45) (1).png" alt=""><figcaption></figcaption></figure>

This alternative name will also appear on the ticket.

In the office, the alternative name will replace the hotel name.

### The P.CH (Price Change) option <a href="#the-pch-price-change-column" id="the-pch-price-change-column"></a>

The P. Ch. column stands for Price Change. This will adjust the price relative to what is currently in the column.

<figure><img src="../.gitbook/assets/image (46) (1).png" alt=""><figcaption></figcaption></figure>

When something is selected in this column, another set of options will appear in the upper section.

Pr. Change -> sets the column to be modified

Value -> sets the value that is added to the current value in the selected column. (Example: P1 is 1000 and you set 200, P1 will be set to 1200)

Run -> makes the change take effect in the interface. Repeated pressing will increase/decrease prices again.

Difference from Price -> This option is available only for Discount columns. This makes discount values modify relative to P in the period (example: D1 is relative to P1, D2 is relative to P2 , etc.).

<figure><img src="../.gitbook/assets/image (47) (1).png" alt=""><figcaption></figcaption></figure>

When **Difference from Price** is checked, after Run, discount values are calculated by decreasing the price with the value set. If Price P1=2000 and D1=200 and Difference from Price is checked, after Run, PD1=2000-200=1800. Only after Save, new values are saved in the PriceList.
