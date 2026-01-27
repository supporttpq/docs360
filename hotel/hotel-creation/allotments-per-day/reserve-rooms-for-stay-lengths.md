# Reserve rooms for stay lengths

### Overview

The **Reserve rooms for stay length**s feature allows agencies to reserve hotel rooms for guests on specific arrival days, **independent of transport**.&#x20;

This is useful in cases where:

* A destination has multiple transports arriving on the same day.
* Agencies want to reserve rooms for arrivals on a certain weekday (e.g., Friday), regardless of which transport the guests use.
* Room reservations need to be managed by **stay duration** (e.g., reserving rooms for long stays vs. short stays).
* The agency protects the rooms from being booked in between their normal charter flights, thus using the rooms every day.

{% hint style="warning" %}
This option requires **Room Occupancy** to be enabled by a **superadmin**.
{% endhint %}

### How to access

1. Go to **Hotel → Allotment per day**.
2. Open **Search with Stay Lenght**.
3. Find **Reserve rooms for stay lengths**.

{% hint style="info" %}
If you need the basics of the daily allotment screen first, see [Allotments per day](./).
{% endhint %}

### How it works

You reserve rooms for an **arrival day** and a **stay length**.

This lets you “hold back” rooms for specific durations.

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

### Fields

| Column        | Meaning                                                                                                                                                                                                                       |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ROOM TYPE     | Room type / code.                                                                                                                                                                                                             |
| DATE          | Date of arrival.                                                                                                                                                                                                              |
| DAY           | Weekday.                                                                                                                                                                                                                      |
| NO.           | Total rooms allocated for the date.                                                                                                                                                                                           |
| SECURED       | The number of secured rooms                                                                                                                                                                                                   |
| GUARANTEED    | The number of guaranteed rooms                                                                                                                                                                                                |
| BOOK          | Rooms booked for the date.                                                                                                                                                                                                    |
| FREE          | Rooms still available (`NO. - BOOK`).                                                                                                                                                                                         |
| DAYS          | <p>The number of days before arrival, the release is executed (only daily releases).<br>The cell is empty if no release rules are defined.<br>The cell is editable, allowing the release days to be edited.</p>             |
| R             | <p>If the release is executed, the box is checked, and the release can be undone by removing the checkmark.</p><p>When a release is undone, edit DAYS with the new deadline and update AR and SR to make rooms available.</p> |
| AR            | <p>The number of allotment rooms released. </p><p>Edit AR when a release is undone to adjust the number of rooms moved back.</p>                                                                                              |
| SR            | <p>The number of secured rooms released.<br>Edit SR when a release is undone to adjust the number of rooms moved back</p>                                                                                                    |
| PAX 1 - PAX 4 | Max rooms by occupancy (1–4 pax).                                                                                                                                                                                             |
| MIN           | Minimum stay (nights).                                                                                                                                                                                                        |
| STAY LENGTH   | Columns where you reserve rooms per stay length.                                                                                                                                                                              |

{% hint style="warning" %}
**Stay length (5,6,7,8)**: Hover a cell to see reserved, booked, available, and free rooms for that stay length.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

The tooltip helps you interpret what the cell value actually means.

| **Value**           | **Explanation**                                                                                                                                                            |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Reserved rooms**  | The number of rooms reserved for the current stay length. This is the same number shown in the cell, displayed in the tooltip for easier visibility.                       |
| **Booked rooms**    | The number of rooms booked with a stay length equal to the current stay length, or a multiple of it.                                                                       |
| **Available rooms** | The number of rooms still available from the total reserved rooms.                                                                                                         |
| **Free rooms**      | The number of rooms that are not reserved for any stay length and are free to book. “Free” indicates that it is possible to reserve additional rooms for this stay length. |

{% hint style="info" %}
Stay length reservations are applied per eligible transport interval.
{% endhint %}

For each possible duration (based on the eligible transport intervals), rooms can be reserved for a specific arrival day. For example, if three transports arrive on Friday with durations of 5,6,7, and 8 days, rooms can be reserved for that Friday separately for each duration.

The **Free Hotel Allotment (FHA)** in the price list represents the total of **Available** plus **Free** rooms.

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
* After changes are made, the system may require up to one minute to update and display the new values.
* Updates to the price list, including **Free Hotel Allotment (FHA)** values, may take a few minutes to be reflected in the system.
{% endhint %}

In Tourpaq there is a service called FRC (free room count) that runs between 2 minutes and up to several hours, depending on how many tasks are in the database.&#x20;

Depending on the FRC and the Elastic search engine, it depends on how long before a setting takes effect when attempting to make a reservation:

* in office takes effect immediately&#x20;
* in site you have to wait for price list update (only after running FRC + Elastic).



### Reserve rooms (workflow)

{% stepper %}
{% step %}
### Open the screen

Go to **Hotel → Allotment per day**.
{% endstep %}

{% step %}
### Pick date and room

Select the arrival **Date** and **Room**.

Run the **Search with Stay Lenghts**
{% endstep %}

{% step %}
### Enter stay length reservations

In the **Stay length** columns, enter how many rooms you want reserved.

Use this when you need to protect long stays or short stays.
{% endstep %}

{% step %}
### Save
{% endstep %}
{% endstepper %}

### FAQ

<details>

<summary>When should I use stay length reservations?</summary>

Use it when availability must be protected by **arrival weekday** and **duration**.

Typical cases are mixed durations arriving on the same day.

</details>

<details>

<summary>Does this depend on the selected transport?</summary>

No.

You reserve rooms for an arrival day.

Guests can arrive on any transport that day.

</details>

<details>

<summary>Why does <strong>Booked</strong> count “multiples” of the stay length?</summary>

It avoids overlaps.

Example: a 14-night booking also consumes capacity relevant for 7-night “buckets”.

</details>

<details>

<summary>What does <strong>Free</strong> mean in the stay length tooltip?</summary>

It is capacity not reserved for any stay length.

It can still be booked.

It also means you can reserve more rooms for that stay length.

</details>

<details>

<summary>I can’t see or edit the stay length columns. Why?</summary>

Common causes:

* **Room Occupancy** is not enabled for your company.
* No eligible transport intervals exist for the date/market setup.

</details>

<details>

<summary>What’s the difference between <strong>RESV</strong> and stay length reservations?</summary>

**RESV** limits sales per **transport**.

Stay length reservations allocate rooms per **duration** on the arrival day.

</details>
