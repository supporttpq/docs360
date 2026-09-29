# Prices

###

###

### Overview

In **Tourpaq Office**, each **Extra** (such as insurance, car rental, excursions, or other optional services) can have one or more **price configurations**.\
Prices are defined using specific **intervals** to ensure flexibility while maintaining data consistency. The system includes validation rules that prevent overlapping intervals.

There are **three types of intervals** that determine when a price is applied:

1. **Age From / To** – Applies the price based on the passenger’s age range.
2. **Departure Date From / To** – Applies the price to bookings departing within a specific date range.
3. **Booking Date From / To** – Applies the price to bookings made within a specific date range.

Each interval defines the **conditions** under which the price is valid.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Prices section for an Extra."><figcaption></figcaption></figure></div>

### Purpose

The **Extras / Prices** setup allows agencies to manage dynamic pricing for additional products or services associated with a booking.\
By defining rules based on age, booking dates, and travel periods, the system ensures that every passenger pays the correct price according to their travel details.

This helps:

* Maintain consistent and accurate pricing across bookings.
* Support promotional or seasonal offers.
* Differentiate costs and profit margins across age groups, dates, and brands.

### How to use

**Define a Price for an Extra**

1. **Open the Extra** from the list in Tourpaq Office.
2. Navigate to the **Prices** section.
3. Click **Create** to configure a new price rule.
4.  Fill in the following fields:

    | Field                        | Description                                                                                                                                                                                               |
    | ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **Age From / To**            | Sets the age range for which the price applies.                                                                                                                                                           |
    | **Departure Date From / To** | Defines the departure period covered by this price.                                                                                                                                                       |
    | **Booking Date From / To**   | Defines when the booking must be created for the price to apply.                                                                                                                                          |
    | **Start Time / End Time**    | Shown only when the Extra is an Extra Order. Limits the price line to part of the day, so a morning and an afternoon excursion on the same date can have different prices. Defaults: `00:00` and `23:59`. |
    | **Price**                    | The amount paid by the passenger (in local currency).                                                                                                                                                     |
    | **Group Price**              | The group rate, if applicable.                                                                                                                                                                            |
    | **Cost Price**               | The agency’s cost for this extra (based on creditor or local currency).                                                                                                                                   |
    | **Days**                     | The number of days the extra is available. If the booking duration is shorter than this, the extra will not be available.                                                                                 |
    | **Margin**                   | Defines the profit margin applied (especially for car rentals).                                                                                                                                           |
    | **Max Cost**                 | Sets the maximum car cost the agency can sell.                                                                                                                                                            |
    | **Per Day**                  | If enabled, the price and cost are calculated per day.                                                                                                                                                    |
    | **Contract**                 | References the contract name related to this price.                                                                                                                                                       |
5. Click **Save** once all details are completed.

### Price calculation

The total price per day is calculated using the following formula:

* If **Days** is filled:\
  `Extra_Price = Price × Days`
* If **Days** is empty:\
  `Extra_Price = Price × Booked_Days`

### Price per brand <a href="#price-per-brand" id="price-per-brand"></a>

Tourpaq supports defining different prices per brand.

* If only a **default price** is set, it applies to all agencies.
* If a **brand-specific price** is added, that price will apply only to the selected agency or brand.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Price per brand settings."><figcaption></figcaption></figure></div>

* Editing prices is available only for the **default** configuration; for agency-specific prices, only **Price**, **Group Price**, **Margin**, and **Max Cost** can be updated.

To enable price-per-brand functionality, please contact **Tourpaq Support**.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Default price configuration."><figcaption></figcaption></figure></div>

* The system supports editing prices across multiple rows within the same view and saving all changes in a single operation.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Multiple price rows for an Extra."><figcaption></figcaption></figure></div>

To optimize production workflow, users can perform multiple price corrections or updates at the same time and save everything with one click, instead of saving each row individually.

#### Split prices

The **Split** function allows dividing existing price or cost intervals — for example, when updating prices or managing stop sales.\
Prices can be split by:

* **Age**
* **Departure Date**
* **Booking Date**

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Split prices option."><figcaption></figcaption></figure></div>

**How to split a price**

1. Click on the **Split** button below the price lines.
2.  Choose how many splits you want to create.

    <div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Number of price splits."><figcaption></figcaption></figure></div>
3.  Adjust the date or age intervals as needed:

    * When splitting by **Departure** or **Booking Date**, set the **Date From** of the first line to the original start date and the **Date To** to the new stop date.
    * The **second line** will automatically use the new **Date From** and original **Date To**.
    * It’s recommended to use the **current day** or **next day** as the stop date for the first line.

    <div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Date and age intervals for split prices."><figcaption></figcaption></figure></div>
4. Click **Split** to confirm.

After splitting, the system will display separate price lines for each new interval.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Separate price lines after splitting."><figcaption></figcaption></figure></div>

**Prices for Extra Orders**

Prices for Extra Orders (Extras assigned to **Guide sale**) are defined on this tab. The separate **Generic Product Price Rules** page is no longer used; its prices have been moved to the **Prices** tab of the relevant Extras.

* **Adult and child prices** — create one line for children, **From Age** `2` **To Age** `11`, and one for adults, **From Age** `12` **To Age** `120`. The Guest App, Guide App and the **Extra Orders** tab show them as **Adult Price** and **Child Price**.
* **Time of day** — the **START TIME** and **END TIME** columns sit between **DEPARTURE TO** and **BOOKING FROM**, with their own **S** split button. Split a line by time to price two periods of the same day separately.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (349).png" alt="Prices tab with START TIME and END TIME columns and three price lines for adults, children and a late departure"><figcaption><p>Price lines of an Extra Order with START TIME and END TIME.</p></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (352).png" alt="Prices tab of a Manual allotment Extra with an adult line aged 12 to 120 at 200 DKK and a child line aged 0 to 11 at 100 DKK, without time columns"><figcaption><p>Adult and child price lines on a Manual allotment Extra.</p></figcaption></figure></div>

{% hint style="danger" %}
**TO VERIFY** — On staging, START TIME and END TIME are visible on the Generic allotment Extra `TFS-EG` but not on the Manual allotment Extra `JJR_TEST_MAN_ALL`, which is also assigned to Guide sale. Confirm the rule and adjust the Start Time / End Time row above.
{% endhint %}
