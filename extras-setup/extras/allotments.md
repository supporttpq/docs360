# Allotments

## **Manual Allotments**

<figure><img src="../../.gitbook/assets/image (412).png" alt=""><figcaption></figcaption></figure>

#### Overview

This feature is usually used for **products available at the destination** (e.g., excursions, events, or additional services). Extra allotments allow you to manage availability for these products independently from the main hotel or transport allotments.

#### Functionality

* The user can generate allotments using a **simple generator**, making it easy to define when the product is available.
* In the **booking module**, the system will display the product as **available** if:
  * The booking’s arrival and departure dates fall within the extra allotment period.
  * There is still allotment left (i.e., availability has not been fully consumed).

#### How to Create Extra Allotments

1. **Navigate to the Allotments Tab**
   * Go to: _Extras Setup → Extras_&#x20;
   * Select the product you want to manage.
   * Open the **Allotments** tab.
2.  **Generate New Allotments**

    * Press the **Generate New Allotments** button in the upper-right corner.
      *   Select a type (Daily or Weekly) when the product should be available.

          * If the type is set to Daily, it needs to follow the next steps:

          <figure><img src="../../.gitbook/assets/image (414).png" alt=""><figcaption></figcaption></figure>

          &#x20;\- Frequency - every X days

          * Start date - date when the allotment will be generated
          * End date - date when the allotment will end
          * Allotment - how many allotments will be generated daily &#x20;
          * If the type is set to Weekly:

          <figure><img src="../../.gitbook/assets/image (413).png" alt=""><figcaption></figcaption></figure>

          * Frequency - every X weeks. It requires to set at least one day or all day
          * Start date - date when the allotment will be generated
          * End date - date when the allotment will end
          * Allotment - how many allotments will be generated weekly

    After all the fields are set - click to Genarate.
3. Allotments table view

*   **Change values selector -** checkbox - enable bulk editing. Allow to make changes to the following columns:

    * Allotment - change the actual allotment's value with a new value (+, -, or =) inserted in the Value field
      * **Day** – Moves all bookings from the selected day to another day. The new day can be either earlier or later in the schedule. Use this option to shift all bookings forward or backward to a different date as required.

    There are two options available:

    1. **Move to weekday (forward)** – Move bookings to the next available weekday.
    2. **Move to weekday (backward)** – Move bookings to a previous available weekday.

    &#x20;        \- The system will only enable the action if all selected bookings meet the requirements. A list of available weekdays will appear.

    &#x20;        \- Only weekdays that exist for **all selected lines** will be shown.

    * Example: If you select Tuesday, then all Tuesday lines must be followed by a Friday line for Friday to be selectable.

    &#x20;           \- Select the new weekday.

    .

    <figure><img src="../../.gitbook/assets/image (415).png" alt=""><figcaption></figcaption></figure>

    &#x20;        \- The system checks if all bookings are eligible to move.

&#x20;                \- Once confirmed, bookings are reassigned to the new weekday.

&#x20;                 \- The table updates automatically, showing the new **Booked** figures

* Block - all the selected lines will block the allotments
* **Date** – Each row represents a date for which allotment is available.
* **Day** – The day of the week is displayed automatically.
* **Allotment** – Number of units available for that date.
* **BO1** – (Booked Out 1 Interval) Displays the number of units already booked.
* **Block** – Check this box if you want to block allotment for that date.

4. **Filter & Manage Allotments**

* Use **Start date / End date** filters to display specific periods.
* Use **Week Days** to filter by specific days (e.g., only Saturdays).
* Use **Show hidden** if some allotments are hidden from the list.
* **Display / Clear** allows you to manage the current view.

5. **Save & Apply**

* Any changes made (e.g., adjusting allotment numbers or blocking dates) will be saved automatically and reflected in the booking system.

## **Linked to transport Allotments**

#### Overview

**Linked to Transport Allotments** are used for **products available only on transport** (e.g., luggage, catering, onboard services). Unlike standard Extra Allotments, these are directly tied to a transport departure and can only be booked by passengers traveling on that specific transport.

This ensures that products with limited supply or availability for certain departure dates are managed correctly.

#### How It Works

* Allotments are linked to transport departure dates.
* The system checks for availability based on the **departure interval** set for the transport.
* Products will be displayed as available in bookings only if:
  * The passenger is traveling on the linked transport.
  * Allotment is still available for the selected interval.

#### Setup Instructions

1. **Create a New Extra**
   * Go to: _Extras → Create New Extra_.
   * Fill in the product details.
   * Under **Allotment Type**, select **Linked to Transport**.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

2. After the general settings have been set, and the extras saved, the next step is setting the brand and establishing the prices and resources.&#x20;
3. At the **Resource** tab, a must is setting the **Transport** filter.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

4. The next step is setting up the allotments.

* Navigate to the **Allotments Tab** for the extra.
* Press **Generate New Allotments**.
* Define the period, interval, and availability that should match the transport departure dates.

