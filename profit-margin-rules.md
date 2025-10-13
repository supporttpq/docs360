# Profit margin rules

Under **Price List → Profit Margin Rules**, users can define rules to set profit margin values in price lists.

### Overview

The Profit Margin Rules system is a comprehensive tool for managing pricing strategies and commission structures across different travel products, destinations, and customer segments. This interface allows you to create, modify, and monitor profit margin rules that automatically apply to bookings based on specific criteria such as destination, passenger type, travel dates, and accommodation preferences.

<figure><img src=".gitbook/assets/image (5) (1) (1) (1) (1) (2).png" alt=""><figcaption></figcaption></figure>

#### Filtering and Searching

* **Rule Types**: Use the dropdown to filter by "All types" or specific rule categories (Transport, Resort)
* **Date Range**: Set departure start and stop dates using the calendar pickers to focus on specific time periods
* Click **"More Filters"** to access additional search criteria
* Select specific countries from the "Countries" dropdown
* Choose arrival locations using the "Arrivals" dropdown
* Filter by resort destinations in the "Resorts" dropdown
* **Passenger Type**: Filter rules by customer categories (Adult, Child)
* **Stay Length**: Set duration parameters for length-of-stay requirements. Used to filter rules for a specific stay length
* **Show Codes**: Check this box to display internal system codes for technical reference

#### Managing Profit Margin Rules

**Creating New Rules**

1. Click the **"Create"** button (blue button in top-right corner)
2. Fill in all required fields based on your pricing strategy
3. Configure profit margin values (PM1, PM2, PM3, PM4) as needed
4. Set the "IS PERCENT" indicator to specify whether margins are percentage-based or fixed amounts

**Editing Existing Rules**

1. Click the **edit icon (pencil)** next to the rule you want to modify
2. Update the necessary fields in the edit dialog
3. Save changes and verify they appear correctly in the grid

**Key Identification Fields**

* **AGENCY**: The agency name&#x20;
* **RULE TYPE**: Classification showing whether the rule applies to "Resort", "Transport"
* **PASSENGER TYPE**: Customer segment the rule applies to
* **COUNTRY**: Destination country for the rule
* **ARRIVAL**: Specific arrival airport or location
* **RESORT**: Resort or destination name
* **HOTEL**: Specific hotel property&#x20;
* **TRANSPORT**: Transport service codes and identifiers
* **DEPARTURE START/STOP**: Date range when the rule is active
* **STAY**: The stay length of interval 1.
* **PM1, PM2, PM3, PM4**: Four-tier profit margin structure allowing complex pricing models
* **IS PERCENT**: Visual indicator (red/green dots) showing calculation method.

There are two types of rules: **Transport Rules** and **Resort Rules**.

For **Transport Rules**, users must:

* Select the **brand** and one or more **transports**.
* Define **departure start** and **departure stop** intervals.
* Set the profit margin values (**PM1–PM4**). Negative profit margins can be set, but this requires the "Use negative value in profit margin" company feature. Please contact an administrator for assistance.

The system will then update all price lists created with the selected transports. For example, a rule setting **PM1–PM4** for the interval **10.09.25 - 10.09.25** will apply to all price lists using transports **and** BLL-BCN-SES, covering all hotels at the corresponding destination for agency **TorpaqDK.**

<figure><img src=".gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (2).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src=".gitbook/assets/image (6) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (7) (1) (2).png" alt=""><figcaption></figcaption></figure>

The value in the price list will be the sum of profit margins from Transport, Resort, and Hotel.

<figure><img src=".gitbook/assets/image (8) (1) (3).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (158).png" alt=""><figcaption></figcaption></figure>

Based on the profit margin value, prices are calculated.

* **Manual Changes**: Any manual changes in the price list will overwrite values set by the rules.
* **Rule Updates**: If a rule is later updated and scheduled, it will overwrite manually updated values in the price list.
* **Automatic Scheduling**: A Resort Rule can be scheduled automatically when new price lists are created for hotels in that resort.
