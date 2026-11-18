---
description: What the Tourpaq XML feed contains and how to set it up for a brand.
hidden: true
---

# XML feed

**Users › Brands › Xml Feed**

## Purpose

The XML feed is a file with the offers of a brand that Tourpaq builds for an external partner. Each offer is one hotel stay on one departure date, with the prices, the flights, and the hotel information. Each offer has a booking link to your website.

You set up the brand-level settings of the feed in Tourpaq Office.

## How to use

If the brand has no feed yet, contact Tourpaq support first. See [Before you start](xml-feed.md#before-you-start).

### Set up the feed of a brand

1. Open the brand, and then click the **Xml Feed** tab.
2. In **Adults Number**, enter the number of adults.
3. In **Hotel Image Size**, enter the size of the hotel images in the format width x height, such as `800x600`.
4. In **Presentation Site Url**, enter the address of your website.
5. In **URL Format**, build the booking link: select a placeholder in the list to add it to the text, and complete the rest of the address by typing.
6. Click **Save**.

{% hint style="info" %}
The **URL Format** is the part of the address that changes per offer. Placeholders such as `[HotelID]` and `[DepartureDate]` are replaced with the values of each offer.
{% endhint %}

### Name a facility for the feed

A hotel facility can have a separate name in the feed, so you can change it without changing the name guests see. See the **Name for Feeds** section of [Facilities](facilities.md).

## Examples

### Example of an offer

The file starts with an `Offers` node that has a date and time. Each `Offer` node inside has the nodes below. The example is shortened.

```xml
<Offers DateTime="18-11-2026 09:58:11">
  <Offer id="14303813">
    <Duration>7</Duration>
    <Currency>DKK</Currency>
    <Prices>
      <Price required_pax="2" price_for_pax="2" normal_price="10398">7398</Price>
      <Price required_pax="3" price_for_pax="3" normal_price="15597">8597</Price>
    </Prices>
    <BookingURL><![CDATA[https://www.example.com/booking?hotel_id=11383&departure_date=21-11-2026&adults=2&departures=44&travel_length=7]]></BookingURL>
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
      <Name>Example Hotel</Name>
      <Rating>3+</Rating>
      <Type>Hotel</Type>
      <Room>2-room apartment (2-4 persons)</Room>
      <Latitude>27.783</Latitude>
      <Longitude>-15.707</Longitude>
      <Amenities>
        <AllInclusive>No</AllInclusive>
        <Pool>Yes</Pool>
        <ChildPool>Yes</ChildPool>
        <DistanceBeach>500 meters</DistanceBeach>
        <DistanceCenter>3000 meters</DistanceCenter>
      </Amenities>
    </Accommodation>
    <Products>
      <Product ProductID="20444" Code="THA145-STD-MAI" Name="Mini All Inclusive" Days="0" BoardTypeCode="MAI" />
    </Products>
    <Transports>
      <Transport Direction="Outbound" Mode="plane">
        <Segments>
          <Segment No="1">
            <Departure Name="Billund" IATA="BLL" FlightNo="CAT711" Date="2026-11-21" Time="06:50" CountryCode="DK" />
            <Arrival Name="Las Palmas" IATA="LPA" FlightNo="CAT711" Date="2026-11-21" Time="11:15" CountryCode="ES" />
          </Segment>
        </Segments>
      </Transport>
    </Transports>
  </Offer>
</Offers>
```

## Reference

### Before you start

* Roles: Administrator, BrandManager, Support, and SuperAdministrator can open and change the **Xml Feed** tab. All except SuperAdministrator can open only the brands of their own company.
* The brand needs a feed record. If you click **Save** and Tourpaq Office asks you to contact support, ask Tourpaq support to set up the feed for the brand.

### Configuration

| Field                     | Description                                                                                                               | Values                                               | Required |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------- | -------- |
| **Adults Number**         | Number of adults.                                                                                                         | Whole number                                         | Yes      |
| **Hotel Image Size**      | Size of the hotel images.                                                                                                 | Width and height separated by `x`, such as `800x600` | Yes      |
| **Presentation Site Url** | Address of your website.                                                                                                  | Text                                                 | Yes      |
| **URL Format**            | The booking link of an offer. Add placeholders from the list, such as `[HotelID]`, `[DepartureDate]`, and `[TripLength]`. | Text and placeholders                                | Yes      |

### What the file contains

| Group        | Nodes                                                                                                                                                             | What it shows                                                                     |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Offer        | `Offer` (attribute `id`), `Duration`, `Currency`, `BookingURL`                                                                                                    | The offer, the length of the stay, the currency, and the link to your website.    |
| Prices       | `Prices` with one `Price` per party size                                                                                                                          | The price, and the normal price in the attribute `normal_price`.                  |
| Departures   | `Name`, `IATA`, `Country`, `CountryCode`, `Time`, `Date`                                                                                                          | The departure airport and the departure date and time.                            |
| Destinations | `Name`, `IATA`, `Country`, `CountryCode`, `Resort`, `ResortCode`                                                                                                  | The destination, resort, and arrival airport.                                     |
| Hotel        | `Accommodation` (attribute `id`) with `Name`, `Rating`, `Type`, `Room`, `Description`, `HtmlDescription`, `Address`, `URL`, `Latitude`, `Longitude`, and `Images` | The hotel and the room type of the offer.                                         |
| Facilities   | `Amenities` with `AllInclusive`, `Pool`, `ChildPool`, `DistanceBeach`, and `DistanceCenter`                                                                       | Yes or No for the facilities, and the distances to the beach and the town center. |
| Products     | `Product` with `ProductID`, `Code`, `Name`, `Days`, and `BoardTypeCode`                                                                                           | The board and the extras that come with the offer, such as a visa.                |
| Transport    | `Transport` with `Direction` (Outbound or Homebound) and `Mode`, and one `Segment` per flight with `Departure` and `Arrival`                                      | The flights: airport, flight number, date, and time of each leg.                  |

### Related pages

* [Brands](brands/)
* [Facilities](facilities.md)
* [Integration overview](integration/overview.md)
