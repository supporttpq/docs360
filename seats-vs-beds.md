# Seats vs Beds

### Overview

The **Seats vs Beds** feature provides a comprehensive view of transport availability and the corresponding linked hotels on a per-departure basis. This allows users to efficiently manage capacity and ensure bookings align with transport and hotel resources.

### Location

* Found under: **Hotel → Seats vs Beds Overview**

### Structure

The feature is divided into two main parts:

1. **Overview** – Displays transport departures, seat availability, and linked hotel allotments.
2. **Communication** – Facilitates sending lists or notifications based on the availability shown in the overview.

## Overview <a href="#overview" id="overview"></a>

The **Overview** section of **Seats vs Beds** displays the occupancy rates for both transports and linked hotels. This provides a clear view of seat and room availability for each departure, helping users manage bookings efficiently.

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
* **Date From / Date To** – Mandatory. Define the date range according to departure start weeks from **Setup**.
* **Allotment Rooms** – If checked, only hotels marked as **Allotment** in **Contract Type** will be shown.
* **Commitment Rooms** – If checked, only hotels marked as **Guarantee** in **Contract Type** will be shown.
* **Bed Bank Rooms** – If checked, only hotels marked as **Bed Bank** in **Contract Type** will be shown.
* **Hide Dynamic Flights** – If checked, all dynamic transports (real transports and GDS) will be hidden.

<figure><img src=".gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

In the example below, only the transport part of the export is shown to facilitate the understanding and explanations.

The report lists all details listed above in the **Transport**, along with:

* Percentage of seats sold in the transport
* ROE - a set value used to calculate the variance and rooms needed, it can be set in **Setup**/**Average pax/room sold**
* Rooms needed
* Available rooms Allotment
* Available rooms Commitment
* Variance

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (3).png" alt=""><figcaption></figcaption></figure>

The hotels and rooms display are color-coded based on settings from the hotel setup. The legend is posted below and can be found at the bottom of the display. The first column is hotels, the second is used for rooms.

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The hotel's display would look like this. The user has the option to also see all the rooms in the hotel.

<figure><img src=".gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The user also has the option to export the report in an XML format file.

## Communication <a href="#communication" id="communication"></a>

The **Communication** feature in **Seats vs Beds** allows users to automatically send XML reports via email based on transport and hotel occupancy data. The sent file contains the same information as the exported Seats vs Beds overview. This helps agencies and suppliers stay updated on availability without manually exporting data.

#### Available Filters&#x20;

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
* **Emai**l - email address where the schedule will be sent
* **Stop** - Pause the schedule

#### Scheduler Management

* The schedule can be **stopped** without deleting it, allowing it to be resumed later.
* The schedule can also be **deleted entirely** if no longer needed.
