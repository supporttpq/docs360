# New Booking

## **Overview**

The **New Booking** functionality in Tourpaq allows users to create a booking by selecting a brand, adding transport and hotel options, managing passengers, and customizing extras, discounts, and supplements. It also includes advanced tools such as **passenger import** and **package product handling**.

## **Purpose**

This tool is designed to:

* Create new bookings from scratch.
* Assign transport, accommodation, and optional services.
* Manage passenger data individually or via file import.
* Apply complex product logic such as packages, extras, discounts, and insurance.

## **Preconditions**

Before creating a booking, ensure:

* You are logged in with permission to create bookings.
* All relevant products (transport, hotels, extras) are configured and active in the system.
* You have customer data ready.

<figure><img src="https://sonat.com/api/Document/Image/19670ef0-8b8a-4cda-8eb6-249681e07016/60a72aeb-a272-4428-a118-b6074b1b35b5/095769e7-32fd-4f22-8e55-e504ab071f34.webp?width=1915" alt="" width="900"><figcaption></figcaption></figure>

## **Instructions to** Create a New Booking

### **Navigation:**&#x20;

Go to **Booking menu → Click on “New Booking”**

## Steps:

### **1. Choose the Brand.**

<figure><img src="../../../.gitbook/assets/image (518).png" alt=""><figcaption></figcaption></figure>

### **2. Customer details**&#x20;

<figure><img src="../../../.gitbook/assets/image (519).png" alt=""><figcaption></figcaption></figure>

**Insert the customer’s mobile number** to identify or create a customer.&#x20;

### 3. Passengers&#x20;

<figure><img src="../../../.gitbook/assets/image (520).png" alt=""><figcaption></figcaption></figure>

**Add Passenger Count** – Select the number of:

* Adults
* Children
* Infants

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### 4. Add Transport

The **Select Transport** dialog allows the user to search for and select a transport (flight, bus, or other transport types) for the booking. It provides flexible filtering options and a detailed table showing all matching transport departures within the selected date range.

#### **Filter Section**

At the top of the dialog, users can refine the search using the following filters:

#### **Date Range**

* **From** – Start date for the search period.
* **To** – End date for the search period.\
  The system returns all transports departing between these two dates.

#### **Gateways**

* **Departure Gateway** – Filters transports that depart from a specific gateway/airport.
* **Arrival Gateway** – Filters transports that arrive at a selected gateway/airport.

#### **Transport Code**

Input for narrowing results to a specific transport code (e.g., flight code).

#### **Period**

An optional field used for searching transports based on a predefined period. Used to get transports from a specific interval.

#### **Additional Options**

* **Search waitlist also** – Includes transports that have no available allotment and are in waitlist mode.
* **Clear** – Resets all filters.

#### **Search Button**

Executes the search based on the selected filters.

#### **Transport List Table**

The lower section shows all matching transport departures. Each row represents a transport option and contains the following columns:

| Column               | Description                                                     |
| -------------------- | --------------------------------------------------------------- |
| **Status**           | Visual indicator of availability (color bar).                   |
| **Date**             | Departure date of the transport.                                |
| **Day**              | Corresponding weekday (e.g., Monday).                           |
| **Departure**        | Departure gateway/airport.                                      |
| **Arrival**          | Arrival gateway/airport.                                        |
| **Transport**        | Transport code (e.g., flight code).                             |
| **Type**             | Transport type (e.g., C, D).                                    |
| **Stay**             | Number of nights associated with that transport.                |
| **ALI 1–ALI 4**      | Allotment capacity per allotment group.                         |
| **OW OUT / OW HOME** | One-way out and one-way home availability.                      |
| **ALL. EXT. PROD.**  | Allotment Extra Product (Hover to see the number of allotments) |
| **Flight Number**    | Actual flight number (if applicable).                           |
| **Stop Sale**        | Shows if stop sale is active for this transport.                |
| **Select**           | Button used to choose this transport for the booking.           |

The table supports vertical scrolling when many departures are available.

#### **Selection**

To choose a transport:

1. Click on **Edit** in the Transport section.

<figure><img src="../../../.gitbook/assets/image (514).png" alt=""><figcaption></figcaption></figure>

2. **Select the Period** (departure/arrival range) to check availability.
3. Click **Search** to retrieve available transports.
   * Each result includes **transport allotment** and a hoverable **popup** showing extra quotas.
4.  Select the **desired transport**.

    <figure><img src="../../../.gitbook/assets/image (516).png" alt=""><figcaption></figcaption></figure>
