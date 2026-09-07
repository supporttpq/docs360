---
description: >-
  Create hotel-only bookings in Tourpaq Office using a car-type transport as a
  placeholder. Covers setup, allotment (Fix quota), pricing.
---

# Hotel Only Bookings

### Overview

**Hotel Only Bookings** let you book **accommodation without flights/buses**.

Tourpaq handles this by using a **ALC transport** as a placeholder.

### Precondition

*   It needs to have a hotel defined in the system. The hotel should have the Custom hotel day Booking checkbox marked.&#x20;

    <figure><img src="../../.gitbook/assets/07.09.2026_11.43.56_REC.png" alt=""><figcaption></figcaption></figure>


*   An ALC transport defined in the system. Need to have For A La Carte checkbox&#x20;

    <figure><img src="../../.gitbook/assets/07.09.2026_11.50.04_REC.png" alt=""><figcaption></figcaption></figure>

### Setup (recommended)

{% stepper %}
{% step %}
**1. Create an ALC transport**

Create a transport with the For a la carte checkbox marked

Configure it like a normal transport (interval + timetable in the period).

See [Transport creation](../../transport/transport/transport-creation/) if you need the full transport setup flow.
{% endstep %}

{% step %}
**Create/Use a Hotel with the checkbox  Custom Hotel Day booking marked**

Configure it like a normal hotel ( define room type, allotment, allotment per day, room cost, etc)

The room types used need to be marked to be Used for custom hotel days&#x20;

<figure><img src="../../.gitbook/assets/07.09.2026_12.00.08_REC.png" alt=""><figcaption></figcaption></figure>


{% endstep %}

{% step %}
**3. Create a pricelist between the ALC transport and the hotel**

Create a pricelist hotel day for the **hotel** you want to sell as hotel-only

See  [Pricelist Hotel Day](../../price-list-custom-hotel-days-service.md) if you need the pricelist workflow.

Give the transport a short, recognisable code (ALC, OWN) — it appears as the Transports filter in the price list.
{% endstep %}
{% endstepper %}

### Book a hotel-only stay

Start a booking as usual in [New Booking](new-booking/).

Then:

1. In the Transport panel, you don't choose nothing
2.  In the Hotel panel, click **Hotel Only**.&#x20;

    <figure><img src="../../.gitbook/assets/07.09.2026_13.05.10_REC.png" alt=""><figcaption></figcaption></figure>
3.  In the **Select Independent Hotel** popup, search by resort, hotel, and dates, then select the room. The total price for the stay is shown in the **P** column.&#x20;

    <figure><img src="../../.gitbook/assets/07.09.2026_13.04.24_REC.png" alt=""><figcaption></figcaption></figure>
4. Complete passenger details, extras, and payments as normal.

The booking now shows the hotel-only stay with its total price.

#### Pricing

The total price shown in the **Select Independent Hotel** popup (the **P** column) is the sum of the prices **P1** from the price list for every stay day. (P=P1 DAY1 + P1 DAY 2+ P1 DAY3 +P1 DAY 4 + P1DAY5).&#x20;

<figure><img src="../../.gitbook/assets/07.09.2026_13.18.40_REC.png" alt=""><figcaption></figcaption></figure>

&#x20;This total does not include supplements or discounts from the pricelist. Supplements and discounts are not applied on a per-night basis, so they cannot currently be summed into a single per-stay total for Hotel Only.
