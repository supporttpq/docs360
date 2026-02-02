# SkiStar Sync

SkiStar Sync lets Tourpaq automatically import **allotment** and **cost prices** from SkiStar’s FixedPeriodProduct API.

The sync runs once per day and keeps SkiStar-managed accommodations up to date in Tourpaq.

This page explains how the sync works, how it is configured, and how Tourpaq processes allotment and pricing.

Go to [System Setup – Hotel Providers](./) for provider configuration and mappings.

{% hint style="warning" %}
This sync does **not** create bookings in SkiStar.

It only updates allotment and cost prices in Tourpaq.
{% endhint %}

### Overview

SkiStar Sync retrieves availability for the current or upcoming season.

It uses the SkiStar Resort IDs configured on hotels in Tourpaq.

In SkiStar, each property is an individual accommodation unit (house/apartment).

When an accommodation is available, SkiStar returns a free allotment of **1**.

Tourpaq maps each SkiStar accommodation as a **Base Room Type** linked to the correct hotel.

The sync performs API calls for configured stay lengths and Sunday departures within the season window.

### Purpose

* Ensure Tourpaq always has the **current allotment and cost information** for all SkiStar accommodations.
* Remove the need for manual maintenance of allotment and costs.
* Guarantee that pricing and availability used in offers, bookings, and operations remain correct throughout the ski season.

Bookings in SkiStar are handled externally.

Tourpaq Sync only updates **allotment** and **cost prices**.

### Expected behavior

* Tourpaq performs a **daily synchronization** with SkiStar.
* The sync updates **only**:
  * Allotment
  * Cost prices
* If the accommodation/room is **hidden** in Tourpaq, Tourpaq does not apply updates.
* Each SkiStar accommodation corresponds to a **Base Room Type** in Tourpaq where:\
  **Room Code = SkiStar Accommodation ID**
* If the returned currency differs from the hotel creditor currency, Tourpaq shows a **notification warning**.

### SkiStar structure

SkiStar uses the following data structure:

**Resort → Area → SubArea → Group → Accommodation**

Each **Accommodation** is a **unique unit** (house, apartment). If the accommodation is available, the free allotment is always 1.

### Mapping SkiStar data into Tourpaq

To integrate SkiStar accommodations into Tourpaq, the following structure is used:

* Each SkiStar **Hotel/Resort** is added in Tourpaq and linked using the corresponding **SkiStar Resort ID**.
* Every SkiStar **Accommodation** is created in Tourpaq as a **Base Room Type**, where:
  * **Room Code = SkiStar Accommodation ID**
* The Base Room Type is then assigned to the correct hotel in Tourpaq.

This setup ensures that each accommodation is individually represented and correctly tied to its parent resort, allowing Tourpaq to work with SkiStar’s hierarchical structure while maintaining precise allotment and availability control.

### Season logic

A SkiStar season is always: **12 December → 20 April (next year)**

The system synchronizes according to the current date:

* **21 April 2025 → 20 April 2026:** sync from _today_ until **20 April 2026**
* **From 21 April 2026:** sync from **12 December 2026 → 20 April 2027**
* And so on for future years.

This ensures that the upcoming ski season is always included.

### Company & hotel settings

For a company to have access to the SkiStar feature, a SuperAdmin will need to activate this feature for the company.

#### Enable/disable “SkiStar Sync”

Once the feature is enabled per company, additional hotel-level fields become available:

#### Hotel settings

<figure><img src="../../../.gitbook/assets/image (521).png" alt=""><figcaption></figcaption></figure>

* **Managed by: SkiStar** appears below “Managed by AvailPro”.
* **SkiStar Resort ID** is only visible when “Managed by SkiStar” is enabled.
* **Stay lengths** defines which lengths should be synced for this hotel.

<figure><img src="../../../.gitbook/assets/image (522).png" alt=""><figcaption></figcaption></figure>

* Example:
  * Sälen: `7,5`
  * Hemsedal & Trysil: `7,5,4`

