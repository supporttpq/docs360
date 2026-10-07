---
description: >-
  The Version 2 ticket is a multi-page PDF booking document laid out as plain
  tables, with no brand colours, custom fonts, or decorative imagery.
tags:
  - '15.5'
---

# Ticket V2 - Structure

### Overview

Ticket Version 2 (BILLET) is one of three selectable e-ticket layouts, configured on the Brands General Settings page, under Ticket → Version.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/11.09.2026_09.09.33_REC.png" alt="Version 2 ticket preview showing the booking header, itinerary, accommodation, passengers, and payment plan."><figcaption><p>Version selection</p></figcaption></figure></div>

It is generated from the same booking data — transport (flights, buses, and trains), accommodation, passengers, pricing, payment plan and hotel information.

Version 2 presents this data as a sequence of plain tables under section headings in the brand's configured language — Danish (Rejseplan, Opholdet, Rejsedeltagere, Betalingsplan, Specifikation af rejsebestilling, Forklaringer) or Swedish for a brand configured that way.

### Purpose

Use this page to:

* Confirm what a customer will see on their printed or emailed ticket before departure.
* Check where a configured price component, discount, or special service request will print, when troubleshooting a customer query about their ticket.

### Preconditions

* The booking exists and contains at least one product (hotel, transport, or similar).
* The brand's ticket layout is set to Version 2 on the General Settings page, under Ticket → Version.
* You know which Extras and discounts are configured on the booking, so you can locate them on the printed ticket.
* For Bus or Train segments, you know the pickup point configured on the transport's route, since it determines the ticket's Fra / Från value.

### How-to

{% stepper %}
{% step %}
Set the ticket version

Go to System Setup → Brands → General, open the brand, expand Ticket, and set Version to Version 2. Click Save.
{% endstep %}

{% step %}
Generate the ticket

Go to Booking → Open Booking → Click Print Ticket ->Save
{% endstep %}
{% endstepper %}

Tourpaq generates a PDF in the structure described under Field Reference below, using the booking's current data.

{% hint style="info" %}
Ticket Customization is not available on this layout. Brand colours, fonts, star icons, and decorative images cannot be configured for it. A Version 2 ticket always prints in the plain black-and-white table layout shown below, regardless of any customisation saved for the brand.
{% endhint %}

### Field Reference

### Page 1 — Booking summary, itinerary and payment plan

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/11.09.2026_09.28.35_REC.png" alt="First page of a Version 2 ticket showing the booking header, Rejseplan, Opholdet, Rejsedeltagere, and Betalingsplan sections."><figcaption><p>Page 1 combines the booking summary, itinerary, accommodation, passenger details, and payment plan.</p></figcaption></figure></div>

#### Booking header

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/11.09.2026_09.38.14_REC.png" alt="Ticket booking header with Booking nr., customer details, booking date, print date, Ferierådgiver, and brand company details."><figcaption><p>Booking header showing customer, booking, travel consultant, and brand company information.</p></figcaption></figure></div>

Left column:

* Shows Booking nr.,
* the customer's name and address,
* Bestillingsdato (booking date),
* Udskriftsdato (print date),
* Ferierådgiver (travel consultant),

Right column:

* The brand's company details (name, address, phone, CVR No.). The company details come from General Settings → Ticket
* Company logo / banner - Displays the brand's Logo and Banner images from General Settings

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/11.09.2026_09.40.30_REC.png" alt="Min billet login callout showing Bookingnr. and Adgangskode Internet for Customer Center access."><figcaption><p>Set the Logo and Banner in Brands -> Ticket</p></figcaption></figure></div>

\
Min billet - login:

A boxed callout with the Bookingnr. and Adgangskode Internet (web password) the customer uses to log in to Customer Center

#### Rejseplan (itinerary)

One row per transport segment in the booking. Flight segments show:

* Afrejsedato (departure date),
* Afgang (departure time),
* From (departure airport),
* Flyselskab (airline),
* Fly nr. (flight number),
* Ankomstdato,
* Ankomst (arrival time),
* Flytid (flight duration),
* Til (arrival airport).

Bus and Train segments use the same table structure as Flight, with brand-specific column names matching the brand's language.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/11.09.2026_09.54.59_REC.png" alt="Rejseplan table showing transport segment dates, times, departure and arrival locations, airline, flight number, and flight duration."><figcaption><p>Rejseplan lists each transport segment with its schedule, route, and transport details.</p></figcaption></figure></div>

* The `Fra` / `Från` (From) value is the pickup point configured on the transport's route (also shown elsewhere as `Opsamlingssted`). Pickup points, and meeting, departure and return times, all come from that route setup.
* When no pickup point is selected on the booking, the field shows a fallback message instead of being left blank.
* The arrival-date column is labelled `Ankomstdato` (Danish brands) or `Ankomstdatum` (Swedish brand), matching the Flight table's naming.
* No summary block appears above the table — the departure date, arrival date, and passenger count are shown only in the detailed rows.
* No `Kørselsvejledning` (driving/collection instructions) line prints for Bus and Train segments.

#### Opholdet (accommodation)

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/11.09.2026_09.59.15_REC.png" alt="Opholdet table showing destination, hotel, star rating, arrival date, departure date, number of units, and room type."><figcaption><p>Opholdet lists every booked stay, including hotel, dates, quantity, and Værelser.</p></figcaption></figure></div>

