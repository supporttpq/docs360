# Reserve rooms for stay lengths

### Overview

Use **Reserve rooms for stay lengths** to reserve rooms on an arrival day.

It is **independent of transport**.

Use it when:

* A destination has multiple transports arriving on the same day.
* Agencies want to reserve rooms for arrivals on a certain weekday (e.g., Friday), regardless of which transport the guests use.
* Room reservations need to be managed by **stay duration** (e.g., reserving rooms for long stays vs. short stays).

{% hint style="warning" %}
This option requires **Room Occupancy** to be enabled by a **superadmin**.
{% endhint %}

### How to access

1. Go to **Hotel → Allotment per day**.
2. Open **Search with Allotment Control**.
3. Find **Reserve rooms for stay lengths**.

{% hint style="info" %}
If you need the basics of the daily allotment screen first, see [Allotments per day](./).
{% endhint %}

### How it works

You reserve rooms for an **arrival day** and a **stay length**.

This lets you “hold back” rooms for specific durations.

Example:

* Friday arrivals exist for 5, 7, and 14 nights.
* You can reserve rooms separately for each duration.

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Fields

| Column           | Meaning                                                                                                      |
| ---------------- | ------------------------------------------------------------------------------------------------------------ |
| ROOM             | Room type / code.                                                                                            |
| DATE             | Date of arrival.                                                                                             |
| DAY              | Weekday.                                                                                                     |
| NO.              | Total rooms allocated for the date.                                                                          |
| SECURED          | Rooms secured by contract.                                                                                   |
| GUARANTEED       | Rooms guaranteed financially.                                                                                |
| BOOK             | Rooms booked for the date.                                                                                   |
| FREE             | Rooms still available (`NO. - BOOK`).                                                                        |
| R                | True (green) if the room is released.                                                                        |
| FOR R            | Rooms available for release.                                                                                 |
| MAX              | Max rooms allowed.                                                                                           |
| EXTRA            | Extra rooms.                                                                                                 |
| PAX 1 - PAX 4    | Max rooms by occupancy (1–4 pax).                                                                            |
| MIN              | Minimum stay (nights).                                                                                       |
| STAY LENGTH      | Columns where you reserve rooms per stay length.                                                             |
| RESV             | Reserved allotment per transport. Use `0` to block sales for that transport. Leave empty for no extra limit. |
| BOOK (transport) | Seats booked on the transport (shown in the transport columns).                                              |

{% hint style="warning" %}
**Stay length (3, 7)**: Hover a cell to see reserved, booked, available, and free rooms for that stay length.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The tooltip helps you interpret what the cell value actually means.

| **Value**     | **Explanation**                                                                                                                                                            |
| ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Reserved**  | The number of rooms reserved for the current stay length. This is the same number shown in the cell, displayed in the tooltip for easier visibility.                       |
| **Booked**    | The number of rooms booked with a stay length equal to the current stay length, or a multiple of it.                                                                       |
| **Available** | The number of rooms still available from the total reserved rooms.                                                                                                         |
| **Free**      | The number of rooms that are not reserved for any stay length and are free to book. “Free” indicates that it is possible to reserve additional rooms for this stay length. |

{% hint style="info" %}
Stay length reservations are applied per eligible transport interval.

They also consider **multiples** of a stay length when counting bookings.
{% endhint %}

### Reserve rooms (workflow)

{% stepper %}
{% step %}
### Open the screen

Go to **Hotel → Allotment per day**.

Open **Search with Allotment Control**.
{% endstep %}

{% step %}
### Pick date and room

Select the arrival **Date** and **Room**.

Run the search.
{% endstep %}

{% step %}
### Enter stay length reservations

In the **Stay length** columns, enter how many rooms you want reserved.

Use this when you need to protect long stays or short stays.
{% endstep %}

{% step %}
### Save

Click **Update**.
{% endstep %}
{% endstepper %}

<details>

<summary>Validation checklist: booking availability updates as expected</summary>

