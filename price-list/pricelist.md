# Pricelist

### Overview

Hotel **Price List** is the place where prices are created or managed for particular packages. Usually a package contains a [Transport](../transport/transport/) and a [Room types](../base-room-types.md) Hotel but this is not necessarily the case. The price can be added based on interval, discounts, children, or groups, or it can be set for one way or round trip. Each package has a date assigned; this date is pointing to the departure date of the trip.

### Purpose

A **Price List** is the foundation of how trips and offers are sold in Tourpaq.

Its purpose is to:

1. **Define the selling price of a trip**
   * Combines **Transport** (flight/bus/ship seats) + **Hotel** (room types, allotments) + other conditions (discounts, stay length, children rates, groups).
   * Ensures every departure date and room type has a price assigned.
2. **Control availability**
   * Price lists link prices with **allotments** (how many rooms/seats are available).
   * Without a price list, even if there are seats/rooms available, the package cannot be booked.
3. **Support different sales channels**
   * The same price list is used by:
     * **Agencies** (offers presented on agency sites).
     * **Web Booking (WB)** (online sales).
     * **Office** (internal bookings by staff).
4. **Enable flexibility**
   * Prices can be adjusted per:
     * Interval (P1, P2, P3, P4 = different stay lengths or price periods).
     * Age groups (child/adult discounts).
     * Trip type (one-way, round-trip).
     * Brand (same hotel/transport may have different prices depending on the brand).
5. **Provide historical and operational control**
   * Price lists track **changes over time** (history log).
   * Manual recalculations or adjustments can be made when allotments or transport costs change.

### How it Works

### Create/copy price list <a href="#createcopy-price-list" id="createcopy-price-list"></a>

Creating a price list is straightforward. In the **Price List** tab, click **Create/Copy Price List** and follow the steps below:

1. Choose the **brand** for which you want to create the price list.
2. Select the **transport**.
3. Select the **transport’s fixed quota**.
4. Select the **hotel**.
5. Choose the **rooms**.
6. Click **Create new price list**.

<figure><img src="../.gitbook/assets/image (29) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

When a user is creating a price list, and will not use PM rule, the price list will be generated but without any prices.

The behaviour from the "Create new price list" action has multiple possible warning outputs:

* If no prices are created a warning message appears saying "The price lists were NOT created. Please check transport and hotel allotments and recreate the price lists"

<figure><img src="../.gitbook/assets/image (502).png" alt=""><figcaption></figcaption></figure>

* If some prices are generated (but not for all the possible selected combinations) a warning message appears saying "The price lists were not created for ALL allotments. Press display to see the generated price list or check transport and hotel allotments and recreate the price list"

<figure><img src="../.gitbook/assets/image (503).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (504).png" alt=""><figcaption></figcaption></figure>

### Price List Search <a href="#price-list-search" id="price-list-search"></a>

The search helps to find prices based on brands, Transport, Hotel, Room and the departure date interval. To get results The most basic search you can get is by choosing All Brands and Transport but for the best performance, try to fill most of the fields. The list of transports from the drop-down list is filtered based on the brand selection.

<figure><img src="../.gitbook/assets/image (291).png" alt=""><figcaption></figcaption></figure>

### Top Section (Filters related to Dates and Transport):

* **Date From/To Fields**: Set the date range for price list queries (format  DD-MM-YYYY)
* **Resorts Dropdown**: Select specific resorts to include in the price list
* **Transports Dropdown**: Configure transport options with code format
* **Transport Type Dropdown**: Filter by transport categories&#x20;
* **Hotels Dropdown**: Select specific hotels
* **Allotment Type Dropdown**: Select the allotment type
* **Room Dropdown**: Select a specific room type
* **Fix Quotas Dropdown**: Select a transport fix quota&#x20;
* **Display Names Checkbox**: Toggle to show hotel names in results
* **Display Checkbox**: Toggle to show the price list results
* **Clear Button**: Reset all filter selections (shows "1" indicator, possibly indicating active filters)
* **Stay Length Field**: Used to filter price lists for a specific stay length. It is possible to specify one stay, several stays or a range.

### Price Display Options

