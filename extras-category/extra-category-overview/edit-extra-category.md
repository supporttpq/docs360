# Edit Extra Category

### Overview

The **Extras Category** page is used to create and manage groups of optional products or services (extras) that can be sold alongside a main product (e.g., accommodation, transport, package).

An _Extras Category_ helps organize related extras (e.g., Activities, Insurance, Equipment Rental) and control how they are displayed, filtered, and booked in both internal systems and web booking.

This page contains three main sections:

1. **General Information**&#x20;
2. **Filtering Options**
3. **Settings**

***

### Purpose

The purpose of this page is to:

* Structure extras into logical categories.
* Control visibility and behavior in Web Booking and internal booking flows.
* Define ordering and booking rules.
* Manage sold-out logic and display behavior.
* Improve user experience for both agents and customers.

Proper configuration ensures:

* Correct display on the website.
* Accurate booking logic.
* Clear communication when products are sold out.
* Organized reporting and statistics.

***

### Section-by-Section Field Explanation

{% hint style="info" %}
Texts from general settings can be customized per active brand.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (688).png" alt=""><figcaption></figcaption></figure>

#### A. General Information

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Name** - Internal name of the extras category.

* **Purpose:** Identifies the category in the system.
* **Example:** `Activity`

**List Name** - Display name shown in listings.

* **Purpose:** Defines how the category appears in overviews and selection lists.
* **Example:** `Activity Extra`

**Replace product name when Sold Out -** Text that replaces the product name when the extra is sold out.

* **Purpose:** Improves customer communication instead of simply hiding the product.

&#x20;**Description** - Rich text field allowing formatted content.

* **Purpose:** Provides a detailed explanation of the category.
* **Where displayed:** Web booking or internal interfaces (depending on setup).
* **Tip:** Use this to explain conditions, inclusions, or important notes.

**Icon** - Upload area for a category icon.

* **Purpose:** Visual representation of the extras category.
* **How to use:** Click to browse or drag & drop a file.

**Photo** - Main image for the category.

* **Purpose:** Enhances visual presentation in Web Booking.
* **Action:** Click **Upload photo**.

#### B. Filtering Options

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;**Display in Remember Extras** - Allows this category to appear in the "Remember Extras" functionality.

**Use for Extras Statistic** - Includes this category in statistical reporting.

**Display in Hotel List** - Makes the category visible in hotel list

**Hide as filter on lists** - Prevents the category from appearing as a filter option in listings.

#### C. Settings

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

This section controls operational logic.

Code - Unique short identifier.

* **Purpose:** Used internally and for system integrations.
* **Example:** `AKT`

Sold Out Text - Text for pop up in webbooking and customer center

* **Example:** `No availability for selected dates.`

Status - Controls if the category is active in the system.

* **Options:** Visible / Hidden

Behavior on Web - Determines when the category appears during booking flow.

* **Example option:** Step 1: Always Show

Category Type - Assign to a category type

* **Example:** Party Package

Ticket Category - Connects extras to ticketing logic

* **Default:** None

Hide for Customer - If checked, this will hide the extras on the ticket, in webbooking, and in customer center. This is often combined with " Include in Basic Price", which is set on the Extras.

* **Checkbox**

Category Order - Setting this will influence order of categories in webbooking. Two categories of equal order number will be ordered alphabetical between them. The smaller the number, the higher the category will appear in the list.

Category Order Booking - Setting this will influence order of categories in the booking window. Two categories of equal order number will be ordered alphabetical between them. 0 to 9 are located leftmost, then Transport, 10 to 19 before Hotel, and then the rest.

Days after booking category locks -  Number of days after booking when changes are no longer allowed.

Link to column in transport - Shows allotment for “linked to transport” extras in the transport selection pop-up.

* **Checkbox**

Show description & photo opened in WebBooking - Automatically expands description and image in booking flow.

* **Checkbox**

Stop default product selection for all passengers in WB - Prevents automatic selection of extras for all passengers.

* **Checkbox**

&#x20;Accepts multiple product selection - Allows customers to select more than one extra from this category.

* **Checkbox**

Sold Out Behaviour - Enables sold-out behaviour for products in this category.

One product must be selected - When selected, the user is forced to select an extra in the booking flow.

* **Checkbox**

Out/Home - Use for individual transports, to distinguish between out and home products.

* **Checkbox**
