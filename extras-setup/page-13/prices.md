# Prices

A extras can have one or more prices. The prices are defined based on some intervals. The interval can not overlap each other to prevent that there are some validation in place. There are three intervals as follow:

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* **Age From/To** - The price is applying for the passengers that has the age in interval.
* **Departure Date From/To** - The Price is applying to passengers that have made the booking to depart in this interval.
* **Booking Date From/To** - The Price is applying to passengers that have made the booking in this specific interval.
* **Price** - The amount that the passenger will pay for this extras. The amount is in the local currency.
* **Group Price** - Price for groups
* **Cost Price** - The Amount that the agency will pay for this extras. If a creditor is selected the amount is in the creditor information other wise the amount is in the local currency.
* **Days** - This extra is available for the specified number of days. For a booking with 7 stay days, if days parameter is set to 9 days or more, product will not be available for selection anymore.
* **Margin** - Margin of profit when rent a car is checked in the extras configuration and defines the amount of money added in plus to the basic cost of the car.
* **Max cost** - Defines the maximum cost that a car can have so that the agency can sell it.
* **Per Day** - The price and cost is calculated per day. In case the Days is specified the price will be calculated based on this number otherwise the cost and price will be calculated based on the number of booked days.
* **Contract**&#x20;

The cost/price per day is calculated based on the formula: If Days is filled: `Price*Days=Extra_Price` If Days is empty: `Price*Booked_Days=Extra_Price`

### Price per brand <a href="#price-per-brand" id="price-per-brand"></a>

A new feature in Tourpaq that allows the setting of different prices for each brand. In order to use it please contact Tourpaq Support.

If only the default price is set, it will be applied to all agencies. If an agency price is set different of the default price, the agency price will be available only for the selected agency.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Editing the price is only available for the default price. For the agency price the only editable fields are **Price**, **Group Price**, **Margin** and **Max cost**

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Split prices**

The split function can be used in case of stop sales as well as price and cost changes.

Prices can be split by:

* age
* departure
* booking date

<figure><img src="../../.gitbook/assets/image (17) (1).png" alt=""><figcaption></figcaption></figure>

When clicking on the Split button, an option will appear bellow the price lines to set the number of splits to be made

<figure><img src="../../.gitbook/assets/image (18) (1).png" alt=""><figcaption></figcaption></figure>

If spliting by Departure or Booking date, the Date from of the first line is the original date and Date to is the new stop date.

The second line will contain the new Date from and the Date to will be the original stopping date.

It is advised to use the current day or next day Date to of the first line when splitting.

<figure><img src="../../.gitbook/assets/image (19) (1).png" alt=""><figcaption></figcaption></figure>

After filling in the details, click on **Split**

The result will look like:

<figure><img src="../../.gitbook/assets/image (20) (1).png" alt=""><figcaption></figcaption></figure>
