# Facilities

## Main page

#### Overview

The **Hotel Facilities** page is used to manage and categorize all facilities and amenities available at hotels in our system. Each facility can be configured to determine how it is displayed on the web and app, whether it is required, and additional attributes like type and maximum characters.

This page is accessible under the **Hotel Management** module and is essential for ensuring that hotel data is accurately presented to clients and internal teams.

#### Purpose

* **Centralize Facility Management**: Maintain a single source of truth for hotel facilities.
* **Custom Display Options**: Control which facilities are visible on the web, app, or both.
* **Data Consistency**: Ensure all required fields are completed and formatted correctly.
* **Categorization**: Organize facilities into categories such as `HotelFacilities`, `Pension`, `Distance`, or `Rooms` for easier filtering and reporting.

Can be defined from **Hotel/Facilities** and can be set from the hotel **Web** tab

There are 4 tabs:

* Facilities - list of facilities
* Categories - used in web tab for grouping facilities
* Templates - used by hotels to group the facilities based on the type of hotel, can be chosen in the hotel general tab
* Name for Feeds

<figure><img src=".gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

#### Fields Overview

| Field                   | Purpose                                                                            | Instructions                                                                                                                                                                                                                                                                                                                                                                     |
| ----------------------- | ---------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**                | The name of the facility.                                                          | Enter a clear, descriptive name for the facility. Example: “WiFi”, “Mini Market”, or “Outdoor Yoga”. Names should be concise yet descriptive.                                                                                                                                                                                                                                    |
| **Category**            | Defines the type or classification of the facility.                                | Select an appropriate category such as `HotelFacilities`, `Pension`, `Rooms`, or `Distance`. This helps organize and filter facilities.                                                                                                                                                                                                                                          |
| **Required**            | Specifies whether this facility must be completed when adding or updating a hotel. | ✔ = required, ✖ = optional. Check the box if the facility is mandatory.                                                                                                                                                                                                                                                                                                          |
| **Filter on Web**       | Determines if the facility can be used as a filter option on the website.          | ✔ = users can filter hotels based on this facility. ✖ = cannot be used as a filter.                                                                                                                                                                                                                                                                                              |
| **Show on Web**         | Controls whether the facility is displayed on the website.                         | ✔ = facility visible to web users, ✖ = hidden. Useful for internal or optional facilities.                                                                                                                                                                                                                                                                                       |
| **Show in App**         | Controls whether the facility is displayed in the mobile app.                      | ✔ = visible in app, ✖ = hidden. Useful for facilities not relevant to app users.                                                                                                                                                                                                                                                                                                 |
| **Max Chars**           | Maximum number of characters allowed for this field (if applicable).               | Enter a numeric limit for text fields, e.g., 150 characters for long descriptions. Leave blank if not applicable.                                                                                                                                                                                                                                                                |
| **Type**                | Determines the type of data that can be entered for the facility.                  | <p>Options include:<br>• <code>Text</code> – free text<br>• <code>Multiline text</code> – multiple lines<br>• <code>Message</code> – short notification<br>• <code>Time</code> – specific time<br>• <code>Activity</code> – activity description<br>• <code>Date</code> – calendar date<br>• <code>Yes/No</code> – binary selection<br>• <code>Integer</code> – numeric only</p> |
| **Flag on Web**         | Indicates if this facility should have a special flag or highlight on the website. | ✔ = facility flagged on web (special attention). ✖ = no flag. Usually used for promotional or highlighted services.                                                                                                                                                                                                                                                              |
| **Delete (trash icon)** | Allows removal of the facility from the system.                                    | Click the trash icon to delete the facility. This action is permanent and should be used carefully.                                                                                                                                                                                                                                                                              |

#### Example Workflow

1. **Creating a New Facility**
   * Click **Create** in the top-right corner.
   * Enter the **Name** and select the **Category**.
   * Configure whether it is **Required**, visible on **Web/App**, and if it should **Filter** or **Flag** on web.
   * Choose the **Type** based on the nature of the data.
   * Set **Max Chars** if needed.
   * Save the facility.
2. **Editing an Existing Facility**
   * Click the facility name.
   * Update any relevant fields.
   * Save changes to apply.
3. **Deleting a Facility**
   * Click the **trash icon** next to the facility.
   * Confirm deletion.

## Facilities <a href="#facilities" id="facilities"></a>

#### Overview

The **Facilities** tab allows administrators to define and manage hotel facilities. These facilities can be displayed on the website, used for filtering, or highlighted in the booking process. Each facility can be customized with specific attributes, data types, and visibility settings.

#### Purpose