5.  Set the **trip interval** (duration in days).&#x20;

    <figure><img src="../../../.gitbook/assets/image (517).png" alt=""><figcaption></figcaption></figure>

### 5. Add Hotel & Room

The **Select Hotel** dialog provides the user with a filtered list of available hotels, allowing quick selection based on resort, hotel, star rating, pension type, and room availability. The interface uses a combination of dropdown filters, checkboxes, and a tabular overview to help users identify suitable hotel options efficiently.

<figure><img src="../../../.gitbook/assets/image (511).png" alt=""><figcaption></figcaption></figure>

#### **Filter Options**

The top section contains multiple filters:

* **Resort** – Dropdown for selecting a specific resort or viewing _All Resorts_.
* **Hotel** – Dropdown for selecting a specific hotel or viewing _All Hotels_.
* **Stars** – Multi-select dropdown for filtering by hotel star rating.
* **Pension** – Multi-select dropdown for filtering available board types.

Additional checkboxes allow further control:

* **Show only free rooms** – Displays only rooms with availability.
* **Display all rooms** – Shows all rooms regardless of availability.
* **Display Names** – Toggles between hotel names and internal codes.
* **Display PriceList Hotel Names** – Shows the hotel names defined in the PriceList.

#### **Hotel List Table**

The main table lists hotels that match the selected filter criteria. Each row represents a hotel/room combination and displays the following information:

| Column              | Description                                                                                                                  |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **Status**          | Indicates availability status with color-coded icons.                                                                        |
| **Hotel**           | Code or name of the hotel, depending on filter settings.                                                                     |
| **Stars**           | Star classification displayed visually.                                                                                      |
| **Resort**          | Code of the resort.                                                                                                          |
| **Room**            | Room type or board type description.                                                                                         |
| **MB / XB / XB CH** | Capacity fields and Extra Bed Rules (Minimum Beds, Possible Extra Beds adults/child, Possible Extra Beds for Children Only). |
| **Avail.**          | Availability count for the selected period.                                                                                  |
| **P1**              | Price per interval 1                                                                                                         |
| **D1 / G1**         | Discount or group price per interval.                                                                                        |
| **N, D, G**         | Selection options (checkboxes) for Normal Price, Discount Price, and Group Price.                                            |
| **Magic Stick**     | Pencil icon allowing Reset Free Room Count                                                                                   |

#### **Selection**

A **Select** button in the top right corner becomes active when a hotel/room line is chosen.\
The user can confirm the selection and return to the booking flow.

<figure><img src="../../../.gitbook/assets/image (512).png" alt=""><figcaption></figcaption></figure>

#### **Workflow: Selecting a Hotel**

This workflow describes how a user interacts with the **Select Hotel** dialog to choose a hotel and room combination for a booking.

#### **1. Open the Select Hotel Dialog**

The dialog typically opens when the user clicks **Select Hotel**  in the booking flow.\
The dialog appears as an overlay containing filtering options and a list of available hotels.

#### **2. Apply Filters (Optional)**

#### **2.1 Select Resort**

* Open the **Resort** dropdown.
* Choose a specific resort or keep **All Resorts** to view all options.

#### **2.2 Select Hotel**

* Open the **Hotel** dropdown.
* Select a hotel or keep **All Hotels** to view all available hotels.

#### **2.3 Filter by Stars**

* Open the **Stars** multi-select dropdown.
* Select one or more star ratings to narrow down the results.

#### **2.4 Filter by Pension**

* Open the **Pension** multi-select dropdown.
* Choose one or more board types.

#### **2.5 Additional Filter Settings**

Use the checkboxes:

* **Show only free rooms** – displays only hotel rooms with availability above zero.
* **Display all rooms** – shows every room regardless of availability.
* **Display Names** – toggles between hotel names and codes.
* **Display PriceList Hotel Names** – shows hotel names as defined in the PriceList.

#### **3. Review the Hotel List**

The table updates automatically based on the filters. Each row displays key information:

* Hotel name or code
* Star rating
* Resort
* Room type or board type
* Extra bed rules in hotel selection (MB, XB, XB CH)
* Availability
* Pricing indicators (P1, D1, G1)
* Selection checkboxes (N, D, G)

The user scrolls or reviews the list to find the desired option.

#### **4. Select a Hotel and Room Combination**

* Click on the desired row to highlight it.
* The **Select** button becomes active once a selection is made.

#### **5. Confirm the Selection**

* Click **Select** in the upper-right corner of the dialog.
* The dialog closes, and the selected hotel and room are applied to the booking.

#### **6. Continue the Booking Process**

After the hotel is selected, the user proceeds with the remaining steps of the booking flow, such as take allotment.

