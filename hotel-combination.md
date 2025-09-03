# Hotel combination

### What is a hotel combination? <a href="#what-is-hotel-combination" id="what-is-hotel-combination"></a>

A hotel combination is like an itinerary of hotels where a customer stays two days in one hotel and five in another during the holiday. The itinerary hotels (a list of hotels that are defined) are hotels that exist already in the Tourpaq system. This type of hotel is like a regular hotel except that it has no allotments; instead, it will rely on the allotments of the hotel defined in the itinerary.

### How to define a hotel combination? <a href="#how-to-define-a-hotel-combination" id="how-to-define-a-hotel-combination"></a>

You can add a new combination hotel in the same way a regular hotel is created, but make sure you check the Hotel Combination checkbox. In order to use the hotel in the booking, you should complete the next steps.

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Add hotel list and transport <a href="#add-hotel-list-and-transports" id="add-hotel-list-and-transports"></a>

Under the Hotel Combination tab, you can define a list of hotels where the customer can stay. The order in which the hotels are added is important. The first hotel in the list is the first hotel where the customer will spend. You can add two or multiple hotels. Here can be added transports as well. This means that this hotel is available only for this transport.

<figure><img src=".gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

If you select only one hotel in the list, then a checkbox will appear. If the checkbox is checked, then the hotel from the list will appear in the ticket; else, if it is not checked, then the main hotel will be the one to appear.

### Assign the rooms <a href="#assign-the-rooms" id="assign-the-rooms"></a>

A hotel has multiple room types. Also, our hotel combination has room types, but these are not real; they are just some fake rooms. In reality the hotel room has one room for every regular hotel. You can map the rooms of the hotel combination with the regular hotel rooms in the Hotel Combination Room tab. In this section are two grids; one is mapping rooms. The rooms have to be close together as specification. In the second grid, you have many transports with many intervals mapped with hotels. For every combination, you have to add the number of days that the customer will spend in that hotel.

<figure><img src=".gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

In the picture above is shown transport BLLPVK-A7-5A. This transport has 4 intervals: interval 1 has 7 days, interval 2 has 14 days, interval 3 has 21 days, and interval 4 has 28 days. A customer can book for interval 1, 4 days for hotel SIV150 and 3 days for hotel AGI150 during this 7-day holiday. Since interval 2 has 14 days, the customer can book 7 days in SIV150 and 7 days in AGI 150. The same things can be made for intervals 3 and 4 also. These values are presets, so the customer can’t choose how many days to stay in each hotel. Now that all is set, you can create a price list with the transport, hotel, and room. **Note:** If the price list is defined, you can’t change the transport, room, or hotel in the hotel combination. Also make sure you defined allotments for the itinerary hotels. The price list will not be created otherwise.

### What to do if the price list can’t be generated <a href="#what-to-do-if-the-price-list-cant-be-generated" id="what-to-do-if-the-price-list-cant-be-generated"></a>

There are some situations where the price list can’t be generated. To find out what the problem is, you have to make sure you’ve completed the following verifications.

### Regular hotel allotment <a href="#regular-hotel-allotment" id="regular-hotel-allotment"></a>

If we take our example where we have a combination hotel with two hotels, SIV150 and AGI150, in order to successfully create a price list, you have to navigate to Hotel -> Hotel (SIV150/AGI150) -> Allot. and check the list of allotments to see if a record with period, room, and allotment number complies with the price list requirements.

### Transport allotments <a href="#transport-allotments" id="transport-allotments"></a>

There are cases where you want to create a price list for an interval, let's say for 07.06.2026, but the transport may not have an allotment on that date. In this case you have to add an allotment for that date and recreate the price list. You can add an allotment in a fixed quota.
