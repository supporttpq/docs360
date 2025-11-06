# Live Offer Profit Margin

#### **Overview**

The **Live Offer Profit Margin** page allows users to view and manage profit margins applied to hotel offers generated through the Live Offer functionality.\
This page ensures that each agency or brand has visibility and control over the margin applied to real-time hotel data received from external providers (such as BedBanks).

Users can filter, edit, or create new profit margin entries that apply to hotels within specific destinations and travel dates.

#### **Purpose**

The purpose of this page is to define how much profit margin is applied to hotel prices when Live Offers are created for customers.\
These profit margins are typically added on top of the net price returned by external providers so that the final selling price shown to the customer reflects the agency’s revenue policy.

***

#### **Tabs**

* **Hotel** – Displays live profit margins related to hotels.
* **Transport** – Displays live profit margins related to a destination.

***

#### **Filters and Controls**

<figure><img src=".gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

| **Field**                            | **Description**                                                                                                                                    |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Agency**                           | Filters results by the selected agency (e.g., _Tourpaq DK_). Determines which agency’s profit margins are shown.                                   |
| **Provider Source**                  | Filters by the source of the hotel data (e.g., _BedBank_, _Anixe, Alpinco, etc_). Useful when different providers have distinct margin structures. |
| **Country**                          | Filters results by the country of the hotel.                                                                                                       |
| **Departure Start / Departure Stop** | Defines the travel period for which the profit margin is valid. For example, 01-11-2025 to 31-12-2025.                                             |
| **Destination**                      | Filters by the arrival or destination city (e.g., _Andorra_, _Pitești_).                                                                           |
| **Hotel**                            | Filters by specific hotel name if the margin is defined only for certain properties.                                                               |
| **Star Rating (⭐ selector)**         | Allows users to filter by hotel rating (1–5 stars). Useful when margin rules differ per category.                                                  |
| **Display**                          | Applies the selected filters and displays the filtered list of profit margin rules.                                                                |
| **Clear**                            | Removes all applied filters and reloads the full list.                                                                                             |
| **Create**                           | Opens the form to create a new profit margin rule for hotels.                                                                                      |

#### **Table Columns**

| **Column**                           | **Description**                                                                                                                                                   |
| ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **✏️ (Edit icon)**                   | Opens the selected profit margin rule for editing.                                                                                                                |
| **Agency**                           | Indicates the agency the rule belongs to. Each agency can have its own set of profit margin rules.                                                                |
| **Hotel Provider**                   | Shows the source of hotel data (e.g., _BedBank_).                                                                                                                 |
| **Country**                          | The country where the hotel is located.                                                                                                                           |
| **Departure Start / Departure Stop** | Defines the validity period of the rule. Margins apply only to offers with departures within this range.                                                          |
| **Arrival**                          | Destination city where the hotel is located.                                                                                                                      |
| **Hotel**                            | The specific hotel name to which the rule applies.                                                                                                                |
| **Stars**                            | The hotel’s rating (used for filtering and verification).                                                                                                         |
| **Price**                            | Shows the current calculated prices according to the defined margin. Clicking **View Prices** opens a detailed view with net, margin, and total price breakdowns. |
| **🗑️ (Delete icon)**                | Deletes the profit margin rule. This action removes the margin for the selected hotel and destination.                                                            |

#### **Typical Workflow**

1. **Filter** by agency, provider, or destination to locate existing profit margin rules.
2. **View Prices** to verify the effect of the defined profit margin on current hotel offers.
3. **Edit** the rule if adjustments are needed (e.g., to align with seasonal policies).
4. **Create** new entries when introducing new destinations, hotels, or travel periods.
5. **Delete** outdated rules once the travel period has ended or the contract is no longer valid.

### Create New live Offer Profit margin

#### **Purpose**

The **Create** function allows users to add a new profit margin rule that applies to hotels included in Live Offers.\
This ensures that new destinations, hotels, or providers can have tailored profit margins reflecting contractual agreements or marketing strategies.

#### **Steps to Create a New Rule**

1. **Click “Create”**\
   Located in the upper-right corner of the **Live Offer Profit Margin** page.
2. **Select the Agency**\
   Choose which agency the rule will belong to (e.g., _Tourpaq DK_).\
   Each agency manages its own margin settings.
3. **Choose the Provider Source**\
   Select the external provider (e.g., _BedBank_).\
   This determines which supplier’s hotels will use the defined margin.
4. **Define the Validity Period**
   * **Departure Start** – The first date when the rule becomes active.
   * **Departure Stop** – The last date when the rule remains valid.\
     Only bookings departing within this period will have the margin applied.
5. **Select the Country and Destination**
   * **Country** – The country where the hotel is located.
   * **Destination** – The specific city. This helps narrow the rule’s scope to a specific area.
6. **Select the Hotel (optional)**\
   Choose a particular hotel if the margin applies to a single property.\
   If left empty, the margin applies to all hotels matching the other filters.
7. **Set the Star Rating (optional)**\
   You can define margins that apply only to certain hotel categories (e.g., 4★ and 5★ hotels).
8. **Define the Profit Margin**\
   Input the percentage or value to be added on top of the provider’s net price.\
   Example: a 15% margin means the final customer price will be 15% higher than the net cost.
9. **Save the Rule**\
   Click **Save** to store the new profit margin configuration.\
   Once saved, the rule becomes active immediately and is visible in the list.

#### **Result**

After creating the new rule:

* The rule appears in the main **Live Offer Profit Margin** list.
* The **Price** column updates automatically to reflect the new margin effect.
* When a Live Offer is generated, the system applies this margin to all matching hotel results (based on the selected filters such as provider, destination, and date).
