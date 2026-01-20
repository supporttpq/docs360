# New Booking search support

### Overview

The **Search** page is the starting point for creating a new booking in the Tourpaq Office system. It enables users to search and match available **flights** and **hotels** based on specific travel criteria, such as departure dates, destination, hotel, budget, and stay duration. The page combines filtering and sorting tools with live availability data to help tour operators quickly identify matching options and initiate a booking.

***

### Purpose

This interface helps you:

* Provide travel package suggestions based on user-defined filters.
* Display all possible **flight + hotel** combinations.
* Enable direct booking initiation from matching hotel results.
* Compare availability, stay durations, pricing, and discounts efficiently.

***

### Preconditions

Before using this screen, the following conditions must be met:

* You must be signed in with a Tourpaq Office account that has booking rights.
* Price lists and allotments must be configured for the hotels and transports to return availability.
* System dates and departure data should be up to date.
* Workflows must be configured if you want to filter by workflow (for example, **Charter & Dynamic**).

***

### Workflow and expected results

{% stepper %}
{% step %}
### Start a new booking

1. Click **New Booking**.
2. Select a **Brand**.

New booking page is displayed.

<figure><img src="../../../.gitbook/assets/image (10) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Open Search

In the **Passengers** section, click **Search**.

The Search page can be opened without filling in the number of passengers in the booking window.
{% endstep %}

{% step %}
### Enter travel criteria (required)

Required inputs:

* **Departure**
* At least one of **Arrival**, **Resort**, or **Hotel**
* **Date from** and **Date to**

If something is missing, you will see validation warnings.

<figure><img src="../../../.gitbook/assets/image (12) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Run the search

Fill the main fields (Adults, Departures, Arrivals, Date From/To), then click **Search**.

<figure><img src="../../../.gitbook/assets/image (13) (1) (1).png" alt=""><figcaption></figcaption></figure>

Flights and hotels load as two result grids.

<figure><img src="../../../.gitbook/assets/image (14) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Review flight results (top grid)

You can sort all visible flight columns.

Common columns:

* Departure, Arrival, Date, Day
* Transport
* Interval 1–4

Select a flight row to enable **Clear selected row**.

<figure><img src="../../../.gitbook/assets/image (15) (1).png" alt=""><figcaption></figcaption></figure>

Use **+ Filters** for flight filters.

<figure><img src="../../../.gitbook/assets/image (16) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Review hotel results (bottom grid)

Hotel rows show hotel, stay, availability, and prices.

Use **+ Filters** for advanced hotel filters.

<figure><img src="../../../.gitbook/assets/image (17) (1).png" alt=""><figcaption></figcaption></figure>

You can switch the display mode:

* **Pagination & Sorting** (default)
* **More/Less** (no pagination, no sorting)

Hover the eye icon to see **View details**.

<figure><img src="../../../.gitbook/assets/image (18) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Create the booking

Select a hotel row to show actions.

You will see **Create booking** and **Clear selected row**.

<figure><img src="../../../.gitbook/assets/image (19) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

#### Relevant Prices Shown in Search Results

When a search is performed, all displayed prices represent **relevant and accurate values** for the booking. Each price field has a specific definition:

* **Price PA (Price per adult)**

Shows the **average discounted price per adult**, calculated from the booking’s discount price.

* **Price PC (Price per child)**

Shows the **average discounted price per child**.\
If the booking does not include children, this value is **0**.

* **Normal price**

Displays the **full, undiscounted price** of the booking.\
This amount still includes any **auto-selected supplements**, and matches the "normal price" shown on the presentation website.

* **Discount**

Shows the **total value of all discounts** applied to the booking.\
This includes:

1. The difference between P-price and D-price
2. All additional discounts applied to the booking

This value aligns with the discount information shown on the presentation website.

* **Discount price**

Displays the **final discounted price** for the booking.\
It includes:

1. All discounts
2. All supplements (including auto-selected ones)
3. All required Extras
4. Any relevant optional Extras

This price matches the discounted booking price shown on the presentation website.

{% hint style="info" %}
**Important:** The Search page uses an updated **Discount price** calculation. The value should match the presentation site.
{% endhint %}

#### Creating a Booking

When you click **Create booking**, a new page opens. It is pre-filled with the selected flight and hotel. From there, you complete the booking using the standard booking flow.

<figure><img src="../../../.gitbook/assets/image (20) (1).png" alt=""><figcaption></figcaption></figure>

### Instructions and field descriptions

<figure><img src="../../../.gitbook/assets/image (21) (1).png" alt=""><figcaption></figcaption></figure>

#### Search filters (top section)

| **Field**                 | **Description**                                                                                                                           |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Adults / Child ages**   | Define number of adults and ages of children for accurate price and room matching.                                                        |
| **Workflow**              | Selects the type of booking workflow (e.g., "Charter & Dynamic"). Filters transport and hotel offers based on workflow-specific settings. |
| **Display Names**         | Option to show or hide internal or display-friendly hotel/transport names.                                                                |
| **Departures / Arrivals** | Define origin and destination airport codes. Multiple arrivals can be selected.                                                           |
| **Date from / Date to**   | The date range within which travel must begin.                                                                                            |
| **Travel length**         | Filters by stay duration (e.g., 1–7 days, 7–14 days).                                                                                     |
| **Resort / Hotel**        | Refines results by destination resort or specific hotel code.                                                                             |
| **Rooms no.**             | Filters hotels that support a specific number of rooms.                                                                                   |
| **Budget (max)**          | Filters hotels based on the maximum price per person.                                                                                     |
| **Stars**                 | Filters based on hotel star rating.                                                                                                       |
| **Clear**                 | Resets all filters to default.                                                                                                            |
| **Show availability**     | Ensures only results with actual availability are shown.                                                                                  |
| **Search (Button)**       | Executes the search using the defined filters.                                                                                            |

