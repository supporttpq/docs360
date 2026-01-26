# Allotments per day

### Overview

Use **Allotments per day** to set room availability per date and room type.

It shows what is allocated, booked, and still free.

This is the daily “inventory control” screen for hotels.

### Purpose

Use it to:

* Allocate a daily number of rooms for each room type.
* Define secured and guaranteed allotments with the hotel.
* Track how many rooms are already booked and how many remain free.
* Adjust daily availability to match contracts, demand, or sales limits.
* Avoid overselling by keeping availability accurate.

{% hint style="info" %}
Daily values typically come from your generated allotment periods. Set those on [Hotel allotments](../hotel-allotments.md).
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### Fields

<table><thead><tr><th width="224">Field</th><th>Description</th></tr></thead><tbody><tr><td><strong>Room Type</strong></td><td>The room type / category. Example formats: <code>2/2 + 2B</code>, <code>1/2-mel10</code>.</td></tr><tr><td><strong>Date</strong></td><td>The calendar date for which allotment is being defined.</td></tr><tr><td><strong>Day</strong></td><td>The day of week.</td></tr><tr><td><strong>No.</strong></td><td>Total rooms allocated for that date.</td></tr><tr><td><strong>Secured</strong></td><td>The number of secured rooms</td></tr><tr><td><strong>Guaranteed</strong></td><td>The number of guaranteed rooms</td></tr><tr><td><strong>Book</strong></td><td>Rooms already booked for that date.</td></tr><tr><td><strong>Free</strong></td><td>Rooms still available (<code>No. - Book</code>).</td></tr><tr><td><strong>Days</strong></td><td>The number of days before arrival, the release is executed (only daily releases).<br>The cell is empty if no release rules are defined.<br>The cell is editable, allowing the release days to be ed</td></tr><tr><td><strong>R</strong></td><td><p>If the release is executed, the box is checked, and the release can be undone by removing the checkmark. </p><p>When a release is undone, edit DAYS with the new deadline and update AR and SR to make rooms available.</p></td></tr><tr><td><strong>AR</strong></td><td>If the release is executed, the box is checked, and the release can be undone by removing the checkmark.<br>When a release is undone, edit DAYS with the new deadline and update AR and SR to make rooms available.</td></tr><tr><td><strong>SR</strong></td><td>The number of secured rooms released.<br>Edit SR when a release is undone to adjust the number of rooms moved back.</td></tr><tr><td><strong>PAX 1–4</strong></td><td>Max rooms by occupancy (1–4 pax).</td></tr><tr><td><strong>Min</strong></td><td>Minimum stay in nights.</td></tr><tr><td><strong>Stay length</strong></td><td>Rooms allocated per charter transport, based on selected stay days.</td></tr></tbody></table>

{% hint style="warning" %}
**PAX1, PAX2, PAX3, PAX4** – When you hover over these cells, a tooltip appears showing the number of booked rooms for each corresponding PAX category (PAX1, PAX2, PAX3, PAX4).
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (580).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If a **Stop Sale** exists for a date, you will see a yellow warning icon next to the room. Stop sales are configured in [Stop Sales](../../../stop-sales.md).
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (581).png" alt=""><figcaption></figcaption></figure>

### Search with allotment control

<figure><img src="../../../.gitbook/assets/image (582).png" alt=""><figcaption></figcaption></figure>

Use this search when you need availability split by transport departures.

#### Functionality

When searching with **Allotment Control**:

* The search is based on **departure date**.
* Results display per transport, with columns for:
  * **RESV (Reserved allotment)** – Rooms reserved for that transport.
  * **BOOK** – What is already booked on that transport.

The columns together provide a quick overview of remaining availability.

{% hint style="info" %}
If **RESV** is empty, no extra transport limit applies. Use `0` to block sales for that transport.
{% endhint %}

#### Stay length

Stay length columns reserve rooms for specific trip durations.

When you reserve rooms for a stay length, Tourpaq also reserves multiples of it. Example: reserving 7 days impacts 14 days too.

For the full workflow, see [Reserve rooms for stay lengths](reserve-rooms-for-stay-lengths.md).

{% hint style="warning" %}
**STAY LENGTH (7)** – Hover a cell to see reserved, booked, available, and free rooms.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (583).png" alt=""><figcaption></figcaption></figure>

The tooltip for each cell displays detailed reservation data to make it easier to interpret the information behind the cell values.

