---
description: >-
  Set up Tourpaq Office Custom Hotel Days price lists for hotel-only stays and
  custom night counts without transport packages. Configure rooms, sales period,
  prices, and tiered profit margin rules.
---

# Price List Custom Hotel Days

### Overview

A **Custom Hotel Day Price List** lets you price stays per hotel day. It replaces fixed stay patterns.

To use this, the hotel and room setup must support **Custom Hotel Day bookings**. Then you can create a dedicated price list.

### Purpose

The purpose of this feature is to:

* Enable brands (agencies) to sell **hotel-only stays** or **custom night counts**.
* Offer flexibility to customers who may not require a full transport + hotel package.
* Control availability and pricing independent of transport schedules.

This setup is typically used when you do not sell fixed stay packages. Pricing is calculated per hotel day.

<figure><img src=".gitbook/assets/image (9) (1) (3) (1).png" alt=""><figcaption><p>Example: Custom Hotel Day price list setup.</p></figcaption></figure>

### Instructions

#### A. Configuration Prerequisites

Before creating a Custom Hotel Day Price List, the hotel must be configured accordingly.

1.  **Create the Hotel**\
    Create the hotel as usual. The only difference is in **Additional Settings**. Enable **Custom Hotel Days Booking**.

    <figure><img src=".gitbook/assets/image (699).png" alt=""><figcaption><p>Hotel setup: enable <strong>Custom Hotel Days Booking</strong> in Additional Settings.</p></figcaption></figure>
2.  **Create Room Types**\
    Configure the required room types.\
    For rooms that will be used in Custom Hotel Day bookings, enable the **Used for Custom Hotel Day** checkbox.

    <figure><img src=".gitbook/assets/image (700).png" alt=""><figcaption><p>Room type setup: check <strong>Used for Custom Hotel Day</strong>.</p></figcaption></figure>
3.  **Create Allotment**\
    Generate allotment for the rooms that will be used in Custom Hotel Day bookings.

    <figure><img src=".gitbook/assets/image (701).png" alt=""><figcaption><p>Create allotment for room types used in Custom Hotel Day bookings.</p></figcaption></figure>
4.  **Configure Room Cost**\
    Define the room cost for the configured rooms.

    <figure><img src=".gitbook/assets/image (702).png" alt=""><figcaption><p>Configure room cost for the selected room types.</p></figcaption></figure>

**Note:**\
After you generate the allotment, you can click **Copy Room Cost** to simplify setup. This automatically creates room cost lines for the defined interval. You only need to enter the price for the generated interval.

<figure><img src=".gitbook/assets/image (703).png" alt=""><figcaption><p>Tip: use <strong>Copy Room Cost</strong> after generating the allotment.</p></figcaption></figure>

#### B. Creating a Custom Hotel Day Price List

1. Navigate to **Price List → Price List Hotel Days**.
2.  Click **Create**.

    <figure><img src=".gitbook/assets/image (704).png" alt=""><figcaption><p>Create a new Price List Hotel Days record.</p></figcaption></figure>
3.  Fill in the required fields:

    * **Agency** – Select the agency or brand responsible for the setup.
    * **Country / Arrival / Resort / Hotel** – Select the destination and hotel configuration.
    * **Rooms** – Select the room types and configure their allotments.
    * **Departure Start / Departure Stop** – Define the sales period for the price list.

    <figure><img src=".gitbook/assets/image (705).png" alt=""><figcaption><p>Fill in Agency, destination, rooms, and Departure Start/Stop (sales period).</p></figcaption></figure>
4.  Use the **Enabled** toggle to activate or deactivate the price list.

    <figure><img src=".gitbook/assets/image (706).png" alt=""><figcaption><p>Use <strong>Enabled</strong> to activate or deactivate the price list.</p></figcaption></figure>
5.  Click **View Prices** to define or adjust the hotel prices for the selected period.

    <figure><img src=".gitbook/assets/image (707).png" alt=""><figcaption><p>Open <strong>View Prices</strong> to set daily hotel prices.</p></figcaption></figure>
6. Save the configuration.

### Profit margin rules (field explanations)

<figure><img src=".gitbook/assets/image (10) (1) (3) (1).png" alt=""><figcaption><p>Profit margin rules: define markup tiers based on room cost ranges.</p></figcaption></figure>

#### **Profit Margin**

Profit added on top of the base room cost.

* If **Is Percent** is enabled, the value is a percentage.
  * Example: `15` means **+15%**.
* If **Is Percent** is disabled, the value is a fixed amount.
  * Example: `15` means **+15 currency units**.

#### **Is Percent (checkbox)**

* Defines how the **Profit Margin** should be applied.
* **Checked:** Applied as a **percentage** of the room cost.
* **Unchecked:** Applied as a **fixed amount**.

#### **Room Cost Start**

Minimum base room cost for the rule.

Example: If set to `1`, the rule applies from `1` and up.

#### **Room Cost End**

Maximum base room cost for the rule.

Example: If set to `2000`, the rule applies up to `2000`.

#### **Add Price (button)**

Adds another profit margin rule row for a different cost range.

Example:

* Rule 1: `15%` for `1–2000`
* Rule 2: `10%` for `2001–5000`

#### **Save (button)**

Saves the rule setup.

#### **Trash/Delete Icon**

Deletes a rule row.

This setup supports **tiered profit margin rules** based on room cost ranges.

#### Highlighted Rows

Rows with a **red background** indicate scheduled rules used to generate price lists.

<figure><img src=".gitbook/assets/image (708).png" alt=""><figcaption><p>Red rows indicate scheduled rules used by the generator service.</p></figcaption></figure>

**Note:**\
The scheduled rule is configured by the **Super Administrator** for each agency.\
By default, the service runs every **15 minutes**, but the interval can be adjusted by the Super Administrator according to the agency’s needs.

After the scheduled service has run and the rule becomes active, the user can click on the **icon available in the interface**, which redirects directly to the **Price List page**. From there, the generated **Custom Hotel Day Price List** can be reviewed and managed.

<figure><img src=".gitbook/assets/image (710).png" alt=""><figcaption></figcaption></figure>

This step allows the user to verify that the automated rule has successfully created the price list and that the configured hotel, rooms, and date intervals are correctly reflected before proceeding with bookings.

### Creating a Booking with Custom Hotel Day

After the service has run, the rule is active, and the **Price List has been generated**, you can create Custom Hotel Day bookings.

#### Steps

1. Click **New Booking**.
2. Select the **number of passengers**.
3. Select the **customer**.
4. Select the **hotel** configured for Custom Hotel Day bookings.
5. Click **Take Allotment**.
6. Save the **passenger information**.
7. Save the **booking**.

<figure><img src=".gitbook/assets/image (709).png" alt=""><figcaption></figcaption></figure>
