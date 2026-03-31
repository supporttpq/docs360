---
description: >-
  Define Tourpaq Office profit margin rules (markup) for price lists. Set
  PM1–PM4 by resort or transport, passenger type, dates, and stay length. Rules
  feed the Price List Generator.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# Profit margin rules

Under **Price List → Profit Margin Rules**, you define rules that write **profit margin (markup)** values into **Tourpaq Office price lists**.

### Overview

Profit Margin Rules control how profit is applied across combinations of:

* Brand (agency)
* Passenger type (adult/child)
* Destination/resort/hotel
* Transport type and transport
* Departure period and stay length

These rules feed the **Price List Generator** and reduce manual price list maintenance.

In generated price lists, profit margins are stored as **PM1–PM4**.

### **Purpose**

Profit Margin Rules are designed for stacking and overrides. This lets you:

* Define **global profit margins** for GDS or charter flights.
* Apply **different margins** for specific **resorts** or **hotels**.
* Create **transport-based rules** that vary by route and stay length.

This produces a scalable setup that directly feeds into the [Price List Generator](generate-pricelist.md).

Using the profit margin rule, all agencies can:

* Configure complex profit structures without duplicate entries.
* Adjust margins easily for specific destinations, hotels, or routes.
* Automatically generate accurate, up-to-date **price lists**.
* Reduce manual maintenance through **flexible**, **reusable**, and **automated** rules.

<figure><img src=".gitbook/assets/image (5) (1) (1) (3) (1).png" alt=""><figcaption></figcaption></figure>

### **Instructions**

**Filters (Top Section)**

Use the filters to narrow down the list of rules displayed below.

* **Rule types:** Select which type of rule you want to view (Resort, Transport).
* **Departure start / stop:** Define the date range for the departure period you want to see or edit.
* **Departures / Arrivals:** Filter rules by departure or arrival locations.
* **Resorts:** Select a specific resort if you want to see only rules for that destination.
* **Passenger Type:** Choose the type of passenger (e.g., Adult, Child) that the rule applies to.
* **Stay Length:** Filter by the length of stay defined in the rule. Used to filter rules for a specific stay length. Valid input: `7`, `6-8`, `7,14`.
* **Show older:** When enabled, displays Profit Margin rules with Departure Stop date in the past.
* **Show codes:** Displays system codes instead of names, useful for internal references.
* **Transports / Hotels (Edit buttons):** Allows you to select specific transport or hotel references to filter results.
* **Display:** Applies the selected filters to show the corresponding rules.
* **Clear:** Resets all filters to default.

**Rule List (Bottom Section)**

Each row represents an existing profit margin rule. The table contains the following columns:

| Field                                 | Description                                                                                                                                                                                            |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Agency**                            | The travel agency to which the profit margin rule applies. Mandatory                                                                                                                                   |
| **Rule**                              | Type of rule (e.g., Resort, Transport). Defines the scope of the profit margin. Mandatory                                                                                                              |
| **Passenger**                         | Indicates which passenger type the rule targets (e.g., Adult, Child). Mandatory                                                                                                                        |
| **Arrival**                           | The arrival destination or city for which the rule is valid. Mandatory                                                                                                                                 |
| **Resort (Optional)**                 | Specific resort linked to the profit margin rule.                                                                                                                                                      |
| **Hotel (Optional)**                  | The hotel associated with the rule, if applicable.                                                                                                                                                     |
| **Transport Type**                    | Specifies the mode of transport (e.g., Charter, Dynamic, Sy-real, System). When a transport type is selected, the **Transport** field is populated with all transports related to that transport type. |
| **Transport (Optional)**              | Select the specific transport line that the rule applies to.                                                                                                                                           |
| **Departure Start / Stop (Optional)** | Date range during which this rule is active.                                                                                                                                                           |
| **Stay (Optional)**                   | Length of stay in days covered by the rule. Supports multiple stay lengths.                                                                                                                            |
| **PM1 – PM4**                         | Actual profit margin                                                                                                                                                                                   |
| **Is Percent**                        | Indicates whether the profit margin values (PM1–PM4) are percentages (✔️) or fixed amounts (❌).                                                                                                        |
| **Edit (✏️ icon)**                    | Opens the rule for editing.                                                                                                                                                                            |
| **History (📄 icon)**                 | Shows the change history for the rule                                                                                                                                                                  |
| **Delete (🗑️ icon)**                 | Removes the selected rule permanently.                                                                                                                                                                 |

**Additional Actions**

* **Create** — Opens a new page to create a profit margin rule. You can define all required parameters such as agency, destination, dates, and profit values.
* **Scheduled Rules** — Indicates that a rule is planned to take effect in the future, replacing the current one.

### **Example Scenario**

#### **Creating New Rules**

If a brand wants to apply a 15% profit margin for adult passengers traveling to Salzburg on `23-10-2029`, you would:

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

1. Click the **edit icon (pencil)** next to the rule you want to modify.
2. Update the required fields in the edit dialog.
3. Save changes and verify they appear correctly in the grid.

Profit Margin Rules support multiple profit margins per rule, which increases flexibility.

Each combination of Departure and Stay is unique within the Profit Margin section.

The system validates this uniqueness on the front end. If a duplicate combination is detected, the corresponding row or field will be highlighted in red.

