# Out / Home - Ticket

## Out / Home - Ticket

### Overview

This page describes direction-specific transport Extras in printed tickets. It covers tickets from the back-office booking system and Web Booking customer center.

See [Out/Home - Web Booking](out-home-web-booking.md) for booking-flow behavior.

### Purpose

Tickets display selected transport Extras by direction. They show accurate pricing, totals, and explanatory notes.

### Requirements

* An existing booking with at least one passenger.
* Transport Extras selected for outbound and homebound directions.
* A booking state that allows ticket printing.
* Access to **Do Booking** or Web Booking customer center.

### Ticket content

The ticket uses the same structure from the back-office booking system and Web Booking customer center.

#### Specifikation af rejsebestilling

**Specifikation af rejsebestilling** groups Extras under their category name. It displays outbound and homebound Extras in separate columns.

Each column shows the direction-specific price. The ticket calculates the corresponding totals.

#### Forklaringer

**Forklaringer** groups Extras under the same category name. It uses separate paragraphs for outbound and homebound directions.

Each paragraph shows the total Extras booked for its direction.

### Print tickets from Do Booking

In **Do Booking**, print a ticket:

1. Open an existing booking.
2. Click **Print ticket**.
3. Open the downloaded ticket.

Confirm that **Specifikation af rejsebestilling** displays category Extras in outbound and homebound columns. Confirm that each column shows the correct price and total.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (322).png" alt="Ticket Specifikation af rejsebestilling section with outbound and homebound Extras"><figcaption></figcaption></figure></div>

Confirm that **Forklaringer** displays each Extra Category in separate outbound and homebound paragraphs. Confirm that each paragraph shows the total booked Extras.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (323).png" alt="Ticket Forklaringer section with outbound and homebound Extras"><figcaption></figcaption></figure></div>

### Print tickets from Web Booking customer center

In Web Booking customer center, print a ticket:

1. Open the booking.
2. Click **Print ticket**.
3. Open the ticket.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (324).png" alt="Web Booking customer center Print ticket control"><figcaption></figcaption></figure></div>

Confirm that **Specifikation af rejsebestilling** and **Forklaringer** match the ticket content described on this page.
