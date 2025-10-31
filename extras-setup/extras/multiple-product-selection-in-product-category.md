# Multiple product selection in product category

**Overview**\
The _Multiple Product Selection_ functionality allows users to purchase several products within the same product category. This feature was developed to give both **Web Booking** users and **Office Booking** users greater flexibility when selecting products such as meal types, upgrades, or optional extras.

**Purpose**\
This functionality enables:

* The purchase of multiple related products in a single category (e.g., several meal types).
* The setup of product upgrades or downgrades from a default selection.
* Advanced scenarios combining autoselected, hidden, or price-included products for greater pricing flexibility.

**How to Use**

**Activation**

The feature is enabled in **Tourpaq Office → Product Category → Edit Category** by selecting the checkbox\
&#xNAN;**“Accepts multiple product selection.”**

Once activated, both the web and office booking systems allow multiple products to be selected within the same product category.

### Various scenarios of work[​](https://docs.tourpaq.com/docs/documentation/multiple-product-selection-in-category#various-scenarios-of-work) <a href="#various-scenarios-of-work" id="various-scenarios-of-work"></a>

**1. Multiple Products Selected in the Same Category**

This scenario covers cases where a customer wants to purchase several products that belong to the same category.\
**Example:**\
A guest can select _Breakfast_, _Lunch_, and _Dinner_ within the **Meal** category during the booking process.

<figure><img src="../../.gitbook/assets/image (168).png" alt=""><figcaption></figcaption></figure>

**2. Upgrade Autoselected Product**

In this setup, the system proposes a **default product** (e.g., a standard rental car).\
The customer can then:

* Upgrade to a higher category by paying the price difference, or
* Downgrade to a lower category if desired.

This ensures flexibility in product selection while maintaining a guided booking flow.

<figure><img src="../../.gitbook/assets/image (169).png" alt=""><figcaption></figcaption></figure>

**3. Unremovable Autoselected Product Hidden in Room Price**

Tourpaq also supports a combined configuration of:

* **Autoselected product**,
* **Multiple product selection** within the same category, and
* **Agency hide autoselected prices (include product price in room price)**.

This combination is typically used when the autoselected product has a **0 DKK** price value.\
The product price is included in the room price and remains invisible to the customer, while other products in the same category remain selectable.

<figure><img src="../../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

> 📝 \*_Note:_ **Please note a scenario that is not supported by the Tourpaq system.**

#### **⚠️ Important Notes and Limitations**

**Unsupported Scenario**

A configuration where an **autoselected product** (included in room price) has a **price higher than 0 DKK** is **not supported**.\
If such a setup is used, the system will display incorrect price differences.

**Example:**

* Autoselected product price: **100 DKK** (included in room price).
* Two additional products available: **101 DKK** and **102 DKK**.
* The system will display differences as **+1 DKK** and **+2 DKK**,\
  but the total booking value will increase by **203 DKK** instead of **3 DKK**.

> The system will display a warning when the user tries to activate both\
> “Agency hide autoselected prices” and “Multiple product selection” simultaneously, as the user must take responsibility for the consequences of such a setup.

<figure><img src="../../.gitbook/assets/image (171).png" alt=""><figcaption></figcaption></figure>

**Known Issue**

**Limitation:** For product categories related to **Catering**, the **Transport Reporting List** will only display the **last product** selected by a passenger in that category.

**Warning**

Tourpaq supports but **does not recommend** disabling **Multiple Product Selection** after bookings have already been made that include multiple products in the same category.\
If deactivated, the system will attempt to display all previously selected products correctly, but **unexpected inconsistencies may occur.**

**Result:**\
Once configured, customers and office users can select multiple products from the same product category, providing a flexible and customizable booking experience. Proper configuration ensures price transparency and compatibility with existing booking and reporting logic.