<figure><img src="../../.gitbook/assets/image (416).png" alt=""><figcaption></figcaption></figure>

* Fields:

| AI1        | Allotment 1 Interval                                |
| ---------- | --------------------------------------------------- |
| AI2        | Allotment 2 Interval                                |
| AI3        | Allotment 3 Interval                                |
| AI4        | Allotment 4 Interval                                |
| AOT        | Allotment Out Total                                 |
| AHT        | Allotment Home Total                                |
| Transport  | Transport for which the allotment will be genearted |
| Fix quotas | Select the fix quota for the allotment generation   |

Note! The extra allotments are set up as the transport allotments. The allotment must be edited by a user, or overbookings may happen.

#### Interface and Fields

When defining **Linked to Transport Allotments**, the system displays a table with all transport departures for the selected period.

<figure><img src="../../.gitbook/assets/image (417).png" alt=""><figcaption></figcaption></figure>

**Filters (Top Section):**

* **Transport** – Select the transport to which the extra is linked.
* **Start date / End date** – Define the active period for the allotment.
* **Week Days** – Select which days of the week allotments should apply.
* **Show hidden** – Displays hidden rows if enabled.
* **Display / Clear** – Quick actions for showing or clearing generated allotments.

**Table Columns:**

* **Transport** – The transport code (e.g., _BLLAYT-D3M_).
* **Date** – Departure date of the transport.
* **Day** – Day of the week for the departure.
* **AI1, AI2, AI3, AI4** – Allotments for different categories of extras (e.g., adult items, premium items).
* **AOT (Allotment Out Total)** – Total number of allotments available.
* **AHT (Allotment Home Total)** – Total number of home allotments
* **BO1, BO2, BO3, BO4** – Booked out for interval 1-4.
* **BOT (Booking Out Total)** – Total booked allotments.
* **BHT (Booking Home Total)** – Total number of booked out allotments.
* **FO1, FO2, FO3, FO4** – Free out allotments (remaining availability for each intervals).
* **Block** – Checkbox to block allotment for a specific departure date.

#### **Calculation for Allotment:**

* Calculation for TOTAL OUT - The Total Out is calculated as a sum from the departures: TO = AI1 + AI2 + AI3 + AI4

#### **Move bookings**

The **Move Bookings** functionality allows you to transfer all bookings for an extra (e.g., excursion) from one weekday to another. This is useful when the planned day of an excursion changes and bookings must be rescheduled to a different weekday.

<figure><img src="../../.gitbook/assets/image (418).png" alt=""><figcaption></figcaption></figure>

#### Purpose

* To **reschedule extras** when the weekday changes (e.g., excursion originally on Tuesday moved to Friday).
* To ensure **all affected bookings are updated consistently** in the system.
* To prevent errors by enforcing rules that guarantee eligibility and data consistency.

#### Instructions

#### Step 1: Select the Bookings

* Go to the **Extras → Allotments/Bookings view**.
* Use the **Change Value** tool to select the booking lines you want to move.
* Only bookings from the **same weekday** can be moved together.

#### Step 2: Choose Move Action

There are two options available:

1. **Move to weekday (forward)** – Move bookings to the next available weekday.
2. **Move to weekday (backward)** – Move bookings to a previous available weekday.

* Select the desired action from the menu.
* The system will only enable the action if all selected bookings meet the requirements.

#### Step 3: Select the New Weekday

* A list of available weekdays will appear.
* Only weekdays that exist for **all selected lines** will be shown.
  * Example: If you select Tuesday, then all Tuesday lines must be followed by a Friday line for Friday to be selectable.
* Select the new weekday.

#### Step 4: Confirm and Apply

* The system checks if all bookings are eligible to move.
* Once confirmed, bookings are reassigned to the new weekday.
* The table updates automatically, showing the new **Booked** figures

#### System Behavior

* **Booking History:** Each moved booking is logged in the booking history.
* **Customer Communication:** No automatic message is sent to the customer.
  * If customers need updated tickets, this must be handled manually.
* **Data Update:**
  * The system updates allotments and booking figures immediately.
  * Only eligible bookings are moved; ineligible ones remain unchanged

✅ This ensures excursions can be rescheduled without canceling and rebooking customers, while maintaining full traceability in the system.

Special case for extras that are from a category that has the **"link to column in transport"** enabled

For these extras, the allotment total and calculation are also displayed on the transport selection pop-up in the booking process. All extras linked to the transport will be taken into consideration when displaying the total, no matter if there are more from the same category or different categories.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/LinkedToTransport-9c2183e4a9db0582d6849ed7fee00404.png" alt=""><figcaption></figcaption></figure>

### **One way usage**

For ONE-WAY flights, another extra is required, as extras are not available for ONE-WAYS unless a specific action is taken, an action that will invalidate the extra for CHARTER flights.
