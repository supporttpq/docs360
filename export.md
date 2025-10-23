# Export

The **Export** page allows users to generate and download booking-related data in Excel format.\
It provides multiple export types and filtering options to include or exclude specific bookings and cost details.\
Exports are generated as `.XLSX` files and can be used for analysis, accounting, or reporting purposes.

***

#### **Export Types**

There are **three export types** available:

| **Export Type**      | **Description**                                                                                                                                                             |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Bookings (XLSX)**  | Exports all bookings within the selected booking or departure period, including general booking details.                                                                    |
| **Discounts (XLSX)** | Exports information related to discounts applied to bookings. Useful for financial reconciliation and promotion analysis.                                                   |
| **Cost (XLSX)**      | Exports all costs associated with bookings, including **Creditor information**. This report is typically used for cost control, supplier invoicing, and financial overview. |

***

#### **Fields and Filters**

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

| **Field**                                                      | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Export Type**                                                | Selects which type of data to export: _Bookings_, _Discounts_, or _Cost_.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Booking start / Booking end**                                | Defines the range based on the **booking creation date**. Only bookings created between these dates are included.                                                                                                                                                                                                                                                                                                                                                                                 |
| **Departure start / Departure end**                            | Filters bookings based on the **departure date**. Only bookings departing within this range are included.                                                                                                                                                                                                                                                                                                                                                                                         |
| **Include Cancelled Bookings and Details**                     | When enabled, cancelled bookings and their related details will also be included in the export.                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Include Moved Bookings and Details**                         | Includes bookings that were moved to a different departure or travel period, along with their updated details.                                                                                                                                                                                                                                                                                                                                                                                    |
| **Include past bookings with changes in the departure period** | <p>Ensures that bookings with <strong>changes made after the departure date</strong> are included if the changes fall within the selected departure period.<br><strong>Tooltip:</strong> <em>This will include bookings where changes are made after the departure, and the changes are made in the departure period specified.</em><br><br>🔹 This option is <strong>available for Bookings and Cost exports</strong>.<br>🔸 This option is <strong>disabled for Discounts exports</strong>.</p> |
| **More filters**                                               | Expands additional filtering options (if available).                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Clear**                                                      | Resets all filters and date selections.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

***

#### **Buttons and Actions**

| **Button**         | **Description**                                                                                                               |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| **Export**         | Generates the export file based on the selected filters and export type. The exported file is downloaded in `.XLSX` format.   |
| **Show Schedules** | Displays a list of all previously generated or scheduled exports. From here, users can monitor progress or re-download files. |

***

#### **Usage Example**

**Scenario:** Export booking and cost data for bookings created in September and October 2025, including changes after departure.

1. Set **Export Type → Bookings (XLSX)** or **Cost (XLSX)**.
2. Define **Booking start** and **Booking end** dates (e.g., 23-09-2025 to 23-10-2025).
3. (Optional) Define **Departure start** and **Departure end**.
4. Enable **Include past bookings with changes in the departure period** to capture all post-departure updates.
5. Enable or disable _Canceled_ and _Moved_ bookings as needed.
6. Click **Export** to generate the report.
7. Use **Show Schedules** to view or download previous exports.

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption><p>Export Booking (XLSX)</p></figcaption></figure>

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption><p>Export Cost (XLSX)</p></figcaption></figure>

<figure><img src=".gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption><p>Export Discounts (XLSX)</p></figcaption></figure>

The data will contain information regarding each booking that corresponds to the given filters:

* **Booking number -** A unique identifier assigned to each booking.
* **Adults number -** The total number of adults included in the booking.
* **Children number -** The number of children included in the booking.
* **Infants number -** The number of infants included in the booking.
* **Seats -** The number of seats reserved for the booking.
* **Booking date -** The date when the booking was created.
* **Booking status -** The current status of the booking (e.g., Confirmed, Cancelled, Pending).
* **Booking total price -** The total price paid for the booking, including all products and services.
* Customer No - The custumer's number.
* Customer name - Name of the customer
* **Customer e-mail -** The primary email address of the customer.
* **Seller -** The individual or platform that made the booking.
* **Agent -** The travel agent or representative involved in the booking, if any.
* **Transport code -** A code identifying the mode or provider of transport.
* **Travel length -** The total duration of the trip in days.
* **Hotel code -** A code representing the booked hotel.
* **Resort code -** A code identifying the resort associated with the hotel.
* **Destination** - The booking destination of the travelers
* **Room code -** A code for the specific room type booked.
* **Room price -** The cost of the room per booking or per night, depending on context.
* **Rooms number -** The number of rooms included in the booking.
* **Gender -** The gender of the passenger.
* **Age -** The age of the passenger at the time of travel.
* **First name -** Passenger’s first name.
* **Last name -** Passenger’s last name.
* **Passenger’s status -** The role or status of the passenger.
* **Customer postcode -** Postal code of the customer’s address.
* **Customer fax -** Fax number provided by the customer.
* **Customer phone number -** Contact phone number of the customer.
* **Customer CPR -** The customer’s CPR (civil registration number or ID, depending on locale).
* **Customer city -** The city in which the customer resides.
* **Customer address -** The full street address of the customer.
* **Has cancellation insurance -** Indicates whether cancellation insurance was purchased (Yes/No).
* **Cancellation insurance price -** The cost of the cancellation insurance.
* **Has transfer -** Indicates whether a transfer service (e.g., airport shuttle) is included.
* **Transfer price -** The price paid for transfer services.
* **Travel insurance type -** The type or tier of travel insurance selected.
* **Travel insurance price -** The price of the travel insurance policy.
* **VIP product—**&#x53;pecifies if a VIP product or service was included.
* **VIP product price -** The cost associated with the VIP product.
* **Party package product -** Indicates if a party package was added to the booking.
* **Party package product price -** The price of the party package product.
* **Pension product -** Describes whether a pension/meal plan product was booked.
* **Pension product price -** The price for the pension product.
* **Catering product -** Shows if a catering or food service product was included.
* **Catering product price -** The cost of the catering product.
* **Car product -** Indicates if a rental car or car-related product was booked.
* **Car product price -** The total price for the car product.
* **Extra bed discount -** Discount applied for an extra bed, if applicable.
* **Cancellation fee -** Any fee charged for cancelling the booking.
* **Passenger total price -** The total price assigned to a specific passenger.
* **Departure date -** The date of departure from the origin location.
* **Arrival home date -** The date the traveler returns home.
* **Discounts/Supplements -** Any discounts or additional charges applied.
* **Other products -** Additional products included in the booking not listed above.
* **Transport costs -** Total costs related to transportation.
* **Transfer cost -** Total cost for transfer services.
* **VIP cost -** Total cost for VIP services.
* **Party package cost -** Total cost for party package.
* **Pension cost -** Total cost for pension/meal plan.
* **Catering cost -** Total cost for catering or food service.
* **Car cost -** Total cost of car rental or car services.
* **Other products cost -** Cumulative cost of all other additional products.
* **Insurance cost -** Total cost of all types of insurance (travel, cancellation, etc.).
* **Discounts/Supplements cost -** Total value of discounts and supplements applied.
* **Hotel cost -** Total cost paid for the hotel accommodation.
