# Passenger information

## Passenger information

### Overview

The **Passenger Information** tab configures informational messages displayed to passengers during the booking process for a specific product, such as BAG20A.

These messages can be:

* Time-based (valid only for specific stay or booking periods)
* Mandatory (require passenger acknowledgment)
* Informational only (displayed without required confirmation)

This functionality ensures that important travel, baggage, or operational details are clearly communicated to customers before completing a booking.

### Purpose

The purpose of this page is to:

* Inform passengers about special conditions (e.g., baggage rules, travel requirements).
* Ensure legal or operational compliance by requiring acknowledgment.
* Control when specific information appears (based on stay dates or booking dates).
* Maintain brand-specific messaging if needed.

### Interface fields

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1).png" alt="Passenger Information tab"><figcaption></figcaption></figure></div>

| Field / Button      | Description                                                         |
| ------------------- | ------------------------------------------------------------------- |
| **Default text**    | Displays the default brand text configuration.                      |
| **Tourpaq DK**      | Indicates the brand/language context where the information applies. |
| **Create** (button) | Used to create a new Passenger Information rule.                    |

### How it works

A Passenger Information rule becomes active only when:

* The **Stay Date** falls within _Stay From – Stay To_\
  AND/OR
* The **Booking Date** falls within _Booking Date From – Booking Date To_

If both stay and booking dates are defined, both conditions must be met.

If booking dates are empty, the rule is triggered based only on stay dates.

### Instructions

#### Create a new Passenger Information rule

1. Navigate to **Passenger Information** tab.
2. Click **Create**.
3. Fill in:
   * Stay From / Stay To
   * Booking Date From / Booking Date To (optional)
   * Information text
   * Enable **Acknowledge** if confirmation is required
4. Save the rule.

#### Edit an existing rule

1. Click the **pencil icon**.
2. Modify the necessary fields.
3. Save changes.

#### Delete a rule

1. Click the **trash icon**.
2. Confirm deletion.

⚠ Deleting a rule removes it permanently. It no longer appears in the booking flow.

### Example scenarios

#### Informational only

| Field       | Value                     |
| ----------- | ------------------------- |
| Stay From   | 01-04-2026                |
| Stay To     | 31-05-2026                |
| Information | Free baggage for children |
| Acknowledge | ✔                         |

**Result:**\
Passengers traveling between April 1 and May 31, 2026 see a message about free baggage for children. They must acknowledge it before completing the booking.

#### Booking period based rule

| Field             | Value                      |
| ----------------- | -------------------------- |
| Stay From         | 31-12-2025                 |
| Stay To           | 31-12-2026                 |
| Booking Date From | 01-01-2025                 |
| Booking Date To   | 31-12-2025                 |
| Information       | Extra customer information |
| Acknowledge       | ✔                          |

**Result:**\
Only bookings made during 2025 for travel in 2025–2026 show this message and require confirmation.

{% hint style="info" %}
**Passenger information allows overlapping periods**

Ex: If fixed info is made for the entire season (31.12.25 - 31.12.26) - Extra customer info, and another info is made for a short period (01.04.26 - 31.05.26) - Free baggage for children. Even if the periods overlap, the system will allow and display both on the ticket.
{% endhint %}

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1).png" alt="Passenger Information rule in the booking flow"><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Passenger Information acknowledgment"><figcaption></figcaption></figure></div>

### Passenger information on the ticket

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1).png" alt="Passenger information displayed on a ticket"><figcaption></figcaption></figure></div>
