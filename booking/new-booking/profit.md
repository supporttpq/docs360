# Profit

### **Overview**

The **Profit** tab provides a detailed breakdown of the financial outcome of a booking by comparing **turnover**, **costs**, and **profit**. It shows how each component (for example, room, transport, extras, discounts) contributes to the total revenue and expenses of the booking.

***

### **Purpose**

* Track and analyse the profitability of individual bookings.
* See how much each product, service, or discount contributes to revenue and cost.
* Adjust internal cost data for rooms, transports, and other components when needed for financial reporting or recalculation.

***

### **Preconditions**

* The booking must contain at least one product, room, or transport service.
* The user must have permission to access financial data and, if applicable, to update internal costs.
* Prices and cost structures must be configured for the components used in the booking.

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Instructions**

1. **Open the Profit tab**
   * Go to the relevant booking.
   * Click the **Profit** tab to view detailed turnover and cost information.
2.  **Understand the columns**

    | **Column**   | **Description**                                                          |
    | ------------ | ------------------------------------------------------------------------ |
    | **Category** | The **type** of item (for example, Product, Discount/Supplement, Room).  |
    | **Item**     | The specific product, discount, supplement, room, or service.            |
    | **Turnover** | The amount the customer pays for each item or service.                   |
    | **Cost**     | The internal cost associated with each item or service.                  |
    | **Profit**   | The calculated difference between **Turnover** and **Cost** for the row. |
3.  **Edit costs**

    You can update the **Cost** values manually for the booking when you need to adjust internal margins or align with supplier invoices.

    _To update the cost for **all passengers** in a category:_

    * Enter the new total cost (to be shared across all passengers) in the **empty cost field** for that category.
    * Click **Save for all**.
    * Add the required **note** (mandatory).
    * Save the changes.

    _To update the cost **for specific passengers only**:_

    * Click **Save individual**.
    * In the popup, select the passengers that should receive the new cost.
    * Enter the new **cost per passenger** and the required **note** (mandatory).
    * Save the changes.

    <div data-gb-custom-block data-tag="hint" data-style="warning" class="hint hint-warning"><p>When you edit <strong>Cost</strong>, all previous cost changes for that <strong>Cost Category</strong> (Transport, Hotel, Extra, etc.) are overwritten. Only the <strong>most recent</strong> cost update for that category is applied to the booking.</p></div>
4.  **Open the detailed Hotel Cost Price view**

    <figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

    * Click the blue **info** icon next to the hotel cost line to open the detailed **Hotel Cost Price** page in a new window.

    <figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (3) (1).png" alt=""><figcaption></figcaption></figure>

    This view provides a detailed breakdown of the **hotel cost** for a specific booking. It displays daily and total pricing information for each passenger, along with a cost summary useful for comparison and control.

    *   The **left panel** lists all passengers in the booking (for example, adults and children) along with their daily cost components, such as:

        * **Room Cost**
        * **Extra Included / Extra Bed**
        * **Stay and Pay / Extra Room Price / Per Pax Night**
        * **Early Booking**

        Each component is shown **per date**, so you can see how the cost changes over the stay period.
    * The **Invoice Hotel Details Cost** box on the right summarises all hotel-related cost elements in EUR, including:
      * Room Cost
      * Extra Bed discounts and related offers
      * Early Booking and Extra Cost components
      * A **Total** line representing the total hotel cost used for invoicing.

    At the bottom of the page:

    * **Total Cost** shows the total hotel cost in DKK.
    * **Total Turnover** shows the total sales amount (including profit margin).
    * **Booking Date** indicates when the booking was last updated.

    This section helps administrators and finance staff verify that hotel pricing is correct and compare **cost versus turnover** for each booking.

***

### **Cost Cache Tab Overview**

The **Cost Cache** tab shows a summarised breakdown of all cost components associated with each passenger in a booking. It is used to validate and compare **cached** cost data against the current calculation, ensuring that prices are consistent and up to date.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Key columns**

* **Firstname / Lastname / Age** – Identifies each passenger.
* **Discount Cost** – Any cost impact related to discounts.
* **Hotel Cost** – The total accommodation cost per passenger.
* **Insurance Cost** – Cost of any insurance products.
* **Product Cost** – Cost of additional products or extras.
* **Transport Cost** – Cost of transport or transfers.
* **Booking No / Passenger ID / Booking ID** – Links the row to the correct booking and passenger in the system.
* **Cost Reference** – Internal reference for how costs are mapped and calculated.
* **Cached** (True/False) – Indicates whether cost data for that passenger is currently stored in the cache.

At the bottom of the page, the **Hotel Cost** summary box shows:

* The **total hotel cost** for all passengers.
* The **cached cost value**, used to check that displayed costs match stored data.
* An **Update** button, which administrators can use to refresh cached costs if a recalculation is required.

This tab helps maintain consistency between live calculations and cached data, supporting financial accuracy and stable system performance.

***

### **FAQ**

#### **How is the Profit tab different from the Economics tab?**

* **Economics** focuses on the **payment structure and due dates** (deposit, second payment, rest, release payment, etc.).
* **Profit** focuses on the **relationship between turnover, cost, and profit** for each booking component.

Use **Economics** when working with payments and due dates, and **Profit** when analysing margins and internal costs.

***

#### **Why does the profit look wrong or show 0 for some items?**

Typical reasons:

* **Cost** is missing or set to 0, so Profit = Turnover.
* **Turnover** is 0 (for example, a complimentary item or a 100% discount).
* Costs were updated manually and no longer match the underlying supplier price.

Check the **Cost** and **Turnover** columns for the affected row, and if needed, adjust cost values or verify pricing in the underlying setup.

***

#### **What happens when I change the cost for a category?**

When you change the **Cost** for a category (for example, Hotel, Transport, Extra):

* The system recalculates **profit** for that category and for the booking.
* All previous manual cost edits for that **same category** are overwritten – only the most recent change applies.

If you need to keep a history of why costs were changed, always use clear notes and follow your internal approval procedures.

***

#### **When should I use the Cost Cache tab?**

Use the **Cost Cache** tab when you need to:

* Verify that stored (cached) costs still match the current price logic.
* Investigate differences between older reports and the current Profit view.
* Refresh cached costs after significant price rule or configuration changes.

If you are unsure whether to press **Update**, consult with your finance or system administrator, as recalculation can affect reported margins.

***

#### **Does changing costs in Profit affect supplier invoicing?**

Changing costs in the **Profit** tab primarily affects **internal cost and profit calculations** in Tourpaq. Supplier invoices are usually based on your contracts and external documents. Use the detailed **Hotel Cost Price** view and Profit tab to **reconcile** against supplier invoices, but always follow your organisation’s finance procedures for handling invoice discrepancies.
