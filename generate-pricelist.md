# Price List Generator

### Generate Price List Service <a href="#generate-price-list-service" id="generate-price-list-service"></a>

The **Generate Price List Service** automatically creates price lists based on a **resort** and **transport**.

#### Key Points

* All hotels with allotments in the selected **Fix Quota** period will be scheduled and assigned to the **current agency** according to the schedule rule.
* The transport must have the **same brand** as the one set for the price list generation rule. Set the brand in the **Transport** settings.
* Only **future departures** are processed. Fix quotas with past departures are ignored.

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Steps to Add a Generation Rule

1. **Save Initial Rule** – After defining the basic resort and transport, save the rule to continue.
2. **Select Fix Quota** – Choose any available fix quota. Each fix quota is unique, and an interval can be set for it.
   * The **new interval** must be included within the parent fix quota.
3. **Add Rule to System** – Once added, the rule is active.
4. **Generate Price List** – The system will generate price lists for the current combination of resort, transport, and fix quota according to the rule.
