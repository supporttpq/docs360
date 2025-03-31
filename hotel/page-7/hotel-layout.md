# Hotel Layout

### Description <a href="#description" id="description"></a>

Hotel layout is a feature that allows the user to define a floor-plan of a hotel with active-elements (rooms) and décor elements (logos / icons , anything basically). These floor-plans will be used in back-office for assigning a passenger to a specific room in a hotel as well as in webbooking where the customer can choose the room he wants to be booked for him and pay an extra fee for this (Room selection supplement)

### Workflow <a href="#workflow" id="workflow"></a>

#### **Create the supplement**

Create the "room reservation" supplement. This supplement will automatically be added when a room will be selected in the layout and it has to be configured like this:

* Discount/Suppl Code: RR
* Discount or Suppl: Supplement
* General/Specified: General
* Fixed/Manual: Manual
* Available for first pass: Checked

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Add elements to be used on the layout**

This can be done from "Hotel-> Layout Elements"

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

There are 4 element types: Seat, Decor, Room and Room Icon. It's very important to remember this, because when we will later associate a room number with a room type from the hotel, we will only use "room icon" element types.

We will start by adding a new hotel background, and then some elements to be placed on it.

Afterwards, on the hotel we want a layout. For this, we go to the “Layout” tab and then press “Create Layout”

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

On this screen we now have the possibility to create multiple sections of a hotel (floors , per example), but we will focus on editing a single section\ Adding a background is as simple as clicking the background image Important note: in order to see when a room is reserved on a booking on not (by using backgrounds shown yellow/red/green), please use room icon with transparent background.

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Now for adding several other elements (rooms , décor) we click them and they appear in the top-left corner of the background image. Then we are able to drag and drop them (even more than one at once) on the background image of the layout (I also resized the background image in this step by dragging the corner):

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Configure the room numbers**

We now need to define “Real” rooms for the room types of this hotel.

&#x20;For this, we first define some room numbers from the tab "Room numbers", sub-tab "Room number". We do this by inserting a start value (for example:1) and an end value (for example:7). Numbers from 1 to 7 will be generated.&#x20;

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

We associate a room type of the hotel with a room number from the tab "Room numbers", subtab "Room Icons". For this, we need to insert a room icon.

Room number 1 is of type 2/22-H between the 1st of March and 31th of March and in the layout will be represented by the room icon "Room Normal". The elements from the drop down list "Room Icon" are layout elements of type "Room icon". Based on this record defined in room icon, allotments will be generated. We can see the generated allotments from tab "Room numbers" - subtab "Allotments"

<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The prices can be updated, as well as the availablity of the room. This can be done by selecting several records and then check or uncheck the checkbox. The colors have the following meanings:

\*yellow - room have already been booked \*green - room is available \*red - room is unavailable

#### **Assign room numbers with room icons on the layout**

After defining the rooms, we can now assign “Real” room numbers on the layout. We go back to the layout tab. When you right-click a room you have now the possibility to select a room number from the list defined in room types.

<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

\*Each real room can be configured and we can set a price for it in Allot. Per Day tab. Each “real room” can be also marked as unavailable on a specific period

#### **Creating and editing a booking**

The new HotelRoom tab shows us the layout and the possibility to select the room we want for this booking (if we have multiple room types, or more rooms of the same kind, it will show them all in the list to the left).

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

By clicking room names in the list on the left, and then clicking rooms marked as Green in the layout, we can book the “real room/s” for this booking, and then we will see that the passenger’s supplements also are changed with the price defined in allotment per day for the room.

#### **Hotel layout for hotel combination**

For hotel combination, layouts are available from combined hotels, if they have this feature set.

In order to use this feature, hotel combinations have to be assigned to the Room supplement resources from Disc/Suppl.

#### **Please be aware**

\*Is it possible to see Hotel Layout section, but when you access it there is an warning message: "No information was found". \*This is happens because first time when you open webbooking, the system checks only the basic conditions(hotel has layout, there is defined supplement per company, LMS etc.), and only when you access hotel layout all the validations are made. \*We chose this workflow because will take a lot of time to validate hotel layout on first call, when webbooking is accessed for the first time.