* **Hotel Disc on Top Checkbox**: Show hotel discounts prominently
* **Only Set Prices Checkbox**: Display only confirmed/set prices
* **Hide Zero FTA Checkbox**: Exclude zero-value FTA (likely "Free to Agent") rates
* **Hide Zero PHA Checkbox**: Exclude zero-value PHA rates

### View Management

* **Save View Button**: Preserve current filter configuration
* **Update View Button**: Modify existing saved view
* **Menu Icon (⋮)**: Additional options menu

#### Example: Running a Search

1. Open the **Price List Search** page.
2. In the **Date From / To** fields, enter _01-07-2025_ to _15-07-2025_ to search for the first half of July.
3. From the **Brand** drop-down, select TourpaqDK.
4. The **Transports** list is now filtered for TourpaqDK. Select the transport option _FLY-RO_.
5. In the **Hotels** drop-down, select _Hotel Marina_.
6. Choose **Double Room with Balcony** from the **Room** field.
7. Enter _7_ in the **Stay Length** field to filter for week-long stays.
8. Under **Price Display Options**, check **Only Set Prices** to display confirmed rates only.
9. Click **Display** to run the search.

✅ The system displays all available TourpaqDK **→ FLY-RO transport → Hotel Marina → Double Room with Balcony → 7-night stays between 01–15 July 2025**, showing only confirmed prices.

#### Transport and Hotel Selection Behavior

* **All Brands Selected:**
  * When **All Brands** is selected, all available transports will appear in the **Transport** drop-down list.
* **Specific Brand Selected:**
  * If a specific brand is chosen, only transports assigned to that brand will appear.
  * Transports are assigned to brands via **Transport → Brands Tab | Brands Tab → Edit Transport**.
  * Transports marked as **hidden** will not appear in the drop-down list. Transport visibility can be managed in **Transport → General Tab → General**.
* **Transport Selection Effects:**
  * Once a transport is selected, the **Fix Quota** field is automatically populated in the multiple selection view.
  * The **Hotels** drop-down is filtered to display only hotels associated with the selected transport’s price list.
  * Hotels marked as **hidden** will not appear. Visibility can be configured in **Hotel → Hotel Tab → General Tab**.
* **Hotel Selection Effects:**
  * Selecting a hotel reveals two additional fields.
  * These fields provide tools to help save prices using algorithms described in:
    * **Price List → Also Update Prices on Transports**
    * **Price List → Update Prices Based on Transport**

### Display Price List <a href="#display-price-list" id="display-price-list"></a>

After performing a search, the **Price List** results are displayed in a table format. For performance optimization:

* Prices are **not loaded all at once**.
* Clicking the **Display** button loads the **first 25 entries**.
* As you scroll down, the next 25 entries are loaded incrementally until the entire list is displayed.
* By default, most columns are **hidden** to improve performance and maintain clarity.

<figure><img src="../.gitbook/assets/image (290).png" alt=""><figcaption></figcaption></figure>

#### Column Overview

Column titles are abbreviated to keep the table tidy. Most fields include **tooltips** that display the full column name. Below is a full list of columns with explanations:

| Column        | Description                                                                                                                                                                                                                                                                                                                                      |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **PLTA ID**   | Price List Unique Identifier. Double-clicking the ID redirects to the **Web Booking Page** for the specific booking configuration.                                                                                                                                                                                                               |
| **Hotel**     | Hotel Code corresponding to the booking configuration.                                                                                                                                                                                                                                                                                           |
| **Room**      | Room Code corresponding to the booking configuration.                                                                                                                                                                                                                                                                                            |
| **Dep. Date** | Departure date for the booking configuration.                                                                                                                                                                                                                                                                                                    |
| **STAYS**     | Length of stay for interval 1 of the transport.                                                                                                                                                                                                                                                                                                  |
| **FHA**       | Free Hotel Allotment – Number of rooms available for this departure. Default value represents a one-week trip (interval 1). Hover displays allotments for 1, 2, 3, or 4 weeks.                                                                                                                                                                   |
| **FTA**       | Free Transport Allotment – Number of transport seats available. Default represents a one-week round trip. Hover displays available seats for 1, 2, 3, or 4 weeks round trip, as well as one-way outbound and inbound trips.                                                                                                                      |
| **P1**        | Price for Interval 1.                                                                                                                                                                                                                                                                                                                            |
| **P2**        | Price for Interval 2.                                                                                                                                                                                                                                                                                                                            |
| **P3**        | Price for Interval 3.                                                                                                                                                                                                                                                                                                                            |
| **P4**        | Price for Interval 4.                                                                                                                                                                                                                                                                                                                            |
| **CH1**       | Child Price Interval 1 – Price for a child occupying an extra bed. Calculated using an extra bed discount applied to the Grundprins (base price).                                                                                                                                                                                                |
| **Status**    | <p>Guarantee Availability of the PLTA (Transport + Hotel). Possible statuses:<br>- <strong>GREEN</strong> – Both transport and hotel have guaranteed allotments.<br>- <strong>YELLOW</strong> – One of transport or hotel lacks Guarantee Availability.<br>- <strong>PINK</strong> – Neither transport nor hotel has Guarantee Availability.</p> |

