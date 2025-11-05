# Profit

#### **Overview**

The **Profit** tab provides a clear breakdown of the financial outcome of a booking by comparing **turnover**, **costs**, and **profit**. It allows for insight into how much each component (e.g., room, transport, extras) contributes to the total earnings and expenses of the booking.

***

#### **Purpose**

* Track and analyze the profitability of individual bookings.
* Understand how much each product, service, or discount contributes to revenue and cost.
* Adjust internal cost data for rooms, transports, and other components as needed for financial reporting or recalculation.

***

#### **Preconditions**

* The booking must be created with at least one product, room, or transport service.
* User must have permission to access financial data and make adjustments (if applicable).
* Pricing and cost structures must be defined for the associated components.

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Instructions**

1. **Access the Profit Tab:**
   * Go to the desired booking.
   * Click on the **Profit** tab to view detailed cost and turnover information.
2.  **Understand the Columns:**

    | **Column**   | **Description**                                                            |
    | ------------ | -------------------------------------------------------------------------- |
    | **Category** | Indicates the **type** of item (e.g., Product, Discount/Supplement, Room). |
    | **Item**     | The specific item, product, discount, or room used in the booking.         |
    | **Turnover** | The price paid by the customer for each item or service.                   |
    | **Cost**     | The internal cost associated with each item or service.                    |
    | **Profit**   | The calculated difference between Turnover and Cost.                       |
3.  **Edit Costs:**

    You can update Cost manually for the booking.

    * To update cost for **all passengers**:
      * Enter the new total cost (split across all passengers) in the emtpy field.
      * Click **Save for all**
      * Add a mandatory note
      * Save changes.
    * To update the Cost **individually for one or more passengers**:
      * Click **Save individual**
      * In the popup, select the passengers that should have new cost
      * Enter the new cost per passenger and note (mandatory)
      * Saves changes.
    * Important: When editing Cost, all previous cost changes on all passengers will be overwritten for the specific Cost Category (Transport, Hotel, Extra etc). Only the most recent Cost change will apply for the Category!
4. **Detailed Hotel Cost Price Section**

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Click on the blue info point to see detailed Hotel Cost Price (a new page opened).

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

This section provides a detailed overview of the **hotel cost breakdown** for a specific booking. It displays daily and total pricing information for each guest, along with a cost summary for invoicing purposes.

* The **left panel** lists all passengers in the booking (e.g., adults and children) along with their respective daily cost components such as:
  * **Room Cost**
  * **Extra Included / Extra Bed**
  * **Stay and Pay / Extra Room Price / Per Pax Night**
  * **Early Booking**\
    Each component is displayed per date, allowing visibility of cost variation over the stay period.
* The **Invoice Hotel Details Cost** box on the right summarizes all hotel-related costs in EUR, including:
  * Room Cost
  * Extra Bed Discount and related offers
  * Early Booking and Extra Cost components
  * A **Total** representing the hotel’s total invoice amount.

At the bottom:

* **Total Cost** represents the total hotel cost in DKK.
* **Total Turnover** shows the total sales amount (including profit margin).
* **Booking Date** indicates when the booking was last updated.

This section helps administrators and accountants verify accurate hotel pricing and compare cost versus turnover for each booking.

**Cost Cache Tab Overview**

The **Cost Cache** tab provides a summarized breakdown of all cost components associated with each passenger in a booking. It helps users validate and compare cached versus current cost data to ensure price accuracy.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

**Key Columns:**

* **Firstname / Lastname / Age** – Identifies each passenger in the booking.
* **Discount Cost** – Displays any applied discount amount.
* **Hotel Cost** – The total accommodation cost per passenger.
* **Insurance Cost** – Shows any insurance-related expenses.
* **Product Cost** – Represents the cost of additional products or extras.
* **Transport Cost** – Indicates transport or transfer-related expenses.
* **Booking No / Passenger ID / Booking ID** – Links each entry to its corresponding booking and system identifiers.
* **Cost Reference** – Displays internal cost mapping details for traceability.
* **Cached Indicator (True/False)** – Specifies whether the cost data for that passenger is stored in the cache.

At the bottom of the page, the **Hotel Cost** summary box displays:

* The **total hotel cost** for all passengers.
* The **cached cost value**, ensuring the displayed cost matches stored data.
* An **Update** button allowing administrators to refresh cached cost values if recalculation is needed.

This section ensures consistency between live and cached cost data, helping maintain financial accuracy and system performance.

