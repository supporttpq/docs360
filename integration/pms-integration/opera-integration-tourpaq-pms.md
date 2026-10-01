---
description: >-
  Configure and understand the Tourpaq–Opera integration: room codes, block
  allotment, Extras categories, booking transfer and the Disable Opera Connect
  option.
---

# Opera integration

Hotels on Oracle Opera PMS manage their rooms in Opera. The Opera integration lets Tourpaq sell those rooms and send each booking back to the hotel as a reservation.

#### Overview

The **Opera integration** connects Tourpaq Office with **Oracle Opera PMS**, the system in which the hotel manages its rooms. Tourpaq reads room inventory from Opera and sends bookings, customers, passengers, products and transport details to Opera.

Data moves in two directions:

* **Opera → Tourpaq** — inventory. A Tourpaq service reads the **House**, **Room** and **Block** inventory from Opera every hour. When Opera confirms a reservation, its confirmation number comes back to the Tourpaq booking.
* **Tourpaq → Opera** — bookings. Tourpaq sends each created or updated booking to Opera as a reservation.

```
Opera                                        Tourpaq
House inventory ──┐
Room inventory  ──┼── read every hour ────▶  Hotel allotment (NO.)
Block inventory ──┘

Tourpaq                                      Opera
Booking (created or updated) ─────────────▶  Reservation
  Booking No · Customer · Passengers · Products · Transport · Block Code

Opera                                        Tourpaq
Reservation confirmation number ──────────▶  Booking → Bed Bank tab → Reference

Matching rules
  Room Types tab: ROOM CODE   ═══ must match exactly ═══   Opera room type code
  Extra: Code                 ═══ naming convention  ═══   Opera package code
  Transport                   ═══ block code         ═══   Opera Block Code
```

For a hotel managed by Opera, availability comes from Opera and manual allotment handling in Tourpaq is overridden.

{% hint style="info" %}
This page describes the integration from the Tourpaq side. Opera screens are shown only where they help you check a mapping. Integration pages in the manual use this structure: Overview, Purpose, Preconditions, How-to (setup tasks in Tourpaq and the external system), and Field Reference (fields, rules, data exchanged, an example and logging).
{% endhint %}

#### Purpose

Use the Opera integration to:

* Sell rooms that the hotel manages in Opera, without maintaining manual allotment in Tourpaq.
* Deliver Tourpaq bookings to the hotel as reservations in Opera.
* Check that Tourpaq room codes, Extras and block codes match what exists in Opera.
* Find the Opera reservation of a Tourpaq booking.
* Work on a booking without sending its changes to Opera, when you update Opera by hand.

#### Preconditions