### Price List History <a href="#price-list-history" id="price-list-history"></a>

Price list history is a way to see the evolution in time of prices.

<figure><img src="../.gitbook/assets/image (32) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

At the beginning of each row, there are tree icons:

* View History - where you can see the evolution of prices like in Figure 3.
* Clear API Cache - by clicking the icon, you can clear the cache on the API for that particular prices
* Free Rooms Count|Recalculate Free room count - you can recalculate on demand both transport and hotel allotment for current prices

### Column Filters <a href="#column-filters" id="column-filters"></a>

<figure><img src="../.gitbook/assets/image (33) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Column Filters** allow you to display specific portions of information from the Price List grid.

* Each **interval group** has a corresponding checkbox: **Interval 1 (P1), Interval 2 (P2), Interval 3 (P3), Interval 4 (P4)**.
* Example: If **ALL PRICES (P1, P2, P3, P4)** is checked and **Interval 1** is selected as the active filter, only the **P1** column will be displayed in the table.
* Columns **not grouped into intervals** are always shown by default.

### Discounts <a href="#discounts" id="discounts"></a>

<figure><img src="../.gitbook/assets/image (34) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Relation PL & Related PL <a href="#relation-pl--related-pl" id="relation-pl--related-pl"></a>

These are covered in [Relation pricelist](pricelist.md#relation-pl--related-pl)

#### Also Update Prices on Transports <a href="#also-update-prices-on-transports" id="also-update-prices-on-transports"></a>

The fields are displayed only if the hotel is selected in the search form.

This function is used to update the prices that share the same hotel but have different transports. Let's take, for example, transport T0 and the Transport T1 and each one has a price list with the same hotel, H0, so we have price lists T0\_H0 and T1\_H0. Let's say that the difference between the price in T0 and T1 is 100, so we set this value on the transport T1 in the column Transport Price (**TP**). When the price on the T0\_H0 is changed, we have the option to update the price on the T1\_H0 as well.

`T1_H0_Price = T0_H0_Price + T1_H0_Transport_Price`

If Override Transport Price is checked and the filed next to the check-box is filled, the column Transport Price, will be overwritten in the transport T1\_H0

![!](https://docs.tourpaq.com/assets/images/updatePriceOnTransports-2ce165a0ee01856d1fa742c9bdb84fb1.png)

A simple workflow could be:

* Select in the search form Brand, Transport, Fix Quota and Hotel, and click Display button
* Check Also update prices on transports and select one or more Transport in the list (The list of transports in this drop down list are transport that have price list with the same hotel)
* Check the Override Transport Price and fill the amount
* Change one or more prices on the grid and click the Save button.

After the save, you will notice that the price on the selected transport with the same hotel and room has been changed accordingly by the formula above.

### Update Prices Based on Transport <a href="#update-prices-based-on-transport" id="update-prices-based-on-transport"></a>

This function allows prices to be **automatically recalculated when the Transport Price changes**.

* The fields are **displayed only when a hotel is selected** in the search form.
* **Purpose:** Update prices (P1, P2, D1, D2, etc.) based on changes in the selected transport.
* The **transport drop-down list** shows only transports that share the **same hotel and room**.
* Example: If **P1** was previously updated using the **Also Update Prices on Transports** tool, and the **Transport Price** is modified, **P1** will be recalculated accordingly based on the price list for that transport.

![!](https://docs.tourpaq.com/assets/images/updatePriceBasedOnTransport-b76eb367aade9faa3c6b2428cdd5760c.png)
