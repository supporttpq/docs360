# Profit margin rules

Under **Price List → Profit Margin Rules**, users can define rules to set profit margin values in price lists.

### Overview

The **Profit Margin Rule** feature defines how profit margins are calculated for different combinations of transport types, destinations, and stay lengths.\
The feature introduces more flexibility, allowing agencies to configure profit margins at multiple levels — global, resort, and transport — with dynamic combinations of departure gateways and stay lengths.

This enables the **automatic creation of a large number of price lists**, drastically **reducing manual work** and improving efficiency in price list generation and maintenance.

The **Profit Margin Rules** page allows you to define and manage profit margin settings across different destinations, transports, and agencies. These rules determine how much profit is applied to bookings based on specific parameters such as resort, passenger type, and travel period.\
This tool ensures that pricing strategies remain consistent, flexible, and automatically applied within the system.

### **Purpose**

The purpose of this feature is to make the Profit Margin Rule system more adaptable to each agency’s by allowing multiple overlapping rule sets that can be stacked and combined.\
This ensures that agencies can:

* Define **global profit margins** for GDS or charter flights.
* Apply **different margins** for specific **resorts** or **hotels**.
* Create **transport-based rules** that vary by route and stay length.

The result is a **flexible, automated, and scalable** system for defining profit margins that directly feeds into the **Price List Generator**.

Using the profit margin rule, all agencies can:

* Configure complex profit structures without duplicate entries.
* Adjust margins easily for specific destinations, hotels, or routes.
* Automatically generate accurate, up-to-date **price lists**.
* Reduce manual maintenance through **flexible**, **reusable**, and **automated** rules.

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

### **Instructions**

**Filters (Top Section)**

Use the filters to narrow down the list of rules displayed below.

* **Rule types:** Select which type of rule you want to view (Resort, Transport).
* **Departure start / stop:** Define the date range for the departure period you want to see or edit.
* **Departures / Arrivals:** Filter rules by departure or arrival locations.
* **Resorts:** Select a specific resort if you want to see only rules for that destination.
* **Passenger Type:** Choose the type of passenger (e.g., Adult, Child) that the rule applies to.
* **Stay Length:** Filter by the length of stay defined in the rule. Used to filter rules for a specific steay length. Valid imput "7", "6-8", "7,14"
* **Show older:** When enabled, displays Profit Margin rules with departure in the past.
* **Show codes:** Displays system codes instead of names, useful for internal references.
* **Transports / Hotels (Edit buttons):** Allows you to select specific transport or hotel references to filter results.
* **Display:** Applies the selected filters to show the corresponding rules.
* **Clear:** Resets all filters to default.

**Rule List (Bottom Section)**

Each row represents an existing profit margin rule. The table contains the following columns:

| Field                                 | Description                                                                                                                                                                                                                                                                                                       |
| ------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Agency**                            | The travel agency to which the profit margin rule applies. Mandatory                                                                                                                                                                                                                                              |
| **Rule**                              | Type of rule (e.g., Resort, Transport). Defines the scope of the profit margin. Mandatory                                                                                                                                                                                                                         |
| **Passenger**                         | Indicates which passenger type the rule targets (e.g., Adult, Child). Mandatory                                                                                                                                                                                                                                   |
| **Arrival**                           | The arrival destination or city for which the rule is valid. Mandatory                                                                                                                                                                                                                                            |
| **Resort (Optional)**                 | Specific resort linked to the profit margin rule.                                                                                                                                                                                                                                                                 |
| **Hotel (Optional)**                  | The hotel associated with the rule, if applicable.                                                                                                                                                                                                                                                                |
| **Transport Type**                    | Specifies the mode of transport (e.g., Charter, Dynamic, Sy-real, System).                                      <mark style="color:$info;background-color:red;">Note: When a Transport type is selected, the Transport field will be populated with all transports related to the selected Transport type.</mark> |
| **Transport (Optional)**              | Select the specific transport line that the rule applies to.                                                                                                                                                                                                                                                      |
| **Departure Start / Stop (Optional)** | Date range during which this rule is active.                                                                                                                                                                                                                                                                      |
| **Stay (Optional)**                   | Length of stay in days covered by the rule. Support multiple stay lengths.                                                                                                                                                                                                                                        |
| **PM1 – PM4**                         | Actual profit margin                                                                                                                                                                                                                                                                                              |
| **Is Percent**                        | Indicates whether the profit margin values (PM1–PM4) are percentages (✔️) or fixed amounts (❌).                                                                                                                                                                                                                   |
| **Edit (✏️ icon)**                    | Opens the rule for editing.                                                                                                                                                                                                                                                                                       |
| **History (📄 icon)**                 | Shows the history on the specific rule made                                                                                                                                                                                                                                                                       |
| **Delete (🗑️ icon)**                 | Removes the selected rule permanently.                                                                                                                                                                                                                                                                            |