| **Value**     | **Explanation**                                                                                                                                                            |
| ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Reserved**  | The number of rooms reserved for the current stay length. This is the same number shown in the cell, displayed in the tooltip for easier visibility.                       |
| **Booked**    | The number of rooms booked with a stay length equal to the current stay length, or a multiple of it.                                                                       |
| **Available** | The number of rooms still available from the total reserved rooms.                                                                                                         |
| **Free**      | The number of rooms that are not reserved for any stay length and are free to book. “Free” indicates that it is possible to reserve additional rooms for this stay length. |

#### Room control status

Each transport displays a **control status value** that determines how many rooms can be sold:

* **-1** → No room limit (unlimited sales possible).
* **0** → No rooms can be sold on this transport.
* **1+** → The exact maximum number of rooms that can be sold for the specified transport and interval.

#### Usage notes

* This feature is critical for **capacity planning** and ensuring correct allocation of hotel rooms per flight.
* The status values should be monitored regularly, especially during peak booking periods, to avoid overselling.
* Adjustments to allotments must be coordinated with both transport and hotel availability.

### Search with Stay Lenghts

<figure><img src="../../../.gitbook/assets/image (576).png" alt=""><figcaption></figcaption></figure>

The **Search with Stay Length** option is used to filter hotel allotment data based on the selected stay duration.

When **Search with Stay Length** is used:

* The search **does not include Transport allotments**
* Only **hotel-related allotments and controls** are shown
* Results reflect availability based on the defined stay length rules

This helps users focus strictly on hotel availability without mixing transport data into the results.

### How to update daily allotments

{% stepper %}
{% step %}
### Open the screen

Go to **Hotel → Allotment per Day**.
{% endstep %}

{% step %}
### Search the dates you need

Select **Period**, **Room Type**, and optional **Week Days**.

Click **Search**.
{% endstep %}

{% step %}
### Edit the values

Update **No.**, **Secured**, and **Guaranteed** as needed.

Check **Book** and **Free** for sanity.
{% endstep %}

{% step %}
### Save or revert

Click **Update** to save.

Click **Cancel** to discard changes.
{% endstep %}
{% endstepper %}

### How to edit releases (manual adjustment)

Use this when you need to override the automated release result for specific dates.

{% stepper %}
{% step %}
### Open the screen

Go to **Hotel → Allotment per Day**.
{% endstep %}

{% step %}
### Search the dates and room types

Select **Period** and **Room Type**.

Click **Search**.
{% endstep %}

{% step %}
### Adjust release status and quantity

Edit **R** to mark/unmark as released.

Edit **For R** to control how many rooms are available for release.
{% endstep %}

{% step %}
### Save

Click **Update**.
{% endstep %}
{% endstepper %}

### SkiStar Allotment per Day

When a hotel is managed by **SkiStar**, each hotel represents one house or apartment. Availability is therefore binary per unit.

* If the unit is available, allotment is always `1`.
* If the unit is not available, allotment is `0`.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### FAQ

<details>

<summary>What’s the difference between <strong>No.</strong>, <strong>Secured</strong>, and <strong>Guaranteed</strong>?</summary>

**No.** is what you plan to sell for that date.

**Secured** is what the hotel commits to allocate.

**Guaranteed** is what you pay for even if unsold.

</details>

<details>

<summary>Why is <strong>Free</strong> lower than expected?</summary>

Start with the basics: **Free = No. - Book**.

Then check **Stop Sales**, **releases**, and any transport limits.

</details>

<details>

<summary>I can’t sell a room, but <strong>Free</strong> is positive. Why?</summary>

Common causes:

* Stop sale on the date. See [Stop Sales](../../../stop-sales.md).
* Room is released or release rules limit sales. See [Releases](../releases/).
* Transport-level limits in **Search with allotment control** (status `0` or a low number).
* Minimum stay restrictions (**Min**).

</details>

<details>

<summary>What does the <strong>R</strong> column mean?</summary>

It indicates release status for that room/date.

Released rooms can behave differently depending on your release setup.

</details>

<details>

<summary>When should I use “Search with allotment control”?</summary>

Use it when you need availability per transport departure.

It helps you spot transport-specific limits and stay-length reservations.

</details>

<details>

<summary>How do stay length reservations affect availability?</summary>

They reserve rooms for specific trip durations.

Multiples are also reserved to avoid overlaps.

See [Reserve rooms for stay lengths](reserve-rooms-for-stay-lengths.md).

</details>
