# Hotel combination

#### Overview

A **hotel combination** is a type of itinerary where a customer stays in multiple hotels during a single holiday. For example, a customer might spend two days in one hotel and five days in another. The hotels used in a combination must already exist in the **Tourpaq system**.

Unlike regular hotels, combination hotels **do not have their own allotments**. Instead, they rely on the allotments of the individual hotels defined in the itinerary.

#### Purpose

The hotel combination feature allows agencies to offer multi-hotel packages, providing flexibility in designing holiday itineraries while maintaining accurate pricing and allotments from existing hotels.

#### How to Define a Hotel Combination

1.  **Create a New Hotel Combination**

    * Add a new hotel in the same way as a regular hotel.
    * Make sure to **check the "Hotel Combination"** checkbox.

    <figure><img src=".gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>
2.  **Add Hotel List and Transport**

    * Navigate to the **Hotel Combination tab**.

    <figure><img src=".gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

    * Define the list of hotels the customer will stay in. **The order matters**: the first hotel in the list is where the customer will start their stay.
    * Multiple hotels can be added.
    * Optionally, assign transports to the hotel combination; this restricts the combination to specific transport services.

    **Single-Hotel Option:**

    * If only one hotel is in the list, a checkbox will appear.
    * Checked: the hotel appears on the ticket.
    * Unchecked: the main hotel appears instead.
3.  **Assign Rooms**

    * Each hotel has multiple room types.
    * Hotel combinations also have room types, but these are placeholders (“fake” rooms).
    * Map the combination hotel rooms to the actual rooms in the **Hotel Combination Room tab**.

    <figure><img src=".gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

    **Room Mapping Grids:**

    * **Grid 1:** Map combination rooms to regular hotel rooms. Rooms must match specifications closely.
    * **Grid 2:** Map transports with intervals to hotels. Specify the number of days the customer will spend at each hotel per interval.

    **Example:**

    * Transport **BLLPVK-A7-5A** has 4 intervals:
      * Interval 1: 7 days
      * Interval 2: 14 days
      * Interval 3: 21 days
      * Interval 4: 28 days
    * A customer booking interval 1 could stay 4 days in **SIV150** and 3 days in **AGI150**.
    * Interval 2 could split evenly: 7 days in each hotel.
    * These day distributions are **predefined**; customers cannot change them.
4. **Create Price List**
   * Once rooms, hotels, and transports are defined, create a **price list** for the combination.
   * **Important:** After the price list is created, you cannot change the hotels, rooms, or transport.
   * Ensure allotments exist for the itinerary hotels; otherwise, the price list cannot be generated.

#### Troubleshooting Price List Generation

1. **Check Regular Hotel Allotments**
   * Navigate to: `Hotel → Hotel (SIV150/AGI150) → Allot.`
   * Verify that allotments exist for the required period, room, and quantity.
2. **Check Transport Allotments**
   * If creating a price list for a specific date (e.g., 07.06.2026) fails, the transport may not have an allotment on that date.
   * Add an allotment in **Fixed Quota** and recreate the price list.
