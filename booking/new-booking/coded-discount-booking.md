# Coded discount booking

### **Overview**

This flow describes how to apply a **discount using a bonus code** during the booking process. Bonus codes are predefined in the system and can be applied to reduce the total price or add a supplement based on campaign rules.

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Purpose

The **Bonus Code** feature allows agencies to apply predefined discounts or supplements to a booking. Bonus codes are typically configured by brand and can be linked to marketing campaigns, partner agreements, or seasonal promotions.\
This functionality ensures that eligible customers receive the correct price adjustment automatically during the booking process.

### Instruction

Creating a booking with a bonus code follows the same process as a standard booking, with one additional step where the bonus code is applied.\
The user begins by opening the **New Booking** page from the **Booking** menu and selecting the **Brand** under which the booking is created.\
Next, the **Customer** is selected — either by searching for an existing record or adding a new one — and the number of passengers is defined, including adults, children, and infants.

After the customer and passenger details are entered, the user proceeds to select the relevant **transport options** (for example, outbound and return flights) and the **hotel accommodation**.\
Once the main components are defined, the user must **take allotment**, which reserves the corresponding flight seats and hotel rooms.

Before saving the booking, all **passenger information** must be confirmed in the **Booking Details** section.\
The **Bonus Code** can then be applied by entering it in the **Discount/Supplement Bonus Code** field. When the user clicks outside the field, the system automatically validates the code and applies the corresponding **discount or supplement**, updating the total booking price in real time.

Once all details have been verified, the booking can be saved. The system stores the booking with the applied bonus code and its resulting price adjustment.

***

### **Notes**

* Bonus codes are configured per **Brand**, and their availability depends on agency setup.
* The system automatically validates each code against its active period, brand, and applicable products.
* If a code is invalid or expired, the system will not apply any discount or supplement, and a warning message may appear.
* Once a booking with a valid bonus code is saved, the price calculation reflects the adjustment permanently unless the booking is later modified or recalculated.
* Only authorized users may access or apply certain bonus codes, depending on system permissions.
