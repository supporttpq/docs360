# Hotel Layout

### Overview

Hotel Layout lets you build a hotel floor plan with:

* **Active elements** (rooms you can book).
* **Decor elements** (icons/logos, facilities, etc.).

The layout is used in:

* **Office (Back office)**: assign a passenger to a specific room.
* **WebBooking**: let the customer pick a room and pay a supplement.

### Prerequisites

To make Hotel Layout available (the **Hotel Room** tab in Office and room selection in WebBooking), you must:

* Create the **room reservation** supplement and add the hotel as a resource.
* Add **backgrounds** and **layout elements**.
* Configure **room numbers** and generate **allotments** for them.
* Build the hotel layout using the background and elements.
* Link **room numbers** to the room elements on the layout.

{% stepper %}
{% step %}
### Create the room reservation supplement

Create a supplement used for room selection.\
It is added automatically when a room is selected in the layout.

Configure it like this:

* **Discount/Suppl Code**: `RR`
  * The code `RR` connects the supplement to Room Reservation.
* **Discount or Suppl**: Supplement
* **General/Specified**: General
* **Fixed/Manual**: Manual
* **Available for first pax**: enabled
* In the **Resources** tab, add the hotels that should support room reservation.

This supplement is reused across hotels.\
The **price** is set per **room number** later.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (7).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Add backgrounds and layout elements

Open **Hotel → Layout Elements** (see [Layout Elements](../../layout-elements.md)).

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Add a background in the **Backgrounds** tab.\
Add elements in the **Elements** tab.

{% hint style="warning" %}
Use the correct pixel sizes. Tourpaq does not scale images.
{% endhint %}

Element types:

* **Room icon**: connects a room number to a room type.
* **Room**: a placeable room element on the layout.
* **Decor**: non-bookable decoration (toilet, pool, bar, etc.).

{% hint style="info" %}
Use transparent images for room icons. It makes availability colors visible.
{% endhint %}
{% endstep %}

{% step %}
### Configure room numbers and generate allotments

Define the “real” rooms for the hotel’s room types.

1. Go to **Room numbers → Room numbers**.
2. Enter a start and end value (example: `1` to `7`).
3. Save to generate room numbers.

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Then connect room numbers to room types:

1. Go to **Room numbers → Room Icons**.
2. Add a layout element of type **Room icon** to each room number.

Based on the **Room Icons** setup, Tourpaq generates room allotments.\
You can view and update them in **Room numbers → Allotments**.

Update:

* **Availability** per date.
* **Price** (the `RR` supplement price) per date.

<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Allotment color meanings:

* **Yellow**: already booked
* **Green**: available
* **Red**: unavailable
{% endstep %}

{% step %}
### Build the hotel layout

Open the hotel and go to the **Layout** tab.\
Click **Create Layout**.

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

You can create multiple sections (for example, one per floor).\
Pick a background by clicking the background image.

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

To add rooms and decor:

1. Click an element.
2. It appears in the top-left corner.
3. Drag and drop it into place.

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Link room numbers to room elements

Assign real room numbers to **Room** elements on the layout:

1. Right-click a room element.
2. Choose the room number.

<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Use Hotel Layout in a booking

In Office bookings, the **Hotel Room** tab shows the layout and available rooms.

If you have multiple room types (or multiple rooms of the same type), they appear in the left list.

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Workflow:

1. Select a room type from the left list.
2. Click an available room in the layout.
3. Save.

After saving, Tourpaq adds the `RR` supplement (and the price for the selected room number) to the **first passenger** on the booking.

Availability colors in the layout:

* <mark style="color:green;">Green</mark>: available for the booking
* <mark style="color:yellow;">Yellow</mark>: already selected on this booking
* <mark style="color:red;">Red</mark>: not available

{% hint style="info" %}
If you don’t see colors, your Room Icon image is probably not transparent.
{% endhint %}
{% endstep %}
{% endstepper %}

### Hotel layout in hotel combinations

Hotel combinations can show layouts from the combined hotels (if the feature is enabled on those hotels).

To use room selection in a hotel combination, make sure the **hotel combination** is included in the **Resources** list on the `RR` supplement.

### FAQ

**Q: I can see the Hotel Layout section in WebBooking, but it shows “No information was found”. Why?**\
**A:** WebBooking only checks basic conditions on first load (layout exists, supplement exists, etc.).\
Full validation runs when you open the Hotel Layout section. This avoids slow initial loading.

**Q: Can Tourpaq scale my background and icons?**\
**A:** No. Use correct pixel sizes for both backgrounds and elements.

**Q: Why don’t I see any availability colors on the room icons?**\
**A:** Your Room Icon image likely lacks transparency. Use a transparent background.

**Q: What connects the room selection supplement to Hotel Layout?**\
**A:** The supplement code must be `RR`.

**Q: Where do I set the price for choosing a specific room?**\
**A:** In **Room numbers → Allotments**, per room number and date. This becomes the `RR` supplement cost.

**Q: Why isn’t the “Hotel Room” tab available in Office bookings?**\
**A:** One of the prerequisites is missing. Usually the `RR` supplement resource assignment, room numbers, or the layout-room linking.
