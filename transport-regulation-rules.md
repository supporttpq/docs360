# Transport Regulation Rules

Applies to Administrator

This function allows users to automatically change the prices on all pricelists for a transport allotment. The rules are available for the company, and the rules are set on a transport allotment from the Transport –FixQuotas(view) – transport allotment table. For Load Factor usage within the corresponding feature rules, the Factor Matrix and Price Regulation functionalities must not be blocked. Please contact Tourpaq Support for this. The rule has the following 2 sets of fields:

<figure><img src=".gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**General fields** (used for going prices UP) :&#x20;

* Name (required) - name of the rule
* Code (required) - it will be displayed in the price lists table&#x20;
* Amount (required)&#x20;
* Days number & Offers number (at least one of those is required)

**Example:** \*If the amount is 300, days number 5 and offers number 3: If there are 3 offers made in the last 5 days raise the price with 300. (after that, the transport allotment has a timer that is reset, so on the next verification, only the offers buy after this point are counted). \*If the amount is 400, days are not set, offers number 3: on every 3 offers raise the price with 400. \*If the amount is 500, days number 3, offers number not set: on every 3 days raise the price with 500.

* Optional fields (used for going the prices DOWN; those can be ignored, then the rule takes the prices only up. If you fill at least one of these fields, you need to fill all)&#x20;
* Amount (down)
* Days number (down)
* Offers number (down)
* Lowest price1 - the price will not go under this price for interval 1&#x20;
* Lowest price2 - the price will not go under this price for interval 2&#x20;
* Lowest price3 - the price will not go under this price for interval 3
* Lowest price4 - the price will not go under this price for interval 4
* Load Factor Start and Load Factor End - rule will be applied for transports with load factor variation % within a defined interval.
* Week Start (x) and Week End (y) - the departures for the rule to be applied - starting from today, will be applied to the departures over x weeks until y weeks; eg: rule has start week=3 and end week=5 and service runs on 01.01, the rule will be set for departures between 22.01 and 05.02 and so on
* Currency - the currency for the amount set; the currency exchange will be applied on calculating PLTA, according to brand setup&#x20;
* Rounding Rule - rounding rule will be applied to the amount set on the rule, after currency exchange: for eg: an amount of 200 EUR and rounding rule 49,99, the amount that the pricelist will increase with is 1549 DKK - for an exchange rate of 7.5

Load factor is calculated based on the defined Factor Matrix, under Transport -> Factor Matrix tab. Here user can define the load factor based on weeks for a transport. Load Factor for a certain transport is calculated behind and can be checked into Transport->Transport Price Control on the Load Factor tab.

<figure><img src=".gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Based on the load factor, the price regulation rules can be set. Rule can be assign for a departure of a transport under Fix Quota:

<figure><img src=".gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Based on an interval of values for Load Factor, certain price regulation rule will be applied or not.

**Example:** \*If the amount(down) is 300, days number(down) 5 and offers number(down) 3: If in the last 5 days at least 3 offers were not done, decrees the price with 300(only if the price doesn’t go under the lowest price). (after that the transport allotment has an timer that is reset, so on the next verification only the offers buy after this point are counted).

The rule count the offers for all the agency, and if the rule pass the price for all the pricelists for all the agency is changed. If the price list has a price regulation rule set on it, for Down – price part we verify that the price don’t go under the lowest price from the rule set on pricelist (if is set) and ignore price lowest price from the transport rule. The price list rule and the transport rule run individually, so it is possible that the price for one pricelist is modify by both rules in the same time without a problem.

The system has a service(PRRS) that verify if there are rules set on transport allotments that pass. If exist such rules, the service modify the price and keep the modifications. Those modifications can be seen from the price list table- modifications popup – automatic modifications.

The service verify every interval individually and set the prices by the following rules:

* If the discount is not 0, modify the discount else modify the price. For the Up –price part, if the discount is modified and the price became smaller that the discount, modify the price to.\\
* If the Up-price part PASS, the system doesn’t verify the Down-price part.\\
* For the Down – price part, the discount / price go down until he reach the lowest price (from pricelist rule if is defined, else from the transport rule) so is possible that the rule pass but the discouts/prices remain the same.

### Schedules <a href="#schedules" id="schedules"></a>

This feature permits the user to set up schedulers to maintain an automatic change of the regulation rules.

They can be added under the menu Transport -> Tr. Regulation Rules -> Schedules.

<figure><img src=".gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Create Schedule**

In order to create a schedule, the following fields have to be completed:

* **Rule** - The rule to be set
* **Transport** - The transport to be applied on
* **Weeks Before Arrival** - With how many weeks to set the rule before. This setup will consider the exact date (day) , meaning that if schedule is set for eg, on Monday with 3 weeks before, but the departures on that transport are on Wednesday, then, the rule will be applied only on Wednesday for the departure over 3 weeks.
* **Active** - The status of the schedule

<figure><img src=".gitbook/assets/image (11) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Workflow**

Every day a service will run (CTRS) and will check every schedule. If the departure date meets the weeks condition, the regulation rule will be applied.

First the service will just apply the rule set on schedule.Then the same service will check the conditions and will apply the first regulation rule that meets them for all transports and departures: setting a new one, overwriting or just removing the rule (if conditions are not met)

**Very important:** the service will consider only transports with "Use Change Rule Service" set.

<figure><img src=".gitbook/assets/image (12) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* If the rule is not set, it will be set up.
* If a rule is already set, will be changed (if the case) with the first rule (from all the existing ones) that meets the conditions .
* The rule on the schedule will be applied only to the departures according to the weeks set.
* The regulation rule is applied according to the load factor variation % calculated according to \[\[transport\_matrix|transport matrix set-up]] and weeks interval (if set). If the conditions are not met, will remove any rule