#### 7. **Take Allotment** to lock the room for the booking

<figure><img src="../../../.gitbook/assets/image (513).png" alt=""><figcaption></figcaption></figure>

After the user selects **Take Allotment**, the system updates the Total Amount right away.\
The calculation includes:

* All applicable **discounts** and **supplements**
* **Auto-selected extras,** and **all extras** added manually by the user for every passenger
* **Passenger age** adjustments

***

### 6. Passenger Information

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

1. Edit **Passenger Details**:
   * Gender, First Name, Last Name, Age
2. **Add Extras**:
   * Per passenger, or use the **yellow “C” icon** to apply extras to all eligible passengers.
3. **Add Discounts/Supplements**:
   * Click **Show/Hide Discount/Supplements**
   * Click **Add Discount/Supplement**
   * Select available options for one or all passengers
   * Multiple discounts or supplements can be added simultaneously.
4. Click **Save Passenger** to save changes.

{% hint style="success" %}
The Total Amount updates instantly whenever the user modifies any passenger-related information:

* **Selecting or unselecting Supplements or Discounts** updates the Total Amount immediately.
* **Selecting or unselecting Extras** updates the Total Amount immediately.
* **Changing the passenger’s age** recalculates the price instantly based on the new age.
{% endhint %}

***

### 7.  Booking Totals

The **Booking panel** provides a quick summary of financial details, booking metadata, and status indicators for a reservation. It is used by staff to monitor pricing, profitability, and the confirmation state of related services (hotel, transfer, etc.).

The **Total Amount** always reflects the user’s latest selections. The price includes all eligible **discounts**, **supplements**, **auto-selected extras**, and any **age-based price adjustments**.

The system continuously recalculates the Total Amount as the user interacts with the booking. The displayed price always reflects the current state of the booking and does not wait for **Save Passenger** or **Save** to trigger updates.

<figure><img src="../../../.gitbook/assets/image (507).png" alt=""><figcaption></figcaption></figure>

This section provides an overview of the booking’s financial and status details. At the top, the **Total amount** field highlights the total price (7.206), applied discount (300), and resulting total (6.906), along with the **Total Profit** value (-2.094).

#### **Field Explanations**

#### **Financial Summary (Green Area)**

* **Total amount** – The final selling price of the booking (after discounts).
* **Price - Price without discounts, including extras, supplements etc.**
* **Discount** – The sum of discounts on the hotel, price list adjustment and the discounts added to each passenger.
* **Total Profit** – The margin earned after subtracting supplier costs from the selling price.

{% hint style="success" %}
The total profit is displayed when expanding the green area that shows the total amount, and it will be shown after the full booking is saved.
{% endhint %}

#### **Booking Details**

* **Booking Number** – The unique identifier for the booking. In the example: 3633 `+ 1` (the `+1` indicates a sub-booking).
* **Status** – The current state of the booking (e.g., _OK_, _Pending_, _Cancelled_).
* **User** – The system user or agent who created/owns the booking. Example: RWBTPQ.
* **Added** – The date when the booking was created.
* **Updated** – The date when the booking was last modified.

#### **Flags (Checkbox Options)**

* **Is Group Booking** – Indicates if the booking is part of a group reservation.
* **Remember Extras** – Ensures that selected extras (e.g., transport, insurance) are saved for future modifications.
* **Hotel Confirmed** – Marks whether the accommodation portion of the booking has been confirmed.
* **Transfer Confirmed** – Marks whether the transport/transfer services have been confirmed.

### 8. Finalize Booking

1. Review all details.
2. Click **Save** to complete the booking.
3. Send the ticket:
   * Click **Send Email** to send manually, or
   * Let the system auto-generate and send it.

### 9. Cancel passenger or booking

The **Cancel passenger or booking** button allows users to cancel an entire booking or remove individual passengers from a booking, depending on the situation. It is located at the bottom-right corner of the _Booking → Overview → Passengers_ section.

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

#### **Overview**

This feature gives booking administrators full control over cancellations.\
Depending on the configuration of the booking and the selected passenger, the system will:

* Cancel **one or more passengers**, or
* Cancel the **entire booking**, if all passengers are selected or if cancellation rules require a full cancellation.

The function ensures that all transport, hotel, extras, and supplements connected to the passenger(s) are removed or recalculated correctly.

#### **Purpose**

The button is used when:

* A traveler drops out of the trip
* A booking needs to be partially canceled
* A booking must be fully canceled, including all passengers and services

#### **How It Works**

#### 1. **Select Passenger(s)**

