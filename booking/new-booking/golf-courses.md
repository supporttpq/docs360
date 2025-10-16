# Golf Courses

## Golf Courses Booking page

### Overview

The **Golf Courses** page allows you to manage golf-related activities linked to a specific booking. It is used to assign passengers to golf rounds, define their handicaps and club numbers, and set up golf course reservations, including prices and times.

This feature ensures that golf course participation and scheduling are accurately recorded and communicated between the travel agency, the customer, and the golf provider.

### Purpose

* To record which passengers are participating in golf activities.
* To manage player information such as **Handicap (HCP)** and **Club** number.
* To add and schedule golf course rounds with pricing and timing details.
* To centralize golf-related booking data for reporting and confirmation.

**Preconditions**

* A booking must be created and saved with at least one passenger.
* The booking must contain an **extra product** that uses a golf course reservation system.
* The product must have pre-configured availability (time slots) in the system.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Instructions

#### 1. Passengers List Section

This section lists all passengers in the booking and allows you to configure their golf-related details.

| Field               | Purpose                                                        | Instructions                                                                                                           |
| ------------------- | -------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Passenger**       | Displays all passengers included in the booking.               | Each passenger appears automatically based on the booking details.                                                     |
| **Golf (checkbox)** | Marks whether the passenger participates in a golf activity.   | Tick the box if the passenger will play golf. Only selected passengers will appear in the **Golf Courses List** below. |
| **HCP (Handicap)**  | Indicates the passenger’s golf handicap.                       | Enter the numeric handicap value (e.g., 5).                                                                            |
| **Club**            | Identifies the club number or associated golf club membership. | Enter the club number (e.g., 2). This field can also be used to track club equipment if applicable.                    |

***

#### 2. Golf Courses List Section

This section displays the details of the golf rounds added for the selected passengers.

| Field                 | Purpose                                                                 | Instructions                                                                                                                                                        |
| --------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Golf Course**       | Name of the golf course where the round will be played.                 | This is automatically populated when you add a course.                                                                                                              |
| **Round**             | Identifies the specific round (e.g., Round 1, Round 2).                 | Maximum number of rounds for one booking. Valid numbers are 1 to 10. Use the **plus icon (+)** to add an additional round or the **trash icon (🗑)** to delete one. |
| **Passenger**         | Displays which passenger is assigned to the specific golf round.        | Automatically linked to the passenger(s) who have Golf checked in the list above.                                                                                   |
| **Price (DKK)**       | The cost per passenger or round.                                        |  Show the price per round for each golf participant. The total is calculated automatically at the bottom.                                                           |
| **Request Date/Time** | The time the guest request to play the round.                           | Use the date picker to select the requested date and start time. You can use the copy icon to group the guests by assigning the same time.                          |
| **Confirmed Time**    | The confirmed time for the golf course.                                 | Select the confirmed time once the booking has been validated. You can use the **copy icon** to duplicate the same time to all passengers.                          |
| **Total**             | Displays the total amount for all passengers and rounds in the booking. | Automatically calculated based on individual prices.                                                                                                                |

***

#### 3. Buttons and Icons

| Element               | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| **Add Golf Course**   | Opens a new entry to add another golf course to the booking. |
| **➕ (Add Round)**     | Adds a new round for the same course.                        |
| **🗑 (Delete Round)** | Removes a round from the course.                             |
| **📋 (Copy Icon)**    | Copies the date/time value to all similar entries below.     |

***

## Ticket

The ticket contains all relevant information for guests who have booked golf courses through the system.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The ticket shall list all information relevant to the golf booking, such as:

* Guest name(s)
* Golf course name
* Number of booked rounds (free and paid, if applicable)
* Requested and confirmed tee times
* Booking reference
* Included Extras or packages
* Supplier or course contact information (if applicable)

#### Example Workflow

1. **Select Golf Players**
   * Tick the **Golf** checkbox for each passenger playing golf.
   * Fill in **HCP** and **Club** fields for each selected player.
2. **Add Golf Course**
   * Click **Add Golf Course**.
   * Enter course details, add a round, and assign the passengers.
3. **Set Dates and Times**
   * Choose a **Request Date/Time** when the customer wants to play.
   * Once confirmed by the provider, fill in the **Confirmed Time**.
4. **Review Total**
   * The total amount in **DKK** is automatically updated.
   * Verify accuracy before saving or sending confirmation.

***

#### Notes

* Only passengers with the **Golf** box checked appear in the Golf Courses List.
* **Request Date/Time** and **Confirmed Time** can differ depending on course availability.
* Ensure all prices and times are confirmed before issuing final documentation to customers.
* You can add multiple golf courses per booking (e.g., for multi-day trips).

## **Golf Courses Extra Category**

The **Extras Category** page is used to configure and manage extra services offered to customers — in this case, **Golf Courses**.

The **Type** defines the behaviour of the Extra. In this case, the **Type** must be set to **“Golf”**.

Once the Type is defined as _Golf_, you can create one or more extra **categories** that use this type. The category determines how the Golf Extras are grouped and managed within the system. This configuration determines how the golf product behaves in the booking system and which rules apply to it.

Each extra category can be customized per brand and contains general, visual, and technical settings for booking, visibility, and integration.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Example Workflow