One row per stay:

* Rejsemål (destination),
* Hotel (hotel name),
* a custom star-rating text,
* Ankomst (arrival day),
* Afrejse (departure day),
* Antal (number of units),
* Værelser (room type).

#### Rejsedeltagere (passengers)

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/11.09.2026_10.05.17_REC.png" alt="Rejsedeltagere table showing Bookingnr., passenger name, date of birth, room type, transport, pension, price, total price, deposit, and amount due."><figcaption><p>Rejsedeltagere lists passenger details, booked services, and payment amounts.</p></figcaption></figure></div>

One row per traveller:

* Bookingnr.,
* Navn (passenger name),
* Fødselsdato (date of birth),
* Værelser (room type),
* Transport,
* Pension (Board Type),
* Price. Followed by Total Price, Deposit, and Skyldigt (amount due).

#### Betalingsplan (payment plan)

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/11.09.2026_10.08.06_REC.png" alt="Betalingsplan table showing payment amounts, due dates, IBAN-number, and BIC-kode or SWIFT-adresse."><figcaption><p>Betalingsplan shows each instalment, its due date, and payment account details.</p></figcaption></figure></div>

One row per rate (deposit, balance) with amount and due date, followed by IBAN-number and BIC-kode/SWIFT-adresse.

This part can be hidden when **Hide Payment Details** is enabled in General Settings

### Page 2 — Price specification and seat/room assignment

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/11.09.2026_10.37.14_REC.png" alt="Second page of a Version 2 ticket showing travel booking specifications, room assignments, and flight seat reservations."><figcaption><p>Page 2 contains price specifications, Tildelinger, and Flysæde reservation.</p></figcaption></figure></div>

#### Field Description

Specifikation af rejsebestilling (Travel booking specifications)

* A single table listing every passenger in one row, with columns Grundpris (base price), Rabat (discount), Forsikring (insurance), Afb.fors. (cancellation insurance), Golf Course, AutIndDirection, Seating, TREX, Tillæg i alt (supplements total), Pris pr. pers., and one column per instalment due date. A Totalpris DKK row sums every column.
* Tildelinger (room assignments) - One row per passenger:
  * Rejsedeltagere (passenger name),
  * Hotel,
  * Værelser (room type),
  * Room Number — shows how passengers are allocated to rooms (how they are grouped by room)
* Flysæde reservation (seat reservation)- One row per passenger, showing the seat chosen (sædevalg) for each flight date, followed by the aircraft seat-map type (for example A320 Seat Type). It is shown when seating is selected as an Extra Category

### Page 3 — Explanations and special service requests

#### Field Description

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/11.09.2026_10.51.45_REC.png" alt="Forklaringer section showing the explanations legend for price components, extras, discounts, and passenger quantities."><figcaption><p>Page 3</p></figcaption></figure></div>

#### Forklaringer (explanations)

* A legend that expands every extras, discounts/supplemnets used on page 2 — Vaerelse, Rabat, Forsikring, Golf Course, AutIndDirection, Seating, TREX, Tillæg i alt — each with the passenger number(s) it applies to and a quantity (Antal).
* Bemærkninger (remarks) - Ticket help text comment - it can be configured under the Brands -> General settings-> Ticket -> Ticket help text comments

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/11.09.2026_10.56.50_REC.png" alt="Special service request list showing passenger names, SSR codes, and plain-language service descriptions."><figcaption><p>Ticket help text comment</p></figcaption></figure></div>

* List of special services (SSR) - One entry per participant, listing every requested SSR code with its plain-language description (for example AVML ( Vegetarian Meal Requested )) — shown when Show SSR On Ticket is enabled in General Settings Show SSR On Ticket is a general Ticket setting.

### Pages 4–5 — Room/Hotel information

#### Field Description

* Værelsesbeskrivelse (room description) - The booked room's name in bold, followed by its description text on the next line. It is shown when Show room info is enabled and the room type has a description Uses the Brand Description if one exists, otherwise the Default Description; rooms with no description at all are skipped with no placeholder shown.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/11.09.2026_11.07.29_REC.png" alt="Værelsesbeskrivelse section showing a booked room name and its descriptive text."><figcaption><p>Værelsesbeskrivelse shows the booked room name and available room description.</p></figcaption></figure></div>

* Hotelfaciliteter (hotel facilities) - shows the hotel facilities — shown when the hotel has facility data configured

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/11.09.2026_11.08.57_REC.png" alt="Hotelfaciliteter section showing facilities configured for the booked hotel."><figcaption><p>Hotelfaciliteter lists facilities configured for the booked hotel.</p></figcaption></figure></div>

### Related pages

* [.](./ "mention") configures the brand's **Ticket** settings and ticket version.
* [print-tickets.md](../../tickets/print-tickets.md "mention") explains how to generate, print, and email ticket PDFs.
* [customer-information-displayed-on-the-ticket.md](../../customer-information-errata/customer-information-displayed-on-the-ticket.md "mention") explains where customer information appears in ticket versions 1–3.
* [e-tickets-overview.md](../../e-tickets-overview.md "mention") explains how to verify e-ticket email delivery.
