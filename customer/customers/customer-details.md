# Customer Details

{% hint style="info" %}
**How to access:** Open a customer profile by going to [Customers](./) and clicking the customer’s **Customer No**.

**Permissions:** Editing fields and seeing all panels depends on your user role and your organization’s setup.
{% endhint %}

### Overview

The **Customer Details** page shows everything Tourpaq knows about a single customer in one place:

* Contact details (name, email, phone, address)
* Activity and history (bookings, offers, service cases, etc.)
* A financial summary (turnover, profit, pax counts, and breakdowns)

Use this page when you need to verify customer information, update contact details, or understand the customer’s booking history and value.

***

### Page layout

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (3) (1).png" alt="Customer Details layout"><figcaption></figcaption></figure>

The page is typically split into three areas:

1. **Customer information** (left)
2. **Customer activity & history** (center)
3. **Totals summary** (right)

***

### Typical workflow

{% stepper %}
{% step %}
### Confirm you’re looking at the right person

Check the **name**, **email**, and **phone** first. If anything looks wrong, verify the customer number from the booking or from the [Customers](./) list.
{% endstep %}

{% step %}
### Update contact details (if needed)

Edit the fields in the **Customer information** panel and click **Update** to save.
{% endstep %}

{% step %}
### Review bookings and related history

Expand **Bookings** (and other panels like **Service Cases**) to see what is connected to the customer.
{% endstep %}

{% step %}
### Check totals

Use the **Totals summary** panel to understand turnover/profit and booking counts.
{% endstep %}
{% endstepper %}

***

### Customer information (left panel)

This panel contains the customer’s contact details and internal indicators. It commonly has two tabs:

* **Primary**: the customer’s main contact details
* **Secondary**: alternative contact details (if your organization uses them)

#### Common editable fields

These fields are typically editable (depending on permissions):

* **First Name / Last Name**
* **Email**
* **Phone** (and other phone number fields)
* **Address / Zip Code / City / Country**

#### Common informational fields

These fields are often used for reporting or internal workflows:

* **Gained Bonus**: bonus points accumulated for the customer
* **Special Guest**: marks a customer with special status (meaning is defined by your organization)
* **Happiness Overall / Happiness Represent.**: internal satisfaction/quality metrics (if enabled)
* **Total Complaints**: number of complaints/service records registered for the customer

{% hint style="warning" %}
**Remember to save:** changes are not stored until you click **Update**.
{% endhint %}

***

### Customer activity & history (center panel)

The center panel contains expandable sections. What you see here depends on your setup.

#### Bookings

Shows the customer’s bookings in a list/table.

* **BKG. No** is usually clickable and opens the booking
* Use the available **filters** to narrow the booking list (for example to find upcoming departures)

#### Other sections you may see

* **Offers**: offers linked to the customer (if used)
* **Service Cases**: complaints, requests, or support-related records linked to the customer
* **Old Bookings**: historical bookings
* **Bonus Packages**: bonus programs linked to the customer (if used)
* **Catalog Orders**: customer orders (if used)

You can expand/collapse sections individually. If available, use **Close all** to collapse everything and reduce clutter.

***

### Totals summary (right panel)

This panel is a financial and volume overview based on the customer’s bookings.

You’ll typically find:

* **Total Turnover** (often shown in EUR, depending on configuration)
* **Booking Numbers** (how many bookings are linked to the customer)
* **Pax Number / Inf Number** (passenger and infant counts)
* Breakdown totals (for example **Insurance**, **Transfers**, **Discounts/Supplements**, and other categories)
* Profit metrics (for example **Total Profit** and **Profit per PAX**) if enabled

Use this area to quickly understand the customer’s overall value and what makes up the totals.

***

### Tips

* If you don’t see expected sections (Offers, Bonus Packages, etc.), it may be due to **permissions** or because your organization does not use that module.
* If totals look outdated after changes, refresh the page or reopen the customer.
* If you discover duplicate customer profiles, use [Merge customers](../../merge-customers.md) (if available to your role).

***

### FAQ

<details>

<summary><strong>I updated a field, but it didn’t change. Why?</strong></summary>

Most updates require clicking **Update** in the customer information panel. If you navigated away without saving, the changes will be lost.

If you clicked **Update** and it still doesn’t save, you may not have permission to edit that field.

</details>

<details>

<summary><strong>Why can’t I edit the customer details?</strong></summary>

Editing depends on your user role. Some users can view customer data but not change it.

</details>

<details>

<summary><strong>I don’t see bookings for this customer. What should I check?</strong></summary>

* Ensure you opened the correct customer (verify **email/phone**).
* Check whether a filter is hiding results.
* The booking may be linked to a different (duplicate) customer profile.

If you suspect duplicates, use [Merge customers](../../merge-customers.md).

</details>

<details>

<summary><strong>What does “Special Guest” mean?</strong></summary>

This is an internal flag. The exact meaning (and how it should be used) is defined by your organization’s workflow.

</details>

<details>

<summary><strong>What are “Happiness” fields used for?</strong></summary>

If enabled, these are internal customer-satisfaction indicators used for quality tracking and reporting.

</details>

<details>

<summary><strong>Why do totals look wrong (turnover/profit/pax)?</strong></summary>

Totals depend on what bookings are linked to the customer and how your system calculates turnover/profit.

Common causes:

* The customer has no bookings (or bookings are linked to a different profile)
* A booking was recently edited and the page hasn’t been refreshed
* Profit fields may be hidden/disabled depending on permissions and configuration

</details>

<details>

<summary><strong>How do I get back to the customer list?</strong></summary>

Go back to [Customers](./).

</details>
