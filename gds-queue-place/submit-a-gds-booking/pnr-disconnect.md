---
description: >-
  Disconnect a Tourpaq booking from its Amadeus PNR to regain editability.
  Covers when to use it, workflow steps, reassignment criteria, and cancellation
  handling.
---

# PNR Disconnect

#### Overview

PNR Disconnect allows a booking in Tourpaq to be detached from its associated GDS PNR. This restores full editability of the booking in Tourpaq while keeping the PNR intact in the GDS. The feature is designed to support workflows where certain changes cannot be synchronized automatically between Amadeus and Tourpaq.

To support these cases, Tourpaq provides the ability to **disconnect a PNR** from a booking. This allows the booking to be edited independently in both systems and later reconnected.

#### Purpose

Tourpaq supports only a limited set of updates coming from Amadeus. While name updates are supported, other common changes cannot currently be reflected automatically in Tourpaq.

Examples of unsupported changes include:

* Changing titles (for example MR to MS)
* Changing the number of passengers

In these cases, the recommended workflow is to disconnect the PNR, perform the required adjustments independently in both systems, and then reassign the PNR to the booking.

Another important use case is cancellation handling. In some scenarios, it is economically beneficial to postpone the cancellation in Amadeus. By disconnecting the PNR, the Tourpaq booking can be cancelled without cancelling the PNR in the GDS.

#### When to use PNR Disconnect

Use this feature when:

* Passenger titles must be changed
* Passenger count must be changed
* Structural booking changes are required that Tourpaq cannot sync from Amadeus
* A Tourpaq booking must be cancelled while keeping the Amadeus PNR active

#### Location in the system

* Booking
* GDS tab

<figure><img src="../../.gitbook/assets/image (588).png" alt="GDS tab in a booking showing the PNR Disconnect action"><figcaption><p>Find <strong>Disconnect PNR</strong> in the booking’s GDS tab.</p></figcaption></figure>

#### Functionality

A new action is available on the booking:

**Disconnect PNR**\
When selected, the PNR link between Tourpaq and the GDS booking is removed.

#### Behavior after disconnect

Once the PNR is disconnected:

* The booking is no longer locked by the GDS
* Passenger details can be edited in Tourpaq
* Passenger count can be adjusted
* Titles can be changed
* The booking can be cancelled in Tourpaq without affecting the Amadeus PNR

The booking returns to a standard editable state, similar to a non-GDS booking.

#### Recommended workflow

1. Open the booking in Tourpaq
2. Go to the GDS tab
3.  Click **Disconnect PNR**

    <figure><img src="../../.gitbook/assets/image (589).png" alt="Disconnect PNR button in the GDS tab"><figcaption><p>Click <strong>Disconnect PNR</strong>.</p></figcaption></figure>
4.  Confirm the action

    <figure><img src="../../.gitbook/assets/image (590).png" alt="Confirmation dialog for disconnecting the PNR"><figcaption><p>Confirm the disconnect action.</p></figcaption></figure>
5. Apply the required changes:
   * Update passengers or titles in Tourpaq
   *   Apply corresponding changes in Amadeus if needed

       <figure><img src="../../.gitbook/assets/image (591).png" alt="Amadeus change example after PNR disconnect"><figcaption><p>Apply the same structural changes in Amadeus if required.</p></figcaption></figure>
6. Save the booking after making the changes.
7.  Reassign the PNR to the booking and continue the synchronization.

    <figure><img src="../../.gitbook/assets/image (592).png" alt="Reassign PNR action in the GDS tab"><figcaption><p>Reassign the PNR after both systems match again.</p></figcaption></figure>

For a PNR to be assigned to a booking, it must meet these criteria:

* the PNR is not assigned to another booking
* the PNR code has at least 6 characters
* the PNR has the same number of passengers as the booking (cancelled passengers are not counted)
* the PNR has the same number of passengers per title (MR, MS, CHD, INF). This check is skipped when the first and last name of every passenger in the booking is found in the PNR
* the outbound and homebound journeys start and end at the same airports as in the booking. Connection airports may differ (see Airports below)
* the outbound and homebound departure dates are the same as in the booking

The booking must have both an outbound and a homebound flight.

If one of these criteria is not met, the system will display an error message. The message also lists the route and the travellers found in the PNR.

Example: In the original booking, there are 2 MR passengers:

<figure><img src="../../.gitbook/assets/image (593).png" alt="Original booking passenger list with two MR passengers"><figcaption><p>Example: original booking has two MR passengers.</p></figcaption></figure>

And we changed one of them to an MS passenger:

<figure><img src="../../.gitbook/assets/image (594).png" alt="Updated passenger list after changing one passenger title to MS"><figcaption><p>After changing a title, passenger distribution per gender changes.</p></figcaption></figure>

When we try to assign the PNR, we will receive a warning message and the PNR will not be assigned:

<figure><img src="../../.gitbook/assets/image (595).png" alt="Warning message when PNR reassignment criteria are not met"><figcaption><p>PNR reassignment is blocked if criteria don’t match.</p></figcaption></figure>

#### Airports

Each journey in the PNR, outbound and homebound, must start and end at the same airports as in the booking. The connection airports in between may differ.

Example for a round trip BLL – LPA:

| Journey   | Booking in Tourpaq | PNR in Amadeus  | Result                                            |
| --------- | ------------------ | --------------- | ------------------------------------------------- |
| Outbound  | BLL → AMS → LPA    | BLL → PAR → LPA | Accepted: same first and last airport             |
| Homebound | LPA → AMS → BLL    | LPA → PAR → BLL | Accepted: same first and last airport             |
| Homebound | LPA → AMS → BLL    | LPA → PAR → BCN | Not accepted: the journey ends at another airport |

After **Assign PNR**, the booking shows the flights booked in Amadeus, including their connection airports. See [Show flight info from Amadeus when Assign/Load PNR is used](show-flight-info-from-amadeus-when-assign-load-pnr-is-used.md).

#### How passengers are matched to the PNR

When a PNR is assigned or loaded, each traveller in the PNR is linked to one passenger in the booking:

1. Tourpaq looks for a passenger with the same first and last name. Upper and lower case are ignored, and special characters in the Tourpaq name are compared in their GDS spelling (for example Ø as OE).
2. If no passenger has that name, the traveller is linked to a passenger with the same title who has not been linked yet.

Each passenger is linked to one traveller only.

{% hint style="warning" %}
Matching by title cannot tell two passengers with the same title apart. Make sure the names are spelled the same way in Tourpaq and in Amadeus before you assign the PNR.
{% endhint %}

#### Titles

Passengers in Tourpaq have one of these titles: **MR**, **MS**, **CHD** (child) or **INF** (infant).

In Amadeus, the title is written after the first name, for example `JOHN MR`. Tourpaq reads it as follows:

| In the PNR         | Title in Tourpaq |
| ------------------ | ---------------- |
| MR                 | MR               |
| MRS or MS          | MS               |
| Passenger type CHD | CHD              |
| Passenger type INF | INF              |

When Tourpaq creates the PNR itself, it sends the Tourpaq title after the first name.

#### Passenger names after Assign PNR and Load PNR

After **Assign PNR** or **Load PNR**, the first and last name of each linked passenger is updated to the name in the PNR, without the title. The passenger names in Tourpaq then follow the spelling used in Amadeus.

#### Important notes

* Disconnecting a PNR does not cancel or modify the booking in Amadeus
* After disconnect, Tourpaq will no longer receive updates from the GDS until the PNR is reassigned
* Always ensure that Tourpaq and Amadeus are aligned before reassigning a PNR

### Cancel booking in Amadeus

To cancel a booking in Amadeus, follow these steps:

* Open the booking in **Tourpaq**
* Go to the **GDS tab**
*   Assign the **PNR Code**

    <figure><img src="../../.gitbook/assets/image (597).png" alt="Assign PNR code field in GDS tab"><figcaption><p>Assign the PNR code in the GDS tab.</p></figcaption></figure>
*   Click on **Cancel Booking**

    <figure><img src="../../.gitbook/assets/image (596).png" alt="Cancel Booking button in the GDS tab"><figcaption><p>Cancel Booking sends the cancellation to Amadeus.</p></figcaption></figure>
* Confirm the action

### PNR Visibility in All Bookings

#### Overview

The **PNR (Passenger Name Record)** assigned to a booking remains visible in the **All Bookings** view at all times.

***

#### Behavior

* The **PNRS** column continues to display the assigned PNR as usual.
* The PNR remains visible even if:
  * The **booking is cancelled**
  * The **PNR is disconnected** from the booking

This ensures consistent access to PNR information regardless of booking status.

***

#### Purpose

Keeping the PNR visible allows users to quickly access and reference PNR details, even for cancelled or disconnected bookings, without needing additional lookup steps.

***

#### Example

A cancelled booking will still display its associated PNR in the **All Bookings** list, just like an active booking. This provides continuity and simplifies follow-up actions or investigations.

***

#### Screenshot

<figure><img src="../../.gitbook/assets/image (786).png" alt=""><figcaption></figcaption></figure>
