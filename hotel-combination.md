# Hotel combination

### Overview

A **hotel combination** is an itinerary where the customer stays in multiple hotels in one trip.

Example: 2 nights in one hotel, then 5 nights in another.

The hotels in the itinerary must already exist in Tourpaq.

Hotel combinations **do not have their own allotments**.

They use the allotments of the itinerary hotels.

### Purpose

Sell multi-hotel packages while keeping pricing and allotments tied to the real hotels.

### Key rules

* A hotel combination is created as a “hotel”, but it behaves differently.
* The room types on the combination are **placeholder rooms**.
* You must map placeholder rooms to real hotel rooms.
* After you create a price list, you cannot change the hotels, rooms, or transports.

{% hint style="warning" %}
Create and verify room mappings and allotments before generating the price list. Afterwards, the combination setup is locked.
{% endhint %}

### Before you start

* You have created the hotels that will be part of the itinerary.
* Each itinerary hotel has room types and allotments for the needed dates.
* The transports you want to use are configured and have the right intervals.
* You have permissions to create hotels and price lists (typically an admin).

### How to set up a hotel combination

{% stepper %}
{% step %}
### 1) Create the combination hotel

Create the hotel like a normal hotel.

Enable **Hotel Combination**.

<figure><img src=".gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### 2) Add itinerary hotels and (optional) transports

Open the **Hotel Combination** tab.

<figure><img src=".gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

Add the hotels the customer will stay in.

**Order matters.** The first hotel is the check-in hotel.

Optional: assign transports. This limits the combination to the selected transports.

#### Single-hotel combinations

If you add only one hotel, you may see a ticket option:

* Enabled: show that hotel on the ticket.
* Disabled: show the “main” hotel on the ticket instead.
{% endstep %}

{% step %}
### 3) Map combination rooms to real hotel rooms

Open the **Hotel Combination Room** tab.

<figure><img src=".gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

#### Grid 1: room mapping

Map each placeholder room on the combination to a room on each itinerary hotel. Match room specs as closely as possible (beds, occupancy, etc.).

#### Grid 2: interval split (transport → hotel days)

For each transport interval, define how many nights belong to each hotel.

These splits are **predefined**. Customers cannot change the distribution.

**Example**

Transport `BLLPVK-A7-5A` has 4 intervals: 7 / 14 / 21 / 28 nights.

* Interval 1 (7 nights): 4 nights in `SIV150` + 3 nights in `AGI150`
* Interval 2 (14 nights): 7 nights in `SIV150` + 7 nights in `AGI150`
{% endstep %}

{% step %}
### 4) Create the price list

Once hotels, rooms, and transports are defined, create a **price list** for the combination.

{% hint style="danger" %}
After the price list is created, you cannot change the hotels, rooms, or transports.
{% endhint %}

If the itinerary hotels do not have enough allotment, the price list cannot be generated.
{% endstep %}
{% endstepper %}

### Troubleshooting price list generation

1. **Check itinerary hotel allotments**
   * Go to: `Hotel → Hotel (SIV150/AGI150) → Allot.`
   * Verify allotments exist for the right period and room types.
   * Verify the allotment quantity is enough for the expected sales.
2. **Check transport allotments**
   * If price list generation fails for a specific date, the transport may be missing allotment.
   * Add an allotment in **Fixed Quota**, then regenerate the price list.
3. **Check room mappings**
   * Make sure every placeholder room is mapped.
   * Missing mappings can block price list generation.
4. **Check interval splits**
   * Ensure each interval adds up to the full length.
   * Example: a 7-night interval must total 7 nights across hotels.

### Related docs

* [Hotel creation](hotel/hotel-creation/)

### FAQ

<details>

<summary>Does a hotel combination have its own allotment?</summary>

No.

The combination uses allotments from the itinerary hotels.

</details>

<details>

<summary>Can customers choose how many nights they stay in each hotel?</summary>

No.

The split per transport interval is predefined in the combination setup.

</details>

<details>

<summary>Why can’t I change hotels/rooms/transports after creating the price list?</summary>

Price lists are generated from the combination definition.

Changing the definition would invalidate the price list.

Create a new hotel combination if you need a different itinerary.

</details>

<details>

<summary>What happens if one of the itinerary hotels is sold out?</summary>

The combination is effectively sold out for that period.

The system cannot take allotment from a hotel that has none available.

</details>

<details>

<summary>Why does only one hotel show on the ticket for a single-hotel combination?</summary>

Single-hotel combinations have a ticket option.

It decides whether the itinerary hotel or the “main” hotel is shown.

</details>

<details>

<summary>How do I restrict a hotel combination to specific transports?</summary>

Assign the allowed transports on the **Hotel Combination** tab.

The combination will only be available for those transports.

</details>
