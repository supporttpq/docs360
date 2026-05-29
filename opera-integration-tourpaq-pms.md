# Opera Integration (Tourpaq → PMS)

## Overview

Opera is a portal (Leisure & Hospitality Service) in which a hotel must be managed (rooms, allotment, etc.), as well as a booking system.\
Each room in the Opera has a certain state: ready for accommodation, if the room is clean, if it needs room service, etc.

The Opera integration connects Tourpaq with **Oracle Opera PMS**, enabling synchronization of hotels, allotments, extras, bookings, and customer data.

This integration ensures that availability, pricing elements, and reservations created in Tourpaq are correctly reflected in Opera, while maintaining a clear mapping between the two systems.

This page describes how the integration is configured and how data flows from Tourpaq to Opera.

{% hint style="info" %}
This documentation describes the integration strictly from the Tourpaq perspective.
{% endhint %}

## Prerequisites (Tourpaq Side)

Before using the integration, ensure:

* Hotels are correctly flagged as **Managed by Opera**
* Room types are mapped
* Extras categories are configured and mapped
* Transport blocks are linked to Opera blocks
* Required fields in the booking are available
* Customer data is properly structured.

## Scope of Integration

The integration covers:

* Hotel mapping and management
* Allotment and availability synchronization
* Extras and product mapping
* Booking data transfer
* Customer/profile mapping
* Logging and monitoring

## Hotel

### Hotel – Managed by Opera

#### Overview

Hotels that are managed in Opera must be clearly identified in Tourpaq to enable correct synchronization.

#### Configuration

* A hotel is marked as **“Managed by OracleOpera”** in Tourpaq

<figure><img src=".gitbook/assets/image (771).png" alt=""><figcaption></figcaption></figure>

* This flag indicates that:
  * Availability is controlled externally (Opera)
  * Tourpaq acts as a distribution and booking layer

#### System Behavior

* Manual allotment handling in Tourpaq is overridden
* Availability updates depend on Opera data (directly or via mapping) – (mapping is static)

{% hint style="info" %}
If a hotel is not marked as Managed by Opera, the integration will not correctly handle availability or bookings.
{% endhint %}

### Opera Allotment Mapping

#### Overview

Opera allotments must be mapped to Tourpaq hotel and room structures.

Allotments, in Tourpaq, per hotel, are synchronized through a service called Bad Bank Service. Depending on the hotel's settings, this service pulls all the allotments related to the hotel connected to the opera

#### Allotments (Inventory)

In Opera, there are 3 types of inventory:

*   Block -> defines the rooms that can be bought with/without transport;

    <figure><img src=".gitbook/assets/image (775).png" alt=""><figcaption></figcaption></figure>
* Room
*   House -> represents the total number of rooms we have in a hotel

    <figure><img src=".gitbook/assets/image (774).png" alt=""><figcaption></figcaption></figure>

For each individual room, there are other rooms assigned. The Bad Bank service looks at Opera every day and notices if it has a shortage or availability.\
The first time he searches the House, then on the individual room. If the latter is 0 or negative, the NO value from Hotel Allotment in Tourpaq will be updated.

<figure><img src=".gitbook/assets/image (776).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (778).png" alt=""><figcaption></figcaption></figure>

#### Behavior

* Each Opera allotment corresponds to a specific:
  * Hotel
  * Room type
  * Date range
* Tourpaq uses this mapping to:
  * Validate availability
  * Allocate rooms during booking

### Opera Block / House Availability Mapping

#### Overview

Opera distinguishes between:

* **Block availability**
* **House availability**

These must be mapped into Tourpaq’s allotment structure.

#### Mapping

| Opera Concept      | Tourpaq Mapping                         |
| ------------------ | --------------------------------------- |
| House availability | General hotel/room allotment            |
| Block availability | Transport blocks / dedicated allotments |

{% hint style="info" %}
The mapping is done by convention (if there is a room with the code CF1 in Tourpaq, then there must also be a block with the code CF1 in Opera)
{% endhint %}

#### Behavior

* House availability is treated as general inventory
* Blocks are treated as reserved capacity linked to specific transports or contracts

{% hint style="info" %}
Blocks are typically linked to transports or contracts and should be configured carefully to avoid overbooking.
{% endhint %}

<figure><img src=".gitbook/assets/image (763).png" alt=""><figcaption></figcaption></figure>

Ex: Block code: BLL2505261 where:

* BLL = departure gateway
* 25 = day
* 05 = month
* 26 = year
* 1 = interval 1 (7 days)
* 2 - interval 2 (14 days)

## Extras

### Opera Extras Category Types

#### Overview

Opera supports different types of extras that must be aligned with Tourpaq categories.

#### Supported Types

**1. Opera Package**

* Bundled services (e.g. meals, spa packages)
* Typically mapped to Tourpaq Extras

<figure><img src=".gitbook/assets/image (767).png" alt=""><figcaption><p>Extras in Tourpaq</p></figcaption></figure>

<figure><img src=".gitbook/assets/image (768).png" alt=""><figcaption><p>Package in Opera</p></figcaption></figure>

**2. Opera Item Inventory**

* Individual sellable items
* Example: equipment, add-ons

<figure><img src=".gitbook/assets/image (765).png" alt=""><figcaption></figcaption></figure>

**3. Opera Baggage**

* Special category for luggage-related services

#### Mapping in Tourpaq

* Each type is mapped to a corresponding **Extras Category**
* Category defines:
  * Pricing behavior
  * Availability rules
  * Mapping target in Opera

{% hint style="warning" %}
Incorrect mapping may result in missing or invalid extras in Opera bookings.
{% endhint %}

## Booking