**Additional Actions**

* **Create** — Opens a new page to create a profit margin rule. You can define all required parameters such as agency, destination, dates, and profit values.
* **Scheduled Rules** — Indicates that a rule is planned to take effect in the future, replacing the current one.

### **Example Use Case**

#### **Creating New Rules**

If Tourpaq DK wants to apply a 15% profit margin for Adult passengers traveling to Salzburg between 23-10-2029 and 23-10-2029, you would:

1. Click **Create**.
2. Select _Agency_: Tourpaq DK.
3. Choose _Rule_: Resort.
4. Define _Passenger Type_: Adult.
5. Set _Arrival_: Salzburg.
6. Enter _PM1–PM4_ values (e.g., 10, 15, 20, 30).
7. Mark **Is Percent** as true.
8. Save the rule.

The system will automatically apply these margins to all bookings that match the defined criteria.

#### **Editing Existing Rules**

1. Click the **edit icon (pencil)** next to the rule you want to modify
2. Update the necessary fields in the edit dialog
3. Save changes and verify they appear correctly in the grid



The Profit Margin functionality support more than one profit margin per rule, providing greater flexibility for agency configurations.

Each combination of Departure and Stay is unique within the Profit Margin section.

The system validates this uniqueness on the front end. If a duplicate combination is detected, the corresponding row or field will be highlighted in red.

Additionally, the system supports defining different profit margins for different departures, even when the stay length is the same within the same rule.

There are two types of rules: **Transport Rules** and **Resort Rules**.

For **Transport Rules**, users must:

* Select the Agency, Rule (Transport), Passenger, Arrival, Transport
* Define **departure start** and **departure stop** intervals.
* Set the profit margin values (**PM1–PM4**) using the button Add Profit Margin rule. Negative profit margins can be set, but this requires the "Use negative value in profit margin" company feature. Please contact an administrator for assistance.
* Also, here it is possible to add a Departure location and the stay length.

The system will then update all price lists created with the selected transports. For example, a rule setting **PM1–PM4** for the interval **17.10.25 - 31.10.25** will apply to all price lists using transports **and** B-AG, covering all hotels at the corresponding destination for agency **TorpaqDK.**

<figure><img src=".gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

**Resort Rules** can be created in three ways:

1. **All Resorts Rule**\
   Applies to all price lists created with all hotels from all resorts available for the selected brand within the specified departure interval.
2. **Resort-Specific Rule**\
   Applies to all price lists created with all hotels from a selected resort for the chosen brand within the specified departure interval.
3. **Hotel-Specific Rule**\
   Applies to price lists created with selected hotels for the chosen brand.

STAY: The stay length of interval 1.  If a hotel is specified, in the case of two matching rules (overlap), the most precise rule wins (if there is a rule with no stay and a rule that matches with stay, then the rule with stay is used).

**Profit Margin Calculation:**\
For a given brand and departure interval, the profit margin (**PM**) is calculated as:\
**PM = PMT + PMD + PMH**

Where:

* **PM**: The profit margin is set in the price list.
* **PMT**: Profit margin from the **Transport Rule**.
* **PMD**: Profit margin from the **Destination Rule**.
  * **PMD = PMA**: Profit margin from the **All Resorts Rule** (defined at the destination).
  * **PMD = PMR**: Profit margin from the **Resort-Specific Rule** (overrides **PMA**).
* **PMH**: Profit margin from the **Hotel-Specific Rule**.

Once added, rules are scheduled to update the profit margins.\
The same rule can be defined for different departure intervals.

**Example:** Profit margin rules are defined below:

<figure><img src=".gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

The value in the price list will be the sum of profit margins from Transport, Resort, and Hotel.

<figure><img src=".gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

Based on the profit margin value, prices are calculated.

* **Manual Changes**: Any manual changes in the price list will overwrite values set by the rules.
* **Rule Updates**: If a rule is later updated and scheduled, it will overwrite manually updated values in the price list.
* **Automatic Scheduling**: A Resort Rule can be scheduled automatically when new price lists are created for hotels in that resort.
