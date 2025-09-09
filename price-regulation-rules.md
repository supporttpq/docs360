# Price regulation rules

#### **Overview**

The **Price Regulation Rule** defines automatic pricing adjustments for offers in the system. It allows you to configure how prices should change based on time, number of offers, and predefined limits. This ensures competitive pricing while maintaining control over minimum values.

***

#### **Purpose**

The purpose of this rule is to:

* Automate price increases or decreases for offers.
* Control how often and by how much a price can change.
* Ensure prices never go below defined minimum thresholds.
* Reduce manual intervention when managing multiple offers.

***

#### **Preconditions**

* The user must have permissions to create or edit price regulation rules.
* A valid **Name** and **Code** must be provided.
* Business rules for pricing (amounts, hours, and limits) should be clear before configuring.

<figure><img src=".gitbook/assets/image (52) (1).png" alt=""><figcaption></figcaption></figure>

#### **Instructions**

1. Navigate to **Price Regulation Rules** in the system and select **Create/Edit Rule**.
2. Fill in the fields as follows:

**Fields Explanation**

* **Name \***
  * The descriptive name of the rule (e.g., _Weekend Discount Rule_).
  * Mandatory.
* **Code \***
  * A unique identifier for the rule, often used internally.
  * Mandatory.
* **Amount \***
  * The standard adjustment amount (e.g., increase by 100).
  * Mandatory.
* **Amount (down)**
  * The adjustment amount applied when lowering the price.
  * Mandatory.
* **Hours number**
  * Time interval (in hours) after which the **Amount** increase adjustment applies.
  * Mandatory.
* **Hours number (down)**
  * Time interval (in hours) after which the **Amount (down) decrease** adjustment applies.
  * Mandatory.
* **Offers number**
  * The number of offers required before applying the **Amount** increase adjustment.
  * Mandatory.
* **Offers number (down)**
  * The number of offers required before applying the **Amount (down)** decrease adjustment.
  * Mandatory.
* **Lowest price** / **Lowest price2** / **Lowest price3** / **Lowest price4**
  * Minimum allowed price thresholds.
  * The system will never lower prices below these defined values.
  * Multiple fields allow flexibility for different categories, products, or scenarios.
  * Mandatory.

3. After filling in the details:
   * Review all minimum price values carefully to prevent underpricing.
   * Save the rule.
4. The rule will now automatically regulate prices based on the defined triggers (time, offers, and limits).

***

✅ **Best Practices for New Employees**

* Always set realistic **Lowest price** values to avoid unprofitable sales.
* Use **Hours number** carefully—too small values may cause frequent price changes.
* Clearly label rules using **Name** so they can be easily identified later.
* Double-check both **Amount** and **Amount (down)** to ensure they follow company pricing policies.

{% hint style="info" %}
Note!  When a pricelist regulation rule is set , a pricelist history is automatically updated and it it is possible to be viewed that a service has run every time the price is adjusted according the pricelist regulation rule set.

The feature to set price list goup/godown limits to be available needs to be configured in [System Setup](setup/system-setup.md)

<img src=".gitbook/assets/image (349).png" alt="" data-size="original">
{% endhint %}

To use the price list rules, after you have activated the feature and the service runs, you'll go to the price list, choose the transport, choose a hotel and a room type, and then click Display. Here you have a column where you can set the rules&#x20;

<figure><img src=".gitbook/assets/image (53) (1).png" alt=""><figcaption></figcaption></figure>

Click Save.
