# Multiple product selection in product category

## Multiple product selection in product category

### Overview

The _Multiple Product Selection_ functionality allows users to purchase several products within the same product category. This feature was developed to give both **Web Booking** users and **Office Booking** users greater flexibility when selecting products such as meal types, upgrades, or optional extras.

### Purpose

This functionality enables:

* The purchase of multiple related products in a single category (e.g., several meal types).
* The setup of product upgrades or downgrades from a default selection.
* Advanced scenarios combining autoselected, hidden, or price-included products for greater pricing flexibility.

### How to use

#### Activation

The feature is enabled in **Tourpaq Office → Product Category → Edit Category** by selecting the checkbox\
**“Accepts multiple product selection.”**

Once activated, both the web and office booking systems allow multiple products to be selected within the same product category.

### Various scenarios <a href="#various-scenarios-of-work" id="various-scenarios-of-work"></a>

#### Multiple products selected in the same category

This scenario covers cases where a customer wants to purchase several products that belong to the same category.\
**Example:**\
A guest can select _Breakfast_, _Lunch_, and _Dinner_ within the **Meal** category during the booking process.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (168).png" alt="Multiple products selected in the Meal category"><figcaption></figcaption></figure></div>

#### Upgrade an autoselected product

In this setup, the system proposes a **default product** (e.g., a standard rental car).\
The customer can then:

* Upgrade to a higher category by paying the price difference, or
* Downgrade to a lower category if desired.

This ensures flexibility in product selection while maintaining a guided booking flow.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (169).png" alt="Autoselected product upgrade"><figcaption></figcaption></figure></div>

#### Unremovable autoselected product hidden in room price

Tourpaq also supports a combined configuration of:

* **Autoselected product**,
* **Multiple product selection** within the same category, and
* **Agency hide autoselected prices (include product price in room price)**.

This combination is typically used when the autoselected product has a **0 DKK** price value.\
The product price is included in the room price and remains invisible to the customer, while other products in the same category remain selectable.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (170).png" alt="Autoselected product included in room price"><figcaption></figcaption></figure></div>

> 📝 **This scenario is not supported by Tourpaq.**

**⚠️ Important notes and limitations**

**Unsupported Scenario**

A configuration where an **autoselected product** (included in room price) has a **price higher than 0 DKK** is **not supported**.\
If such a setup is used, the system displays incorrect price differences.

**Example:**

* Autoselected product price: **100 DKK** (included in room price).
* Two additional products available: **101 DKK** and **102 DKK**.
* The system displays differences as **+1 DKK** and **+2 DKK**,\
  but the total booking value increases by **203 DKK** instead of **3 DKK**.

> The system displays a warning when both\
> “Agency hide autoselected prices” and “Multiple product selection” are activated. Activating both options requires accepting the consequences of this setup.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (171).png" alt="Warning for incompatible product selection settings"><figcaption></figcaption></figure></div>

**Known Issue**

**Limitation:** For product categories related to **Catering**, the **Transport Reporting List** displays only the **last product** selected by a passenger in that category.

**Warning**

Tourpaq supports but **does not recommend** disabling **Multiple Product Selection** after bookings have already been made that include multiple products in the same category.\
If deactivated, the system attempts to display all previously selected products correctly, but **unexpected inconsistencies may occur.**

**Result:**\
Once configured, customers and office users can select multiple products from the same product category, providing a flexible and customizable booking experience. Proper configuration ensures price transparency and compatibility with existing booking and reporting logic.
