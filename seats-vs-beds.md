# Seats vs Beds

### Overview

**Seats vs Beds** gives you a per-departure view of transport capacity and linked hotel availability. Use it to keep seats and rooms in sync when managing bookings.

### Location

Found under: **Hotel → Seats vs Beds Overview**

### Structure

The feature is divided into two main parts:

1. **Overview** – Displays transport departures, seat availability, and linked hotel allotments.
2. **Communication** – Sends scheduled XML reports based on the overview data.

### Seats vs Beds overview

This view shows occupancy for both transports and linked hotels. It helps you spot capacity gaps early.

#### Transport Occupancy

* **Total Available Seats** – Total number of seats offered for the transport.
* **Booked Seats** – Number of seats already booked.
* **Free Seats** – Number of seats still available.

#### Hotel Occupancy

* **Total Number of Rooms** – Total rooms available in the linked hotel.
* **Sold Rooms** – Number of rooms already booked.
* **Available Rooms** – Number of rooms still available.

### Available Filters / Fields

* **Transport** – Mandatory. Select the transport to display occupancy.
* **Resort** – Optional filter to narrow down hotels by resort.
* **Hotel** – Optional filter to select a specific hotel.
* **Date From / Date To** – Mandatory. Define the date range based on departure start weeks from **Setup**.
* **Allotment Rooms** – If checked, only hotels marked as **Allotment** in **Contract Type** will be shown.
* **Commitment Rooms** – If checked, only hotels marked as **Guarantee** in **Contract Type** will be shown.
* **Bed Bank Rooms** – If checked, only hotels marked as **Bed Bank** in **Contract Type** will be shown.
* **Hide Dynamic Flights** – If checked, all dynamic transports (real transports and GDS) will be hidden.

<figure><img src=".gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

In the example below, only the transport part of the export is shown.

The report includes the transport values above, plus:

* Percentage of seats sold
* **ROE** – A set value used to calculate variance and rooms needed. Configure it in **Setup → Average pax/room sold**.
* Rooms needed
* Available rooms (Allotment)
* Available rooms (Commitment)
* Variance

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (15).png" alt=""><figcaption></figcaption></figure>

Hotel and room values are color-coded based on your hotel setup settings. The legend is shown below and also appears at the bottom of the page. The first column is hotels. The second column is rooms.

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Hotel view looks like this. You can also expand a hotel to see all room types.

<figure><img src=".gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

You can export the report as an XML file.

### Communication

**Communication** lets you automatically send XML reports by email, based on transport and hotel occupancy. The attached XML contains the same data as the exported Seats vs Beds overview.

#### Available Filters

<figure><img src=".gitbook/assets/image (411).png" alt=""><figcaption></figcaption></figure>

* **Interval** – Choose how often the report is sent: Daily, Weekly, Monthly, or Annually.
* **Agency** – Select the agency that will receive the report.
* **Date From / Date To** – Specify a date range. Cannot be used together with **Days Before**.
* **Days Before** – Generate a report for bookings arriving in a set number of days. Cannot be used with **Date From / Date To**.
* **Hour** – Specify the time of day the email will be sent.
* **Transport** – Filter by specific transport.
* **Resort** – Optional filter to narrow down hotels by resort.
* **Hotel** – Optional filter to select a specific hotel.
* **Is Allotment** – If checked, only hotels set as **Allotment** in **Contract Type** will be included.
* **Is Commitment** – If checked, only hotels set as **Guarantee** in **Contract Type** will be included.
* **Bed Bank** – If checked, only hotels set as **Bed Bank** in **Contract Type** will be included.
* **Email** – Recipient email address for the schedule.
* **Stop** – Pause the schedule.

#### Scheduler Management

* The schedule can be **stopped** without deleting it, allowing it to be resumed later.
* The schedule can also be **deleted entirely** if no longer needed.

### FAQ

#### What’s the difference between **Overview** and **Communication**?

**Overview** is for interactive checking. **Communication** is for scheduled sending of the same data as XML.

#### Why can’t I use **Days Before** together with **Date From / Date To**?

They define the time window in two different ways. Use one or the other.

#### What does **Hide Dynamic Flights** remove?

It hides dynamic transports, including real transports and GDS.

#### Where does **ROE** come from?

It’s a configured value. Set it in **Setup → Average pax/room sold**.

#### Can I export the report without emailing it?

Yes. Use the export option in the overview to download an XML file.

#### I don’t see any hotels for a departure. What should I check first?

Start with filters. Then confirm the hotel contract type (Allotment/Guarantee/Bed Bank) matches your selected checkboxes.
