# Prices

#### Overview

In **Tourpaq Office**, each **Extra** (such as insurance, car rental, excursions, or other optional services) can have one or more **price configurations**.\
Prices are defined using specific **intervals** to ensure flexibility while maintaining data consistency. The system includes validation rules that prevent overlapping intervals.

There are **three types of intervals** that determine when a price is applied:

1. **Age From / To** – Applies the price based on the passenger’s age range.
2. **Departure Date From / To** – Applies the price to bookings departing within a specific date range.
3. **Booking Date From / To** – Applies the price to bookings made within a specific date range.

Each interval defines the **conditions** under which the price is valid.

<figure><img src="../../.gitbook/assets/image (5) (1) (2).png" alt=""><figcaption></figcaption></figure>

#### Purpose

The **Extras / Prices** setup allows agencies to manage dynamic pricing for additional products or services associated with a booking.\
By defining rules based on age, booking dates, and travel periods, the system ensures that every passenger pays the correct price according to their travel details.

This helps:

* Maintain consistent and accurate pricing across bookings.
* Support promotional or seasonal offers.
* Differentiate costs and profit margins across age groups, dates, and brands.

#### How to Use

**Define a Price for an Extra**

1. **Open the Extra** from the list in Tourpaq Office.
2. Navigate to the **Prices** section.
3. Click **Create** or **Edit** to configure a new price rule.
4.  Fill in the following fields:

    | Field                        | Description                                                                                                               |
    | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
    | **Age From / To**            | Sets the age range for which the price applies.                                                                           |
    | **Departure Date From / To** | Defines the departure period covered by this price.                                                                       |
    | **Booking Date From / To**   | Defines when the booking must be created for the price to apply.                                                          |
    | **Price**                    | The amount paid by the passenger (in local currency).                                                                     |
    | **Group Price**              | The group rate, if applicable.                                                                                            |
    | **Cost Price**               | The agency’s cost for this extra (based on creditor or local currency).                                                   |
    | **Days**                     | The number of days the extra is available. If the booking duration is shorter than this, the extra will not be available. |
    | **Margin**                   | Defines the profit margin applied (especially for car rentals).                                                           |
    | **Max Cost**                 | Sets the maximum car cost the agency can sell.                                                                            |
    | **Per Day**                  | If enabled, the price and cost are calculated per day.                                                                    |
    | **Contract**                 | References the contract name related to this price.                                                                       |
5. Click **Save** once all details are completed.

#### Price Calculation

The total price per day is calculated using the following formula:

* If **Days** is filled:\
  `Extra_Price = Price × Days`
* If **Days** is empty:\
  `Extra_Price = Price × Booked_Days`

### Price per brand <a href="#price-per-brand" id="price-per-brand"></a>

Tourpaq supports defining different prices per brand.

* If only a **default price** is set, it applies to all agencies.
* If a **brand-specific price** is added, that price will apply only to the selected agency or brand.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (3) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Editing prices is available only for the **default** configuration; for agency-specific prices, only **Price**, **Group Price**, **Margin**, and **Max Cost** can be updated.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

To enable price-per-brand functionality, please contact **Tourpaq Support**.

**Split prices**

The **Split** function allows dividing existing price or cost intervals — for example, when updating prices or managing stop sales.\
Prices can be split by:

* **Age**
* **Departure Date**
* **Booking Date**

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

**How to Split a Price:**

1. Click on the **Split** button below the price lines.
2. Choose how many splits you want to create.

<figure><img src="../../.gitbook/assets/image (4) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

3. Adjust the date or age intervals as needed:
   * When splitting by **Departure** or **Booking Date**, set the **Date From** of the first line to the original start date and the **Date To** to the new stop date.
   * The **second line** will automatically use the new **Date From** and original **Date To**.
   * It’s recommended to use the **current day** or **next day** as the stop date for the first line.

<figure><img src="../../.gitbook/assets/image (5) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

4. Click **Split** to confirm.

After splitting, the system will display separate price lines for each new interval.

<figure><img src="../../.gitbook/assets/image (6) (4).png" alt=""><figcaption></figcaption></figure>
