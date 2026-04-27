---
description: New Booking → Search
---

# Booking Search – Room Allocation Support

### Overview

The **Booking Search** functionality now supports **room allocation without requiring a hotel to be selected**.

This aligns Booking Search with the existing behavior in **Offer Search**, allowing users to define room distributions upfront and retrieve matching results across all hotels.

{% hint style="info" %}
This enhancement removes a key limitation that previously required users to select a hotel before defining room allocation.
{% endhint %}

***

### Customer Outcome

Users can:

* Search using **room allocation directly**
* Avoid manual hotel-by-hotel filtering
* Handle **family and mixed occupancy bookings faster**
* Use Booking Search as a full replacement for Offer Search in most scenarios

***

### Functional Behavior

#### Room Allocation Without Hotel Selection

Room allocation is now available even when:

* No hotel is selected

<figure><img src="../../../../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

**System behavior:**

* Searches across all hotels
* Filters only results that match:
  * Occupancy distribution
  * Room configuration

***

#### Rooms No Field

The **Rooms No** field controls how many rooms are included in the allocation.

<figure><img src="../../../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Rules:**

* Always editable
* Minimum value: 1
* Changing the value:
  * Dynamically updates room rows

**Behavior:**

| Value      | Result                   |
| ---------- | ------------------------ |
| 0 or empty | Room allocation disabled |
| ≥ 1        | Room allocation enabled  |

{% hint style="success" %}
Room allocation becomes active only when Rooms No is set.&#x20;
{% endhint %}

<figure><img src="../../../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

#### Room Allocation Input

Each room includes:

* Room type (e.g. 2BR, 2/2/2)
* Adults
* Child ages
* Infants

**Rules:**

* Total passengers must match overall passenger selection
* Child ages must be valid (non-empty if children exist)
* Allocation is used directly in search filtering

<figure><img src="../../../../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

#### Room Column Behavior

| Scenario          | Behavior  |
| ----------------- | --------- |
| No hotel selected | Read-only |
| Hotel selected    | Editable  |

**Explanation:**

* Without hotel:
  * Room types are system-driven
* With hotel:
  * Room types reflect hotel configuration

***

#### Search Execution

When the user clicks **Search**:

The system evaluates:

* Room allocation
* Passenger distribution
* Travel dates
* Transport
* Board

**Result:**

* Only valid combinations matching the allocation are returned

***

### UI Behavior

* Rooms No → always editable
* Room rows → dynamically generated
* Room column:
  * Disabled when no hotel is selected
  * Enabled when the hotel is selected
* Allocation fields:
  * Always visible when Rooms No ≥ 1

***

### Validation Rules

| Rule               | Behavior              |
| ------------------ | --------------------- |
| Rooms No not set   | Disable allocation    |
| Passenger mismatch | Show validation error |
| Missing child ages | Block search          |
| Invalid occupancy  | Exclude results       |

{% hint style="info" %}
Validation is enforced before search execution.
{% endhint %}

***

### Example Scenarios

#### Example 1

**Input:**

* Rooms No: 2
* Room 1: 1 adult + 1 child (age 4)
* Room 2: 1 adult + 1 child (age 8)
* No hotel selected

**Result:**

* System returns:
  * All hotels matching this distribution
  * Valid transport + stay combinations

<figure><img src="../../../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Example 2:

**Input:**

* Hotel selected: BCN\_HO
* Rooms No: 2
* Room 1 (2BR): 1 adult + 1 child (age 4)
* Room 2 (2/22): 1 adult + 1 child (age 8)

**Result:**

* System returns:
  * All rooms distribution for the specific hotel
  * Valid transport + stay combinations

<figure><img src="../../../../.gitbook/assets/image (6) (1) (1).png" alt=""><figcaption></figcaption></figure>