* The hotel exists in Tourpaq — see [Hotel creation](https://tourpaq.gitbook.io/staging-tourpaq-docs/hotel/hotel-creation) and the [General tab](https://tourpaq.gitbook.io/staging-tourpaq-docs/hotel/hotel-creation/general-tab).
* Every room type used at the hotel has a **ROOM CODE** identical to the room type code in Opera — see [Room Types](https://tourpaq.gitbook.io/staging-tourpaq-docs/hotel/hotel-creation/room-types) and [Base room types](https://tourpaq.gitbook.io/staging-tourpaq-docs/base-room-types).
* The Opera endpoint and credentials are added to the Config system. They are added manually.
* Extras that go to Opera are in an extras category with an Opera **Category Type**, and each Extra's **Code** follows the naming convention of the Opera package — see [Edit Extra Category](https://tourpaq.gitbook.io/staging-tourpaq-docs/extras-category/extra-category-overview/edit-extra-category).
* For package trips with transport, the Opera block exists with its block code, for the departure and period.

#### How-to

{% stepper %}
{% step %}
**Mark the hotel as managed by Opera**

1. Go to **Hotel → Hotels** and open the hotel.
2. On the **Basic setup** tab, open **Additional settings**.
3. In **Managed by**, select `OracleOpera`.
4. Click **Save**.

The hotel now shows `OracleOpera` in the **BED BANK** column of the **Hotels** list. Select **Display only Bed Banks** in the list to show only these hotels.
{% endstep %}

{% step %}
**Match the room codes**

1. Open the hotel and go to the **Room Types** tab.
2. Compare each **ROOM CODE** with the room type code in Opera. In Opera, room type codes appear in the **Rooms Availability Summary** on the dashboard.
3. Correct any code that differs.

Tourpaq reads the inventory of every room type of the hotel from Opera. Codes must match exactly.
{% endstep %}

{% step %}
**Set up the Extras**

1. Go to **Extras Setup → Extras Category** and open the category.
2. Under **Settings**, set **Category Type** to `Opera Package`, `Opera Item Inventory` or `Opera Baggage`.
3. Click **Save**.
4. Go to **Extras Setup → Extras**, open the Extra and check that **Extras Category** is the Opera category.
5. Set **Code** to the code of the matching Opera package.
6. In Opera, open any reservation, click **Packages** and check that a package with the same **Code** exists in the list of available packages.

Extras in this category are sent to Opera with their code. Only the code is mapped.
{% endstep %}

{% step %}
**Check that Opera has the block**

1. In Opera, go to **Bookings → Blocks → Manage Block**.
2. Search for the block by **Block Code**.
3. Check that **Block Status**, **Start Date** and **End Date** cover the departure.
4. Check that the room types you want to sell from the block have rooms on the block.

Opera inventory for the block becomes sellable in Tourpaq after the next hourly synchronisation — see Availability calculation.
{% endstep %}

{% step %}
**Find the Opera reservation of a booking**

1. Open the booking in Tourpaq Office and go to the **Bed Bank** tab.
2. Copy the **Reference**. This is the Opera confirmation number.
3. In Opera, go to **Bookings → Reservations → Manage Reservation**.
4. Enter the number in **Conf / Cxl / External** and click **Search**.

Opera lists the reservation under that confirmation number, for the same property, room type and stay dates as the Tourpaq booking. A booking with several rooms is listed with one line per room under the same confirmation number.
{% endstep %}

{% step %}
**Work on a booking without sending changes to Opera**

1. Open the booking.
2. In the booking summary panel on the right, select **Disable Opera Connect**.
3. Make your changes and click **Save**.
4. In the confirmation dialog, click **Save**.

<figure><img src="https://1539646852-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FZCqO8EQ5P5Mioq1zbQAc%2Fuploads%2FzjeZ8IIMOBDFRzIClYbL%2Fimage.png?alt=media&#x26;token=4286863d-a774-45e4-b634-ba63d9632d81" alt="The Disable Opera Connect checkbox on the booking page"><figcaption><p>The Disable Opera Connect checkbox on the booking page.</p></figcaption></figure>

The booking and passenger changes are saved in Tourpaq. Nothing is sent to Opera. The checkbox is shown only for bookings that have an Opera setting.

{% hint style="danger" %}
Creating or updating a booking sends the booking data to Opera, unless **Disable Opera Connect** is selected. A booking or passenger cancelled while it is selected stays active in Opera until you cancel it there.
{% endhint %}
{% endstep %}
{% endstepper %}

#### Field Reference

| Field                     | Description                                                                                                                                                            | Required                                                            | Notes                                                                                |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| **Managed by**            | **Hotel → Hotels → hotel → Basic setup → Additional settings.** Selects the system that manages the hotel. `OracleOpera` makes Opera the source of availability.       | Conditional — select `OracleOpera` for every hotel managed in Opera | Overrides manual allotment handling in Tourpaq.                                      |
| **BED BANK**              | Column in the **Hotels** list. Shows `OracleOpera` for hotels managed by Opera.                                                                                        | –                                                                   | Filter with **Display only Bed Banks**.                                              |
| **ROOM CODE**             | Column on the hotel **Room Types** tab. The code that Tourpaq matches to the Opera room type.                                                                          | Yes                                                                 | Must match the Opera room type code exactly.                                         |
| **NO.**                   | Column on the hotel **Allotment** tab, next to PERIOD START, PERIOD STOP, ROOM TYPE, MIN. STAY and BOARD BASIS. The number of rooms available for the period.          | –                                                                   | Filled from Opera for hotels managed by Opera.                                       |
| **Category Type**         | **Extras Setup → Extras Category → Settings.** `Opera Package`, `Opera Item Inventory` or `Opera Baggage` links the category to the Opera integration.                 | No                                                                  | Extras in the category are sent to Opera.                                            |
| **Code** (Extra)          | **Extras Setup → Extras.** The code of the Extra. Tourpaq maps it to the Opera package.                                                                                | Yes                                                                 | The mapping is a naming convention: use the Opera package code.                      |
| **Reference**             | **Booking → Bed Bank** tab. The Opera confirmation number of the reservation.                                                                                          | –                                                                   | Read-only. Use it to find the reservation in Opera.                                  |
| **Disable Opera Connect** | Booking summary panel on the right, between **Is Group Booking** and **Remember Extras**. Stops changes to this booking from being sent to Opera while it is selected. | No                                                                  | Shown only for bookings that have an Opera setting. Each save asks for confirmation. |

**Inventory values**

Opera holds three inventory values. Tourpaq reads all three.

| Value     | Description                                                                                                                                                                           |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **House** | The number of rooms in the hotel that are still available for sale.                                                                                                                   |
| **Room**  | The number of rooms available for one room type.                                                                                                                                      |
| **Block** | Rooms reserved in Opera under a block code, for a specific name and period. Block allotments are available only to bookings that include transport. Opera has no notion of transport. |

**Availability calculation**

The synchronisation service reads House, Room and Block inventory every hour. A full synchronisation of all room types, including the whole season of the blocks and the House availability, took about 40 minutes in a load test. New block inventory in Opera therefore becomes sellable in Tourpaq, in Office and online, after 40 minutes to 1 hour 40 minutes, depending on when the service runs.

**Package trips with transport.** The Block and House calculation applies only to package trips with transport, and to all room types. For every room type, Tourpaq checks availability in this order:

1. **Block** allotment of the booking's block.
2. If the Block allotment for the room type is 0 or negative, **House** allotment. House can be booked only when its value is greater than zero. House is also limited by the Room value of the room type: Tourpaq uses the smaller of House and Room.

If a booking needs more rooms than the block holds, Tourpaq takes the available rooms from the block and the rest from House.

| Situation                                                                                 | Result                                                                                                  |
| ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| The room type has 1 room on the block and none on House.                                  | The booking succeeds. The Block allotment drops to 0, and the Opera reservation carries the block code. |
| The booking asks for 2 rooms of a room type. The block holds 1 room and House holds more. | The booking succeeds. Tourpaq takes 1 room from the block and 1 room from House.                        |

**Hotel Only bookings.** Availability is limited to the House and Room inventory. Block allotment is not checked. The Block and House order above does not apply to Hotel Only bookings.

For a room type, Tourpaq treats House and Room together as follows:

| House | Room | Available rooms |
| ----- | ---- | --------------- |
| 2     | 4    | 2               |
| 4     | 3    | 3               |

A room type is available when both House and Room are larger than zero. The number of available rooms is the smaller of the two.

{% hint style="warning" %}
Tourpaq does not check that a room is linked to the right block in Opera. If the same block code is used for more than one departure, Tourpaq does not prevent a booking across those departures. Opera rejects a booking when the room is linked to a different block, and the booking does not go through.
{% endhint %}

**Block codes**

The name of a block in Opera is free text. Tourpaq uses the **Block Code** of the block. In the Opera staging environment, for example, block codes such as `BLL202620271` and `CPH202620271` start with a departure airport code and run from 01-11-2026 to 01-11-2027.

Opera shows these fields for each block in **Bookings → Blocks → Manage Block**:

| Column                       | Description                                     |
| ---------------------------- | ----------------------------------------------- |
| **Block Name**               | The name of the block.                          |
| **Block ID**                 | The Opera identifier of the block.              |
| **Block Status**             | For example `ACT` (active) or `DEF` (definite). |
| **Block Code**               | The code that Tourpaq uses.                     |
| **Start Date**, **End Date** | The period that the block covers.               |

On the Opera reservation, the used block appears in **Block Code**. The field is empty when the room comes from House.

**Extras sent to Opera**

Extras that Tourpaq sends to Opera use an Opera **Category Type**:

| Category Type            | Description                                                                |
| ------------------------ | -------------------------------------------------------------------------- |
| **Opera Package**        | Extras that Opera receives as a package, for example the Pension category. |
| **Opera Item Inventory** | Extras that Opera receives as an individual item.                          |
| **Opera Baggage**        | Extras for baggage.                                                        |

Only the Extra's code is mapped, by naming convention.

In Opera, the reservation has a **Packages** dialog with the tabs **Packages**, **Inventory Items** and **Daily View**. The **Packages** tab lists the available packages by **Code**, **Description**, **Calculation Rule**, **Rhythm** and **Price**, and the packages already on the reservation under **Selected Packages**. The **Item Inventory** link on the reservation shows the inventory items.

{% hint style="warning" %}
If Opera does not recognise the code of an Extra in an Opera category, Opera returns an error for the Extra. The booking is still created in Tourpaq. Create the matching package in Opera, or move the Extra to a category that is not an Opera category.
{% endhint %}

**Data sent to Opera**

When a booking is created, Tourpaq sends:

| Data           | Fields                                                                       |
| -------------- | ---------------------------------------------------------------------------- |
| **Booking**    | Booking No                                                                   |
| **Customer**   | Name, first name, phone, email, birthday, nationality                        |
| **Passengers** | Name, first name, phone, email, birthday, gender                             |
| **Products**   | Products on the booking                                                      |
| **Transport**  | Departure date and time, departure code, arrival date and time, arrival code |
| **Block**      | Block Code                                                                   |

When a booking is updated, Tourpaq sends all of the booking data again, not only the changed data. The room, transport, customer, passenger and Extra details are compared with the existing booking, and the update is sent to Opera.

**Passenger profiles.** Each passenger is matched or created as an individual profile in Opera. If a matching profile exists, Tourpaq reuses it. If not, Tourpaq creates a new profile in Opera. Consistent customer data improves matching and reduces duplicate profiles.

Enter all customer details before you click **Take Allotment**, to avoid duplicate customers in Opera.

If a required mapping is missing, the booking can fail during export.

**Bed Bank tab**

The **Bed Bank** tab of a booking shows the hotel reservation held in the external system. For a hotel managed by Opera, it shows:

| Field            | Description                                                                                                                                    |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| **Reference**    | The Opera confirmation number.                                                                                                                 |
| **Status**       | The status of the reservation, for example `Confirmed`.                                                                                        |
| **Booking Date** | The date of the reservation.                                                                                                                   |
| **Hotel**        | The hotel code, which is the Opera property code.                                                                                              |
| **Check In/Out** | The arrival and departure dates.                                                                                                               |
| **Price**        | The price of the reservation.                                                                                                                  |
| **Added by**     | The user shown as having added the reservation.                                                                                                |
| **Holder**       | The name of the reservation holder.                                                                                                            |
| **Room**         | The room type, with one block per room, and the passengers (Full Name, Gender) in each room.                                                   |
| **History**      | Earlier versions of the reservation, with Reference, Check In, Check Out, Confirmation Status, Creation Date, Net Price, Currency and Updated. |

{% hint style="info" %}
The panel title in Tourpaq Office reads **Hotel Beds Reservation**, because the tab is shared by all bed banks.
{% endhint %}

**Example: booking in Tourpaq and reservation in Opera**

A staging booking for two rooms with a bus transport, and the reservation that Opera holds for it:

|                        | Tourpaq (booking 228039)                                       | Opera (confirmation 575010084)                                                                                            |
| ---------------------- | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Hotel                  | A hotel managed by Opera. **Bed Bank** tab → **Hotel** `ESCLS` | **Property** `ESCLS`                                                                                                      |
| Room type              | `CF1`                                                          | **Room Type** `CF1`                                                                                                       |
| Stay                   | 30-10-2026 to 06-11-2026                                       | **Arrival** 30/10/2026, **Departure** 06/11/2026                                                                          |
| Outbound transport     | `BLL-ACE`, `JTD531`, 30.10                                     | **Transportation → Pick Up**: 30/10/2026, 11:25, Type `BUS`, Station `ACE`, Carrier `Jet Time`, Transport Number `JTD531` |
| Return transport       | `ACE-BLL`, `JTD532`, 06.11                                     | **Transportation → Drop off**: 06/11/2026, Type `BUS`, Station `BLL`, Carrier `Jet Time`, Transport Number `JTD532`       |
| Block                  | None. The rooms come from House.                               | **Block Code** empty, because no block was used                                                                           |
| Reservation identifier | **Bed Bank** tab → **Reference** `575010084`                   | **Confirmation Number** `575010084`, **External References** type `OPERA`                                                 |
| Status                 | **Bed Bank** tab → **Status** `Confirmed`                      | **Status** `Reserved`                                                                                                     |

**Messages shown when Disable Opera Connect is selected**

| Situation                             | What Tourpaq shows                                             | Result                                                                                                                                       |
| ------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **Disable Opera Connect** is selected | The banner `Opera is disabled`, directly below the action bar. | The banner stays visible while synchronisation is disabled for the booking.                                                                  |
| You click **Save**                    | A confirmation dialog with the message below.                  | **Save** saves the booking and passenger changes without synchronisation to Opera. **Cancel** cancels the save and keeps you on the booking. |
| You cancel a booking or a passenger   | A reminder with the message below.                             | The cancellation is not sent to Opera. Cancel the passenger or reservation in Opera yourself.                                                |

<figure><img src="https://1539646852-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FZCqO8EQ5P5Mioq1zbQAc%2Fuploads%2FiMXf1BzoYMqFDLDlCB4L%2Fdisable%20opera%20connect.png?alt=media&#x26;token=ff4abdfe-b0c3-459c-8276-eb29e609aa0f" alt="The Opera is disabled banner below the action bar of a booking"><figcaption><p>The Opera is disabled banner.</p></figcaption></figure>

```
Opera Connection is disabled. Are you sure you want to save without syncing to Opera?
```

<figure><img src="https://1539646852-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FZCqO8EQ5P5Mioq1zbQAc%2Fuploads%2FN7NNZz0yq9hkNapMNrDC%2Fsave%20bookink%20opera.png?alt=media&#x26;token=63bc4577-e872-4097-b349-06aaf8538630" alt="The confirmation dialog shown when saving a booking with Opera disabled, with Save and Cancel buttons"><figcaption><p>The save confirmation dialog.</p></figcaption></figure>

```
Please remember to cancel the passenger/reservation in Opera as well.
```

<figure><img src="https://1539646852-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FZCqO8EQ5P5Mioq1zbQAc%2Fuploads%2FqJCpKAb7qVP90L5aZuIA%2Fcancel%20pax%20opera.png?alt=media&#x26;token=3365504f-a6af-4cce-80cc-fa132ec8fc49" alt="The reminder shown when cancelling a passenger with Opera disabled"><figcaption><p>The cancellation reminder.</p></figcaption></figure>

**Logging**

The integration logs booking export requests, responses from Opera, errors and validation issues, mapping failures, and profile creation or matching results. The primary logs are stored in the database, including request payloads, response payloads and error messages.

The **Bed Bank** tab of the booking shows the **Reference**, the **Status** and the **History** of the reservation.

#### Related pages

* [PMS Integration](https://tourpaq.gitbook.io/staging-tourpaq-docs/integration/pms-integration)
* [General tab](https://tourpaq.gitbook.io/staging-tourpaq-docs/hotel/hotel-creation/general-tab)
* [Room Types](https://tourpaq.gitbook.io/staging-tourpaq-docs/hotel/hotel-creation/room-types)
* [Hotel allotments](https://tourpaq.gitbook.io/staging-tourpaq-docs/hotel/hotel-creation/hotel-allotments)
* [Edit Extra Category](https://tourpaq.gitbook.io/staging-tourpaq-docs/extras-category/extra-category-overview/edit-extra-category)
* [New Booking](https://tourpaq.gitbook.io/staging-tourpaq-docs/booking/new-booking/new-booking)
