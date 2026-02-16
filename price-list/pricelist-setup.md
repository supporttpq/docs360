# Pricelist Setup

This feature is available for the administrator user type.

> More information on the effects can be found in [Broken link](/broken/pages/jc50ozXeeKjwLpod8Fqn "mention") page

## Create/Copy price list <a href="#createcopy-price-list" id="createcopy-price-list"></a>

### Create price lists <a href="#create-price-lists" id="create-price-lists"></a>

Price lists are created in the **Price List** tab by selecting **Create/Copy Price List**. The creation process involves the following steps:

1. **Select Brand** – Choose the brand for which the price list will be available.
2. **Select Transport** – Choose the transport option for the price list.
3. **Set Fix Quota** – Define the transport’s fixed quota.
4. **Select Hotel** – Choose the hotel that will use the price list.
5. **Select Rooms** – Specify the rooms to include in the price list.

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Not created prices <a href="#not-created-prices" id="not-created-prices"></a>

This feature allows users to identify **price lists that were not created**.

* Common reasons for missing price lists include:
  1. The **fix quota** does not cover the hotel allotment period.
  2. Some required **settings for the transport or hotel** were skipped during price list creation.

<figure><img src="../.gitbook/assets/image (36) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Copy price list <a href="#copy-price-list" id="copy-price-list"></a>

The **Copy Price List** feature allows users to duplicate price lists **within the same brand**.

### Steps to Copy a Price List

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

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Field-by-Field Explanation

#### **Filters (Top Section)**

| Field              | Description                                                                                            |
| ------------------ | ------------------------------------------------------------------------------------------------------ |
| **Departure date** | Defines the travel date range for which prices should be displayed. Example: 03-03-2025 to 03-03-2025. |
| **Resorts**        | Filters the results by specific resorts.                                                               |
| **Transports**     | Filters by available transport options (e.g., flights, buses).                                         |
| **Transport type** | Select transport categories (e.g., all seats, specific seat types).                                    |
| **Hotels**         | Filters by hotel(s).                                                                                   |
| **Allotment type** | Choose between the allotment types: All rooms, Allotment, orGuarantee/Secured.                         |
| **Room**           | Filters specific room categories.                                                                      |
| **Fix quotas**     | Optionally restricts the view to fixed quota contracts.                                                |
| **Display names**  | Toggles whether to show hotel names.                                                                   |
| **Stay Length**    | Defines the length of stay (number of nights).                                                         |
| **Checkboxes**     |                                                                                                        |

A price list is blank when first created.

<figure><img src="../.gitbook/assets/image (41) (1).png" alt=""><figcaption></figcaption></figure>

The fields must then be filled manually by the user with the amounts calculated or required. Some fields are set to autofill based on a formula that takes into consideration the amounts already inserted. In the end, a price list should look like this:

<figure><img src="../.gitbook/assets/image (632).png" alt=""><figcaption></figcaption></figure>

Fields:

* Optional tools, to be used only when needed
  * Show/Hide History (details the changes that have been made to that price line)
  * Reset this pricelist in API v4.1
  * Recalculate the Free Hotel Allotment value
* PLTA ID - pricelist unique identifier
* Hotel (autofill field)
* Room (autofill field)
* Dept date (autofill field, departure date for bookings made with this room)
* Stays - stay days
* FHA (Free Hotel Allotment, autofill field, if the value is 0, but the hotel has allotments, please use Recalculate the Free Hotel Allotment value)
* FTA (Free Transport Allotment, autofill field)
* P1 - P4 (price fields for intervals, filled by user)
* PP1 - PP4 {basic profit forecast of price per interval for 1 pax, PP1 = P1 - (transport + room costs) autofill field}
* POWO (price for one way out transports, filled by user)
* POWH (price for one way home transports, filled by user)
* G1 - G4 (group price, user filled field)
* PG1 - PG4 {basic profit forecast of group price per interval for 1 pax, PG1 `=` G1 - (transport + hotel cost), autofill field}
* GPOWO (group price for one way out transports, filled by user)
* GPOWH (group price for one way home transports, filled by user)
* D1-D4 (discount price for 1 week, overwrites P1 in web booking, filled by user)
* PD1-PD4 {basic profit forecast of discount price per interval for 1 pax, PD1 `=` D1 - (transport + room costs), autofill field}
* DPOWO (discount price for one way out transports, autofill field)
* DPOWH (discount price for one way home transports, autofill field)
* CH1P1-CH1P4 (child price per interval 1-4)
* PCH1P1 - PCH2P1 - Child price 1/2+ profit forecast for P1
* CH1% - CH4% (calculates the CH based on a percentage from P prices)
* DEBD check box - Disable extra bed discount - if checked, disables extra bed discount for all price types: P1-P4 and D1-D4
* DEBDPD check box (Disable extra bed discount for discount price - if checked, disables extra bed discount only for D1-D4 prices)
* CPOWO (child price for one way out)
* CPOWH (child price for one way home)
* CPM1- CPM4 - Child profit margin interval 1-4
* M1-M4 (maximum rooms per transport)
* PM1-PM4 (profit margin for P prices)
* PM% (transforms the value from PM in percentage)
* PA1-PA4 - price adjustment interval 1
* C1PA - Child 1 price adjustment
* C2PA - Child 2+ price adjustment
* WL checkbox (waitlist behavior)
* HD checkbox (hot deal list)
* FB - facebook checkbox
* NFIS checkbox (not for internet sale)
* 1W - Booked one week before&#x20;
* 2W - Booked two weeks before
* PL. REG. RULE. (select between price regulation rules)
* TR R Rule (transport regulation rule)
* LOWP1-LOWP4 (lowest regulation price)
* GR - Guarantee room
* GS - Guarantee seats
* TP - transport price (Value here changes Extra Bed discount as: (P1-TP)\*X%=Ex Bed Discount) (only for percent rules)
* TAG CH (tag change)
* TAG
* STATUS
* HNI1 - HNI4 - Hotel name interval 1-4

