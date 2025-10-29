# Teetime

Available for Admin user types.

Teetimes allows the user to set a time schedule for the availability of a certain product.

It can be set up as a normal product from **Extras Setup/Extras**.

The difference is in the use of **Generic Allotment Type** and the adittion of a few new settings when that type is chosen.

**Pax limit** - how many products can be booked by a guest

**Limit per day** - how many products a guest can book per day

**Limit before hour** - how many products a guest can book per booking before a set hour

**Latitude** - used for displaying the sunrise and sunset when booking the product in office/web

**Longitude** - used for displaying the sunrise and sunset when booking the product in office/web

**Product Parent ID** - used to connect products that share the same allotment across companies

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Also the Extra category has to be se as a Teetime Category Type.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Prices <a href="#prices" id="prices"></a>

Teetime products draw their cost and price from **Generic Product Price Rule**, any value inserted in the Price tab will be disregarded. But a price line is required to enable the product to be sold. The priceline should look like this:

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

It is similar with the seating setting.

Real price of the product is set in **Extras Setup/Generic Product Price Rule**.

<figure><img src="../../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>

TeeTimes products appear in the **Tee Time Extras Lists**.

For this to work, the product needs to have a supplier assigned. The supplier cannot block the allotment of a TeeTime if he doesn't have the rights to do so, but he also has access to the lists

### Special settings <a href="#special-settings" id="special-settings"></a>

**Generic Allotment**

Allotments can be generated on a daily or weekly basis

<figure><img src="../../.gitbook/assets/image (145).png" alt=""><figcaption></figcaption></figure>

### Daily allotments <a href="#daily-allotments" id="daily-allotments"></a>

* Frequency - availability of the product on a daily basis (number of days can be set in the text box)
* Daily frequency - sets the availability of the product for the day:
* It can be chosen at a specific time
* It can be chosen every x minutes in a set hourly interval
* Duration - the period in which the product is available
* Allotment - number of products available according to the rules set ( if the product is sold every 30 minutes, then every 30 minutes the number of products available will be the inserted value)

<figure><img src="../../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

This is an example of how it looks after the allotments have been generated

<figure><img src="../../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

### Weekly allotments <a href="#weekly-allotments" id="weekly-allotments"></a>

The only change from **Daily allotments** is

* Frequency - this time it is in weeks and not days, with the additional selection of days of the week in which the product is available

<figure><img src="../../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

* if "All days" checkbox is selected, the allotment is generate for the entire week, but if you have the departure in one specific day, in the guest app only the first valid day of the respective allotments will be displayed. (Ex: Generate the allotment for the whole week and you have a departure on Tuesday -> it only brings you for Tuesday

<figure><img src="../../.gitbook/assets/image (207).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (208).png" alt=""><figcaption></figcaption></figure>

### Block allotments <a href="#block-allotments" id="block-allotments"></a>

This feature allows the user to block or unblock allotments for a set period of days between certain hours.

<figure><img src="../../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>
