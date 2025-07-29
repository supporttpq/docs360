# New Booking search support

### **Overview**

The **Search** page is the starting point for creating a new booking in the Tourpaq Office system. It enables users to search and match available **flights** and **hotels** based on specific travel criteria, such as departure dates, destination, hotel, budget, and stay duration. The page combines filtering and sorting tools with live availability data to help tour operators quickly identify matching options and initiate a booking.

***

### **Purpose**

The purpose of this interface is to:

* Provide travel package suggestions based on user-defined filters.
* Display all possible **flights** and **hotels** combinations.
* Enable direct booking initiation from matching hotel results.
* Compare availability, stay durations, pricing, and discounts efficiently.

***

### **Preconditions**

Before using this screen, the following conditions must be met:

* A Tourpaq Office user account with booking rights must be used.
* Price lists and allotments must be configured for the hotels and transports to return availability.
* System date and departure data should be up to date.
* Custom workflows must be defined if you want to filter by different booking flows (e.g., Charter & Dynamic).

***

### **Workflow and Expected Results**

| **Step** | **Action**                                          | **Expected Result**                                                                                                                                                                                           | Example                                                                                                         |
| -------- | --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| 1        | Login as user                                       | Login is performed successfully                                                                                                                                                                               |                                                                                                                 |
| 2        | Click "New Booking" and select a Brand              | New booking page is displayed                                                                                                                                                                                 | <div><figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure></div> |
| 3        | Click "Search" in the Passengers section            | Warning: _"You must configure the number of passengers in order to access the search!"_                                                                                                                       |                                                                                                                 |
| 4        | Enter value for _Adults_ only, then click "Search"  | Search page is displayed                                                                                                                                                                                      | <div><figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure></div> |
| 5        | Click "Search" without entering travel criteria     | <p>Validation warnings:<br>– <em>Please select a departure...</em><br>– <em>Please select at least one of the following: arrival, resort or hotel!</em><br>– <em>Please fill in the departure dates!</em></p> | <div><figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure></div> |
| 6        | Fill in: Adults, Departures, Arrivals, Date From/To | Mandatory fields are populated                                                                                                                                                                                | <div><figure><img src="../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure></div> |
| 7        | Verify additional fields in Passengers section      | Fields shown: Child ages, Infants, Workflow, Display names checkbox, Travel Length, Resort, Hotel, Budget (max), Stars, Clear, Show availability                                                              |                                                                                                                 |
| 8        | Click "Search"                                      | Flights and Hotels lists are displayed                                                                                                                                                                        | <div><figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure></div> |
| 9        | Verify columns in _Flights_ section                 | Columns: Departure, Arrival, Date, Day, Transport, Interval 1–4                                                                                                                                               |                                                                                                                 |
| 10       | Check if columns in _Flights_ section are sortable  | All listed columns are sortable                                                                                                                                                                               |                                                                                                                 |
| 11       | Select a flight row                                 | "Clear selected row" button appears                                                                                                                                                                           | <div><figure><img src="../../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure></div> |
| 12       | Click "Clear selected row"                          | Row is unselected, button disappears                                                                                                                                                                          |                                                                                                                 |
| 13       | Click "+ Filters" in Flights section                | Filters displayed: Departure, Arrival, Date from, Date to                                                                                                                                                     | <div><figure><img src="../../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure></div> |
| 14       | Verify "- Filters" view in Flights                  | Contains "Clear" button                                                                                                                                                                                       |                                                                                                                 |
| 15       | Verify columns in _Hotels_ section                  | Columns: Hotel, Stars, Resort, Int., Stay, Room type, Avail., Date, Price PA, Price PC, Normal Price, Discount, Discount Price                                                                                |                                                                                                                 |
| 16       | Click "+ Filters" in Hotels section                 | Filters displayed: Hotel categories, Hotel facilities, Board supplement                                                                                                                                       | <div><figure><img src="../../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure></div> |
| 17       | Verify "- Filters" view in Hotels                   | Checkboxes: Show only free rooms, Price per pax incl. extras; also contains "Clear" button                                                                                                                    |                                                                                                                 |
| 18       | Verify display mode buttons in Hotels section       | Buttons: "Pagination & Sorting" (default), "More/Less"                                                                                                                                                        |                                                                                                                 |
| 19       | Switch to "More/Less"                               | Pagination removed, sorting disabled                                                                                                                                                                          |                                                                                                                 |
| 20       | Click "+ More"                                      | More than 3 records for a hotel are shown                                                                                                                                                                     |                                                                                                                 |
| 21       | Click "- Less"                                      | Display returns to 3 records per hotel                                                                                                                                                                        |                                                                                                                 |
| 22       | Hover over eye icon in Hotels                       | Tooltip "View details" is displayed                                                                                                                                                                           | <div><figure><img src="../../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure></div> |
| 23       | Select a hotel record                               | Buttons: "Create booking" and "Clear selected row" are shown                                                                                                                                                  | <div><figure><img src="../../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure></div> |
| 24       | Click "Clear selected row"                          | Buttons disappear                                                                                                                                                                                             |                                                                                                                 |

#### Creating a Booking

When the **Create Booking** button is clicked, a new page will open, pre-filled with all previously selected information. From this point forward, the process for completing the booking follows the standard steps used for creating any new booking.

<figure><img src="../../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

### **Instructions & Field Descriptions**

<figure><img src="../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

#### **Search Filters (Top Section)**

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

#### **Flights Table (Top Grid)**

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

#### **Hotels Table (Bottom Grid)**

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
* **More/Less**: Expands or collapses additional hotels with the same filters category

***

### **Next Steps After Search**

1. Select the preferred **flight** from the upper table.
2. Choose a suitable **hotel** row.
3. Hover over the row to reveal the **Create booking** button.
4. Click **Create booking** to proceed with booking creation using the selected transport and hotel offer.