* Define hotel facilities with detailed attributes.
* Control how facilities are displayed and used on the website and booking interface.
* Enable advanced filtering and visibility options for customers.
* Support API differentiation for key facilities like **All Inclusive**, **Swimming Pool**, and **Child Pool**.

A new facility can be defined in the **Facilities** tab by pressing the "Create" button in the upper right corner of the screen.

<figure><img src=".gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

#### Field Explanations

* **Name** – The name of the facility.
* **Data Type** – Select the type of data the facility holds (e.g., Text, Integer, Decimal, Multiline Text).
* **Max Chars** – Maximum number of characters (applicable for Decimal, Integer, Multiline Text, and Text types).
* **Category** – Category to which the facility belongs.
* **Default Value** – Predefined value based on the data type.
* **Document Title** - Name of the document, add to the facility (Do not upload files larger than 1Mb).
* **Document** - Add a document to the facility.

{% hint style="danger" %}
There can be a maximum of 5 Facility Documents on a Ticket.\
If a ticket has more than 5 Facilities with Documents, only 5 will be attached to the Ticket.
{% endhint %}

* **Is Mandatory** – If checked, the facility must be filled in when using a **Facilities Template** for a hotel.
* **Show on Hotels Popup** – Displayed on the booking page popup when clicking the hotel code.
* **Show on Web as Filter** – Enables advanced filtering of hotels by this facility on the presentation website.
* **Show on Web** – Displays the facility in the hotel listing on the website.
* **Show on app -** Display the facility in the Guest App, on the hotel details.
* **Flag on Web** – Highlights the facility visually on the website.
* **All Inclusive** – Marks the facility in the API for web differentiation.
* **Swimming Pool** – Marks the facility in the API for web differentiation.
* **Child Pool** – Marks the facility in the API for web differentiation.

#### Instructions for Use

1. Navigate to the **Facilities** tab.
2. Click the **New Facility** button in the upper-right corner.
3. Fill in the facility details:
   * Enter the **Name** and select the **Data Type**.
   * Set **Max Chars** if applicable.
   * Choose the **Category**.
   * Define the **Default Value**.
   * Check **Is Mandatory** if required.
   * Configure **Show on Hotels Popup**, **Show on Web as Filter**, **Show on Web**, and **Flag on Web** as needed.
   * Set **All Inclusive**, **Swimming Pool**, or **Child Pool** flags if required for API differentiation.
4. Save the facility.
5. Repeat to add additional facilities as needed.

## Categories

<figure><img src=".gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

#### Overview

**Categories** are used to group and organize facilities. Each facility must belong to a category. Categories can also be displayed in customer-facing contexts, such as tickets and offers, depending on their configuration.

#### Purpose

* Provide structure and grouping for facilities.
* Control visibility of category information on tickets and offers.
* Simplify facility management and improve presentation on the web and booking flow.

#### Creating a New Category

<figure><img src=".gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

1. Navigate to the **Category** tab.
2. Click the **Create** button in the upper-right corner.
3. Fill in the required fields:
   * **Name** – The name of the category.
   * **Show on Ticket** – If checked, the category will be displayed on tickets.
   * **Show on Select Offer** – If checked, the category will be displayed on offers.
4. Save the category.

#### Field Explanations

* **Name** – Defines the category name (e.g., “Wellness,” “Dining,” “Family Amenities”).
* **Show on Ticket** – Displays this category on the customer’s travel ticket.
* **Show on Select Offer** – Displays this category in the booking offer.

## Templates <a href="#templates" id="templates"></a>

#### Overview

**Templates** allow you to define predefined sets of facilities that can be applied to hotels. Using templates ensures consistency and saves time when assigning multiple facilities to different hotels.

#### Purpose

* Standardize the configuration of hotel facilities.
* Speed up the setup process by reusing predefined facility groups.
* Reduce errors and manual input when managing multiple hotels.

#### Creating a New Template

1. Navigate to the **Templates** tab.
2. Click the **New Template** button in the upper-right corner.
3. Fill in the required fields:
   * **Name** – The name of the template (e.g., “Family Hotel,” “Luxury Resort,” “All-Inclusive”).
   * **Facilities** – Select the facilities that should be included in this template.
4. Save the template.

<figure><img src=".gitbook/assets/image (21) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Field Explanations

* **Name** – Defines the template’s name.
* **Facilities** – A multi-select field to choose from existing facilities that will be bundled into the template.

### Facilities on web <a href="#facilities-on-web" id="facilities-on-web"></a>

On the website, facilities are displayed for the hotel like this:

![!](https://docs.tourpaq.com/assets/images/facilities_on_web-c0f8bedeeb3c056f7c09926e50b999b5.jpg)
