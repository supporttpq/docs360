# Golf Courses

### Overview

The **Golf Courses** page allows you to manage golf-related activities linked to a specific booking. It is used to assign passengers to golf rounds, define their handicaps and club numbers, and set up golf course reservations including prices and times.

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

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

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