Before canceling, verify which passengers are listed in the booking:

* If **one passenger** is selected → the system cancels _only that passenger_
* If **all passengers** are selected or the booking contains only one passenger → the system offers a **full booking cancellation**

#### 2. **Click the Button**

Click on the **Cancel passenger or booking** in the bottom-right corner.&#x20;

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

#### 3. **Choose the Cancellation Type**

A dialog will appear asking:

* **Cancel Passenger**
* **Cancel Entire Booking**

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

The available options depend on the structure of the booking.

#### 4. **Confirm Cancellation**

The user must confirm in the final dialog.\
After confirmation, Tourpaq:

* Removes all services connected to the canceled passenger
* Recalculates pricing

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

* Updates allotment, transport seats, extras, and commissions.  The allotment is **not** updated automatically. If the number of passengers in the booking is not manually reduced, Tourpaq will automatically insert a **TBA passenger** to occupy the seat or room left vacant by the cancelled guest. This ensures the booking maintains its original capacity, and the cancelled space is not released back into the available allotment. This step it requires manual intervention by the sales user in Edit passenger and then in Take allotment to update it manually.
* Marks the booking or passenger as _Cancelled_

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

#### **Expected Behavior**

#### **Cancel Passenger**

The system will:

* Remove all services (transport, hotel, extras, insurance, supplements) tied to the passenger
* Update price calculations
* Preserve remaining passengers and services
* Update allotment and capacity. This step it requires manual intervention by the sales user in Edit passenger and then in Take allotment to update it manually.
  * in the Passenger box, change the number of the passengers that filled in to the booking
  * click on Take allotment
  * save booking
* Keep booking active if at least one passenger remains

#### **Cancel Entire Booking**

The system will:

* Remove all passengers and services
* Release all allotments
* Update all connected modules (Transport, Hotel, GDS, Extras, etc.)
* Mark the booking as _Cancelled_
* Trigger relevant notifications if configured

#### **Warnings & Notes**

⚠ **Cancellation rules apply**\
If cancellation rules or charges are configured for the brand, they will be applied automatically.

⚠ **Manual actions may be needed**\
If external systems (e.g., GDS, API) are used, check if manual cancellation is required outside Tourpaq.

⚠ **Bonus codes/discounts**\
Removing a passenger may change eligibility for discounts, supplements, or bonuses. Recalculation happens automatically.

### Cancellation rules

When a booking is canceled, a cancellation fee is set for each passenger. Cancellation rules are applied for calculating this fee. The fee will is calculated taking into account the remaining days left to departure.

<figure><img src="../../../.gitbook/assets/image (556).png" alt=""><figcaption></figcaption></figure>

Cancellation fee on a booking is calculated as follows:

If a cancellation insurance is paid, when cancelling the passengers we can opt that the cancellation insurance will cover or not cover the booking.

If the cancellation insurance is paid and Cover option is selected when cancelling the booking, the amount of the cancellation fee will be the cancellation insurance.

If the cancellation insurance is paid and Does not Cover option is selected when cancelling the booking, the cancellation fee will contain the price of the cancellation insurance and the amount set in cancellation rules.

Infants do not get cancellation fee.

You can also adjust the cancellation amount applied to the booking. This can be done by selecting **Edit Passenger** and then updating the value under **Total per passenger**. This allows you to manually modify the cancellation fee when needed.

<figure><img src="../../../.gitbook/assets/image (557).png" alt=""><figcaption></figcaption></figure>

## **User Experience**

Users always see the correct Total Amount without needing to save the passenger or the booking.\
This live update behavior ensures:

* Accurate and transparent pricing
* Immediate feedback when modifying selections
* A smoother and more predictable booking process

The system provides a responsive and reliable pricing experience, matching the user’s actions in real time.

## Import Passengers (Optional)

You can import multiple passengers via an Excel file.

#### Accepted File Format:

* Only **Excel files (.xlsx)** are supported.
* Required static columns:
  * `TITLE`, `F NAME`, `L NAME`, `DATE OF BIRTH`
* Optional static columns:
  * `CCL. INS.`, `INSURANCE`
* **Dynamic columns**:
  * Each column must match the **Extras Category Name**
  * Values must be **Extras Codes**

#### Behavior:

* If import **fails**: all changes are reverted.
* If import **succeeds with warnings**:
  * Rows are **highlighted**.
  * Hover over **info icon** to view warning tooltips.

**⚠️ Common Warnings:**

* Selected extra is unavailable for that category.
* Cancellation or travel insurance cannot be selected.
* The category does not support multi-select (only first value used).

## **Static Columns**

