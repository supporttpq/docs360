# Generate Pricelist

### Generate Price List Service <a href="#generate-price-list-service" id="generate-price-list-service"></a>

**Generate Price List** is a service how create Price List based on a resort and transport. Will be scheduled all hotels with allotments in FixQuota's period and assigned to current agency from schedule rule.

The transport has to have the same brand as the one set for the price list generation rule. Set the brand in transport.

<figure><img src=".gitbook/assets/image (58) (1).png" alt=""><figcaption></figcaption></figure>

After saving, to continue to add a rule, it is necessary to add a fix quota. Select a fix quota. We can select any fix quota provided, as they are unique, and for each fix quota we can set an interval. It is mandatory the new interval to be included in the parent fix quota.&#x20;

The system will generate price lists only for future departure. If you have chosen a fix quota with departure in the past, the system will ignore this fix quota.&#x20;

Now we add the rule to the system. After a rule is added, it is set to run, and the system will generate a price list for the current combination.
