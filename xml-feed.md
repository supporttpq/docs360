---
description: >-
  What the Tourpaq XML feed contains, where each value comes from, and how to
  set it up for a brand.
hidden: true
---

# XML feed

**Users › Brands › Xml Feed**

## Purpose

The XML feed is a file with the offers of a brand that Tourpaq builds for an external partner. Each offer is one hotel stay on one departure date, with the prices, the flights, and the hotel information. Each offer has a booking link to your website.

You set up the brand-level settings of the feed in Tourpaq Office. Most of the hotel information in the file comes from the hotel itself, so a change on the hotel shows in the feed. See [Where each value comes from](xml-feed.md#where-each-value-comes-from).

## How to use

If the brand has no feed yet, contact Tourpaq support first. See [Before you start](xml-feed.md#before-you-start).

### Set up the feed of a brand

1. Open the brand, and then click the **Xml Feed** tab.
2. In **Adults Number**, enter the number of adults.
3. In **Hotel Image Size**, enter the size of the hotel images in the format width x height, such as `570x294`.
4. In **Presentation Site Url**, enter the address of your website.
5. In **URL Format**, build the booking link: select a placeholder in the list to add it to the text, and complete the rest of the address by typing.
6. Click **Save**.

{% hint style="info" %}
The booking link of each offer is the **Presentation Site Url** followed by the **URL Format**. Tourpaq replaces each placeholder, such as `[HotelID]` and `[DepartureDate]`, with the value of the offer.
{% endhint %}

### Name a facility for the feed

A hotel facility can have a separate name in the feed, so you can change it without changing the name guests see. See the **Name for Feeds** section of [Facilities](facilities.md).

## Reference

### Before you start

* Roles: Administrator, BrandManager, Support, and SuperAdministrator can open and change the **Xml Feed** tab. All except SuperAdministrator can open only the brands of their own company.
* The brand needs a feed record. If you click **Save** and Tourpaq Office asks you to contact support, ask Tourpaq support to set up the feed for the brand.

### Configuration

| Field                     | Description                                                                                                               | Values                                               | Required |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------- | -------- |
| **Adults Number**         | Number of adults.                                                                                                         | Whole number                                         | Yes      |
| **Hotel Image Size**      | Size of the hotel images. Each image link in the file has this size.                                                      | Width and height separated by `x`, such as `570x294` | Yes      |
| **Presentation Site Url** | The address of your website. It is the start of every booking link.                                                       | Text                                                 | Yes      |
| **URL Format**            | The rest of the booking link. Add placeholders from the list, such as `[HotelID]`, `[DepartureDate]`, and `[TripLength]`. | Text and placeholders                                | Yes      |

### What the file contains

The file starts with an `Offers` node that has a date and time. Each `Offer` node inside has these groups of nodes:

| Group        | Nodes                                                                                                                        | What it shows                                                                                            |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| Offer        | `Offer` (attribute `id`), `Duration`, `Currency`, `BookingURL`                                                               | The offer, the length of the stay, the currency, and the link to your website.                           |
| Prices       | `Prices` with one `Price` per party size                                                                                     | The price, and the normal price in the attribute `normal_price`.                                         |
| Departures   | `Name`, `IATA`, `Country`, `CountryCode`, `Time`, `Date`                                                                     | The departure airport and the departure date and time.                                                   |
| Destinations | `Name`, `IATA`, `Country`, `CountryCode`, `Resort`, `ResortCode`                                                             | The destination, resort, and arrival airport.                                                            |
| Hotel        | `Accommodation` (attribute `id`)                                                                                             | The hotel and the room type of the offer, with the facilities in `Amenities` and the photos in `Images`. |
| Products     | `Product` with `ProductID`, `Code`, `Name`, `Days`, and `BoardTypeCode`                                                      | The board and the extras that come with the offer, such as a visa.                                       |
| Transport    | `Transport` with `Direction` (Outbound or Homebound) and `Mode`, and one `Segment` per flight with `Departure` and `Arrival` | The flights: airport, flight number, date, and time of each leg.                                         |

### Where each value comes from

The hotel information in the file comes from the hotel in Tourpaq Office. Change it there.

| In the file                             | Where you maintain it                                                                                                                                                            |
| --------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Hotel (`Accommodation id`)              | The ID of the hotel. It is also the `[HotelID]` placeholder.                                                                                                                     |
| `Name`                                  | **Hotel Name** on the **Overview** tab of the hotel.                                                                                                                             |
| `Rating`                                | **Stars** on the **Overview** tab.                                                                                                                                               |
| `Address` and `URL`                     | **Address** and **Url** on the **Overview** tab.                                                                                                                                 |
| `Description`                           | **Short Description** on the **Web** tab.                                                                                                                                        |
| `HtmlDescription`                       | **HTML Description** on the **Web** tab.                                                                                                                                         |
| `Latitude` and `Longitude`              | **Latitude** and **Longitude** in the **General settings** section of the **Web** tab.                                                                                           |
| `Room`                                  | **Room Name** of the room type on the **Room Types** tab.                                                                                                                        |
| `persons_per_room`                      | **Ordinary Bed Number** of that room type.                                                                                                                                       |
| `Resort` and `ResortCode`               | **Resort** on the **Overview** tab.                                                                                                                                              |
| `Images`                                | The photos on the **Photos** tab. The size is the **Hotel Image Size** of the brand.                                                                                             |
| `Pool`, `ChildPool`, and `AllInclusive` | The hotel facilities **Pool**, **Børnepool**, and **All Inclusive** in the **Hotel facilities** section of the **Web** tab: Yes when the facility is selected, No when it isn't. |
| `DistanceBeach` and `DistanceCenter`    | **Afstand til strand** and **Afstand til centrum** in the **Afstande** group of the hotel facilities, in meters.                                                                 |
| `BookingURL`                            | **Presentation Site Url** and **URL Format** of the brand.                                                                                                                       |

## Example: follow one offer

This offer is from a real feed. To follow it, open hotel 11383 in Tourpaq Office, and compare each value.

```xml
<Offer id="14303813">
  <Duration>7</Duration>
  <Currency>DKK</Currency>
  <Prices>
    <Price required_pax="2" price_for_pax="2" normal_price="10398">7398</Price>
    <Price required_pax="3" price_for_pax="3" normal_price="15597">8597</Price>
    <Price required_pax="4" price_for_pax="4" normal_price="20796">9796</Price>
  </Prices>
  <BookingURL><![CDATA[https://www.example.com/tourpaq/travel_market/feedRedirect?hotel_id=11383&departure_date=21-11-2026&adults=2&departures=44&travel_length=7]]></BookingURL>
  <Departures>
    <Departure>
      <Name>Billund</Name>
      <IATA>BLL</IATA>
      <Country>Danmark</Country>
      <CountryCode>DK</CountryCode>
      <Time>06:50</Time>
      <Date>2026-11-21</Date>
    </Departure>
  </Departures>
  <Destinations>
    <Destination>
      <Name>Gran Canaria</Name>
      <IATA>LPA</IATA>
      <Country>Spanien</Country>
      <CountryCode>ES</CountryCode>
      <Resort>Puerto Rico</Resort>
      <ResortCode>LPA-PURI</ResortCode>
    </Destination>
  </Destinations>
  <Accommodation id="11383">
    <Description><![CDATA[Holiday Club Puerto Calma ligger i det populære ferieområde Puerto Rico ...]]></Description>
    <HtmlDescription><![CDATA[<h2>Dejligt lejlighedshotel i solrige Puerto Rico</h2><div>...]]></HtmlDescription>
    <Room>2-vær. lejl (2-4 pers.) - skrå havudsigt</Room>
    <Name>Holiday Club Puerto Calma</Name>
    <Rating>3+</Rating>
    <persons_per_room>2</persons_per_room>
    <URL><![CDATA[www.holidayclubcanarias.com/da/club-puerto-calma/]]></URL>
    <Address><![CDATA[C) Joaquín Blanco Torrent 2, 351 30 Puerto Rico]]></Address>
    <Latitude>27.78322736</Latitude>
    <Longitude>-15.70778253</Longitude>
    <Amenities>
      <AllInclusive>No</AllInclusive>
      <Pool>Yes</Pool>
      <ChildPool>Yes</ChildPool>
      <DistanceBeach>1500 meters</DistanceBeach>
      <DistanceCenter>3000 meters</DistanceCenter>
    </Amenities>
    <Images>
      <Image><![CDATA[https://photos.example.com/GetPhoto.ashx?type=Hotel&photosize=570x294&photoid=138326]]></Image>
      ...
    </Images>
  </Accommodation>
  <Transports>
    <Transport Direction="Outbound" Mode="plane">
      <Segments>
        <Segment No="1">
          <Departure Name="Billund" IATA="BLL" FlightNo="CAT711" Date="2026-11-21" Time="06:50" CountryCode="DK" />
          <Arrival Name="Las Palmas" IATA="LPA" FlightNo="CAT711" Date="2026-11-21" Time="11:15" CountryCode="ES" />
        </Segment>
      </Segments>
    </Transport>
    <Transport Direction="Homebound" Mode="plane">
      <Segments>
        <Segment No="1">
          <Departure Name="Las Palmas" IATA="LPA" FlightNo="CAT712" Date="2026-11-28" Time="12:20" CountryCode="ES" />
          <Arrival Name="Billund" IATA="BLL" FlightNo="CAT712" Date="2026-11-28" Time="18:30" CountryCode="DK" />
        </Segment>
      </Segments>
    </Transport>
  </Transports>
</Offer>
```

The example is shortened: empty nodes and most of the images and text are left out. The hotel part of the offer comes from this place:

| In the offer                         | Value                                                                                                                                        | Where it comes from                                                                                                                                                                                                                                          |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `Name`                               | Holiday Club Puerto Calma                                                                                                                    | **Hotel Name** of hotel 11383.                                                                                                                                                                                                                               |
| `Rating`                             | 3+                                                                                                                                           | **Stars** of the hotel.                                                                                                                                                                                                                                      |
| `Address` and `URL`                  | The street address and the hotel website                                                                                                     | **Address** and **Url** of the hotel.                                                                                                                                                                                                                        |
| `Description` and `HtmlDescription`  | The text that starts with "Holiday Club Puerto Calma ligger"                                                                                 | **Short Description** and **HTML Description** on the **Web** tab.                                                                                                                                                                                           |
| `Latitude` and `Longitude`           | 27.78322736 and -15.70778253                                                                                                                 | The same fields on the **Web** tab.                                                                                                                                                                                                                          |
| `Room` and `persons_per_room`        | The room name, and 2                                                                                                                         | **Room Name** and **Ordinary Bed Number** of the room type on the **Room Types** tab.                                                                                                                                                                        |
| `Resort` and `ResortCode`            | Puerto Rico and LPA-PURI                                                                                                                     | **Resort** on the **Overview** tab.                                                                                                                                                                                                                          |
| `Pool` and `ChildPool`               | Yes and Yes                                                                                                                                  | The facilities **Pool** and **Børnepool** are selected.                                                                                                                                                                                                      |
| `AllInclusive`                       | No                                                                                                                                           | The facility **All Inclusive** isn't selected.                                                                                                                                                                                                               |
| `DistanceBeach` and `DistanceCenter` | 1500 meters and 3000 meters                                                                                                                  | **Afstand til strand** and **Afstand til centrum**.                                                                                                                                                                                                          |
| `Images`                             | 18 images, each with `photosize=570x294`                                                                                                     | The 18 photos on the **Photos** tab, and the **Hotel Image Size** `570x294` of the brand.                                                                                                                                                                    |
| `BookingURL`                         | `https://www.example.com/tourpaq/travel_market/feedRedirect?hotel_id=11383&departure_date=21-11-2026&adults=2&departures=44&travel_length=7` | The **Presentation Site Url**, followed by the **URL Format** `/tourpaq/travel_market/feedRedirect?hotel_id=[HotelID]&departure_date=[DepartureDate]&adults=[BedNumber]&departures=[DepartureID]&travel_length=[TripLength]` with the placeholders replaced. |

## Related pages

* [Brands](brands/)
* [Facilities](facilities.md)
* [Integration overview](integration/overview.md)