The columns **TITLE**, **F NAME**, **L NAME**, and **DATE OF BIRTH** **must always** be included in the import file and must match the exact names specified. The optional columns **CCL. INS.** and **INSURANCE** may be included if applicable but are not required.

| **Column Name**   | **Description**                                                                       |
| ----------------- | ------------------------------------------------------------------------------------- |
| **TITLE**         | The title of the passenger. This must be a value selected from a dropdown list.       |
| **F NAME**        | The first name of the passenger. Any string value is acceptable.                      |
| **L NAME**        | The last name of the passenger. Any string value is acceptable.                       |
| **DATE OF BIRTH** | The passenger’s date of birth in the format `dd-mm-yyyy`.                             |
| **CCL. INS.**     | The cancellation insurance for the passenger. This should be a value from a dropdown. |
| **INSURANCE**     | The travel insurance code for the passenger. This should be a value from a dropdown.  |

## **Dynamic Columns (Extras)**

Dynamic columns allow additional optional information about passenger extras. Each dynamic column corresponds to an **Extras Category Name** (case-insensitive) and requires the corresponding **Extras Code** value.

| **Extras Category Name**                      | **Extras Code**                                                                               |
| --------------------------------------------- | --------------------------------------------------------------------------------------------- |
| **Extras Category Name (as in table header)** | The code(s) selected from the dropdown, separated by commas (optional). It can be left empty. |

**Usage:**

| Column Name           | Value                            |
| --------------------- | -------------------------------- |
| **EXTRAS\_CATEGORY1** | **EXTRAS\_CODE**                 |
| **EXTRAS\_CATEGORY2** | **EXTRAS\_CODE1, EXTRAS\_CODE2** |
| **EXTRAS\_CATEGORY3** |                                  |

## **Import Behavior**

1. **If the import fails:**
   * All changes to the passengers will be **reverted**.
2. **If the import succeeds but contains warnings:**
   * Rows with warnings will be **highlighted** with a specific color.
   * An **info icon** will appear for these rows, displaying all warnings as a tooltip.
   * Common warnings include:
     * The selected category is not available for selection.
     * The selected extra is not available for the category.
     * Cancellation insurance is not available for selection.
     * Travel insurance is not available for selection.
     * This category does not support multiselect. Only the first value from the list will be selected.

![](https://docs.tourpaq.com/assets/images/row_with_warnings-19946acdb755f600a02305f2edcef55e.png?width=1754)

An example file for importing passengers can include columns in the following format:

|       |        |        |               |           |           |                       |                        |
| ----- | ------ | ------ | ------------- | --------- | --------- | --------------------- | ---------------------- |
| TITLE | F NAME | L NAME | DATE OF BIRTH | CCL. INS. | INSURANCE | Morgenmad på værelset | BAGGAGE                |
| MR    | TBA1   | TBA1   | 19-11-1988    | 399       |           | MESS\_EX              | BAG-20, BAG-30, BAG-40 |
| MS    | TBA2   | TBA2   | 03-01-1926    |           | AUS       |                       | BAG-20                 |

## **Package products**

When selecting a product that is flagged as a package for a passenger, all the products that are inside the package will be selected after saving the passenger, but with a price of 0, only the package will have the price set.

For a product to be set as package, you need to check the option inside **Edit Product Page** -> **Basic Setup** -> **Other Settings** -> **Package Type**

![](https://docs.tourpaq.com/assets/images/package_and_product_example-fb064df3c22226835850f8ad23aef525.png?width=1645)

For a product to be set as a content type of a package, you need to check the option inside **Edit Product Page** -> **Basic Setup** -> **Other Settings** -> **Content Type**

![](https://docs.tourpaq.com/assets/images/package_and_product_example-fb064df3c22226835850f8ad23aef525.png?width=1645)

You can modify the products that are inside the package inside **Edit Product Page** -> **Package Content** tab

![](https://docs.tourpaq.com/assets/images/package_and_product_example3-83e4c48b16f44d9028b8a8ffcff1d567.png?width=1665)

<mark style="color:red;">**Warning messages**</mark>

* If you select the package, you can't select the products inside the package as well, as you will get a warning message that looks like this one:

![](https://docs.tourpaq.com/assets/images/package_and_product_warning-ecd616e463d185d98ad5ac65be13b1a3.png?width=1797)

* All the products inside the package have to be eligible so that the package can be selected. If they are not all eligible, you will get this warning message:

![](https://docs.tourpaq.com/assets/images/package_and_product_warning_2-182f4c506926ede24ffbcb6c77f7a3c9.png?width=1809)
