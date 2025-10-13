# Stop Sales

### Definition <a href="#definition" id="definition"></a>

A supplier can remove a hotel room from selling by creating a stop sale for that room. He can do that by going to the Stop Sale page and filling in the filters for that room and the period. The stop sale will run for each date and reduce the number of rooms available. It is not possible to make Stop Sale for secured and guaranteed rooms.&#x20;

### **Overview**

The **New Stop Sale** page allows users to create a stop sale for specific hotels and room types within a selected date range.\
A _stop sale_ prevents new bookings for the specified period — it is typically used when a hotel reaches full occupancy or temporarily stops accepting reservations.

### **Purpose**

Use this function to:

* Block sales for specific hotels or room types.
* Control booking availability during peak demand, maintenance periods, or overbooking situations.
* Ensure the system does not allow new reservations for dates under stop sale.

### **How to Access**

Navigate to:\
**Stop Sales → Create New Stop Sale**

### **Field Descriptions**

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

| **Field**      | **Description**                                                                                                                                                                                                                                                                                          |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Start date** | <p>Defines the first day of the stop sale period.<br>Use the calendar icon to select a date.</p>                                                                                                                                                                                                         |
| **End date**   | <p>Defines the last day of the stop sale period.<br>The stop sale will be active from the <strong>Start date</strong> through the <strong>End date</strong>, inclusive.</p>                                                                                                                              |
| **Brand**      | <p>Select the brand to which the stop sale applies.<br>If your system manages multiple brands, this allows precise control.<br>Default: <em>All brands</em>.</p>                                                                                                                                         |
| **Hotel**      | <p>Select the hotel affected by the stop sale.<br>Hotels are listed by code and name.</p>                                                                                                                                                                                                                |
| **Room Type**  | <p>Select one or multiple room types that will be blocked for sale.<br>If no room type is selected, the stop sale applies to the entire hotel.</p>                                                                                                                                                       |
| **Note**       | <p>Add a comment describing the reason for the stop sale (e.g., <em>Fully booked</em>, <em>Maintenance</em>, <em>Renovation</em>).<br>Used for internal reference and reporting.      This field is optional and will respect the settings for the mandatory stop sale note set in the System Setup.</p> |

***

### **Example**

To stop sales for **Inside Elounda** on **13 October 2025** for room type _DBL.VM_, fill the form as follows:

| Field      | Value                              |
| ---------- | ---------------------------------- |
| Start date | 13-10-2025                         |
| End date   | 13-10-2025                         |
| Brand      | All brands                         |
| Hotel      | 107754 – Inside Elounda            |
| Room Type  | DBL.VM                             |
| Note       | Fully booked for the selected date |

Then click **Save** to create the stop sale.

***

### **Important Notes**

* All fields marked with a red asterisk (\*) are mandatory.
* If the **Note** field is left empty, and the setting from System Setup (Stop sale note mandatory) is checked,  an error message _“Note is required”_ will appear.
* The stop sale is effective immediately after saving and will appear in the **Stop Sales Overview**.

\-----------------------------------------------------------------------------------------------------------------------

If the guaranteed rooms are filled and are more than the booked rooms number, the available rooms number is reduced to the guaranteed rooms number. If the guaranteed rooms are not filled or the booked rooms number is bigger, the available rooms number is reduced to the booked rooms number.

### **Scenarios**

| Available rooms before stop sale | Guaranteed rooms number | Booked rooms Number | Available rooms after stop sale |
| -------------------------------- | ----------------------- | ------------------- | ------------------------------- |
| 10                               | 5                       | 4                   | 5                               |
| 10                               | 5                       | 6                   | 6                               |
| 10                               | -                       | 6                   | 6                               |
| 10                               | -                       | 10                  | 10                              |

After the 'Stop Sale' is created, the supplier will be redirected automatically to the 'Hotel Allotment' page so he can see the changes that have been made. Here the filter will be autofilled.

<figure><img src=".gitbook/assets/image (66) (1).png" alt=""><figcaption></figcaption></figure>

A stop sale can be made for all the rooms of the hotel, but the system will treat and save every room as a separate stop sale.

### **Stop Sale Service**

There is a new service that verifies all stop sales created, which includes future dates, and checks if a room (or more) has been canceled. If this is the case, it reduced the rooms available after the rules displayed earlier. To filter out a specific stop sale from the service, go to the "Hotel" menu, Stop Sales page, and click "Disable" for that stop sale.

