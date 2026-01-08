# Hotel allotment overview

### Overview

The **Hotel Allotment Overview** is a reporting view of hotel availability.

It shows **beds**, **rooms**, and (optionally) **guaranteed rooms** for a selected date range.

You can access this feature by navigating to:\
**Hotel → Business Intelligence → Allotment Overview**

### Filters

Use these filters to narrow the results:

1. **Hotel Code** – Search by hotel code. If you search using this filter, all other filters are disabled.
2. **Transport** – Filter allotments by a selected transport option.
3. **Real Transport** – Filter allotments by a selected real transport option.
4. **Resort** – Filter results by resort.
5. **Hotel Name** – Search allotments by the hotel’s name.

<figure><img src="../../.gitbook/assets/image (14) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If a cell has a **red background**, it means there is a **Stop Sale** for that date.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (16) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Displayed data

* **Bed number**
  * Total available beds in the selected period.
* **Rooms number**
  * Rooms available for sale in the selected period.
  * Enable `Show only parent rooms` to hide derived/child room types.
* **Guaranteed rooms**
  * Enable `Guarantee Rooms` to show guaranteed rooms below each allotment line.

<figure><img src="../../.gitbook/assets/image (15) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### FAQ

<details>

<summary>What is this overview used for?</summary>

Use it to get a fast, consolidated view of availability.

It’s useful for spotting shortages, peaks, and stop sales.

</details>

<details>

<summary>Why does <strong>Hotel Code</strong> disable the other filters?</summary>

It’s treated as an exact lookup.

Clear **Hotel Code** if you want to filter by transport, resort, or hotel name.

</details>

<details>

<summary>What does a red cell mean?</summary>

A red cell means **Stop Sale** on that date.

Stop sales are configured in [Stop Sales](../../stop-sales.md).

</details>

<details>

<summary>What’s the difference between <strong>beds</strong> and <strong>rooms</strong>?</summary>

**Beds** are capacity (sleeping places).

**Rooms** are the sellable room units.

They can differ for multi-bed rooms and room mixes.

</details>

<details>

<summary>What are “parent rooms”?</summary>

Parent rooms are the base room types.

Child rooms are derived variants, such as occupancy splits.

Use `Show only parent rooms` when you want a cleaner overview.

</details>

<details>

<summary>Why don’t I see guaranteed rooms?</summary>

Enable the `Guarantee Rooms` checkbox.

Also verify the hotel allotment has guaranteed values set.

See [Hotel allotments](hotel-allotments.md).

</details>

<details>

<summary>Why is the overview empty?</summary>

Check that allotments exist for the period and hotel.

Check that departure stat weeks are configured for the year.

See [Departure stat weeks](../../setup/departure-stat-weeks.md).

</details>

<details>

<summary>Where do these numbers come from?</summary>

They are based on the hotel’s configured allotments and the booked usage.

Daily values are managed in [Allotments per day](allotments-per-day/).

</details>
