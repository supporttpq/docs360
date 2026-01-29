# Reserve rooms for stay lengths

### Overview

The **Reserve rooms for stay lengths** feature allows agencies to reserve hotel rooms for guests on specific arrival days, **independent of transport**.

This is useful in cases where:

* A destination has multiple transports arriving on the same day.
* Agencies want to reserve rooms for arrivals on a certain weekday (e.g., Friday), regardless of which transport the guests use.
* Room reservations need to be managed by **stay duration** (e.g., reserving rooms for long stays vs. short stays).
* The agency protects the rooms from being booked between its normal charter flights, thus using the rooms every day.

{% hint style="warning" %}
This option requires **Room Occupancy** to be enabled by a **superadmin**.
{% endhint %}

### How to access

1. Go to **Hotel → Allotment per day**.
2. Open **Search with Stay Length**.
3. Find **Reserve rooms for stay lengths**.

{% hint style="info" %}
If you need the basics of the daily allotment screen first, see [Allotments per day](./).
{% endhint %}

### How it works

You reserve rooms for an **arrival day** and a **stay length**.

This lets you reserve rooms for specific durations.

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

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
| DAYS          | <p>The number of days before arrival, the release is executed (only daily releases).<br>The cell is empty if no release rules are defined.<br>The cell is editable, allowing the release days to be edited.</p>               |
| R             | <p>If the release is executed, the box is checked, and the release can be undone by removing the checkmark.</p><p>When a release is undone, edit DAYS with the new deadline and update AR and SR to make rooms available.</p> |
| AR            | <p>The number of allotment rooms released.</p><p>Edit AR when a release is undone to adjust the number of rooms moved back.</p>                                                                                               |
| SR            | <p>The number of secured rooms released.<br>Edit SR when a release is undone to adjust the number of rooms moved back.</p>                                                                                                    |
| PAX 1 - PAX 4 | Max rooms by occupancy (1–4 pax).                                                                                                                                                                                             |
| MIN           | Minimum stay (nights).                                                                                                                                                                                                        |
| STAY LENGTH   | Columns where you reserve rooms per stay length.                                                                                                                                                                              |

{% hint style="warning" %}
**Stay length (5, 6, 7, 8)**: Hover a cell to see reserved, booked, available, and free rooms for that stay length.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

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

For each possible duration (based on the eligible transport intervals), rooms can be reserved for a specific arrival day. For example, if three transports arrive on Friday with durations of 5, 6, 7, and 8 days, rooms can be reserved for that Friday separately for each duration.

{% hint style="info" %}
**Important:** When a room is reserved for a specific stay length and arrival day, for example a **7-day stay**, the room is also considered reserved for **any multiple of that stay length** (such as 14 or 21 days).

The same rule applies to the **number of booked rooms**. The booked value reflects not only the exact stay length, but also all multiples of that stay length.
{% endhint %}

The **Free Hotel Allotment (FHA)** in the price list represents the total of **Available** plus **Free** rooms.

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
* After changes are made, the system may require up to one minute to update and display the new values.
* Updates to the price list, including **Free Hotel Allotment (FHA)** values, may take a few minutes to be reflected in the system.
{% endhint %}

In Tourpaq, there is a service called FRC (free room count) that runs between 2 minutes and up to several hours, depending on how many tasks are in the database.

How long a change takes to apply depends on FRC and the Elastic search engine:

* In Office, it takes effect immediately.
* On Site, you must wait for the price list update (only after running FRC + Elastic).

### FAQ

<details>

<summary>Why can’t I see “Reserve rooms for stay lengths”?</summary>

This option requires **Room Occupancy** to be enabled by a **superadmin**.

</details>

<details>

<summary>What does a stay length cell value represent?</summary>

It is the number of rooms **reserved** for that arrival day and stay length.

Hover the cell to see reserved, booked, available, and free rooms.

</details>

<details>

<summary>Does this depend on transport?</summary>

You reserve rooms independently of transport selection.

Tourpaq still evaluates eligible transport intervals to determine valid stay lengths.

</details>

<details>

<summary>Why do I need to wait before I see the effect on Site?</summary>

Office updates apply immediately.

Site availability depends on price list updates after FRC + Elastic.

</details>

<details>

<summary>Why is the “Booked rooms” number higher than expected?</summary>

Booked rooms include bookings with a stay length equal to the current stay length, or a multiple of it.

</details>
