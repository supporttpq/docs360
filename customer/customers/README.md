# Customers

{% hint style="info" %}
**Permissions:** This module is typically available to **Administrators** (or users with equivalent customer-management rights).
{% endhint %}

### Overview

The **Customers** page is your starting point for finding and working with customer records in Tourpaq.

From here you can:

* Search and filter the customer database
* Open a customer profile to view or update details
* Select one or more customers to **send email/SMS** or **export** a list
* Check whether a customer is subscribed to your newsletter

***

### Typical workflow

{% stepper %}
{% step %}
### Find the customer

Use **Search Customer** for a quick lookup, or use filters (name, email, phone, city, etc.) to narrow the results.
{% endstep %}

{% step %}
### Open the customer profile

Click **Customer No** to open the customer’s full profile (contact details, bookings, totals, and history).
{% endstep %}

{% step %}
### Take action (optional)

Select customers using the checkbox column, then choose an action such as **Send Email**, **Send SMS**, or **Export**.
{% endstep %}
{% endstepper %}

***

### Search and filter customers

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (3).png" alt="Customer search and filters"><figcaption></figcaption></figure>

#### Quick search

* **Search Customer** searches across customer records (for example name, email, or phone — depending on your configuration).

#### Common filters

Use these when you know a specific detail:

* **Customer No** (fastest when you have the customer ID)
* **First Name / Last Name**
* **Company**
* **Email / Phone / Mobile / Fax**
* **Contact** (filters by a registered contact person, if used by your organization)
* **Ev Phone** (often used as an _evening_ or _alternative_ phone number)

#### Address and location filters

Use these when you only know where the customer lives:

* **Address**
* **City**
* **Zip Code**
* **Country**

#### Booking-related filter

* **Departure Period (Start / End)**: filters customers based on the departure period connected to their bookings.

<details>

<summary>Advanced filters</summary>

Depending on your setup, you may also see additional filter areas such as **Users**, **Transports**, and **Hotels**.

* If an area has an **Edit** option, it usually means the filter can be configured (for example, selecting which users or items to include).

</details>

#### Filter controls

* **More filters**: shows additional filter fields.
* **Clear**: resets all filters back to default.
* **Display**: switches how results are displayed (for example list view), depending on your configuration.

{% hint style="warning" %}
If you get too many results, add **one more filter** (for example Country + Last Name) instead of scrolling through the full list.
{% endhint %}

***

### Customer list (results)

After you search, the results appear in a table.

#### Key columns

* **Customer No**: the customer’s unique ID. Click it to open the customer profile.
* **Customer Name**: full name.
* **Email / Phone**: primary contact information.
* **Country / Zip Code / City**: location details.
* **Newsletter**: indicates whether the customer is subscribed (the icon shown depends on your configuration).

#### Selecting customers

Use the checkbox on the left side of each row to select customers for bulk actions (email, SMS, export). Available actions depend on your permissions.

***

### Customer actions

Once you have results (and have selected one or more customers), you may have access to these actions:

* **Send Email**: send a message to the selected customers.
* **Send SMS**: send a text message to the selected customers.
* **Export**: export the current list (usually to Excel; available formats depend on your configuration).
* **Show Schedules**: generate a list based on predefined schedules/filters (if your organization uses scheduled customer lists).

<figure><img src="../../.gitbook/assets/2470fd6d-6824-48f2-a602-c842aa595538.webp" alt="Customer actions toolbar"><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/b7376cb3-642c-4cf1-9bfc-a3049420504c.webp" alt="Export options"><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/c0b00615-8a2b-4b45-9461-da8d7f6ba29b.webp" alt="Scheduled lists"><figcaption></figcaption></figure>

***

### Tips

* **Sort the list:** click a column header (for example _Customer Name_ or _City_) to sort.
* **No results:** click **Clear** and try again with fewer filters.
* **Newsletter segmentation:** use the **Newsletter** column/filter to build a list for campaigns.
* **Data quality:** if you find duplicates, use the **Merge customers** tool (if available to your role) to keep your customer database clean.

***

### FAQ

<details>

<summary><strong>I can’t find a customer. What should I try?</strong></summary>

1. Click **Clear** to remove all filters.
2. Try searching by **Email** or **Phone** (these are usually more reliable than names).
3. If the name might be misspelled, try a shorter search (for example only the last name).
4. If the customer still doesn’t appear, they may not exist in your database yet, or your permissions may limit what you can see.

</details>

<details>

<summary><strong>What’s the difference between “Search Customer” and the other filters?</strong></summary>

* **Search Customer** is a quick, broad search.
* The other fields (like **Customer No**, **Email**, **City**) are more specific and usually help you narrow results faster.

</details>

<details>

<summary><strong>What is “Customer No”, and why should I use it?</strong></summary>

**Customer No** is the customer’s unique ID in Tourpaq. If you have it, it’s typically the fastest and most precise way to find the correct customer.

</details>

<details>

<summary><strong>Where do I see more information about a customer?</strong></summary>

Click **Customer No** in the results list to open the customer profile.

See: [Customer Details](customer-details.md)

</details>

<details>

<summary><strong>Why can’t I see “Send Email”, “Send SMS”, or “Export”?</strong></summary>

These actions depend on:

* Your **user permissions/role**
* Your organization’s **system configuration**

If you believe you should have access, contact your administrator.

</details>

<details>

<summary><strong>What does “Newsletter” mean in the list?</strong></summary>

The **Newsletter** column shows whether the customer is subscribed to your newsletter. The exact icon/indicator may vary by configuration.

</details>

<details>

<summary><strong>What are “Contact” and “Ev Phone” used for?</strong></summary>

* **Contact**: filters by a specific contact person (commonly used for B2B customers or when a company has multiple contacts).
* **Ev Phone**: often used as an _evening_ or _alternative_ phone number.

</details>

<details>

<summary><strong>I see the same person multiple times. How do I fix duplicates?</strong></summary>

Duplicates can happen when customers are created from different channels (manual entry, imports, web bookings, etc.). If you have access, you can use the merge tool:

* [Merge customers](../../merge-customers.md)

</details>

<details>

<summary><strong>Does export include all customers or just my filtered list?</strong></summary>

Exports normally follow your **current filters and search results**. If you need a broader list, clear filters or adjust them before exporting.

</details>
