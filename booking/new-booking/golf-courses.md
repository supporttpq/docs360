---
description: >-
  Manage golf course bookings in Tourpaq Office. Mark golf passengers, enter
  handicap (HCP), add rounds, set requested and confirmed tee times, and print
  tickets with golf details.
---

# Golf Courses

## Golf Courses

### Overview

The **Golf Courses** page in **Tourpaq Office** lets you manage **golf extras** linked to a booking. Use it to mark which passengers play golf, enter handicap (**HCP**) and club numbers, add **golf rounds**, and maintain **requested vs confirmed tee times** for the golf provider.

* Mark which passengers are playing golf.
* Maintain player details such as handicap (**HCP**) and club number.
* Add golf rounds and handle **requested** and **confirmed** times.
* Review prices per round and the total amount.

This ensures golf participation and scheduling are recorded consistently and can be communicated to the customer and the golf provider.

***

### Purpose

* Record which passengers participate in golf activities.
* Maintain player information (HCP and club number).
* Add and schedule golf rounds with pricing and timing details.
* Centralize golf booking information for reporting and confirmation.

***

### Preconditions

* The booking must be created and saved with at least one passenger.
* The booking must include an **extra product** that uses the golf course reservation flow.
* The product must have pre-configured availability (time slots) in the system.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Instructions

#### 1. Passengers list

This section lists all passengers in the booking and allows you to configure their golf-related details.

| Field                          | Purpose                                                        | Instructions                                                                                                              |
| ------------------------------ | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Passenger**                  | Displays all passengers included in the booking.               | Each passenger appears automatically based on the booking details.                                                        |
| **Golf (checkbox)**            | Marks whether the passenger participates in a golf activity.   | Enable the checkbox if the passenger will play golf. Only selected passengers appear in the **Golf Courses list** below.  |
| **HCP (Handicap) – mandatory** | Indicates the passenger’s golf handicap.                       | Enter the numeric handicap value (for example, `5`).                                                                      |
| **Club**                       | Identifies the club number or club membership (if applicable). | Enter the club number (for example, `2`). This can also be used to track club/equipment references if your setup uses it. |

Only passengers with the **Golf** checkbox enabled will appear in the **Golf Courses list**.

***

#### 2. Golf Courses list

This section displays the golf rounds added for the selected passengers.

| Field                 | Purpose                                                                 | Instructions                                                                                                                                            |
| --------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Golf Course**       | Name of the golf course where the round will be played.                 | Automatically populated when you add a course.                                                                                                          |
| **Round**             | Identifies the specific round (for example, Round 1, Round 2).          | Valid round numbers are `1–99`. Use the **plus icon (+)** to add a round, or the **trash icon (🗑)** to delete a round.                                 |
| **Passenger**         | Displays which passenger is assigned to the golf round.                 | Automatically linked to passengers with **Golf** enabled in the list above.                                                                             |
| **Price (DKK)**       | The cost per passenger or round.                                        | Shows the price per round per passenger. The total is calculated automatically at the bottom.                                                           |
| **Request Date/Time** | The time the customer requests to play the round.                       | Select the requested date and time. Use the **copy icon** to assign the same requested time to multiple passengers/rounds.                              |
| **Confirmed Time**    | The final confirmed time from the golf course/provider (if applicable). | Enter the confirmed date and time once the reservation is confirmed. You can use the **copy icon** to copy the same confirmed time to multiple entries. |
| **Total**             | Total amount for all passengers and rounds in the booking.              | Calculated automatically based on prices per round and the number of rounds.                                                                            |

***

#### 3. Buttons and icons

| Element               | Description                                        |
| --------------------- | -------------------------------------------------- |
| **Add Golf Course**   | Adds another golf course entry to the booking.     |
| **➕ (Add Round)**     | Adds a new round for the same course.              |
| **🗑 (Delete Round)** | Removes a round from the course.                   |
| **📋 (Copy icon)**    | Copies a date/time value to similar entries below. |

***

#### Example scenario

In the example shown on the page:

