# How to set Payment settings

### **Overview / Purpose**

Payment settings define how a brand handles transactions within Tourpaq. This includes accepted card types, booking payment methods, gift card usage, and last-minute sales (LMS) rules. Proper configuration ensures smooth payment processing and accurate handling of special cases like last-minute bookings.

***

### **How It Works**

* Payment settings are configured per **brand**.
* Administrators can define:
  * Which **card types** the brand accepts.
  * The default **booking payment type**.
  * Whether **gift cards** are accepted.
  * **Special access settings** for last-minute sales, determining LMS eligibility.
* The system uses these settings to validate payments and apply LMS rules automatically.

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Key Features / Functions**

#### **Card Types**

* Select one or multiple **card types** that the brand will accept (e.g., Visa, Mastercard, Amex).
* Ensures customers can only use valid payment methods.

#### **Booking Payment Type**

* Choose the default **payment type** for bookings using the dropdown menu.
* Examples include: credit card, invoice, or cash.

#### **Gift Card Payments**

* Enable or disable **gift card usage** for bookings associated with this brand.

#### **Special Access / LMS Settings**

* Configure **Web Payment LMS Day Limit**:
  * Determines when a booking is considered **last-minute**.
  * A booking is LMS if the booking date is **equal to or fewer days than the set limit** relative to the departure date.
  * Helps apply special payment or booking rules for last-minute sales.

#### **Save Settings**

* After making changes, click **Save Payment** to apply the settings.

***

### **Examples / Scenarios**

1. A brand accepts **Visa and Mastercard**, but not Amex. Customers trying to pay with Amex are blocked.
2. LMS settings are configured to **3 days**:
   * Any booking made 3 days or less before departure is treated as last-minute.
3. Gift cards are enabled, allowing customers to redeem a stored-value card for partial or full payment.

***

### **Notes / Best Practices**

* Regularly review accepted **card types** to ensure compatibility with payment providers.
* Set LMS days according to operational needs; shorter periods allow more flexibility but require quick processing.
* Only enable **gift cards** if the brand is prepared to handle redemptions accurately.
* Always click **Save Payment** to confirm changes; unsaved modifications will not apply.