***

#### Flights table (top grid)

This section lists flights that match the search criteria:

| **Column**       | **Description**                                                                                          |
| ---------------- | -------------------------------------------------------------------------------------------------------- |
| **Departure**    | Airport code where the flight departs from (e.g., BLL).                                                  |
| **Arrival**      | Airport code for the destination (e.g., BCN).                                                            |
| **Date**         | Flight departure date.                                                                                   |
| **Day**          | Weekday of the departure.                                                                                |
| **Transport**    | Internal code representing the transport offer and its duration.                                         |
| **Interval 1–4** | Allotment and capacity-related intervals, often representing available seats per week group or category. |

***

#### Hotels table (bottom grid)

This grid displays hotel options based on the search:

| **Column**                   | **Description**                                                                                                           |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Hotel**                    | Internal hotel code (e.g., BCN\_HO).                                                                                      |
| **Stars**                    | Hotel rating (1 to 5 stars).                                                                                              |
| **Resort**                   | Destination resort code (e.g., BCN, ADEJ).                                                                                |
| **Int.**                     | Interval group the hotel offer belongs to (links to flight intervals).                                                    |
| **Stay**                     | Number of nights included in the hotel stay.                                                                              |
| **Room Type**                | Description of the available room(s), including bed configuration.                                                        |
| **Avail.**                   | Remaining available rooms for the selected date.                                                                          |
| **Date**                     | Check-in date for the hotel stay.                                                                                         |
| **Price P.A.**               | Price per adult (typically in local currency).                                                                            |
| **Price P.C.**               | Price per child.                                                                                                          |
| **Normal Price**             | Regular price without discounts (struck-through if discounted).                                                           |
| **Discount**                 | Applied discount amount.                                                                                                  |
| **Discount Price**           | Final price after discounts.                                                                                              |
| **Create booking (tooltip)** | Appears on hover over a hotel row. Clicking it initiates the booking process for the selected flight + hotel combination. |

Additional UI Elements:

* **+ Filters**: Allows advanced filtering for both flights and hotels.
* **Clear selected row**: Deselects a previously selected hotel row.
* **Pagination & Sorting**: Toggle between paginated view and sorting/filtering controls.
* **More/Less**: Expands or collapses additional results for the same hotel.

***

### Next steps after search

1. Select the preferred **flight** from the upper table.
2. Choose a suitable **hotel** row.
3. Hover over the row to reveal the **Create booking** button.
4. Click **Create booking** to proceed with booking creation using the selected transport and hotel offer.

***

### FAQ

#### Why do I get validation messages when I click **Search**?

You are missing one or more mandatory inputs:

* **Departure**
* At least one of **Arrival**, **Resort**, or **Hotel**
* **Date from** and **Date to**

Fill those fields, then run the search again.

#### What does **Show availability** do?

It hides options that have no availability right now.

Use it when you want only bookable results.

Disable it when you are troubleshooting setup.

#### Why are no flights or hotels shown?

Most cases are configuration-related:

* No valid price list for the period.
* No allotment (or it is sold out) for the selected criteria.
* Filters are too strict (stars, resort/hotel, workflow, travel length, budget).

Try widening filters and disable **Show availability** to verify setup.

#### What does **Display names** do?

It toggles between internal codes and display-friendly names.

Use it if you need to match what customers see.

#### What does **Interval (Int.)** mean in the results?

It groups flights and hotels that can be combined together. It is typically tied to allotment or week groups.

If a hotel line shows `Int. 2`, it is meant to match flights in the same interval group.

#### What’s the difference between **Pagination & Sorting** and **More/Less**?

* **Pagination & Sorting**: paging is on and sorting is enabled.
* **More/Less**: paging is off and sorting is disabled.

Use **More/Less** when you want to expand the same hotel quickly.

#### Why can’t I click **Create booking**?

Common reasons:

* You have not selected a flight row (required in most setups).
* The selected hotel line has no availability.
* Your user role does not have rights to create bookings for the selected brand/workflow.

#### Why is **Price PC** shown as `0`?

It means the search is currently pricing without children.

Add child ages in **Passengers** to get a child price.

#### What’s the difference between **Normal price** and **Discount price**?

* **Normal price** is the undiscounted total. It can still include auto-selected supplements.
* **Discount price** is the final total after discounts. It includes relevant extras and supplements.

#### Why does **Price PA / Price PC** look “too low” compared to totals?

Price PA/PC are averages per passenger type.

They are derived from the booking totals.

Totals can also include supplements and extras.

#### How do I reset all filters quickly?

Use **Clear** in the filter area.

If you opened **+ Filters**, use its **Clear** button too.

#### Can I select multiple arrivals?

Yes. You can select multiple **Arrivals**.

This broadens transport matches and package combinations.

#### Why does changing **Travel length** remove results?

Travel length must match what is configured in the price list.

If no products exist for that stay length, you will get no results.

#### Why does switching **Workflow** remove results?

Workflow filters the set of allowed transports and hotels.

If that workflow is not configured for the selected brand/period, results can disappear.

#### Why does **Discount price** differ from the presentation site?

The **Discount price** in Search should match the presentation site when:

* Brand, workflow, travel length, and passenger ages match.
* Auto-selected supplements and required extras are configured consistently.

If you still see a mismatch, the usual cause is different product/rule configuration between channels.
