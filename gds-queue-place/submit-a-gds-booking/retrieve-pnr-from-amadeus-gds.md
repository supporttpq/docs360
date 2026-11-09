# Retrieve PNR from Amadeus GDS

Some Amadeus reservations exist before the Tourpaq booking does. Flights may be booked directly in Amadeus, or a booking may have been made in another GDS tool first. Retrieving the PNR lets Tourpaq use the reservation that already exists in Amadeus instead of creating a new one.

#### Overview

**Assign PNR** retrieves an existing Amadeus reservation, identified by its PNR (Passenger Name Record) code, and links it to the Tourpaq booking you have open. Tourpaq reads the flight information from Amadeus and maps the travellers in the PNR to the passengers on the booking.

This is the reverse of [Submit a GDS Booking](https://claude.ai/gds-queue-place/submit-a-gds-booking.md), where Tourpaq creates the Amadeus reservation. The feature is available for Amadeus only.

Two actions on the **GDS** tab work with a PNR:

* **Assign PNR** — links a PNR to the booking for the first time, or links a new PNR. Tourpaq checks the PNR before it accepts it.
* **Load PNR** — refreshes a booking that is already linked to a PNR. See [Show flight info from Amadeus when Assign/Load PNR is used](https://claude.ai/gds-queue-place/submit-a-gds-booking/show-flight-info-from-amadeus-when-assign-load-pnr-is-used.md).

#### Purpose

Use Assign PNR to:

* Re-book in Tourpaq a reservation that was first made in another GDS tool, such as Atcom.
* Use the flights of a reservation that was started in Amadeus, including dynamic flights.
* Show the itinerary stored in Amadeus on the booking and on tickets.

You do not need Assign PNR when you submit a booking from Tourpaq. In that case Tourpaq creates the PNR and links it automatically.

#### Preconditions

* The brand is set up for Amadeus — see [How to set GDS](https://claude.ai/brands/how-to-set-gds.md) and [Amadeus](https://claude.ai/integration/transport-providers/amadeus.md).
* The booking exists in Tourpaq and has a transport whose departure airport and departure date match the PNR, for both the outbound and the homebound direction. Tourpaq does not create the transport from the PNR.
* You have the PNR code from Amadeus. It must be alphanumeric, at least six characters long, with no spaces.
* The PNR is not linked to another Tourpaq booking. A PNR linked to a cancelled booking is also rejected.
* The number of non-cancelled passengers on the booking equals the number of travellers in the PNR.
* You have permission to assign a PNR.

#### How-to

{% stepper %}
{% step %}
### **Open the GDS tab**

Open the booking and select the **GDS** tab.

The tab shows the PNR code field and the **Assign PNR** button next to the existing buttons. **Assign PNR** stays disabled until you enter a valid PNR.
{% endstep %}

{% step %}
### **Enter the PNR code**

Type the PNR code from Amadeus into the PNR code field. Enter at least six alphanumeric characters and no spaces.

**Assign PNR** becomes enabled when the code is valid.
{% endstep %}

{% step %}
### **Assign the PNR**

Click **Assign PNR**.

{% hint style="warning" %}
Assign PNR changes the booking. It links the PNR, copies the Amadeus flight information into the booking, and can update passenger names, ticket information and transport costs. Once a PNR is linked, changes that Tourpaq cannot synchronise from Amadeus, such as a passenger count or title change, need PNR Disconnect.
{% endhint %}

Tourpaq retrieves the reservation from Amadeus and runs the checks described below. If a check fails, Tourpaq stops and shows an error message. If all checks pass, Tourpaq links the PNR to the booking.
{% endstep %}

{% step %}
### Confirm the result

Check that the booking now shows the Amadeus flight information, and open the **History** tab to confirm the entry `Assign PNR for booking`
{% endstep %}
{% endstepper %}

The booking is now linked to the PNR. The flights shown on the booking and on tickets come from Amadeus, and the PNR appears in the **PNRS** column of **All bookings**.

**Assign PNR and Load PNR**

The two actions do not run the same checks.

| Action         | Description                                                                                               |
| -------------- | --------------------------------------------------------------------------------------------------------- |
| **Assign PNR** | Runs the full checks for a new PNR (below), then maps passengers and copies flight information.           |
| **Load PNR**   | Refreshes a booking that is already linked. It skips the checks for a new PNR, but still maps passengers. |

**Checks that must pass**

These checks run when you assign a new PNR. Tourpaq runs all of them and collects the failures, so one attempt can report more than one problem.

* **PNR found** — the PNR exists in Amadeus.
* **PNR code length** — the code has at least six characters.
* **Passenger count** — the number of non-cancelled Tourpaq passengers equals the number of Amadeus travellers.
* **Passenger match** — the passengers can be matched by name or, failing that, by passenger type. See the next section.
* **Outbound and homebound** — the departure airport and departure date of each direction match the transport on the booking.
* **Unique PNR** — the PNR is not linked to another booking, including a cancelled one.

Tourpaq checks the departure airport and date for each direction only. It does not compare the full route at this point. Routing differences are handled separately.

**How passengers are matched**

Names do not have to be identical for the PNR to be accepted. Tourpaq matches passengers in this order:

1. **Names.** Tourpaq compares first and last names of each Tourpaq passenger with the Amadeus travellers. Special characters in Tourpaq names are converted with Tourpaq's transliteration table before the comparison.
2. **Passenger type.** If not every name matches, Tourpaq compares the number of passengers of each type. When the counts agree, the PNR passes even though some names differ.

Each Tourpaq passenger is matched to one traveller only.

**What Tourpaq updates automatically**

After a successful assignment, Tourpaq does the following without further action:

* Links the PNR to the booking.
* Copies the flight information from Amadeus into the booking.
* Maps travellers to passengers and may update matched passenger names.
* Records `Assign PNR for booking` in the booking history.
* Can record ticket-number changes in the booking history.
* Can assign transport GDS costs to the matched passengers.

**If the PNR is rejected**

Tourpaq stops and shows an error message. The booking is not linked to the PNR. Correct the cause and click **Assign PNR** again.

| Condition                                 | What you see and what to check                                                                                                                                |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Code is not valid**                     | **Assign PNR** stays disabled. Enter at least six alphanumeric characters with no spaces.                                                                     |
| **PNR not found**                         | Tourpaq aborts with an error message. Compare the code with Amadeus.                                                                                          |
| **PNR does not match the transport**      | Tourpaq aborts with an error message. Check that the transport on the booking has the same departure airport and date as the PNR, outbound and homebound.     |
| **Different number of passengers**        | Tourpaq rejects the PNR. Compare the non-cancelled passengers on the booking with the travellers in the PNR. Passengers cancelled in Tourpaq are not counted. |
| **Names and passenger types both differ** | Tourpaq rejects the PNR. Check the number of adults, children and infants on both sides.                                                                      |
| **PNR already linked to another booking** | Tourpaq rejects the PNR, even if the other booking is cancelled. Find the booking that holds the PNR in the **PNRS** column of **All bookings**.              |
| **Button not available**                  | The feature is enabled for Amadeus only. Check the GDS provider of the transport.                                                                             |

#### Field Reference

| Field          | Description                                                                   | Required                                          | Notes                                                                                                                                                                                   |
| -------------- | ----------------------------------------------------------------------------- | ------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **PNR code**   | The Amadeus reservation code to retrieve.                                     | Yes — to enable **Assign PNR**                    | Alphanumeric, at least six characters, no spaces. Located next to the existing buttons on the **GDS** tab.                                                                              |
| **Assign PNR** | Retrieves the PNR from Amadeus and links it to the booking.                   | Conditional — enabled once a valid PNR is entered | Available for Amadeus only. Runs the full checks for a new PNR.                                                                                                                         |
| **Load PNR**   | Refreshes flight information and passenger mapping for an already linked PNR. | No                                                | See [Show flight info from Amadeus when Assign/Load PNR is used](https://claude.ai/gds-queue-place/submit-a-gds-booking/show-flight-info-from-amadeus-when-assign-load-pnr-is-used.md). |

#### Related pages

* [Submit a GDS Booking](https://claude.ai/gds-queue-place/submit-a-gds-booking.md)
* [Show flight info from Amadeus when Assign/Load PNR is used](https://claude.ai/gds-queue-place/submit-a-gds-booking/show-flight-info-from-amadeus-when-assign-load-pnr-is-used.md)
* [PNR Disconnect](https://claude.ai/gds-queue-place/submit-a-gds-booking/pnr-disconnect.md)
* [GDS Bookings](https://claude.ai/gds-queue-place/gds-bookings.md)
* [Amadeus](https://claude.ai/integration/transport-providers/amadeus.md)