{% hint style="info" %}
### Room Type Display Logic for Allotment Filter

#### Principle

The type shown in filters must reflect the **effective allotment that will be consumed next**, not only the technical configuration.

This ensures that the filter behavior matches operational reality and user expectations.

### Functional Rule

#### 1. Guarantee / Secured Allotment Has Priority

If both **Guarantee/Secured allotment** and **Allotment** exist for the same room type, the system consumes:

1. Guarantee/Secured allotment first
2. Allotment after guarantee is exhausted

#### 2. Display Rule in Filters

**Case A: Guarantee Allotment Still Available**

If Guarantee/Secured allotment > 0:

* The room type is treated as **Guarantee**
* It shall NOT appear when filtering by **Allotment**
* It shall appear when filtering by **Guarantee**

Reason: The next booking will consume guarantee allotment.

**Case B: Guarantee Allotment Fully Consumed**

If Guarantee/Secured allotment = 0 and Allotment > 0:

* The room type is treated as **Allotment**
* It shall appear when filtering by **Allotment**
* It shall no longer be considered Guarantee

Reason: The next booking will consume allotment.

### Rationale

The filter must reflect the **current effective selling logic**, not just the configured allotment types.

This ensures that users selecting the Allotment filter only see rooms that will actually consume allotment.
{% endhint %}

#### Tabs <a href="#tabs" id="tabs"></a>

Below the filters are the following tabs:

**Prices -** Contains the actual pricelist

**Discounts -** Contains discounts from the hotel

<figure><img src="../.gitbook/assets/image (42) (1).png" alt=""><figcaption></figcaption></figure>

**Column filters -** Allows the user to filter among the columns shown in prices. All unchecked filters will be displayed in **PRICES**

<figure><img src="../.gitbook/assets/image (633).png" alt=""><figcaption></figcaption></figure>

Filter categories:

* Price - display prices per intervals, as well as PLTA ID (price list transport allotment ID)
* Profit Price - display profit forecasts for prices per intervals
* Disc price - display discount prices per intervals
* Profit disc. price - display profit forecasts for discount prices per intervals
* Gr. prices - display group prices per intervals
* Profit gr. prices - display profit forecasts for group prices per intervals
* Ch. prices - display child prices per intervals
* Max rooms - display max number of rooms per intervals
* Low. reg. prices - lowest value of price regulation rules
*   Generic filters

    * P. Ch. - increase/decrease prices per interval
    * Hide average profit - hides average real profit per pax
    * TP - transport price�

    ⚠️ **Warning:** Values here change **Extra bed discount** (P1 - TP) \* - TP)\*X%=EBD

    * GR - guarantee rooms
    * GS - guarantee seats
* Regulation rules - display price regulation rule filters
* Other tools
  * Waitlist
  * Hot Deal
  * Facebook
* OW Prices - display one way price filters

#### Alternative hotel name <a href="#alternative-hotel-name" id="alternative-hotel-name"></a>

A handy improvement is being able to customize hotel name for specific departures.

<figure><img src="../.gitbook/assets/image (634).png" alt=""><figcaption></figcaption></figure>

This alternative name will also appear on the ticket.

In the office, the alternative name will replace the hotel name.

## The P.CH (Price Change) option <a href="#the-pch-price-change-column" id="the-pch-price-change-column"></a>

The P. Ch. column stands for Price Change. This will adjust the price relative to what is currently in the column.

<figure><img src="../.gitbook/assets/image (46) (1).png" alt=""><figcaption></figcaption></figure>

When something is selected in this column, another set of options will appear in the upper section.

Pr. Change -> sets the column to be modified

Value -> sets the value that is added to the current value in the selected column. (Example: P1 is 1000 and you set 200, P1 will be set to 1200)

Run -> makes the change take effect in the interface. Repeated pressing will increase/decrease prices again.

Difference from Price -> This option is available only for Discount columns. This makes discount values modify relative to P in the period (example: D1 is relative to P1, D2 is relative to P2 , etc.).

<figure><img src="../.gitbook/assets/image (47) (1).png" alt=""><figcaption></figcaption></figure>

When **Difference from Price** is checked, after Run, discount values are calculated by decreasing the price with the value set. If Price P1=2000 and D1=200 and Difference from Price is checked, after Run, PD1=2000-200=1800. Only after Save, new values are saved in the PriceList.

### FAQ

#### How do I create a new price list?

Use Create or Copy Price List, then select brand, transport, fix quota, hotel, and the rooms to include.

#### Why is a price list not created?

This usually happens when fix quotas do not cover the hotel allotment period or required data is missing.

#### Can I copy an existing price list?

Yes. You can copy prices from an existing price list within the same brand.

#### What copy scopes are available?

You can copy prices from one transport to all brand transports, from one hotel to all hotels on a transport, or from one room to all rooms of a hotel.

#### What must be selected before copying prices?

All checkboxes in the Price Difference section should be selected, even if the values are zero.

#### What filters are available in Pricelist Setup?

You can filter by departure date, resort, transport, transport type, hotel, allotment type, room, fix quota, hotel name, and stay length.

#### Why do no rows appear after filtering?

Common causes are missing brand context, incorrect date range, or no price lists created for the selected criteria.

#### What information is shown in the price list grid?

The grid shows hotel, room, departure date, free hotel and transport allotments, selling prices (P1–P4), child prices, group prices, discounts, and profit-related fields.

#### How are child prices calculated?

Child prices can be entered directly or calculated as a percentage of the adult price using CH% col
