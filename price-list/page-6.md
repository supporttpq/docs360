---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Pricelist

Hotel **Price List** is the place where prices are created or managed for particular packages. Usually a package contains a [Transport](../transport/transport/) and a [Room types](../base-room-types.md) Hotel but this is not necessarily the case. The price can be added based on interval, discounts, children, or groups, or it can be set for one way or round trip. Each package has a date assigned; this date is pointing to the departure date of the trip.

### Create/copy price list <a href="#createcopy-price-list" id="createcopy-price-list"></a>

Creating a price list is fairly easy. From the **Price List** tab, select "Create/Copy Price List."

* Choose the brand for which the price list is created.
* Select the transport.
* Select the transport's fix quota.
* Select the hotel.
* Select the rooms.
* Click **Create new price list**

<figure><img src="../.gitbook/assets/image (29) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Price List Search <a href="#price-list-search" id="price-list-search"></a>

The search helps to find prices based on brands, Transport, Hotel, Room and the departure date interval. To get results The most basic search you can get is by choosing All Brands and Transport but for the best performance, try to fill most of the fields. The list of transports from the drop-down list is filtered based on the brand selection.

<figure><img src="../.gitbook/assets/image (30) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

If All Brands are selected, all the transport will appear in the Transport drop-down list; otherwise, only the transport assigned to that specific brand will appear. The Transports are assigned to the brands in the Transport / Brands tab | Brands Tab under Edit Transport. Also, the Transport is not shown in the drop-down list if the Transport is set as hidden. The visibility of the Transport can be set on the Transport / General\_tab / General tab.

When the Transport is selected in the drop-down list, the Fix Quota is filled in the multiple selection view and also the Hotels. Only the hotels that share the same price list with the selected Transport will be shown. The hotels that are in the hidden status will not be shown in the drop-down list. The visibility for the hotels can be sent from the Hotel / Hotel\_tab / General Tab.

When the hotel is selected, two more fields are displayed. These are some additional tools that can help to save the prices based on an algorithm explained on Price List#Also\_Update\_Prices\_on\_Transports|Also Update Prices on Transports and Price List#Update\_Prices\_Based\_on\_Transport|Update Prices Based on Transport

### Display Price List <a href="#display-price-list" id="display-price-list"></a>

The search will produce a result like the one shown in the next picture. For performance reasons, the prices will not be loaded all at once. When the Display button is hit, the first 25 fields are loaded; when scrolling down, the next 25 fields will be loaded, and so on until the entire list is loaded into the page. By default, most of the columns will be hidden for reasons of performance and visibility.

<figure><img src="../.gitbook/assets/image (31) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The column titles are abbreviated so the table can be more tidy. Most of the fields have a tooltip with the full name of the column. The full list of the columns and explanations is as follows:

* **PLTA ID**- Price List Unique identifier - by double clicking on the ID you will be redirected to the web booking page for the specific booking configuration
* **Hotel** - Hotel Code - The hotel code for this specific booking configuration
* **Room** - Room Code - The room code for this specific booking configuration
* **Dep. date** - Departure Date - The Departure Date for this specific booking configuration
* **FHA** - Free Rooms Count - How many rooms are available for this departure. The default value is for a one-week trip (or interval 1) on hover there can be the allotments for 1, 2, 3, and 4 weeks.
* **FTA** - Free Transport Allotment - How many transport seats are available for this trip. The default value is one week round trip. On hover, there can be displayed the available seats for 1, 2, 3, or 4 weeks round trip and also one-way outbound and one-way inbound.
* **P1** - Price Interval 1&#x20;
* **P2** - Price Interval 2
* **P3** - Price Interval 3&#x20;
* **P4** - Price Interval 4&#x20;
* **CH1**- Child Price Interval 1. Room Price for a child that occupies an extra child bed. From the Grundprins is made an extra bed discount to reach the Child Price.
* **Status** - This column is showing the Guarantee Availability of the PLTA (Transport Guarantee Availability + Hotel Guarantee Availability). It has 3 statuses:&#x20;
  * GREEN - when both instances, transport and hotel, have guaranteed allotments;&#x20;
  * YELLOW - when one of the instances does not have Guarantee Availability,&#x20;
  * PINK - when none of the instances has Guarantee Availability.

### Price List History <a href="#price-list-history" id="price-list-history"></a>

Price list history is a way to see the evolution in time of prices.

<figure><img src="../.gitbook/assets/image (32) (1) (1).png" alt=""><figcaption></figcaption></figure>

At the beginning of each row, there are tree icons:

* View History - where you can see the evolution of prices like in Figure 3.
* Clear API Cache - by clicking the icon, you can clear the cache on the API for that particular prices
* Free Rooms Count|Recalculate Free room count - you can recalculate on demand both transport and hotel allotment for current prices

### Column Filters <a href="#column-filters" id="column-filters"></a>

<figure><img src="../.gitbook/assets/image (33) (1) (1).png" alt=""><figcaption></figcaption></figure>

These filters are a way to show a part of the information from the price list grid. There is a check box for each interval group (Interval 1, Interval 2, Interval 3, and Interval 4). Ex. ALL PRICES (P1, P2, P3, P4) checked, and I1 on top will show the P1 column in the table. The other columns that are not grouped in intervals are shown by default.

### Discounts <a href="#discounts" id="discounts"></a>

<figure><img src="../.gitbook/assets/image (34) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Relation PL & Related PL <a href="#relation-pl--related-pl" id="relation-pl--related-pl"></a>

These are covered in [Relation pricelist](page-6.md#relation-pl--related-pl)

#### Also Update Prices on Transports <a href="#also-update-prices-on-transports" id="also-update-prices-on-transports"></a>

The fields are displayed only if the hotel is selected in the search form.

This function is used to update the prices that share the same hotel but have different transports. Let's take, for example, transport T0 and the Transport T1 and each one has a price list with the same hotel, H0, so we have price lists T0\_H0 and T1\_H0. Let's say that the difference between the price in T0 and T1 is 100, so we set this value on the transport T1 in the column Transport Price (**TP**). When the price on the T0\_H0 is changed, we have the option to update the price on the T1\_H0 as well.

`T1_H0_Price = T0_H0_Price + T1_H0_Transport_Price`

If //Override Transport Price// is checked and the filed next to the check-box is filled, the column Transport Price, will be overwritten in the transport T1\_H0

![!](https://docs.tourpaq.com/assets/images/updatePriceOnTransports-2ce165a0ee01856d1fa742c9bdb84fb1.png)

A simple workflow could be:

* Select in the search form Brand, Transport, Fix Quota and Hotel, and click Display button
* Check Also update prices on transports and select one or more Transport in the list (The list of transports in this drop down list are transport that have price list with the same hotel)
* Check the Override Transport Price and fill the amount
* Change one or more prices on the grid and click the Save button.

After the save, you will notice that the price on the selected transport with the same hotel and room has been changed accordingly by the formula above.

### Update Prices Based on Transport <a href="#update-prices-based-on-transport" id="update-prices-based-on-transport"></a>

The fields are displayed only if the hotel is selected in the search form.

This function is used when the Transport Price is updated and the prices P1, P2, D1, D2, etc., should be changed based on the selected transport. The transports shown in the drop-down list are transports that share the same hotel and room. The price P1 has been updated using the //Also update prices on transports// tool, and if the transport price is changed, the P1 price must be recalculated based on that price list.

![!](https://docs.tourpaq.com/assets/images/updatePriceBasedOnTransport-b76eb367aade9faa3c6b2428cdd5760c.png)
