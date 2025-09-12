# Hotel Layout

### Description <a href="#description" id="description"></a>

Hotel Layout is a feature that allows the user to define a floor-plan of a hotel with active-elements (rooms) and décor elements (logos/icons, anything basically). These floor-plans will be used in back office for assigning a passenger to a specific room in a hotel as well as in webbooking where the customer can choose the room he wants to be booked for him and pay an extra fee for this (Room selection supplement)

### Workflow <a href="#workflow" id="workflow"></a>

For the Hotel Layout to be active on booking, i.e. the "Hotel Room"-tab to be available in Booking in Office and available in WebBooking, we have the following requirements:

* Create Supplement and add Hotel as resource on Supplement
* Add Layout Elements and Backgrounds
* Configure Room Numbers and allotment for Room Numbers on Hotel
* Setup Layout on Hotel using background and elements
* Add Room Numbes to Room Icons on Hotel Layout

#### **Create the supplement**

Create the "room reservation" supplement. This supplement will automatically be added when a room is selected in the layout, and it has to be configured like this:

* Discount/Suppl Code: RR
  * _Important! The Code "RR" connects the supplement to Room Reservation._
* Discount or Suppl: Supplement
* General/Specified: General
* Fixed/Manual: Manual
* Available for first pass: Checked
* In "Resources"-tab, add the hotels that should use Room Reservation.

This supplement will be used on multiple hotels. The price for the Room Reservation is defined for each Room Number in a later step.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Add elements to be used on the layout**

This can be done from "Hotel-> Layout Elements"

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;We will start by adding a new hotel background and then some elements to be placed on it.

The Background is added from tab "Backgrounds".

Then add Layout Elements in tab "Elements"

Make sure that Backgrounds and Layout Elements are added in correct pixel sizes, so that the elements fit on the background. No scaling of images are done in Tourpaq.&#x20;

There are 3 element types relevant for Hotel Layout:

* Element type "Room icon" is used to associate a room number with a room type from the hotel
* Element type "Room" is used to add a Room-element to the hotel layout from Hotel "Layout" tab.
* Element type "Decor" is used to add decorations, e.g. toilets, pool, beach, bar etc.

To make it visible, when a room is reserved on a booking, please use images with transparent background.&#x20;

#### **Configure the room numbers**

We now need to define “real” rooms for the room types of this hotel.

For this, we first define some room numbers from the tab "Room numbers", sub-tab "Room numbers". We do this by inserting a start value (for example:1) and an end value (for example:7). Numbers from 1 to 7 will be generated.&#x20;

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

We associate a room type of the hotel with a room number from the tab "Room numbers", subtab "Room Icons". For this, we need to insert add a Layout Element of type "Room Icon" to the Room Number.

In our example below, room number 1 is of type 2/22-H between the 1st of March and 31st of March. The elements from the drop down list "Room Icon" are layout elements of type "Room icon". Based on the record defined in subtab "Room Icons", allotments will be generated.&#x20;

We can see the generated allotments in subtab "Allotments". The prices  and availabililties for each date can be updated. Availabilities&#x20;

<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The colors have the following meanings:

* yellow - room have already been booked
* green - room is available
* red - room is unavailable

### Setup Layout on Hotel

Afterwards, in the Hotel we want a Layout. For this, we go to the “Layout” tab and then click “Create Layout”

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

On this screen we can create multiple sections of a hotel (e.g. one section per floor).&#x20;

Adding a background is as simple as clicking the background image.

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Now, for adding other elements (rooms and décor), we click them, and they appear in the top-left corner of the background image. Then, we can drag and drop them to the correct placement on the background image.

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



We assign “Real” room numbers to "Room"-type icons on the layout by right-clicking a room where we get the option to choose the Room Number.



<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Creating and editing a booking**

The "Hotel Room" tab in booking shows us the layout and the possibility to select the room we want for this booking. If we have multiple room types, or more rooms of the same kind, it will show them all in the list in left column.

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

By clicking room names in the list on the left, we select the room type we want to book.

Clicking an available room on the Hotel Layout, we can select the actual room numbers for this booking.

After selcting a room number and saving, the supplement (and cost for the actual room number) will be added to the first passenger on the booking.

The background color on the Room Number indicates, if the Room Number is available on the booking:

* <mark style="color:green;">Green</mark>: Available for the booking
* <mark style="color:yellow;">Yellow</mark>: Room Number is added to this booking
* <mark style="color:red;">Red</mark>: Not available

If you do not see any background colors, your image used as Room Icon might not have transparent background.

#### **Hotel layout for hotel combination**

For hotel combination, layouts are available from combined hotels, if they have this feature set.

To utilize this feature, hotel combinations must be assigned to the Room Supplement resources from the Room Resevation Supplement..

#### **Please be aware**

\*Is it possible to see Hotel Layout section, but when you access it there is an warning message: "No information was found". \*This is happens because first time when you open webbooking, the system checks only the basic conditions(hotel has layout, there is defined supplement per company, LMS etc.), and only when you access hotel layout all the validations are made. \*We chose this workflow because will take a lot of time to validate hotel layout on first call, when webbooking is accessed for the first time.