* Three passengers have golf activities assigned.
* Multiple golf products (for example, _GolfProductMIR_, _GolfProductNoChild_) are present, each with several rounds.
* Requested and confirmed times are managed per round.
* The **Total** field sums up the total price of all rounds (for example, `798 DKK`).

***

### Ticket

The ticket contains relevant information for guests who have booked golf courses through the system.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (34).png" alt="Ticket example showing golf course rounds and requested/confirmed tee times"><figcaption></figcaption></figure>

Typically, the ticket includes:

* Guest name(s)
* Golf course name
* Number of booked rounds (free and paid, if applicable)
* Requested and confirmed tee times
* Booking reference
* Included extras or packages
* Supplier/course contact information (if configured)

#### Example workflow

1. **Select golf players**
   * Enable **Golf** for each passenger playing golf.
   * Fill in **HCP** and **Club** for each selected player.
2. **Add a golf course**
   * Click **Add Golf Course**.
   * Add rounds and assign passengers.
3. **Set dates and times**
   * Enter a **Request Date/Time**.
   * When confirmed by the provider, enter the **Confirmed Time**.
4. **Review total**
   * Verify the total amount is correct.
   * Save before printing/sending customer documents.

#### Notes

* Only passengers with **Golf** enabled appear in the Golf Courses list.
* **Request Date/Time** and **Confirmed Time** may differ depending on availability.
* Confirm prices and times before issuing final documentation to the customer.
* You can add multiple golf courses per booking (for multi-day trips).

***

## **Golf Courses Extra Category**

The **Extras Category** configuration controls how golf extras are grouped and behave in the booking flow.

* The **Type** defines the behaviour of the extra category.
* For golf courses, the **Type** must be set to **Golf**.

Once the type is set to **Golf**, you can create one or more categories that use this type.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Example workflow

1. Go to **Extras → Categories → Create**.
2. Set **Name** to _Golf Course_ and **List Name** to _Golf_.
3. Set a unique **Code** (for example, `Golf_GRG`).
4. Keep **Status** as _Visible_ and **Behavior on Web** as _Step1: Always Show_ (if this matches your web flow).
5. Select **Category Type** → _Golf_.
6. Enable **Accepts multiple product selection** to allow multiple rounds per passenger.
7. Add a **Description** and upload an **Image** (optional) for better presentation in WebBooking.
8. Click **Save**.

### Notes

* Ensure the **Code** is unique before saving.
* **Behavior on Web** and **Accepts multiple product selection** are important for correct booking behaviour.
* Use the **Sold Out Text** field to communicate availability clearly to customers.

***

## Golf Courses Extras

### **Overview**

This section describes how to configure golf course extras in the system. The setup controls how golf rounds are created, priced, and linked to suppliers, ensuring that golf courses can be added to bookings with the correct parameters.

***

### **Purpose**

This configuration is used to:

* Define general settings for the **golf course extra**.
* Link the product to the correct **supplier**, **currency**, and pricing setup.
* Manage visibility and sales restrictions.
* Configure the number of rounds and any related product linking.
* Support automated billing (if enabled in your setup).

***

### **Instructions and field explanations**

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (35).png" alt=""><figcaption></figcaption></figure>

#### **Basic setup section**