These settings govern which API calls must be performed for the hotel.

Each hotel may have different stay length rules depending on the Resort.

### Daily sync process

The daily sync performs the following steps:

#### 1. Identify hotels with SkiStar Resort ID

All hotels marked “Managed by SkiStar” are included.

Currently, SkiStar uses:

* `1` = Sälen
* `4` = Hemsedal
* `5` = Trysil

#### 2. Request allotment and cost data

For each Resort ID:

1. Determine all relevant **Sundays** (departures) within the synchronization period.
2. For each Sunday, request each configured **stay length**.
3. Use SkiStar endpoint: **/BookingApi/v1/FixedPeriodProduct/Search**
4. To ensure accurate allotment for shorter stays (5 and 4 days), also retrieve data for the **preceding 7-day period**.

#### 3. Build requests per Sunday

For each resort ID, Tourpaq treats each valid Sunday as a departure day.

For each Sunday, Tourpaq requests the configured stay lengths for that hotel.

To support shorter stays (5 and 4 days), Tourpaq also retrieves data for the **preceding 7-day period** to ensure the final **allotment** is correct.

Example API load per resort:

```
≈ 18 Sundays × 3 stay lengths ≈ 54 requests per Resort per sync
```

#### 4. Retrieve accommodation results

Each response includes:

* Accommodation ID
* Pricing container
* Currency
* Availability (allotment = 1 if available)

#### 5. Cost price calculation

Tourpaq calculates the cost price using:

```
Cost = prices.gross – prices.commission + mandatoryaddonprice.gross
```

#### 6. Currency validation

If SkiStar’s currency differs from the hotel creditor currency, Tourpaq shows a **notification warning**.

#### 7. Update Tourpaq rooms

For each returned accommodation:

* Locate the room by **Room Code = Accommodation ID**

<figure><img src="../../../.gitbook/assets/image (524).png" alt=""><figcaption></figcaption></figure>

For each returned Accommodation ID, Tourpaq updates **allotment** and **cost price** for the matching room.

If the hotel room is hidden, Tourpaq does not update cost or allotment.

#### 8. Cost storage

* The synchronized cost is stored under **Hotel → Room Costs** as **“Per Room Per Stay”** type.

<figure><img src="../../../.gitbook/assets/image (525).png" alt=""><figcaption></figcaption></figure>

### Troubleshooting

* **Nothing updates:** Confirm the company feature is enabled and the hotel is **Managed by SkiStar**.
* **A single hotel does not sync:** Check the hotel has a **SkiStar Resort ID** and stay lengths set.
* **No rooms update:** Confirm Base Room Types exist and **Room Code** matches the SkiStar Accommodation ID.
* **Allotment doesn’t look right for 4/5-day stays:** Verify stay lengths and that the Sunday departures fall within the season window.
* **Currency warnings:** Confirm the hotel creditor currency and your finance process for currency conversion.

### FAQ

<details>

<summary><strong>What exactly does SkiStar Sync update?</strong></summary>

Only **allotment** and **cost prices**.

It does not create or change bookings in SkiStar.

</details>

<details>

<summary><strong>How often does the sync run?</strong></summary>

It runs once per day.

</details>

<details>

<summary><strong>Why is the free allotment always 1 in SkiStar?</strong></summary>

SkiStar models each accommodation as a unique unit.

If the unit is available, the returned free allotment is 1.

</details>

<details>

<summary><strong>How does Tourpaq match SkiStar accommodations to Tourpaq rooms?</strong></summary>

Tourpaq matches by **Room Code**.

It must equal the SkiStar **Accommodation ID**.

</details>

<details>

<summary><strong>Why don’t hidden rooms update?</strong></summary>

Hidden rooms are excluded from updates by design.

This prevents overwriting rooms you intentionally removed from sale.

</details>

<details>

<summary><strong>Why do I see a currency warning?</strong></summary>

It appears when SkiStar’s returned currency differs from the hotel’s creditor currency.

Review your currency handling before using the imported costs in finance reporting.

</details>