Additionally, the system supports defining different profit margins for different departures, even when the stay length is the same within the same rule.

There are two types of rules: **Transport Rules** and **Resort Rules**.

For **Transport Rules**, users must:

* Select the Agency, Rule (Transport), Passenger, Arrival, Transport
* Define **departure start** and **departure stop** intervals.
* Set profit margin values (**PM1–PM4**) using **Add Profit Margin rule**.
  * Negative profit margins require the company feature **Use negative value in profit margin**. Contact an administrator if needed.
* Also, here it is possible to add a Departure location and the stay length.

The system then updates all price lists created with the selected transports.

Example: A rule setting **PM1–PM4** for **17.10.25–31.10.25** applies to all price lists using the selected transports (including `B-AG`). It covers all hotels at the matching destination for the selected agency.

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (3) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Resort Rules** can be created in three ways:

1. **All Resorts Rule**\
   Applies to all price lists created with all hotels from all resorts available for the selected brand within the specified departure interval.
2. **Resort-Specific Rule**\
   Applies to all price lists created with all hotels from a selected resort for the chosen brand within the specified departure interval.
3. **Hotel-Specific Rule**\
   Applies to price lists created with selected hotels for the chosen brand.

**STAY**: The stay length for interval 1.

If two rules overlap, the most specific rule wins. If one rule has **STAY** and the other does not, the stay-specific rule is used.

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

**Example:** Profit margin rules are defined below, and the logic is as follows:

* You place/modify a rule
* The profit margin rule becomes pink
* The system calculates the PM1 on the affected PLTAS

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (4) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Afterwards, the system calculates P1 in relation to PM1.
* The pink disappears when both calculations are completed.

{% hint style="warning" %}
Before the system calculates P1 in relation to PM1, a period of time must be waited until the service runs, depending on how much is set by the super administrator (the calculation is not done immediately).
{% endhint %}

<figure><img src=".gitbook/assets/image (4) (1) (1) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

The value in the price list is the sum of profit margins from Transport, Resort, and Hotel.

<figure><img src=".gitbook/assets/image (3) (1) (1) (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (5) (1) (1) (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

Based on the profit margin value, prices are calculated.

* **Manual Changes**: Any manual changes in the price list will overwrite values set by the rules.
* **Rule Updates**: If a rule is later updated and scheduled, it will overwrite manually updated values in the price list.
* **Automatic Scheduling**: A Resort Rule can be scheduled automatically when new price lists are created for hotels in that resort.

### Behavior of the Profit Margin Value

The **profit margin value** only changes when it is manually updated through the **Profit Margin Rule**.\
When a new value is saved in the Profit Margin Rule, it **overrides** any manually edited profit margin previously entered in the **Price List**.

If other changes are made — such as adding new entities (which generate new price lists) or updating hotel costs — these actions will **not** alter the profit margin value.\
In these cases, the system will simply **recalculate the final price** based on the manually adjusted profit margin defined by the user.

#### Example:

**An agency** uses a **Base Margin** defined through Profit Margin Rules, and then they manually adjust the profit margin directly in the Price List, and they perform manual price adjustments for various purposes.

In this case, PM1 is updated when:

* The **Profit Margin** itself is adjusted (departures, stay, amount)
* The **dates** are adjusted

**PM1 will not be updated when:**

* Adding a new **Transport**
* Adding a new **Hotel**
* Adding a new **Room**
* Adjusting **Allotment**
* Changing **Hotel Costs**
* Changing **Transport Costs**
* Editing **Discounts, Supplements, or Extras**

{% hint style="danger" %}
Currently, the system supports both percentage-based and amount-based profit margins.

Use the same margin type within a rule to avoid incorrect calculations.
{% endhint %}

### FAQ

1. **What’s the difference between Profit Margin Rules and editing the Price List manually?**\
   Profit Margin Rules write profit margins into price lists automatically. Manual edits override the value until a rule writes it again.
2. **How does Tourpaq handle overlapping rules?**\
   The most specific match wins. Hotel-specific beats resort-specific, which beats “all resorts” for the destination. A stay-specific rule beats a rule without stay when both match.
3. **What do PM1–PM4 mean?**\
   They are four separate profit margin fields on the rule. Tourpaq applies them to the corresponding profit margin fields in the generated price lists.
4. **Can I set profit margin as a percentage instead of an amount?**\
   Yes. Enable **Is Percent** to interpret PM1–PM4 as percentages. Disable it to treat them as fixed amounts.
5. **Can I set negative profit margins?**\
   Yes, but only if the company feature **Use negative value in profit margin** is enabled. Ask an administrator if you can’t enter negative values.
6. **How do I enter stay lengths?**\
   Use a single value (`7`), a range (`6-8`), or a list (`7,14`). The same formats are used in filters and in rule definitions.
7. **When do Profit Margin Rules update existing price lists?**\
   When you save a rule, it is scheduled to update matching price lists. The rule scope decides which price lists are affected.
8. **Why didn’t the profit margin change after I changed costs or added hotels/transports?**\
   Cost changes and new entities trigger price recalculation, not margin changes. Margins change only when you edit Profit Margin Rules or edit the price list manually.
9. **How do I see who changed a rule and when?**\
   Click the **History** (📄) icon on the rule row to see a change log.
