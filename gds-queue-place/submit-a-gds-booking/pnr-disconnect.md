# PNR Disconnect

#### Overview

PNR Disconnect allows a booking in Tourpaq to be detached from its associated GDS PNR. This restores full editability of the booking in Tourpaq while keeping the PNR intact in the GDS. The feature is designed to support workflows where certain changes cannot be synchronized automatically between Amadeus and Tourpaq.

To support these cases, Tourpaq provides the ability to **disconnect a PNR** from a booking. This allows the booking to be edited independently in both systems and later reconnected.

#### Purpose

Tourpaq supports only a limited set of updates coming from Amadeus. While name updates are supported, other common changes cannot currently be reflected automatically in Tourpaq.

Examples of unsupported changes include:

* Changing titles (for example MR to MRS)
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

<figure><img src="../../.gitbook/assets/image (588).png" alt=""><figcaption></figcaption></figure>

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

    <figure><img src="../../.gitbook/assets/image (589).png" alt=""><figcaption></figcaption></figure>
4.  Confirm the action

    <figure><img src="../../.gitbook/assets/image (590).png" alt=""><figcaption></figcaption></figure>
5. Apply the required changes:
   * Update passengers or titles in Tourpaq
   *   Apply corresponding changes in Amadeus if needed

       <figure><img src="../../.gitbook/assets/image (591).png" alt=""><figcaption></figcaption></figure>
6. Save the booking after making the changes.
7.  Reassign the PNR to the booking and continue the synchronization.

    <figure><img src="../../.gitbook/assets/image (592).png" alt=""><figcaption></figcaption></figure>

For a PNR to be assigned to Amadeus, it must meet these criteria:

* have the same number of passengers
* have the same number of passengers per gender
* have the same departure and arrival
* have the same departure date and arrival date

If one of these criteria is not met, the system will display an error message.

Example: In the original booking, there are 2 MR passengers:

<figure><img src="../../.gitbook/assets/image (593).png" alt=""><figcaption></figcaption></figure>

And we changed one of them to an MS passenger:

<figure><img src="../../.gitbook/assets/image (594).png" alt=""><figcaption></figcaption></figure>

When we try to assign the PNR, we will receive a warning message and the PNR will not be assigned:

<figure><img src="../../.gitbook/assets/image (595).png" alt=""><figcaption></figcaption></figure>

#### Important notes

* Disconnecting a PNR does not cancel or modify the booking in Amadeus
* After disconnect, Tourpaq will no longer receive updates from the GDS until the PNR is reassigned
* Always ensure that Tourpaq and Amadeus are aligned before reassigning a PNR

### Cancel booking in Amadeus

To cancel a booking in Amadeus, follow these steps:

* Open the booking in **Tourpaq**
* Go to the **GDS tab**
*   Assign the **PNR Code**

    <figure><img src="../../.gitbook/assets/image (597).png" alt=""><figcaption></figcaption></figure>
*   Click on **Cancel Booking**

    <figure><img src="../../.gitbook/assets/image (596).png" alt=""><figcaption></figcaption></figure>
* Confirm the action

### FAQ

#### Does disconnecting a PNR cancel anything in Amadeus?

No. Disconnecting only removes the link in Tourpaq. The Amadeus PNR stays unchanged.

#### Can I reconnect the same PNR later?

Yes. Reassign the PNR from the booking’s **GDS** tab. The PNR must match the criteria listed above.

#### What changes can I make in Tourpaq after disconnecting?

You can edit passenger details, adjust passenger count, change titles, and cancel the Tourpaq booking without affecting the Amadeus PNR.

#### Why can’t I reassign the PNR after changing titles?

Reassignment requires the same passenger count and the same passenger distribution per gender. If these do not match, Tourpaq blocks reassignment.

#### Will Tourpaq keep syncing with Amadeus after disconnect?

No. Tourpaq stops receiving GDS updates until the PNR is reassigned.