| Field                  | Description                                                    | Instructions                                                                                                                                                                                                                                                                                                                                                                               |
| ---------------------- | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Name**\*             | Internal name of the golf course setup.                        | Enter a clear name for identification (for example, _GolfCourses_).                                                                                                                                                                                                                                                                                                                        |
| **List Name**\*        | Name shown in lists or selection menus.                        | Usually the same as **Name**.                                                                                                                                                                                                                                                                                                                                                              |
| **Code**\*             | Unique internal code for the extra.                            | Should be unique and aligned with your internal naming conventions.                                                                                                                                                                                                                                                                                                                        |
| **Status**             | Controls whether the extra is available for sale.              | Choose **Visible** to make it available, or **Hidden** to disable it.                                                                                                                                                                                                                                                                                                                      |
| **Stop sales hours**   | Stops sales a set number of hours before the service starts.   | Enter a numeric value (for example, `24` for 24 hours before).                                                                                                                                                                                                                                                                                                                             |
| **Minimum length**     | Minimum number of days or rounds allowed.                      | Leave empty if not applicable.                                                                                                                                                                                                                                                                                                                                                             |
| **Contract Type**      | Contract or pricing model.                                     | Select an appropriate contract type if required by supplier/contract setup.                                                                                                                                                                                                                                                                                                                |
| **Days prices option** | Number of days forward that prices should be calculated/shown. | Commonly `0` (depends on your rules).                                                                                                                                                                                                                                                                                                                                                      |
| **Allotment Type**     | Specifies the availability model (Generic, Manual, etc.).      | <p>If you use time slots for requested tee times, select <strong>Generic</strong> and define the time-slot pattern and allotment. <em>Guests can then choose a requested tee time.</em></p><p>The allotment number controls how many requests can be made per time slot. In many setups, this is set to a high value to avoid unnecessary limitations (for example, <code>100</code>).</p> |
| **Extras Category**\*  | Extra category this product belongs to                         | Select the golf course category you created (for example, **Golf Course**).                                                                                                                                                                                                                                                                                                                |
| **Age**                | Age rule (if age-based restrictions exist)                     | Select an age rule or leave blank if not used.                                                                                                                                                                                                                                                                                                                                             |
| **Period/Trip length** | Defines which trip lengths the extra applies to (if relevant). | Select from available options if required.                                                                                                                                                                                                                                                                                                                                                 |
| **SSR Codes**          | Special Service Request codes (integrations).                  | Select relevant values (often **NoSSR** unless integrations require otherwise).                                                                                                                                                                                                                                                                                                            |

#### **Supplier and pricing section**

| Field                       | Description                                                      |
| --------------------------- | ---------------------------------------------------------------- |
| **Select supplier**         | The supplier providing the golf service.                         |
| **Round Rule**              | Defines how rounds are calculated or grouped.                    |
| **One-way (only)**          | Restricts the extra to either one-way or non-one-way transports. |
| **Currency**                | Currency used for pricing.                                       |
| **Maximum length**          | Maximum booking duration or number of rounds.                    |
| **Currency prices**         | Enables currency-based pricing.                                  |
| **Show supplier on ticket** | Prints supplier name on customer documents (if enabled).         |
| **Display allotment**       | Shows remaining allotment in Office booking (where supported).   |

#### **Right-side panels**

**Custom Text**

Used for terms, conditions, or additional notes that should appear on documents or vouchers (depending on configuration).

**Automatic Billing**

Enables automatic billing setup for this extra.

Configure if the system should automatically generate invoices or charges for the golf course booking.

**Golf Course**

| Field                | Description                                                                    |
| -------------------- | ------------------------------------------------------------------------------ |
| **Rounds**           | Maximum number of rounds for one booking. Valid numbers are 1 to 99            |
| **Product Child ID** | Use a ProductID if you want to reuse generated allotment from another product. |

**Behaviour Settings**

Configuration that controls how the extra behaves during selection or booking.

**Other Settings**

Additional technical settings (advanced use).

***

### Prices

Golf products are priced using **Extras Prices** when this pricing model is used. In that case, golf rounds are priced directly through the standard extras price setup.

#### Purpose

This approach allows pricing to be fully managed within the **Extras Prices** tab of the golf extra, reducing setup complexity and keeping pricing aligned with other standard extras.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

## Golf Course Packages

### Overview

Golf course extras can either be sold individually or be included as part of a golf package. This feature ensures that golf rounds intended exclusively for packages are not displayed as standalone golf courses during the booking process.

The purpose is to prevent customers from selecting package-only golf rounds unless they have already selected the package that contains them.

{% hint style="warning" %}
Golf courses are currently **not supported in WebBooking**. This functionality applies to the Tourpaq booking application.
{% endhint %}

***

## How It Works

When the **Golf Courses** page is displayed during booking, Tourpaq determines which golf course extras should be available.

The visibility rules are based on the configured price of the golf extra.

| Golf Extra Configuration | Behaviour                                                       |
| ------------------------ | --------------------------------------------------------------- |
| Price greater than 0     | Always displayed if the golf extra is eligible for the booking. |
| Price equals 0           | Displayed only if it is included in a selected package.         |

