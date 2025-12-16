# Packages

### Overview

The **Packages Generator** is used to create **package suggestions** that can be shown to users in **Select Offer** (typically for web/online sales).

A package is a pre-generated combination based on:

* A defined **date interval**
* A selected **agency**
* A selected **stay length/interval type**
* An optional **discount** applied to the total price

After packages are generated, they can be selected in **Select Offer**, and a booking can be created from the chosen package.

***

### Where to find it

Go to **Price List → Packages Generator**.

***

### Create a package rule

{% stepper %}
{% step %}
### 1. Open Packages Generator

Navigate to **Price List → Packages Generator**.
{% endstep %}

{% step %}
### 2. Create a new rule

Click **Create** and fill in:

* **Name** – The package name shown to users.
* **Agency** – Which agency the package should be available for.
* **Start** / **End** – The sales period.
* **Interval** – The basis used for generating packages (stay length / travel interval).
* **Discount** – Discount applied to the total price (if used).

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### 3. Save the rule

Click **Save**.

After saving, the rule appears in the list and is ready for generation.
{% endstep %}
{% endstepper %}

***

### Generate packages

1. Select the rule in the list.
2. Click **Generate** (or the equivalent action in your UI).

After generation, the packages are created and added to the available package list.

<figure><img src="../../../.gitbook/assets/image (6) (2).png" alt=""><figcaption></figcaption></figure>

***

### Remove generated packages

If you need to undo a generation:

1. Click **Remove Packages** to delete the generated packages.
2. If needed, remove the **rule** that generated them.

***

### Use generated packages in Select Offer

After a package is generated, it becomes available in **Select Offer**.

1. Open **Select Offer**.
2. Choose a generated package.
3. Continue to the **Create booking** window.

<figure><img src="../../../.gitbook/assets/image (7) (2).png" alt=""><figcaption></figcaption></figure>

***

### Notes about prices

* Prices displayed in **Select Offer** already include **discounts and supplements**.
* If a transport has **discount prices** defined, those are included in the price shown in the Select Offer pop-up.

{% hint style="info" %}
If you expected a package to appear in Select Offer but it does not, double-check the **agency**, **date interval**, and that the underlying products (hotel/transport/prices) exist for the selected period.
{% endhint %}
