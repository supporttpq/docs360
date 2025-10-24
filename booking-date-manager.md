# Booking Date Manager

#### **Overview**

The **Booking Date Manager** page provides an overview of all bookings within a selected time frame. It allows users to filter, view, and adjust booking dates for specific hotels and brands. The tool is particularly useful for managing booking periods and aligning them with the corresponding departure dates.

#### **Purpose**

This page is designed to help travel operators easily monitor and modify booking-related information. It ensures that booking and departure dates are correctly aligned and allows the user to filter results based on various parameters, such as brand, date range, and hotel.\
Administrators can use this page to quickly view all bookings made during a specific period and make necessary updates before saving the changes.

***

#### **Fields and Filters**

<figure><img src=".gitbook/assets/image (430).png" alt=""><figcaption></figcaption></figure>

| **Field**                  | **Description**                                                                                                                                           |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Brands**                 | Dropdown list to select the desired brand (e.g., _Tourpaq DK_). All data displayed will correspond to the selected brand.                                 |
| **Booking start**          | Defines the start date for the booking period to be displayed. Only bookings made on or after this date will be shown.                                    |
| **Booking end**            | Defines the end date for the booking period to be displayed. Only bookings made on or before this date will be shown.                                     |
| **Departure start**        | Optional filter allowing the user to set the earliest departure date for the bookings to be displayed.                                                    |
| **Departure end**          | Optional filter allowing the user to set the latest departure date for the bookings to be displayed.                                                      |
| **Hotels**                 | Allows the selection of specific hotels for which bookings will be listed. The **Edit** button opens a selection dialog to choose one or multiple hotels. |
| **Display**                | Once all filters are defined, press **Display** to apply them and show the matching bookings in the table below.                                          |
| **+ More filters / Clear** | Add additional filtering options or clear all active filters. The counter (e.g., “3”) shows how many filters are currently active.                        |

***

#### **Table Columns**

| **Column**            | **Description**                                                                                                    |
| --------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **Booking No**        | Displays the booking number. Each booking number is clickable, allowing direct access to the booking details page. |
| **Booking Date**      | The date when the booking was made.                                                                                |
| **Departure Date**    | The date when the customer’s trip departs.                                                                         |
| **Alt. Booking Date** | Alternative booking date, if defined. This can be adjusted to update specific booking information.                 |
| **Hotel**             | The name of the hotel included in the booking.                                                                     |
| **Transport**         | Information about the transport option (e.g., flight or route code) associated with the booking.                   |

***

#### **Buttons and Actions**

| **Button / Action**     | **Description**                                                                                                                                                            |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Save**                | After making any updates to the alternative booking dates, press **Save** to confirm and store the changes.                                                                |
| **Pagination controls** | Located at the bottom of the page. They allow users to navigate between pages of booking records and adjust the number of bookings displayed per page (e.g., 25 per page). |

***

#### **💡 Tip**

* To ensure accurate results, always set both **Booking start** and **Booking end** dates before pressing **Display**.
* You can click on a **Booking No** to open a detailed view of that booking.
* If the system finds matching bookings, the total number (e.g., _Found 13 bookings_) will appear above the table.
