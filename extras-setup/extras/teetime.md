# Teetime

### **Overview**

\
The _TeeTime_ functionality allows administrators to define time-based availability schedules for specific products—typically those that need hourly or daily booking slots, such as golf tee times, spa appointments, or guided tours. TeeTimes can be configured as regular products in **Extras Setup → Extras**, but they use a **Generic Allotment Type**, which enables advanced scheduling and slot control.

### **Purpose**

\
TeeTime helps agencies manage products that depend on time availability by:

* Defining exact booking intervals and durations.
* Controlling the number of guests or bookings per slot.
* Managing allotments dynamically (daily or weekly).
* Automatically calculating prices through the **Generic Product Price Rule**.

This ensures that availability is accurately reflected for both back-office users and customers booking through the web or mobile app.

### Tee Time - Basic Setup Field

<figure><img src="../../.gitbook/assets/image (488).png" alt=""><figcaption></figcaption></figure>

| **Field Name**              | **Description**                                                                                                           |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Name**\*                  | The official name of the tee time product shown in the system and sales channels.                                         |
| **List Name**\*             | The name used in product lists; helps categorize or display products more clearly.                                        |
| **Code**\*                  | Unique identifier for the tee time product used internally and in integrations.                                           |
| **Status**                  | Controls visibility (e.g., visible, hidden). Determines if the product appears in sales channels.                         |
| **Stop sales hours**        | Number of hours before the tee time when bookings stop automatically.                                                     |
| **Minimum length**          | Minimum allowed duration for the tee time (if applicable).                                                                |
| **Contract Type**           | Defines the contract model associated with this tee time (e.g., allotment, guarantee etc ).                               |
| **Days prices option**      | Controls how many days forward the system calculates or displays prices.                                                  |
| **Allotment Type**          | Availability control type (e.g., Generic, Manua Linked to Transportl, ).                                                  |
| **Extras Category**\*       | Classification for the product, identifying it as a tee time in reporting and pricing (e.g., “Tee tider”).                |
| **Age**                     | Age rule for the product (if tee time pricing or access varies by age category).                                          |
| **Period/Trip length**      | Allowed trip or period lengths for which the tee time is valid.                                                           |
| **SSR Codes**               | Special Service Request codes used to pass additional information to suppliers or other systems. Supports multiple codes. |
| **Select Supplier**         | Supplier providing the tee time service. Links the product to its provider.                                               |
| **Round Rule**              | Select the round rule                                                                                                     |
| **One-way (only)**          | If enabled, the product is restricted to **one-way** operations.                                                          |
| **Currency**                | Currency in which the tee time is priced (e.g., EUR, USD).                                                                |
| **Currency prices**         | When enabled, pricing uses the selected currency instead of the system base currency.                                     |
| **Show supplier on ticket** | Displays supplier name on customer-facing documents such as vouchers or tickets.                                          |
| **Display allotment**       | Shows the remaining number of tee time slots to the user (internal or external depending on configuration).               |



**How to Use**

**1. Create a TeeTime Product**

1. Go to **Extras Setup → Extras**.
2. Create a new extra as usual.
3. In the **Allotment Type** field, select **Generic Allotment Type**.\
   This enables the TeeTime-specific settings listed below.

**TeeTime Settings:**

* **Pax limit** – Maximum number of products a guest can book in total.
* **Limit per day** – Maximum number of products a guest can book per day.
* **Limit before hour** – Restricts booking availability before a specific time.
* **Latitude / Longitude** – Used to calculate sunrise and sunset times for displaying in Office or on the web.
* **Product Parent ID** – Used to link products that share the same allotment across multiple companies.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Note:** The Extra Category must be set as **TeeTime Category Type** for the product to function correctly.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Tee Time Rules**

<figure><img src="../../.gitbook/assets/image (489).png" alt=""><figcaption></figcaption></figure>

