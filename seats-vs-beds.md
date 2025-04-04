# Seats vs Beds

**Seats vs beds** is a management feature that allows the users to see the availlablity of transports and linked hotels on departure basis.

It can be founded in **Hotel**/**Seats vs Beds Overview** and is divided into 2 parts:

* Overview
* Communication

### Overview <a href="#overview" id="overview"></a>

The **Overview** part of **Seats vs Beds** displays the occupancy rate of transports and hotels:

* Transport:
  * Total available seats
  * Booked seats
  * Free seats
* Hotel:
  * Total number of rooms
  * Sold rooms
  * Available rooms

Fields Available:

* Transport - mandatory field
* Resort
* Hotel
* Date from/to - mandatory fields, needs to be filled according to **Departure stat weeks** from **Setup**
* Allotment rooms - if checked, only hotel set as **Allotment** in //Contract Type// will be shown
* Commitment rooms - if checked, only hotel set as **Guarantee** in //Contract Type// will be shown
* Bed Bank rooms - if checked, only hotel set as **Bed bank** in //Contract Type// will be shown
* Hide dynamic flights - if checked, all dynamic transports(real transports and GDS) will be hidden

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

In the example below, only the transport part of the export is shown to facilitate the understanding and explanations.

The report lists all details listed above in the **Transport**, along with:

* Percentage of seats sold in the transport
* ROE - a set value used to calculate the variance and rooms needed, it can be set in **Setup**/**Average pax/room sold**
* Rooms needed
* Available rooms Allotment
* Available rooms Commitment
* Variance

<figure><img src=".gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

The hotels and rooms display is color coded based on settings from hotel setup, the legend is posted below and can be found at the bottom of the display. First column is hotels, the second is used for rooms.

<figure><img src=".gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

The hotels display would look like this. The user has the option to also see all the rooms in the hotel.

<figure><img src=".gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

The user also has the option to export the report in a xml format file.

#### Communication <a href="#communication" id="communication"></a>

The **Communication** of **Seats vs Beds** sends an xml file by emails to a set address according to the filters set. The information from the file is the same as the information from the exported file.

Filters:

* Interval(Daily, Weekly, Monthly, Annualy)
* Agency
* Date From/To(cannot be used with **Days Before**)
* Days Before(cannot be used with **Date From/To**)
* Hour
* Transport
* Resort
* Hotel
* All - will send only hotels set as **Allotment** in //Contract Type//
* Commn - will send only hotels set as **Guarantee** in //Contract Type//
* Bed Bank - will send only hotels set as **Bed bank** in //Contract Type//

The schedule also has the option to be stopped without deleting it in order to be resumed at a later date or it can be deleted entirely.

<figure><img src=".gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>
