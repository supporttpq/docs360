# Hotel allotments

### **Overview**

The **Allotments** page allows you to define, manage, and control the number of hotel rooms available for sale during a specific period. Each allotment links to a room category and, optionally, a board type, ensuring proper allocation between secured and guaranteed rooms.

### **Purpose**

The purpose of allotments is to manage contractual agreements with hotels by setting aside a defined number of rooms for sale. This helps the tour operator control availability, guarantee allocations, and ensure that bookings are aligned with hotel contracts.

### **Preconditions**

* The hotel and its room categories must already be set up in the system.
* Relevant board types (meal plans) must be configured.
* A valid contract period must exist for the hotel.

### **Field Explanations**

<figure><img src="../../.gitbook/assets/image (409).png" alt=""><figcaption></figcaption></figure>

* **Period Start** – The start date of the allotment validity.
* **Period Stop** – The end date of the allotment validity.
* **Room** – The room type (e.g., Double Room, Suite, Family Room) defined in the system.
* **Min. Stay** – Minimum nights required for booking this room. `0` means no restriction.
* **Board** – The default board type for the room. The price of the board type shall be included in the room cost.
* **No.** – The total number of rooms available in the allotment for the defined period.
* **Secured** – Number of rooms contractually secured from the hotel.
* **Guaranteed** – Number of rooms financially guaranteed (must be paid even if unsold).
* **Copy** – Checkbox to mark allotments for duplication when generating or extending periods.
* **Generate** – Creates allotments in the system based on the defined criteria.
* **Delete Allotment (calendar/extend)** –
  * Calendar icon: Displays the last generated date of the allotment.
  * Extend: Allows prolonging the allotment validity beyond the stop date.
* **Delete (trash icon)** – Removes the selected allotment.

To finish the process, press **Save**

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Rooms cannot be used in bookings unless the allotment is generated.

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The **Extend** button allows the room's availability period to be extended without creating a new line. Just insert the **Period stop** new date and press **Extend**.

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Hotel allotment control <a href="#hotel-allotment-control" id="hotel-allotment-control"></a>

The hotel allotment can be controlled/limited per transport. The below part of the screenshot is made from the price list rule of the specified transport.

<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

In the above example, the room has 20 total available allotments. For a particular transport, there is a maximum allotment limit set of 5, and 3 rooms have already been sold. This means that for this transport, the available rooms left number is 1. For other transports, it's all or the specific limit for that transport as well.

#### Generate all allotments

This feature will help us to generate all allotments at once and not do it for each one at a time.&#x20;

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

There are cases when you have many allotments to generate for a hotel. Instead of clicking on each one individually, now you're able to generate all at once by using the Generate All button and then clicking OK if you agree to generate.