| **Field Name**            | **Description**                                                                                                                                                                              |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Pax limit**             | How many times this product can be booked for each passenger (per interval) (e.g., 4 players).                                                                                               |
| **Latitude**              | Geographic latitude of the golf course; used for mapping and location services.                                                                                                              |
| **Longitude**             | Geographic longitude of the golf course; used for mapping and location services.                                                                                                             |
| **Product Parent ID**     | Used to link products that share the same allotment across multiple companies.                                                                                                               |
| **TeeTime Pin**           | Unique system-generated identifier for the specific tee time slot; used self checkin module). If the product is a child of another product, the tee time pin will be changed for the parent. |
| **Only first week(s)**    | Allow to select Tee Time only on the first (n) week(s).                                                                                                                                      |
| **Limit Per Day**         | Maximum number of times this tee time can be booked per day (e.g., 1 = only once per day).                                                                                                   |
| **Limit before hour**     | Restricts booking availability: **value = number of hours before**, plus an optional **cut-off time**. For example: “2 / 11:00” means bookings close _2 hours before 11:00_.                 |
| **First available price** | When enabled, the system will automatically show the earliest available tee time price instead of the exact slot price.                                                                      |
| **Requires confirmation** | Booking requires manual confirmation from staff or supplier before becoming valid.                                                                                                           |

### Prices <a href="#prices" id="prices"></a>

Teetime products draw their cost and price from **Generic Product Price Rule**, any value inserted in the Price tab will be disregarded. But a price line is required to enable the product to be sold. The priceline should look like this:

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

It is similar with the seating setting.

Real price of the product is set in **Extras Setup/Generic Product Price Rule**.

<figure><img src="../../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>

TeeTimes products appear in the **Tee Time Extras Lists**.

For this to work, the product needs to have a supplier assigned. The supplier cannot block the allotment of a TeeTime if he doesn't have the rights to do so, but he also has access to the lists

### Special settings <a href="#special-settings" id="special-settings"></a>

**Generic Allotment**

The TeeTime allotment defines when and how often the product is available.

<figure><img src="../../.gitbook/assets/image (145).png" alt=""><figcaption></figcaption></figure>

**Daily Allotments**

* **Frequency** – Number of days in the recurring availability pattern.
* **Daily Frequency** – Defines when during the day bookings can be made:
  * At specific fixed times, or
  * Every _X_ minutes within a defined hourly range.
* **Duration** – Total time span during which the product is available (e.g., 09:00–18:00).
* **Allotment** – Number of available items per slot (e.g., if set to 4 and frequency is 30 minutes, 4 slots open every 30 minutes).

<figure><img src="../../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

**Example:**\
If the product is available every 30 minutes between 09:00–19:00 with an allotment of 4, there will be 20 available slots per day (one every 30 minutes).

<figure><img src="../../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

### Weekly allotments <a href="#weekly-allotments" id="weekly-allotments"></a>

The only change from **Daily allotments** is

* Frequency - this time it is in weeks and not days, with the additional selection of days of the week in which the product is available

<figure><img src="../../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

* If **All Days** is checked, allotments are created for the entire week.
  * When a guest departs midweek, only the first valid day of the allotment will be shown in the Guest App.\
    &#xNAN;_(Example: if allotment is generated for the whole week and the departure is on Tuesday → only Tuesday’s slots appear.)_

<figure><img src="../../.gitbook/assets/image (207).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (208).png" alt=""><figcaption></figcaption></figure>

### Block allotments <a href="#block-allotments" id="block-allotments"></a>

The _Block Allotments_ feature allows admins to temporarily **block or unblock** availability for a defined date and time range.\
Use this when certain days or hours should not be bookable (e.g., maintenance, private events, holidays)

<figure><img src="../../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>

**Result:**\
Once configured, TeeTime products follow the defined schedule and appear in the _TeeTime Extras Lists_. Booking availability and pricing are automatically handled by the system based on the configured rules and linked suppliers.
