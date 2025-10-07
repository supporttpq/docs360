# Campaigns

Campaign is a feature in Tourpaq that allows the user to create a package of discounts and products according to a specific set of rules. Campaign feature can only be used with a campaign code.

A Campaign can be created in office, from **Extra Setup**/**Campaign**.

This page allows system administrators or marketing managers to **view, manage, and control discount campaigns** that can be applied to bookings. Campaigns are typically linked to special promotions, early booking incentives, or seasonal offers.

<figure><img src=".gitbook/assets/image (24) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Campaigns Table Explained

| Column                 | Description                                                                                                                                                                                               |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**               | The name of the campaign, clickable for detailed editing or overview.                                                                                                                                     |
| **Code**               | The campaign code                                                                                                                                                                                         |
| **Status**             | <p>Indicates the current state of the campaign:<br>🟩 <code>Open</code> = Active and available<br>🟥 <code>Full</code> = Fully booked, limit reached<br>🟥 <code>Deleted</code> = No longer available</p> |
| **Category**           | Groups campaigns under relevant discount types.                                                                                                                                                           |
| **Booking Limit**      | The maximum number of bookings allowed under this campaign.                                                                                                                                               |
| **Discount Limit**     | The maximum number of discounts applicable under this campaign.                                                                                                                                           |
| **Combine Discounts**  | ❌ Indicates if this campaign **cannot** be combined with other discounts (most likely disabled by default).                                                                                               |
| **Force Supplements**  | ❌ Indicates whether required supplements are **not** forced by the campaign.                                                                                                                              |
| **Disable Price List** | ❌ Indicates if the campaign disables the default price list.                                                                                                                                              |

### Actions Available

* **Create Campaign** – Use the blue `Create` button in the upper-right to launch a new campaign setup.
* **Edit Campaign** – Click on the campaign name to modify details.
* **Delete Campaign** – Use the 🗑️ trash icon at the end of the row to remove a campaign.

### Filtering and Visibility Options

* **Search Filters**: Filter campaigns by `Name`, `Code`, `Status`, and `Category`.
* **Show Hidden**: Check this to include deleted or hidden campaigns in the list.
* **Clear Filters**: Reset all filters using the `Clear` button.

### Basic Setup

#### &#x20;     Overview

To create a new campaign, click on the “Create” button

You need to complete the following fields:&#x20;

<figure><img src=".gitbook/assets/image (20) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Name: insert the name of the campaign&#x20;
* Category: select the category&#x20;
* Code: insert the campaign code that can be used to trigger the campaign. When using a code for a campaign, inserting the code in a booking will automatically add the extras and discounts available for the campaign to the passengers. When using a campaign without code, the extras available for the campaign have to be selected for the passengers in order for the discounts to be applied.&#x20;
* Status: select the availability of the discount Status can be: open, close, full or deleted.&#x20;
* Alarm: insert the number of bookings per day after which an alarm will be posted on the dashboard&#x20;
* Pricelist: select the pricelist on which the campaign is available Price list can be: normal, discount, group.&#x20;
* Currency: select the currency used for the campaign, must be the same currency used by the brand.&#x20;
* Booking limit: insert the maximum number of bookings that can use the campaign, when the maximum number of valid bookings is reached, the campaign status is changed to full and no more bookings can be made using the campaign; if bookings are canceled after the booking limit is achieved, the campaign doesn't change its status
* &#x20;Discount limit: insert the maximum amount value available for discounts. NOTE: If the limit is set to eg. 30000, the current amount is 25000 and a booking has a discount of 10000, it will go over the limit, but it will be the last booking made with that campaign. When the amount is achieved, the campaign status is set to full.
* &#x20;Estimate turnover: estimated amount of income, used for statistics&#x20;
* Pax: estimated passengers, used for statistics&#x20;
* Do not combine discounts: if checked, same rules from the Do not combine discounts apply.&#x20;
* Do not combine with extra bed discount: if checked, it will not allow extra bed discounts for the booking.&#x20;

### Force Extras&#x20;

1. When the campaign has a code and Force extras is checked, removing an extra from a passenger also removes the campaign discounts from that passenger; if the extra has special features (add one per room, add only the first passenger, add to each x passengers etc) the campaign discounts are removed from all passengers.
2. &#x20;When the campaign has a code and Force extras is unchecked, removing an extra from a passenger will not remove the campaign discounts (when removing the extra, the discount value will remain unchanged)&#x20;
3. When the campaign doesn't have a code, Force extras has to always be checked, else the campaign cannot be created.

### **Code**

* When using a code for a campaign, inserting the code in a booking will automatically add the extras and discounts available for the campaign to the passengers.
* When using a campaign without code, the extras available for the campaign have to be selected for the passengers in order for the discounts to be applied.

### **Brands**

Select the brands for which the campaign is available.

### **Resources tab**

* Departure airport: select from the available starting airports (multiple selection)
* Arrival airports: select from available destination airports (multiple selection)
* Country: select from available countries (multiple selection)
* Resort: select from available resorts (multiple selection)
* Transport: select from available transports (multiple selection)
* Real transport: select from available real transport (multiple choice)
* Hotels: select from available hotels (multiple selection)
* Rooms: select from available rooms (multiple selection)
* Hotel categories: select from available hotel categories (multiple selection)

If no resorts and/or transports are selected, the campaign will be applied to all bookings that use both the selected depature airports and arrival airports.

### **Extras tab**

* Extras: select from available extras (multiple selection)
* New name: the name inserted will appear as the first part of the discounts name in bookings

Display names - when checked will display the names of the products, rooms, hotels, resorts, departures and arrivals instead of their codes.

**Discount calculation**

* Discount type: select from 5 different types of discounts:
  * Per booking
  * Per adult
  * Per child
  * Per extra
  * Per room
* Requirements:
  * Age (from-to): insert the age interval of the passengers elligible for the discount (2-12; 15-20)
  * Rank (from-to): insert the passengers that will acctually receive the discount (if the rank is set 3-4, only the 3rd and 4th passengers that have the required age will receive the discount)
  * Select supplement: select the supplement (only for per supplement discounts)
* Interval 1-4: for each trip period 3 discount rules can be inserted:
  * % (percentage): the passenger will receive a discount based on a percentage of the Room price
  * Discount: the passenger will receive a fixed amount as a discount
  * Fixed price: the passenger will pay a fixed amount, regardless of the room price (Room price - fixed price = discount)

Note: A discount line cannot have more than 1 rule for each interval (if percentage has been decided for the first interval, fixed price and discount rules cannot be used anymore for that interval and line) All intervals must be filled.

### Discount Calculation

* **Per booking discount**

Only the first passenger receives the discount according to the requirements set

* **Per person Adult discount**

Adult passengers receive discounts according to the requirements set

* **Per person Child discount**

Child passengers receive discounts according to the requirements set

* **Per extra**

All passengers receive discounts according to the requirements set.

The extra percentage discount is calculated as a percentage from the total price of the extras available in the campaign for the passenger.

The extra discount gives the inserted amount as a discount regardless of the total price of the extras.

The fixed price discount gives discounts depending on the total price of the extra:

* If the inserted amount is greater than the total price of the extra, the discount will be the total price of the extra.
* If the inserted amount is lower than the total price of the extra, the discount will be the difference between the total price of the extra and the inserted amount.



* **Per room discount**

First passengers in the room receive discounts according to the requirements set. The rank refers to the room, and not the passenger.

A campaign setup should look like this (this is an example, as the campaign can be setup in many ways, depending on the needs):

<figure><img src=".gitbook/assets/image (21) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Discount Limit <a href="#discount-limit" id="discount-limit"></a>

There are 2 types of discount limits

* Per Booking - Discount amount given to all pax on the booking will not be greater then the set value
* Per Pax - Discount amount given to a pax will not be greater then the set value

They can be used separately or combined.

<figure><img src=".gitbook/assets/image (22) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Campaign linked with product (Select your benefit) <a href="#campaign-linked-with-product-select-your-benefit" id="campaign-linked-with-product-select-your-benefit"></a>

This is a special type of campaign that gives a discount in relation with a selected product. The product must be in the list of products and needs a discount line.

More than one product can be selected.

<figure><img src=".gitbook/assets/image (23) (1) (1).png" alt=""><figcaption></figcaption></figure>

The user will receive the discount after inserting the code and selecting the product the discount will apply to.

When selecting the product for which the discount will be applied, the product will also be selected automatically, both in office and webbooking.

The only exception is the seating product:

* In office you will need to first select the seating, save the booking and after that insert the code and select the benefit.
* In webbooking you will need to insert the code, select the product for the discount, then select the seating in transport layout pop-up.

**Special cases regarding combination of campaign features**

Combining some features of the campaign will result in various behaviours as explained below.

### Force Extra + Code + extra + discount <a href="#force-extra--code--extra--discount" id="force-extra--code--extra--discount"></a>

* Per Booking discount
* +basic extra = discount is removed only if the extra is removed from the first pax of the booking
* +Add to basic price = if the extra is removed from a pax, then that pax will loose the discount
* +Add only one per room = all campaign discounts are removed from the booking if the extra is removed from any pax
* +Add only to lead pax = all campaign discounts are removed from the booking if the extra is removed from lead pax
* +Add one to each "x" pax = all campaign discounts are removed from the booking if the extra is removed from any pax
* Per adult / Per Child discount
* +basic extra = discount is removed only if the extra is removed from the first pax of the booking
* +Add to basic price = if the extra is removed from a pax, then that pax will loose the discount
* +Add only one per room = all campaign discounts are removed from the booking if the extra is removed from any pax
* +Add only to lead pax = all campaign discounts are removed from the booking if the extra is removed from lead pax
* +Add one to each "x" pax = all campaign discounts are removed from the booking if the extra is removed from any pax
* Pr extra

1.Select all

a) basic - discount is removed from pax

b) ABP - discount is removed from pax

c) AOPR - discount is removed from booking

d) AOE - discount is removed from booking

e) AOTL - discount is removed from booking

2.Select extra

a) basic - discount is removed from pax

b) ABP - discount is removed from pax

c) AOPR - discount is removed from booking

d) AOE - discount is removed from booking

e) AOTL - discount is removed from booking

3.Any product - discount amount will be related to the assigned product

a) basic - discount is removed from pax

b) ABP - discount is removed from pax

c) AOPR - discount is removed from booking

d) AOE - discount is removed from booking

e) AOTL - discount is removed from booking

When 2 or more types of discounts are assigned to the campaign, removing a product will result in the removal of all discounts assigned to that campaign. (Exception: basic and ABP products)

* Per Room discount
* +basic = discount removed from pax
* +ABP = discount removed from pax
* +AOPR = discount removed from booking
* +AOE = discount removed from booking
* +AOTL = discount removed from booking

### Force Extra + extra + discount (Campaign without a code) <a href="#force-extra--extra--discount-campaign-without-a-code" id="force-extra--extra--discount-campaign-without-a-code"></a>

For no code campaigns, removing a product assigned to the campaign will result in the removal of all discounts assigned to that campaign.

### Code + extra + discount (Campaign without Force Extra enabed) <a href="#code--extra--discount-campaign-without-force-extra-enabed" id="code--extra--discount-campaign-without-force-extra-enabed"></a>

In this case, removal of the product will not result in the removal of the campaign discounts.

### Using Campaign in office <a href="#using-campaign-in-office" id="using-campaign-in-office"></a>

#### Campaigns with bonus codes <a href="#campaigns-with-bonus-codes" id="campaigns-with-bonus-codes"></a>

Campaign can be used in bookings like any other bonus code.

After the allotment has been taken and the passenger details have been set, the Campaign code can be inserted into the Bonus code case.

!!!Please note that the extras selected may be overwriten by the extras assigned to the campaign.

After the bonus code has been entered, click outside of the Bonus code case to validate the campaign code, if the code is valid it will remain in the case.

If the Campaign code is valid, the passengers can be saved.

In order to use a campaign without bonus code, the booking in question must have all products assigned to the campaign selected in a correct format for it's passengers. If the extras are not selected, the discounts will not be applied.

### Campaign alarms <a href="#campaign-alarms" id="campaign-alarms"></a>

It is found on **Dashboard**. In this tab an alert will appear that will notify the user when a set number of bookings per day have been made for the campaigns in progress.
