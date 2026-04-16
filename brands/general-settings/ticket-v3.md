# Ticket V3

## Overview

This page describes the expected behavior and UI/UX improvements for Bravo Ticket V4 based on tested booking scenarios, including support for dynamic flights (GDS-based transport).

## Scope

The following areas are covered:

* Price Specification
* Seating & Room Allocation
* Pagination
* Layout & Design Improvements
* Dynamic Flights (GDS)
* Known Issues

***

## Price Specification

### Departure Airport Handling

{% hint style="info" %}
Applies only when more than one departure airport exists in the booking.
{% endhint %}

#### Expected Behavior

* Display the departure airport per passenger
* Position: below passenger name (blue header line)
* Prefix: **"Departure:"** (dictionary-based, editable)

#### Screenshot

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

***

### Extra Bed Discount&#x20;

#### Expected Behavior

* Add separate line:\
  &#xNAN;**"Voksen ekstra seng rabat"**
* Include in total discount calculation

***

### Supplements Breakdown {#supplements}

> \[!warning]\
> Current implementation aggregates all supplements into one line. This must be split.

#### Expected Behavior

* Display each supplement as a separate line
* Include:
  * all manual supplements
  * auto-generated supplements (e.g. single supplement)
* Exclude:
  * supplements already included in base price

***

### Formatting Rules {#price-formatting}

#### Amount Formatting

* Remove **"kr."** before all amounts
* Add **"kr."** after:
  * "Rabat i alt"
  * "Totalpris"

#### Fixes

* Add missing decimals for "Rabat i alt"
* Remove dot after room type name
* Fix double blue lines → consistent white/blue pattern

#### Text Fix

```
Har du ikke tilkøbt fx indchecket bagage, transfer m.m., vil produkterne ikke fremgå i prisspecifikationen.
```

#### Screenshot

```
[PLACEHOLDER - Price specification fixes]
```

***

## Seating & Room Allocation (TILVALG) {#tilvalg}

### Display Conditions {#tilvalg-conditions}

> \[!info]\
> The table is conditionally rendered.

Display only if:

* Seating is selected (Extra Category), OR
* Room number is selected in booking

***

### Table Structure {#tilvalg-structure}

#### Header

**TILVALG**

#### Columns

| Field             | Header             |
| ----------------- | ------------------ |
| Pax number        | —                  |
| First name        | Fornavn            |
| Outbound seating  | Sæde ved udrejse   |
| Homebound seating | Sæde ved hjemrejse |
| Room number       | Valg af værelse    |

***

### Behavior Rules {#tilvalg-behavior}

* Seating:
  * Show seat number if selected
  * Otherwise display: ❌
* Room number:
  * Display only for passenger 1

***

### Responsive Behavior {#tilvalg-responsive}

> \[!info]\
> Table must adapt to available space.

* Dynamic column width
* Responsive layout

***

### Static Text {#tilvalg-static-text}

```
Der vil kun stå et nummer ud for dit navn, hvis du har valgt et specifikt sæde...
```

#### Screenshot

```
[PLACEHOLDER - Seating and room table]
```

***

## Pagination (Page Splitting) {#pagination}

### Expected Behavior {#pagination-behavior}

* If space allows:
  * Multiple passengers on same page
* Otherwise:
  * Split correctly across pages

***

### Issues to Fix {#pagination-issues}

> \[!warning]

* Duplicate pages (e.g. page 3 rendered twice)
* Header outside printable area

***

## Layout & Design Improvements {#layout-design}

### General UI {#layout-general}

* "Min side" link:
  * Color: **#1e4b74**
* Email:
  * `service@bravotours.dk`
  * No bold / underline

***

### Transport Passenger Box {#transport-box}

* Always display in **2 columns**
* Add spacing below box

***

### Passenger List {#passenger-list}

* Text:
  * "Flere passenger se næste side"
  * Font size: 9 pct
* Ensure consistent font across pages

***

### INDKVARTERING {#indkvartering}

> \[!info]

* Remove blue background
* Use white background
* Use bullet points for multiple passengers

***

### BETALING {#betaling}

* Remove "kr." before amounts
* Add "kr." after "Totalpris"

***

### BEMÆRKNINGER {#remarks}

* Header uppercase
* Text size: 9 pct

***

### HOTEL DESCRIPTION {#hotel-description}

> \[!info]

* Ensure consistent spacing across pages

***

## Dynamic Flights (GDS) {#dynamic-flights}

### Overview {#dynamic-overview}

> \[!info]\
> Applies when transport type is **Dynamic Flight (System Transport / GDS)**.

#### Expected Behavior

* Provide extended flight information:
  * PNR
  * E-ticket number
  * Baggage
* Add dedicated page in the e-ticket
* Display configurable text from:
  * **User > Brands > GDS**

***

### New E-ticket Page {#dynamic-new-page}

> \[!info]\
> A new page must be inserted before the hotel description.

#### Page Structure

* Standard header:
  * Logo
  * Booking number
* Standard footer:
  * Page number

***

### Table 1: Passenger Flight Details {#dynamic-table-1}

#### Header

**DETAJLER OM DIN REJSE MED RUTEFLY**

#### Columns

| Field      | Header    |
| ---------- | --------- |
| Pax number | —         |
| First name | Fornavn   |
| Last name  | Efternavn |
| Baggage    | Bagage    |
| PNR        | PNR       |
| E-ticket   | E-ticket  |

#### Rules

* PNR: from Booking → GDS tab
* E-ticket:
  * from Booking → GDS tab
  * if not issued → leave empty

***

### Table 2: Flight Information {#dynamic-table-2}

* Same structure as:
  * **FLYINFORMATION (page 1)**

***

### GDS Text Display {#dynamic-gds-text}

#### Behavior

* Display text configured in:
  * **Brand > GDS tab**

#### Placement

* Below second table

#### Reference

```
[PLACEHOLDER - Page 7 BT billetdesign]
```

***

### GDS Information on Page 1 {#dynamic-page1}

> \[!info]

#### Expected Behavior

* Display GDS text also on **page 1**

#### Placement

* Below "FLYINFORMATION" table
* Before passenger info (blue box)

#### Screenshot

```
[PLACEHOLDER - GDS text on page 1]
```

***

## Known Issues {#known-issues}

> \[!warning]

### GRUNDPRISEN INKLUDERER

* Displays incorrect data

#### Related Tickets

* THT-60377
* THT-60816