1. Go to **Extras → Categories →Create**.
2. Set **Name** to _Golf Course_ and **List Name** to _Golf_.
3. Assign **Code** as _Golf\_GRG_.
4. Keep **Status** as _visible_ and **Behavior on Web** as _Step1: Always Show_.
5. Select **Category Type** → _Golf_.
6. Check **Accepts multiple product selection** to allow several rounds per passenger.
7. Add a **Description** and upload an **Image** for better presentation in the web booking portal.
8. Click **Save** to confirm.

***

### Notes

* Always ensure the **Code** is unique before saving.
* The **Behavior on Web** and **Accepts multiple product selection** options are essential for correct golf course behavior in the booking flow.
* Use the **Sold Out Text** field to communicate availability clearly to customers.
* The **Description** should be detailed and include rules, price inclusions, and restrictions.

## Golf Courses Extras

### **Overview**

The **GolfCourses** page is used to configure and manage golf course extras within the system. This setup defines how golf rounds are created, priced, and linked to suppliers. It ensures that golf courses can be added to bookings with correct parameters, pricing rules, and behavior settings.

***

### **Purpose**

The purpose of this configuration is to:

* Define the general information and settings for the **Golf Course extra**.
* Link the product to the correct **supplier**, **currency**, and **pricing rules**.
* Manage visibility, sales restrictions, and allotment options.
* Set the number of rounds and related product child IDs for the golf course.
* Customize behavior and billing automatically for streamlined operations.

***

### **Instructions and Field Explanations**

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Basic Setup Section**

| Field                  | Description                                                     | Instructions                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ---------------------- | --------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**\*             | Internal name of the golf course setup.                         | Enter a clear name for identification (e.g., _GolfCourses_).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **List Name**\*        | Name displayed in listings or selection menus.                  | Usually the same as “Name.”                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Code**\*             | Unique internal code for the extra.                             | Should match the product or service code (e.g., _GolfCourses_).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Status**             | Controls visibility of the extra in the system.                 | Choose **Visible** to make it available for sale or **Hidden** to disable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Stop sales hours**   | Defines how many hours before service start sales should stop.  | Enter a numeric value (e.g., _24_ for 24 hours before service).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Minimum length**     | Minimum number of days or rounds allowed for booking.           | Leave empty if not applicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Contract Type**      | Defines contract or pricing type.                               | Select from the available contract types if specific to supplier or agreement.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Days prices option** | Sets the number of days for which price visibility is allowed.  | Usually set to _0_ for immediate availability.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Allotment Type**     | Specifies the allotment source (Generic, Manual, etc.).         | <p>Select <strong>Generic.                             -</strong> This option allows the Agency to define available time slots for golf bookings — for example, every hour with a total of 100 allotments.</p><ul><li>Guests can select one of these time slots as their <strong>requested tee time</strong>.</li></ul><ul><li>The <strong>allotment number</strong> determines how many requests can be made for a specific hour. While it can be used to limit the number of bookings, it is generally recommended to set a high value (for example, 100) to ensure availability.</li></ul> |
| **Extras Category**\*  | Type of extra being configured.                                 | Select **Golf Course** to categorize it correctly.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Age**                | Defines the applicable age range (if age-based pricing exists). | Select from available age ranges or leave blank if not applicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Period/Trip length** | Defines duration type for the extra.                            | Select from available options if the service depends on trip length.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **SSR Codes**          | Defines special service request codes used in integrations.     | Choose relevant **NoSSR** or other SSR types if needed.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |

#### **Supplier and Pricing Section**

| Field                       | Description                                                                                                                                                   |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Select supplier**         | The supplier providing the golf course service.                                                                                                               |
| **Round Rule**              | Defines how rounds are calculated or grouped.                                                                                                                 |
| **One-way (only)**          | This sets the extra to function either                    - on "one way" transports only;                              - or on "non one way" transports only. |
| **Currency**                | The currency used for pricing.                                                                                                                                |
| **Maximum length**          | Sets the maximum booking duration or number of rounds.                                                                                                        |
| **Currency prices**         | Enables currency-based pricing.                                                                                                                               |
| **Show supplier on ticket** | Displays the supplier’s name on the customer’s ticket.                                                                                                        |
| **Display allotment**       | This will display the allotment of the Extra in Office booking when you edit "Transport"                                                                      |

#### **Right-Side Panels**

**Custom Text**

Allows entering specific text related to the golf course (e.g., terms, conditions, or additional notes).\
Use it for customized display messages on documents or tickets.

**Automatic Billing**

Enables automatic billing setup for this extra.\
Configure if the system should automatically generate invoices or charges for the golf course booking.

**Golf Course**

This section defines the main golf course parameters:

| Field                | Description                                                                  |
| -------------------- | ---------------------------------------------------------------------------- |
| **Rounds**           | Maximum number of rounds for one booking.                                    |
| **Product Child ID** | Fill ProductID when you want to use generated allotment from another Product |

**Behaviour Settings**

Contains configuration options controlling how the extra behaves during selection or booking.

**Other Settings**

Additional technical or advanced options for internal configuration.

### Prices

The **Generic Product Price Rules** are used to define the **price per golf round**.\
Each rule specifies how the price is calculated and applied to the corresponding golf course Extra.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
