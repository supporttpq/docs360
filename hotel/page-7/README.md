---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Hotel creation

This feature is available for the administrator user type.

### General <a href="#general" id="general"></a>

Mandatory fields:

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Code - hotel code
* Name - hotel name
* Resort - resort name
* Contract type - used for prioritizing hotels in the **Select Hotel** pop-up when making a booking.
* Standard room

Without these fields, you cannot create the hotel.

Other fields that are necessary for the hotel to work properly:

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Supplier - supplier of the hotel
* Stars
* Infant price - price for infants that stay in the hotel
* Standard room - main room type of the hotel
* Status - set if the hotel is hidden or visible in the hotel dashboard
* Facilities template - select a facility template from those available, which will allow the setting of the facilities available in the hotel from **the Web** tab. more information is available at [Facilities](../../facilities.md)
* Hotel combination - allows for 2 or more hotels to be combined into 1, drawing room allotments from the hotels selected. for more information, please check [Hotel Combination](../../hotel-combination.md)
* Child price ages - age interval that benefits from the child price from price list
* Child ages for extra bed - age interval for children when taking into account the "extra bed child" from the room; if the age is outside of the interval, children will use an adult extra bed (overrides the age set in the base room type)
* Adult hotel - sets an age limit preventing guests to book if there is a passenger with the age below the limit
* Order No. - Tourpaq API, order of the hotels sent to website
* Customise room offer priority
* Issue voucher - allows for vouchers to be issued
* For one way - a hotel used only for one way transports
* Extra Bed Discount Name - Name of the Extra Bed Discount on the ticket and in webbooking
* Managed by Availpro - hotel is using rooms and costs from Availpro
* Hide as filter on lists - hides the hotel from filters on all lists in the system
* Is VisitSun
* Custom Hotel Days Booking - enables rooms to be set for Hotel Price Per Day option (A la carte) in **Room Types**
* Uses infant beds - infant will now occupy beds in rooms assigned to the hotel

### **Customized Stars**

This field allows you to set a custom star rating for the hotel. If specified, the custom rating will be displayed on the ticket instead of the standard star rating.

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The header text for the "Stars" column can also be customized, but only when the Customized Stars field is filled. This setting is located in Users → Brands → Ticket under the name "Customized Star".

![!](https://docs.tourpaq.com/assets/images/customized-stars-ticket-79a66eb479e95b0411db857d7fa5c628.png)

For autobilling feature please check [Autobilling](../../autobilling/)

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Brands <a href="#brand" id="brand"></a>

Brand assignment of a hotel is the next thing to do. A user can choose between the availability of a hotel on a brand. It can be either used:

* only in office
* only on internet
* both in office and internet

<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Room types <a href="#room-types" id="room-types"></a>

Add a new room to the hotel.

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

totoThe override check box allows the creation of a child room type specific for that hotel based on the selected room type. The new room type can be edited.

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The new room will not be displayed in the room dropdown

If mistakes are made when adding a new room, you cannot delete the inserted room, but you can leave it there since for a room to be booked, it needs allotments and prices.

**Hide room** - hides the room, available only if there is no allotment for the room

**Used for Custom Hotel days** - enable prices per day to be created for the room

### Allotment <a href="#allotment" id="allotment"></a>

Generate the number of rooms available at the hotel and the period in which they can be used.

<figure><img src="../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

To finish the process, press Insert, followed by Generate.

### Shared Allotments <a href="#shared-allotments" id="shared-allotments"></a>

Used to sell the same room under different settings and prices. The shared allotment is used for one room to draw its allotment from another existing room in the hotel.

<figure><img src="../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Two room types are needed in the hotel for this feature.&#x20;

**Warning!** Only the room above will have real allotment, the other room taking allotment from this one.

### Allotments per day <a href="#allotments-per-day" id="allotments-per-day"></a>

Used for controlling allotments.

<figure><img src="../../.gitbook/assets/image (62) (1).png" alt=""><figcaption></figcaption></figure>

The number of available rooms can be set from here by increasing or decreasing the value from the NO. RMS column.

Also, from the transport column, the number of rooms available for the transport can be controlled when there is more than one transport assigned to that room type. See more on the Hotel Allotments/Hotel Allotment Control page.

### Disc.Ex.Beds <a href="#discexbeds" id="discexbeds"></a>

Used to define the discount received by the passengers that use an extra bed in a room. Please check [Extra Bed Discount](discount-extra-beds.md)

### Room cost <a href="#room-cost" id="room-cost"></a>

Used to define the amount paid by the agency to the hotel for the rooms. It is found on the contract between the hotel and agency. Please check [Room Cost](room-cost.md)

### Ex. Beds Costs <a href="#exbeds-costs" id="exbeds-costs"></a>

Used to define the cost of the extra bed paid by the agency. Please check [Extra Bed Costs](extra-beds-costs.md)

### Special offers <a href="#special-offers" id="special-offers"></a>

Used to define discounts offered by the hotel to the agency. Please check [Room Cost](room-cost.md)

### Photos <a href="#photos" id="photos"></a>

From here you can add the photos for the hotel and rooms. Photos can be added for each room type by selecting the room type from the dropdown. All photos appear on the website. **Main photo** is the photo that will be displayed for the hotel

### Web <a href="#web" id="web"></a>

Used to define the facilities available at the hotel. Must have the Facilities template activated from the **Hotel** general tab.

### Layout <a href="#layout" id="layout"></a>

Adds layout to a hotel.

More information is available in [Hotel Layout](hotel-layout.md)

To use this feature, please contact Tourpaq Support.

### Room numbers <a href="#room-numbers" id="room-numbers"></a>

Adds numbers to the rooms of a hotel with a layout.

**!!! Can only be used if the layout is used.**

### Communication <a href="#communication" id="communication"></a>

Used to configure the sending of lists with bookings made for the hotel.

Please check [Hotel Reporting](communication/hotel-reporting.md)

### Deposit <a href="#deposit" id="deposit"></a>

This feature works with [Autobilling](../../autobilling/)