### Opera-Specific Fields in Booking

#### Bed Bank Tab

**Overview**

The **Bed Bank tab** contains Opera-specific booking data required for synchronization.

<figure><img src=".gitbook/assets/image (769).png" alt=""><figcaption></figcaption></figure>

**Typical Fields**

* Opera Hotel Code
* External Booking Reference
* Block ID (if applicable)
* Integration status

#### Behavior

* Populated automatically during booking creation
* Used when sending booking data to Opera

### Booking Flow

**Steps**

1. Booking created in Tourpaq
2. Data mapped (hotel, room, extras, customer)
3. Booking sent to Opera
4. Response received and logged

{% hint style="info" %}
If any required mapping is missing, the booking may fail during export.
{% endhint %}

<figure><img src=".gitbook/assets/image (773).png" alt=""><figcaption></figcaption></figure>

In order for a booking to be sent to Opera, the credentials and an endpoint, which are used to communicate with Opera, are manually added to the Config system.

**Disable Opera Connect**

<figure><img src=".gitbook/assets/image (780).png" alt=""><figcaption></figcaption></figure>

Disable Opera Connect checkbox from the booking page, is used when changes are made on Booking, to be communicated to Opera. The checkbox appears only if there are communication settings with Opera.

### Overview

The **Disable Opera Connect** option allows users to work with a booking without synchronizing changes to Opera. When enabled, the system clearly indicates that Opera integration is disabled and provides reminders to prevent missed manual updates.

### User Interface

#### Opera Disabled Indicator

When **Disable Opera Connect** is selected, an information banner is displayed directly below the action bar.

<figure><img src=".gitbook/assets/disable opera connect.png" alt=""><figcaption></figcaption></figure>

The banner contains the message:

> Opera is disabled

This indicator remains visible while Opera synchronization is disabled for the booking.

***

### Saving a Booking

When a user attempts to save a booking while **Disable Opera Connect** is enabled, the system displays a confirmation dialog.

<figure><img src=".gitbook/assets/save bookink opera.png" alt=""><figcaption></figcaption></figure>

**Message**

> Opera Connection is disabled. Are you sure you want to save without syncing to Opera?

**Available actions**

| Action  | Outcome                                                                       |
| ------- | ----------------------------------------------------------------------------- |
| **Yes** | The booking and passenger changes are saved without synchronization to Opera. |
| **No**  | The save operation is cancelled and the user remains on the booking.          |

***

### Cancelling Bookings or Passengers

When a booking or passenger is cancelled while **Disable Opera Connect** is enabled, the system displays a reminder notification.

<figure><img src=".gitbook/assets/cancel pax opera.png" alt=""><figcaption></figcaption></figure>

**Message**

> Please remember to cancel the passenger/reservation in Opera as well.

{% hint style="info" %}
The notification serves as a reminder that the cancellation is not automatically synchronized to Opera and any required updates must be performed manually.
{% endhint %}

### Blocks – Mapping from Transport

#### Overview

Transport blocks in Tourpaq are mapped to Opera blocks.

#### Mapping Logic

* Tourpaq Transport → Opera Block Code

#### Behavior

* When a booking is linked to a transport, the corresponding Opera block is assigned
* Ensures booking is placed within the correct reserved inventory in Opera

{% hint style="warning" %}
Incorrect block mapping can result in bookings being assigned outside the reserved inventory.
{% endhint %}

## Customers / Passengers

### Mapping to Opera Profiles

#### Overview

Passengers in Tourpaq must be mapped to Opera Profiles. Defines how passengers are mapped to Opera profiles.

#### Rules

* Each passenger is matched or created as:
  * Individual profile in Opera
* Matching is typically based on:
  * Name
  * Email
  * Phone
  * Unique identifier

<figure><img src=".gitbook/assets/image (779).png" alt=""><figcaption></figcaption></figure>

#### Behavior

* If a match is found → reuse existing profile
* If not → create a new profile in Opera

{% hint style="info" %}
Consistent customer data improves matching accuracy and reduces duplicate profiles.
{% endhint %}

## Extras (Booking Level)

### Mapping to Opera Products / Packages

#### Overview

Extras selected in Tourpaq bookings must be translated into Opera-compatible products.

#### Mapping Logic

* Tourpaq Extra → Opera Product / Package Code

#### Behavior

* During booking export:
  * Extras are converted into Opera format
  * Attached to the reservation as: packages or individual items

## Logging

### What Is Logged

The integration logs:

* Booking export requests
* Responses from Opera
* Errors and validation issues
* Mapping failures
* Profile creation/matching results

### Where Logs Are Available

#### Backend (Database)

* Primary logs are stored in the database
* Includes:
  * Request payloads
  * Response payloads
  * Error messages

#### UI (if available)

* If exposed:
  * Integration status on the booking level
  * Error indicators or messages

#### Behavior

* Logs are critical for:
  * Troubleshooting failed bookings
  * Verifying successful synchronization
  * Debugging mapping issues

## Best Practices

* Always validate mappings before go-live
* Use consistent naming between systems
*   All customer details must be entered before Take Allotment, to avoid creating duplicates for customers.

    <figure><img src=".gitbook/assets/image (770).png" alt=""><figcaption></figcaption></figure>
* Test:
  * Booking with extras
  * Booking with blocks
  * Multiple passengers
* Monitor logs after initial bookings

## Reusable Structure for Future PMS Integrations

This structure can be reused for other PMS integrations:

✔ Clear and standardized PMS integration framework\
✔ All key components covered and detailed\
✔ Reusable structure for future integrations\
✔ Supports scalability and consistency\
✔ Guided by prerequisites & best practices
