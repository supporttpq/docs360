# Hotel creation

This feature is available for the administrator user type.

### General <a href="#general" id="general"></a>

Mandatory fields:

<figure><img src="../../.gitbook/assets/image (403).png" alt=""><figcaption></figcaption></figure>

* Code - hotel code
* Name - hotel name
* Resort - resort name
* Contract type - used for prioritizing hotels in the **Select Hotel** pop-up when making a booking.
* Standard room

Without these fields, you cannot create the hotel.

Other fields that are necessary for the hotel to work properly:

<figure><img src="../../.gitbook/assets/image (404).png" alt=""><figcaption></figcaption></figure>

* Supplier - supplier of the hotel
* Stars
* Infant price - price for infants that stay in the hotel
* Standard room - main room type of the hotel
* Status - set if the hotel is hidden or visible in the hotel dashboard
* Facilities template - select a facility template from those available, which will allow the setting of the facilities available in the hotel from **the Web** tab. more information is available at [Facilities](../../facilities.md)
* Hotel combination - allows for 2 or more hotels to be combined into 1, drawing room allotments from the hotels selected. for more information, please check [Hotel Combination](../../hotel-combination.md)
* Child price ages - age interval that benefits from the child price from the price list
* Child ages for extra bed - age interval for children when taking into account the "extra bed child" from the room; if the age is outside of the interval, children will use an adult extra bed (overrides the age set in the base room type). If nothing is set, the child's ages for extra beds are not taken into consideration.&#x20;
* Adult hotel - sets an age limit preventing guests to book if there is a passenger with the age below limit
* Order No. - Tourpaq API, order of the hotels sent to the website
* Customise room offer priority - The checkbox allows the user to decide whether they want to use a personalized priority of room types (i.e., by orderId) or let the API decide automatically based on the room configuration (i.e., by number of beds).
* Issue voucher - allows for vouchers to be issued
* For one way - a hotel used only for one-way transport
* Extra Bed Discount Name - Name of the Extra Bed Discount on the ticket and in webbooking
* Managed by Availpro - the hotel is using rooms and costs from Availpro
* Hide as filter on lists - hides the hotel from filters on all lists in the system
* Is VisitSun
* Custom Hotel Days Booking - enables rooms to be set for Hotel Price Per Day option (A la carte) in **Room Types**
* Uses infant beds - infant will now occupy beds in rooms assigned to the hotel

### **Customized Stars**

This field allows you to set a custom star rating for the hotel. If specified, the custom rating will be displayed on the ticket instead of the standard star rating.

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The header text for the "Stars" column can also be customized, but only when the Customized Stars field is filled. This setting is located in Users → Brands → Ticket under the name "Customized Star".

<figure><img src="../../.gitbook/assets/image (406).png" alt=""><figcaption></figcaption></figure>

For the autobilling feature, please check [Autobilling](../../autobilling/)

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Brands <a href="#brand" id="brand"></a>

Brand assignment of a hotel is the next thing to do. A user can choose between the availability of a hotel on a brand. It can be used either:

* only in the office
* only on the internet
* both in the office and internet

<figure><img src="../../.gitbook/assets/image (407).png" alt=""><figcaption></figcaption></figure>

### Room types <a href="#room-types" id="room-types"></a>

The **Room Types** tab defines the room configuration details for a specific accommodation. It allows users to set up and manage how rooms are categorized, how many beds they contain, and what rules apply to them (such as age restrictions or override options).\
This section ensures that all room configurations are standardized and properly linked to the accommodation setup for bookings and pricing.

The purpose of this section is to:

* Assign the correct **room types** available for an accommodation (e.g., Single, Double, Family Room).
* Define the number of **ordinary** and **extra beds** available for both adults and children.
* Specify **minimum age requirements** where applicable.
* Allow certain room configurations to be **overridden** in specific cases.

Accurate configuration here ensures that booking rules, pricing, and capacity limits are applied correctly in the system.

#### **Field Descriptions and Instructions**

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **1. Room Type**

* **Description:** Defines the type of room to be configured (e.g., Single Room, Double Room, Suite).
* **Instruction:** Select a room type from the dropdown list. This list is predefined in the system setup.

***

#### **2. Ordinary Bed Number**

* **Description:** Specifies the standard number of beds included in the room.
* **Instruction:** Enter the total number of fixed beds available (e.g., 1 for a single room, 2 for a double room).
* **Purpose:** Used to calculate the total occupancy capacity for the room.

***

#### **3. Extra Beds Adult**

* **Description:** Indicates how many additional beds can be added for adults.
* **Instruction:** Enter the maximum number of extra adult beds that can be added to this room type.
* **Example:** If the room can accommodate one extra bed for an adult, enter **1**.

***

#### **4. Extra Beds Child**

* **Description:** Indicates how many extra beds can be added for children.
* **Instruction:** Enter the number of additional child beds that can be provided.
* **Example:** If a cot or extra child bed can be added, enter **1**.

***

#### **5. Minimum Age**

* **Description:** Sets the minimum age required for booking or staying in this room.
* **Instruction:** Enter the age limit if applicable (e.g., 18).
* **Purpose:** Helps enforce age-based restrictions (e.g., adult-only rooms).

***

#### **6. Override**

* **Description:** The override check box allows the creation of a child room type specific to that hotel based on the selected room type. The new room type can be edited.
* **Instruction:** Tick the checkbox if you need to override existing rules or capacity settings.
* **Use Case:** For special accommodations or exceptions that differ from the general setup.

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The new room will not be displayed in the room dropdown

If mistakes are made when adding a new room, you cannot delete the inserted room, but you can leave it there, since for a room to be booked, it needs allotments and prices.

**Hide room** - hides the room, available only if there is no allotment for the room

**Used for Custom Hotel days** - enable prices per day to be created for the room

#### **Usage Example**

1. Select **Room Type → Double Room**.
2. Enter **Ordinary Bed Number → 2**.
3. Add **Extra Beds Adult → 1**, **Extra Beds Child → 1**.
4. Set **Minimum Age → 12** (if required).
5. Check **Override** only if this configuration should differ from the general setup.
6. Save your changes before navigating away.the used either

### Allotment <a href="#allotment" id="allotment"></a>

Generate the number of rooms available at the hotel and the period in which they can be used.

<figure><img src="../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

To finish the process, press Insert, followed by Generate.

### Shared Allotments <a href="#shared-allotments" id="shared-allotments"></a>

Used to sell the same room under different settings and prices. The shared allotment is used for one room to draw its allotment from another existing room in the hotel.

<figure><img src="../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

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

Used to define the amount paid by the agency to the hotel for the rooms. It is found on the contract between the hotel and agency. Please check [Room Cost](room-cost/)

### Ex. Beds Costs <a href="#exbeds-costs" id="exbeds-costs"></a>

Used to define the cost of the extra bed paid by the agency. Please check [Extra Bed Costs](extra-beds-costs.md)

### Special offers <a href="#special-offers" id="special-offers"></a>

Used to define discounts offered by the hotel to the agency. Please check [Room Cost](room-cost/)

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

{% hint style="warning" %}
**It can only be used if the layout is used.**
{% endhint %}

### Communication <a href="#communication" id="communication"></a>

Used to configure the sending of lists with bookings made for the hotel.

Please check [Hotel Reporting](communication/hotel-reporting.md)

### Deposit <a href="#deposit" id="deposit"></a>

This feature works with [Autobilling](../../autobilling/)