If a selected package is later removed, any golf course extras that were available solely because of that package are immediately removed from the Golf Courses page.

***

## Eligibility Logic

### Package Eligibility

A package is considered **eligible** for a booking if **at least one extra** contained in the package is eligible.

If **none of the extras** in the package are eligible, the package is not applied.

#### Example

Package **Golf Weekend** contains:

* Extra 1 (eligible)
* Extra 2 (not eligible)
* Extra 3 (not eligible)

Because **Extra 1** is eligible, the package is applied.

If none of the extras were eligible, the package would not be available.

***

## Configuration

Extras Golf courses that should appear on the **Golf Courses** page are configured as:

* **Extras Category = Golf**&#x20;

<figure><img src="../../.gitbook/assets/extras ec.png" alt=""><figcaption></figcaption></figure>

Golf Package- **must not** use the **Golf** extras category.

Instead, they are configured using **any other Extras Category** and are linked to an **Extras Package**.

Typically a package is configured as follows:

*   Extras Category = Any category except **Golf**&#x20;

    <figure><img src="../../.gitbook/assets/pack ec.png" alt=""><figcaption></figcaption></figure>
*   Price should not be 0&#x20;

    <figure><img src="../../.gitbook/assets/pack price.png" alt=""><figcaption></figcaption></figure>
*   Contain more then one Extras&#x20;

    <figure><img src="../../.gitbook/assets/pack content.png" alt=""><figcaption></figcaption></figure>

Golf rounds that should be sold individually are configured with:

* Extras Category = Golf
* Normal selling price

***

## Booking Behaviour

### Case 1 - Golf course sold individually

A golf extra with a price greater than zero is always available for selection when it is valid for the booking.

#### Example

| Golf Extra |   Price | Result                             |
| ---------- | ------: | ---------------------------------- |
| Golf X     | 600 DKK | Displayed on the Golf Courses page |

The customer can purchase the golf round independently.

***

### Case 2 - Golf course included in a selected package

A golf extra with a price of zero is hidden unless the package containing it has been selected.

#### Example

Package selected:

**Mallorca Golf Package**

Included extras:

* Extra 1
* Extra 2
* Extra 3
* Extra 4

| Golf Extra |   Price | Result    |
| ---------- | ------: | --------- |
| Golf X     | 600 DKK | Displayed |
| Extra 1    |   0 DKK | Displayed |
| Extra 2    |   0 DKK | Displayed |
| Extra 3    |   0 DKK | Displayed |
| Extra 4    |   0 DKK | Displayed |

The customer now sees both individually purchasable golf rounds and the package extras included with the selected package.

***

### Case 3 - No package selected

If no package has been selected, golf extras with a price of zero remain hidden.

#### Example

| Golf Extra |   Price | Result    |
| ---------- | ------: | --------- |
| Golf X     | 600 DKK | Displayed |
| Extra 1    |   0 DKK | Hidden    |
| Extra 2    |   0 DKK | Hidden    |
| Extra 3    |   0 DKK | Hidden    |
| Extra 4    |   0 DKK | Hidden    |

Only golf rounds that can be purchased individually are shown.

***

### Case 4 - Package removed

If a previously selected package is removed from the booking, all golf extras that were available exclusively through that package are removed from the Golf Courses page.

#### Example

Before removing the package:

* Golf X
* Extra 1
* Extra 2
* Extra 3
* Extra 4

After removing the package:

* Golf X

The package-only extras are no longer available because they are no longer included in the booking.

***

## Example Scenario

The following configuration is used:

| Golf Extra | Description                    |   Price |
| ---------- | ------------------------------ | ------: |
| Golf X     | Individual golf round          | 600 DKK |
| Extra 1    | Golf round included in package |   0 DKK |
| Extra 2    | Golf round included in package |   0 DKK |
| Extra 3    | Golf round included in package |   0 DKK |
| Extra 4    | Golf round included in package |   0 DKK |

#### Without a package

Customers only see:

* Golf X

#### After selecting a package

Customers see:

* Golf X
* Extra 1
* Extra 2
* Extra 3
* Extra 4

#### After deselecting the package

Customers again see only:

* Golf X
