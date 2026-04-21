# Extra Category Overview

Applies to Administrator

Extra categories group similar extras. They control how extras are shown in Tourpaq Office, WebBooking, tickets, and exports.

See also: [Extra Category Reporting](../extra-category-reporting.md).

### Default text

These fields control the category label and content shown to users.

| Field                                  | Required | Description                                                        |
| -------------------------------------- | -------- | ------------------------------------------------------------------ |
| **Name**                               | Yes      | Category name shown in Tourpaq Office, WebBooking, and on tickets. |
| **List name**                          | Yes      | Category name used in export lists.                                |
| **Replace product name when Sold Out** | No       | Text shown when a product is sold out.                             |
| **Description**                        | No       | Category description shown in WebBooking.                          |
| **Icon**                               | No       | Upload an icon for the category.                                   |
| **Photo**                              | No       | Upload photos shown in WebBooking.                                 |

<figure><img src="../../.gitbook/assets/image (684).png" alt=""><figcaption></figcaption></figure>

### Filtering options

These options control where the category is shown and how it behaves in list filters.

<figure><img src="../../.gitbook/assets/image (685).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
For multi-select brand fields, **no selection means “all brands”**.
{% endhint %}

| Field                          | Type         | Description                                                                                                                                    |
| ------------------------------ | ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| **Display in Remember Extras** | Multi-select | Controls which brands show this category in “Remember Extras”.                                                                                 |
| **Use for Extras Statistic**   | Multi-select | Controls which brands include this category in extras statistics.                                                                              |
| **Display in Hotel List**      | Multi-select | Controls which brands show extras from this category in all [hotel lists](../../export-1/lists.md#report-types-explained) that support extras. |
| **Hide as filter in list**     | Checkbox     | Hides this category as a filter across the system’s lists.                                                                                     |

### Settings

More configuration for how the category behaves.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="220.7777099609375">Field</th><th width="128.33331298828125">Type</th><th width="113.6666259765625">Required</th><th>Description</th></tr></thead><tbody><tr><td><strong>Code</strong></td><td>Text</td><td>Yes</td><td>Category code.</td></tr><tr><td><strong>Sold Out Text</strong></td><td>Text</td><td>No</td><td>Text used in the WebBooking and Customer Center sold-out pop-up.</td></tr><tr><td><strong>Status</strong></td><td>Dropdown</td><td>No</td><td>Set to <code>visible</code> or <code>hidden</code>.</td></tr><tr><td><strong>Behaviour on Web</strong></td><td>Dropdown</td><td>No</td><td>Controls when and where the category is shown in WebBooking. This affects all agencies in the company.</td></tr><tr><td><strong>Category Type</strong></td><td>Dropdown</td><td>No</td><td>Hard-coded values used by different export lists.</td></tr><tr><td><strong>Ticket Category</strong></td><td>Dropdown</td><td>No</td><td>A meta-category used to group one or more extra categories on the ticket.</td></tr><tr><td><strong>Round rule</strong></td><td>Dropdown</td><td>No</td><td>If a round rule is specified, then it is applied to the price before it is used in a booking. If the price is a per-day price, the round rule is applied after the full price for the booking is calculated.</td></tr><tr><td><strong>Hide for Customer</strong></td><td>Checkbox</td><td>No</td><td>If checked, this will hide the extras on the ticket, in webbooking, and in the customer center.<br>This is often combined with "Include in Basic Price", which is set on the Extras.</td></tr><tr><td><strong>Category order</strong></td><td>Number</td><td>No</td><td>Setting this will influence the order of categories in webbooking. Two categories with equal order numbers will be ordered alphabetically between them. The smaller the number, the higher the category will appear in the list.</td></tr><tr><td><strong>Category order booking</strong></td><td>Number</td><td>No</td><td>Setting this, influences the order of the categories in the booking window. Two categories of equal order number will be ordered alphabetically between them. 0 to 9 are located leftmost, then Transport, 10 to 19 before Hotel, and 20 or above after Hotel and Room. The purpose of making this configurable is to ensure that the  Extras are easy to find when working within a wide booking window.</td></tr><tr><td><strong>Category order e-ticket</strong></td><td>Number</td><td>No</td><td><p>Setting this influences the order of the categories on the e-ticket. Two categories of equal order number will be ordered alphabetically between them.<br>This takes effect if "Order extras on e-ticket" is set in System Setup.<br><mark style="color:red;">This is only supported on ticket version 3.</mark> </p><p><br>If "Order extras on e-ticket" is checked, the extras shall be sorted according to the Category Order value on the e-ticket under price specification.</p><p><mark style="color:$success;">Note: The Extra category order has no impact on the order of Travel Insurance and Cancellation Insurance.</mark></p></td></tr><tr><td><strong>Days after booking category locks</strong></td><td>Number</td><td>No</td><td>Setting this will disable adding/removing/changing products in this category if X days pass after initially making the booking.</td></tr><tr><td><strong>Link to column in transport</strong></td><td>Checkbox</td><td>No</td><td>Shows allotment for “linked to transport” extras in the transport selection pop-up.</td></tr><tr><td><strong>Show description &#x26; photo opened in WebBooking</strong></td><td>Checkbox</td><td>No</td><td>This setting affects all agencies of the company.</td></tr><tr><td><strong>All stay days must be available</strong></td><td>Checkbox</td><td>No</td><td><p>If selected, the extra is only eligible if it is available for the full booking period. </p><p><mark style="color:$success;">Available only for:</mark></p><ul><li><mark style="color:$success;">Pension</mark></li><li><mark style="color:$success;">Gala dinner</mark></li></ul></td></tr><tr><td><strong>Stop default product selection for all passengers in WB</strong></td><td>Checkbox</td><td>No</td><td>Applies to all brands.</td></tr><tr><td><strong>Accepts multiple product selection</strong></td><td>Checkbox</td><td>No</td><td>Allows selecting multiple products in the category. If unchecked, bookings with multiple products selected may appear as a single selection. Applies to all brands.</td></tr><tr><td><strong>Sold Out Behaviour</strong></td><td>Checkbox</td><td>No</td><td>Enables sold-out behaviour for products in this category.</td></tr><tr><td><strong>One product must be selected</strong></td><td>Checkbox</td><td>No</td><td><p>Forces the user to select an extra in the booking flow. Often used with auto-selected extras. </p><ul><li>When the option is enabled, the system ensures that the user is never presented with an empty selection.</li><li>If no Extra is marked as <strong>Auto-select</strong>, the system will automatically select the <strong>first Extra in the list</strong>.</li><li>While understanding this option is enabled, the user cannot remove the selected Extra. The selection can only be changed by choosing a different Extra from the list.</li></ul><p>These rules apply consistently in both the <strong>Booking flow</strong> and the <strong>Webbooking</strong></p></td></tr><tr><td><strong>Out/Home</strong></td><td>Checkbox</td><td>No</td><td>Used for individual transports to distinguish between outbound and homebound products.</td></tr></tbody></table>

### Rounding on Extras

This functionality introduces rounding rules for **Extras** and **Discount/Supplement categories**, ensuring that sales prices generated during contract import or booking calculations are consistent and commercially correct.

It extends the existing rounding logic already available in **System Settings (Profit margin round rule)** and makes it applicable at the category level.

The purpose of this feature is to:

* Ensure consistent price rounding across the system
* Avoid incorrect or non-standard pricing (e.g., 123.47 instead of 125)
* Apply rounding automatically during booking calculations and in the booking engine

#### System Behavior

#### General Rule

If a **Round Rule** is defined on the category, it is always applied before the price is used in a booking and for all extras in the category

#### Per-Day Pricing

If the price is defined as **per-day**:

*   The system first calculates the total booking price:

    ```
    total = price_per_day × number_of_days
    ```
* Then applies the rounding rule on the final value

#### Booking Engine & Elastic

* Rounding is always applied when an extra is added to a booking
* Ensures consistency between:
  * Back-office calculations
  * Front-end (booking engine) pricing
  * Elastic search results

#### Supported Round Rules

The available options in the dropdown are identical to those defined in:

* **Setup > System Setup > Settings > Profit margin round rule**

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### How to Configure a New Extras Category

#### Step 1 – Create Basic Information

* Enter Name
* Enter List Name
* Add Description (optional)
* Upload Icon and Photo

***

#### Step 2 – Define Filtering Behavior

* Enable statistics if required
* Configure visibility in hotel lists
* Decide filter availability

***

#### Step 3 – Configure Settings

* Add unique Code
* Set Status to Visible
* Define Web behavior
* Set booking rules (mandatory, multiple selection)
* Configure ordering
* Define sold-out logic

***

#### Step 4 – Save & Test

* Save configuration
* Test in Web Booking & Office
* Verify ordering and behavior
* Validate sold-out handling

***

#### Example: Activity Extras

| Field                        | Value           |
| ---------------------------- | --------------- |
| Name                         | Activity        |
| List Name                    | Activity Extras |
| Code                         | AKT             |
| Status                       | Visible         |
| Accepts Multiple Selection   | Enabled         |
| One Product Must Be Selected | Disabled        |
| Category Order               | 3               |
| Sold Out Text                | Fully booked    |

### FAQ

#### What’s the difference between **Name** and **List name**?

**Name** is customer-facing (Office, WebBooking, tickets).\
**List name** is used for export lists.

#### Why isn’t my category visible in WebBooking?

Check **Status** and **Behaviour on Web**.\
Also check the brand selections in the filtering options.

#### How do I change the text per brand?

Use the brand context (brand selector).\
Then set the brand-specific text values.

#### What’s the difference between **Sold Out Text** and **Replace product name when Sold Out**?

**Replace product name when Sold Out** changes the name shown for the product.\
**Sold Out Text** is used in the sold-out pop-up (WebBooking/Customer Center).

#### What does **Ticket Category** do?

It groups extras from multiple extra categories under one label on tickets.

#### What happens when **Days after booking category locks** is set?

After that many days, customers can’t change extras in this category.\
This applies in Customer Center.
