# Facilities

Available for Administrator user types.

Facilities feature allows a user to define the facilities available at a hotel. Can be defined from **Hotel/Facilities** and can be set from the hotel **Web** tab

There are 4 tabs:

* Facilities - list of facilities
* Categories - used in web tab for grouping facilities
* Templates - used by hotels to group the facilities based on the type of hotel, can be chosen in the hotel general tab
* Name for Feeds

<figure><img src=".gitbook/assets/image (17) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Categories <a href="#categories" id="categories"></a>

Categories are needed to define facilities.

A new category can be defined in the **Category** tab, by pressing the "Create" button, in the upper right corner of the screen.

Fields:

* Name - name of the category
* Show on ticket - displays the category on the ticket
* Show on select offer - display the category on offer

<figure><img src=".gitbook/assets/image (18) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Facilities <a href="#facilities" id="facilities"></a>

A new facility can be defined in the **Facilities** tab, by pressing the "New facility" button in the upper right corner of the screen.

<figure><img src=".gitbook/assets/image (19) (1) (1).png" alt=""><figcaption></figcaption></figure>

Fields:

* Name - name of the facility
* Data type - select from dropdown
* Max chars (available for Decimal, Integer, Multiline Text and Text Data types) - max number of characters
* Category - category of the facility
* Default value - is set according to the Data type
* Is mandatory - when **Facilities template** is chosen for a hotel, the facility must be set from **Web** tab
* Show on hotels popup - will be shown on the booking page, in the hotel selection pop-up when clicking on the hotel code
* Show on web as filter (When this is checked, the presentation website(ex: primotours.dk) will allow a more advanced filtering of hotels by this facility)
* Show on web (When this is checked, the presentation website(ex: primotours.dk) will show this facility on the hotels that use it, on hotels listing)
* Flag on web - used to highlight a facility on web.
* All Inclusive - necessary to differentiate in API on web
* Swimming Pool - necessary to differentiate in API on web
* Child Pool - necessary to differentiate in API on web

### Templates <a href="#templates" id="templates"></a>

A new template can be defined in the **Templates** tab, by pressing the "New template" button in the upper right corner of the screen.

Fields:

* Name - name of the template
* Facilities - choose the facilities available for the template

<figure><img src=".gitbook/assets/image (21) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Facilities on web <a href="#facilities-on-web" id="facilities-on-web"></a>

On the website, facilities are displayed for the hotel like this:

![!](https://docs.tourpaq.com/assets/images/facilities_on_web-c0f8bedeeb3c056f7c09926e50b999b5.jpg)