| Step                                                                           | Expected Results                                                                                                                                                                                                                                                                                                                         |
| ------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Access the **Hotels→Hotel** page                                               | The list displaying all available hotels should open                                                                                                                                                                                                                                                                                     |
| Select a hotel from the list and access the **Allotment per Day** page         | The page should open with the allotments available for the current date                                                                                                                                                                                                                                                                  |
| Select a date and Room and click on **Search with All. Control**               | <p>The list containing all available allotments for the date and room type selected should appear<br><br><em><strong>A column available for each transport should appear with allotment inputs for each departure date</strong></em><br><br><br></p>                                                                                     |
| Add a value for one of the departure days in a specific interval               | <p>The value should appear in the selected input<br><br><img src="https://tourpaq.youtrack.cloud/api/files/8-94884?sign=MTc0NzUyNjQwMDAwMHwxLTMyNnw4LTk0ODg0fE85Y1hab2ZZSXVmaWxQelJoWGJhR3Bvb3V2aEtHX3doaDQ0N0F2YlUyY0kNCg&#x26;updated=1747300918548" alt="image.png"></p>                                                              |
| Click on **Update**                                                            | A success popup should appear and the value should be saved                                                                                                                                                                                                                                                                              |
| Click on **New booking**                                                       | The booking creation menu should open                                                                                                                                                                                                                                                                                                    |
| Select a transport with a different length                                     | <p>The departure length of each transport should appear in the booking menu<br><img src="https://tourpaq.youtrack.cloud/api/files/8-94885?sign=MTc0NzUyNjQwMDAwMHwxLTMyNnw4LTk0ODg1fExWbnAzWTBtTlc3WWlUbURkUVgwMTh4UjhycVQ4c0loOUNTTUo0RzExSk0NCg&#x26;updated=1747302678724" alt="image1.png"></p>                                      |
| Select the hotel used for the allotment                                        | The options should be available for booking                                                                                                                                                                                                                                                                                              |
| In the Hotel tab, check the number of available rooms                          | <p>The number should have the free allotment value without the selected rooms reserved for the travel length<br><br><img src="https://tourpaq.youtrack.cloud/api/files/8-94893?sign=MTc0NzUyNjQwMDAwMHwxLTMyNnw4LTk0ODkzfHJ2eEE2OW4yLVJLSDZZUUdUZ3hUc1lhaU1vT3V2WU1vUkJBdEtSN051dTANCg&#x26;updated=1747304624909" alt="image3.png"></p> |
| Edit the number of rooms and passengers to be greater than the value available | The number should change                                                                                                                                                                                                                                                                                                                 |
| Click on **Take Allotment**                                                    | <p>A warning should appear, stopping the booking from saving<br><br><img src="https://tourpaq.youtrack.cloud/api/files/8-94895?sign=MTc0NzUyNjQwMDAwMHwxLTMyNnw4LTk0ODk1fFNuWjFrbTlOWk9ibDB3aW5wbUF3S3lmYk9YeXkwdUZHRzRSbkV4T3p2Nm8NCg&#x26;updated=1747304711549" alt="image5.png"></p>                                                 |
| Click on **Edit** in the Transport tab                                         | The list of transports should open                                                                                                                                                                                                                                                                                                       |
| Select a transport with the same length as the one used                        | The transport selected should appear in the booking menu                                                                                                                                                                                                                                                                                 |
| Select the hotel used for the allotment                                        | The options should be available for booking                                                                                                                                                                                                                                                                                              |
| In the Hotel tab, check the number of available rooms                          | <p>The number of available rooms should be the one of free rooms<br><br><img src="https://tourpaq.youtrack.cloud/api/files/8-94910?sign=MTc0NzUyNjQwMDAwMHwxLTMyNnw4LTk0OTEwfHRENlQwN3FpM1lTY25qTjhvRG14VWZMUnc3cWRwUm5rZkhRaVdKRzNRZ0kNCg&#x26;updated=1747308508449" alt="image6.png"></p>                                             |
| Return to the hotel menu                                                       | The hotel details page should open                                                                                                                                                                                                                                                                                                       |
| Access the **Allotment per Day** tab                                           | The allotment tab should open                                                                                                                                                                                                                                                                                                            |
| Enter the date and room used for the booking                                   | The details should be available                                                                                                                                                                                                                                                                                                          |
| Add the value of free rooms to one of the departure days                       | The value should appear in the input                                                                                                                                                                                                                                                                                                     |
| Click on **New booking**                                                       | The booking creation menu should open                                                                                                                                                                                                                                                                                                    |
| Select a transport with a different length from the one used                   | The selected option should appear in the menu                                                                                                                                                                                                                                                                                            |
| Click on the **Edit** button on the hotel tab                                  | A list of all available hotels should appear                                                                                                                                                                                                                                                                                             |
| Check if the room is available for booking                                     | The room shouldn't be available for booking                                                                                                                                                                                                                                                                                              |
| Click on **Edit** in the Transport tab                                         | The list of transports should open                                                                                                                                                                                                                                                                                                       |
| Select a transport with the same length as the one used                        | The transport selected should appear in the booking menu                                                                                                                                                                                                                                                                                 |
| Select the hotel used for the allotment                                        | The options should be available for booking                                                                                                                                                                                                                                                                                              |
| In the Hotel tab, check the number of available rooms                          | The number of available rooms should be the one of free rooms                                                                                                                                                                                                                                                                            |

</details>

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
