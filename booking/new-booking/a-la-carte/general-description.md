# General Description

### Description <a href="#description" id="description"></a>

“A La Carte” Booking is a new type of booking that allows the user to create a booking without selecting a transport, hotel, or passenger. User only sees the customer (that is also considered the first passenger), and is able to modify its data or choose an existing customer. User is able to edit the travel insurance of the customer and the discounts and supplements. The booking also takes in consideration automatically applied discounts and supplements, which are not editable in the interface by the end-user.

### Office implementation <a href="#office-implementation" id="office-implementation"></a>

The “New A La Carte Booking” option in the Booking menu is only available for a company, after several “A La Carte” fictive entities have been defined:

### Base Room Type <a href="#base-room-type" id="base-room-type"></a>

This can be defined in the Hotel > Base room types menu, creating a new base room type, and applying the checkbox “For A La Carte”, several fields will become un-editable, and the base room type will comply with the “A La Carte” System.

### Hotel <a href="#hotel" id="hotel"></a>

Creating a new Hotel by checking the “For A La Carte” checkbox will input the minimum necessary data in the Hotel window, and will automatically create allotments and everything necessary for the “A La Carte” System.

### Transport <a href="#transport" id="transport"></a>

An “A La Carte” transport will only be able to be created after an “A La Carte” Hotel has been defined. Creating a new transport will also generate allotments, price lists, and everything necessary for the “A La Carte” System.

### Creating a new booking <a href="#creating-a-new-booking" id="creating-a-new-booking"></a>

After these entities have been defined by the user, in the Booking menu we have a new option: “New A La Carte Booking”, that allows us to create this type of booking, and save it.

Customer should be in edit mode, completion of a phone number retrieves data from the server and automatically fills the customer data, and then the user is able to save the customer for this booking. User is also able to select the customer by clicking Choose and then searching the customer by Name.

After saving the selected discounts we are able to save the booking, or continue editing insurances and discounts by repeating the previous steps. After saving the booking the page reloads and the booking is in edit mode, and the status changes from ERROR to OK.
