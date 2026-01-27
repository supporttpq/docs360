# Extra Category Overview

Applies to Administrator

Extra categories group similar extras. They control how extras are shown in Tourpaq Office, WebBooking, tickets, and exports.

See also: [Extra Category Reporting](extra-category-reporting.md).

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

<figure><img src="../.gitbook/assets/ExtraCategoryOverview-cc8404247963c69e65035b9fe43a31e8.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
All texts can be customized per active brand.
{% endhint %}

<figure><img src="../.gitbook/assets/ExtraCategoryCustomBrand-594461f051027d3ba8bb1f54ee2bc7e8.png" alt=""><figcaption></figcaption></figure>

### Filtering options

These options control where the category is shown and how it behaves in list filters.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
For multi-select brand fields, **no selection means “all brands”**.
{% endhint %}

| Field                          | Type         | Description                                                                                                                                 |
| ------------------------------ | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **Display in Remember Extras** | Multi-select | Controls which brands show this category in “Remember Extras”.                                                                              |
| **Use for Extras Statistic**   | Multi-select | Controls which brands include this category in extras statistics.                                                                           |
| **Display in Hotel List**      | Multi-select | Controls which brands show extras from this category in all [hotel lists](../export-1/lists.md#report-types-explained) that support extras. |
| **Hide as filter in list**     | Checkbox     | Hides this category as a filter across the system’s lists.                                                                                  |

### Settings

More configuration for how the category behaves.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="220.7777099609375">Field</th><th width="128.33331298828125">Type</th><th width="113.6666259765625">Required</th><th>Description</th></tr></thead><tbody><tr><td><strong>Code</strong></td><td>Text</td><td>Yes</td><td>Category code.</td></tr><tr><td><strong>Sold Out Text</strong></td><td>Text</td><td>No</td><td>Text used in the WebBooking and Customer Center sold-out pop-up.</td></tr><tr><td><strong>Status</strong></td><td>Dropdown</td><td>No</td><td>Set to <code>visible</code> or <code>hidden</code>.</td></tr><tr><td><strong>Behaviour on Web</strong></td><td>Dropdown</td><td>No</td><td>Controls when and where the category is shown in WebBooking. This affects all agencies in the company.</td></tr><tr><td><strong>Category Type</strong></td><td>Dropdown</td><td>No</td><td>Hard-coded values used by different export lists.</td></tr><tr><td><strong>Ticket Category</strong></td><td>Dropdown</td><td>No</td><td>A meta-category used to group one or more extra categories on the ticket.</td></tr><tr><td><strong>Hide on Ticket</strong></td><td>Checkbox</td><td>No</td><td>Hides all extras in this category on the e-ticket. Often combined with <strong>Include in Basic Price</strong>.</td></tr><tr><td><strong>Category order</strong></td><td>Number</td><td>No</td><td>Sort order for categories in WebBooking.</td></tr><tr><td><strong>Category order booking</strong></td><td>Number</td><td>No</td><td>Setting this, influences the order of the categories in the booking window. Two categories of equal order number will be ordered alphabetically between them. 0 to 9 are located leftmost, then HOTEL, 10 to 19 before TRANSPORT, and then the rest. The purpose of making this configurable is to ensure that the  Extras are easy to find when working within a wide booking window.</td></tr><tr><td><strong>Days after booking category locks</strong></td><td>Number</td><td>No</td><td>Locks this category in Customer Center after X days from booking creation.</td></tr><tr><td><strong>Link to column in transport</strong></td><td>Checkbox</td><td>No</td><td>Shows allotment for “linked to transport” extras in the transport selection pop-up.</td></tr><tr><td><strong>Show description &#x26; photo opened in WebBooking</strong></td><td>Checkbox</td><td>No</td><td>Applies to all brands.</td></tr><tr><td><strong>Stop default product selection for all passengers in WB</strong></td><td>Checkbox</td><td>No</td><td>Applies to all brands.</td></tr><tr><td><strong>Accepts multiple product selection</strong></td><td>Checkbox</td><td>No</td><td>Allows selecting multiple products in the category. If unchecked, bookings with multiple products selected may appear as a single selection. Applies to all brands.</td></tr><tr><td><strong>Sold Out Behaviour</strong></td><td>Checkbox</td><td>No</td><td>Enables sold-out behaviour for products in this category.</td></tr><tr><td><strong>One product must be selected</strong></td><td>Checkbox</td><td>No</td><td><p>Forces the user to select an extra in the booking flow. Often used with auto-selected extras. </p><ul><li>When the option is enabled, the system ensures that the user is never presented with an empty selection.</li><li>If no Extra is marked as <strong>Auto-select</strong>, the system will automatically select the <strong>first Extra in the list</strong>.</li><li>While understanding this option is enabled, the user cannot remove the selected Extra. The selection can only be changed by choosing a different Extra from the list.</li></ul><p>These rules apply consistently in both the <strong>Booking flow</strong> and the <strong>Webbooking</strong></p></td></tr><tr><td><strong>Out/Home</strong></td><td>Checkbox</td><td>No</td><td>Used for individual transports to distinguish between outbound and homebound products.</td></tr></tbody></table>

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