### **Stop Sale Log**

As an administrator, you can see the stop sales changes and logs from the release/stop sale logs from the hotel tab. The last column specifies if the log has been made from the release, from the stop sale, or from the stop sale service.

<figure><img src=".gitbook/assets/image (67) (1).png" alt=""><figcaption></figcaption></figure>

### **Stop Sale on Notification**

There is a new tab in the notification where the new stop sales created are listed.

<figure><img src=".gitbook/assets/image (68) (1).png" alt=""><figcaption></figcaption></figure>

In this tab you can see all the stop sales created. For each one, you have the option to **view details**.

<figure><img src=".gitbook/assets/image (69) (1).png" alt=""><figcaption></figcaption></figure>

If you choose the **View Details** for one of those stop sales, the system will redirect you to the log page, fill the filters with data from the stop sale, and display the changes.

### **Stop sales in Admin**

In the "Stop Sale" page from the hotel menu, it can be seen that all the stop sales, including the ignored ones, can be seen. The ignored "stop sales" can be seen with a red background. Here you can disable/enable a stop sale. If you disable a stop sale, the stop sale service filters it out so that the allotments of the hotel can be changed.

<figure><img src=".gitbook/assets/image (3) (2).png" alt=""><figcaption></figcaption></figure>

In the "Stop sales" page from the Hotel menu, it can be seen all the Stop Sales including the ignored ones. The Ignored "Stop sales" can be seen with a red background. Here you can disable/enable a stops sale. If you disable a stop sale, the Stop sale service filters out it so that the allotments of the Hotel can be changed.

#### Filters & Search

At the top of the screen, a filtering panel is provided to refine the stop sale records:

* **Start Date / End Date**: Specify the date range for viewing stop sales.
* **Create Date**: Filter records by the date they were created.
* **Hotels**: Use the "Edit" button to select one or more hotels.
* **Rooms**: Filter by room types.
* **Supplier Name**: Search by the supplier's name.
* **Show All**: Check this box to remove filters and show all records.
* **Display**: Applies the current filter settings.
* **More Filters**: Expands additional filter options.
* **Clear**: Clears all selected filters.

#### Data Table

The main table displays a list of stop sale entries with the following columns:

| Column Name      | Description                                                                       |
| ---------------- | --------------------------------------------------------------------------------- |
| Edit ✏️          | Edit the Stop Sale                                                                |
| **View Details** | Link to detailed view and edit form for each stop sale record.                    |
| **Start / End**  | The date range during which the stop sale is in effect.                           |
| **Hotel**        | The hotel affected by the stop sale.                                              |
| **Room**         | Specific room category to which the stop sale applies.                            |
| **Supplier**     | The supplier associated with the stop sale record.                                |
| **Hidden**       | Indicates whether the stop sale is hidden from visibility (`✔️` = Yes, `❌` = No). |
| **Enabled**      | Indicates whether the stop sale is currently active (`✔️` = Yes, `❌` = No).       |
| **Created**      | Date when the stop sale record was created.                                       |
| **Remove**       | Indicates whether the stop sale has been removed (`✔️` = Yes, `❌` = No).          |
| **Agreed**       | Shows the number of agreed entries or a checkmark (✔️) if agreed.                 |



#### **Remove (Undo) Stop Sale**

### **Stop sales in Supplier**

<figure><img src=".gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

A supplier, if it has the "Allow to make stop sale" right activated, can see his stop sales in the "Agent" menu, "Stop sales list" page. A supplier can only disable/enable a service.

### **Stop Sale Mail**

After a new stop sale is made, an email is sent to the company with the stop sale filters. For this functionality to be available, there are two things that must be set:

1. In **system setup**, each company must fill in the **email address for stop sale**.

<figure><img src=".gitbook/assets/image (72) (1).png" alt=""><figcaption></figcaption></figure>

2. Each agency must create the **email template** for this from the email center.

<figure><img src=".gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

### **Stop Sale Room Reservation**

We'll add a stop sale option per hotel that will

* Do not allow either the customer on web booking or the salesperson in the office to make room selection during the stop sale hours if they do not already have anything chosen.
* Do not allow either the customer on web booking or the salesperson in the office to make changes to the room selection during the stop sale hours if they have already made the selection.

<figure><img src=".gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>
