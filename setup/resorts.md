# Resorts

### Overview

The **Resorts** interface provides a structured way to manage resorts associated with different arrival gateways. This system allows users to search, filter, and manage resort data efficiently.

<figure><img src="../.gitbook/assets/image (370).png" alt=""><figcaption></figcaption></figure>

### Features

* **Search Functionality:** A search bar allows users to quickly find specific resorts.
* **Filtering Options:** Users can filter by selecting a specific resort from the dropdown.
* **Show Hidden:** A toggle option enables the display of hidden resorts.
* **Create New Entry:** A "Create" button allows users to add new resorts.
* **Delete Functionality:** Each entry includes a trash bin icon for easy removal.

### Column Explanation

* **Code**
  * A short unique identifier for the resort (e.g., _BCN_, _TFS_, _Antalya_).
  * Used internally in the system to reference the resort quickly.
  * Often based on airport or city codes but can also be custom.
* **Name**
  * The full name of the resort (e.g., _Barcelona_, _Costa Adeje_, _Malaga_).
  * This is the descriptive label shown to users and customers.
* **Country**
  * The country in which the resort is located (e.g., _Spanien_, _Romania_, _Thailand_).
  * Ensures that resorts are categorized correctly geographically.
* **Destination**
  * Groups the resort into a broader travel destination category (e.g., _Valencia_, _Chania Dest_).
  * Useful for package creation and filtering offers by larger travel areas.
* **Arrival**
  * The arrival airport or point of entry associated with the resort (e.g., _Barcelona_, _Varna_, _Bangkok_).
  * Defines how travelers reach the resort and links it with transport routes.
* **Delete (Trash Bin icon)**
  * Allows the removal of a resort from the system.
  * Deletion should be done carefully, as removing a resort can affect linked price lists, hotels, and packages.

### User Actions

#### Searching for a Resort

1. Use the search bar at the top to enter a resort name or keyword.
2. The table dynamically updates to show matching results.

#### Filtering Resorts

1. Select a specific resort from the **Resort/ Destination/ Arrival** dropdown.
2. The list updates to display only relevant entries.
3. The **Show Hidden** toggle can be used to reveal hidden resorts.

#### Creating a New Entry

1. Click on the **Create** button.
2. Enter the required details (Resort ID, name, code, country, arrival gateway, etc.).
3. Save the entry to add it to the list.

#### Deleting an Entry

1. Locate the resort to remove.
2. Click the trash bin icon under the "Actions" column.
3. Confirm deletion if prompted.

### Edit a resort

<figure><img src="../.gitbook/assets/image (375).png" alt=""><figcaption></figcaption></figure>

### Field Explanation

#### Left Section

* **Resort**\*
  * Unique code for the resort (e.g., _CALETA-FUE_).
  * Acts as the system identifier and must be unique.
* **Name**\*
  * The full name of the resort (e.g., _Caleta De Fuste_).
  * This is the label displayed to users.
* **Url-Alias**
  * Defines the URL alias for the resort.
  * Used for SEO-friendly links.
* **Url Prefix Alias**
  * Optional prefix for the resort URL.
  * Helps structure URLs under a broader category (e.g., destination prefix).
* **Arrival**\*
  * The airport or point of arrival associated with the resort (e.g., _Fuerteventura Airport_).
* **Alternative Country**
  * Optional field if the resort belongs to a different country grouping than the default.
* **Destination**
  * Destination grouping that the resort belongs to (e.g., _Fuerte DEST_).
  * Used for travel package creation and filtering.
* **Sales Internet**
  * Checkbox to enable the resort for online sales.
* **Show alternating text on web**
  * Displays alternate marketing text on the website if enabled.
* **Teaser Text**
  * Short promotional text shown in website teasers.
* **Metadesc**
  * Meta description for search engines (SEO).
* **Keywords**
  * SEO keywords related to the resort.
* **Title**
  * Title used for web/SEO purposes.
* **Latitude / Longitude**
  * Geographical coordinates of the resort.
  * Useful for maps and geo-location features.
* **Hide as filter on lists**
  * If checked, the resort will not appear as a filter option in search/listing views.
* **Show in Vab as Country**
  * When using statistics in View All Bookings, resort will be considered country when grouping by country.

***

#### Right Section

* **Status**
  * Visibility status of the resort (e.g., _visible_).
  * Controls whether the resort is visible or hidden.
* **Source Agency**
  * Defines which agency/brand the resort belongs to (e.g., _All brands_).
* **Administration**
  * Cost assigned for administration related to this resort.
* **Destination cost**
  * Cost applied for the specific destination.
* **Handeling**
  * Handling fee linked to the resort.
* **Transfer**
  * Cost of transfers (e.g., airport–hotel transfers).
* **Miscellaneous**
  * Additional costs that don’t fall under other categories.
* **Description**
  * Rich-text editor field where a full description of the resort can be added.
  * Supports formatting, links, and images.

### Resort - Photos tab <a href="#resort---photos-tab" id="resort---photos-tab"></a>

Insert multiple photos in one step and sort them by drag and drop.

Fields:

* Title - Picture name
* Photo - Click to add photo(s)
* Description - Short description&#x20;
* Main photo - If it is checked, the selected picture will be made the main photo of the resort

<figure><img src="../.gitbook/assets/image (376).png" alt=""><figcaption></figcaption></figure>

You can choose multiple images to be saved:

<figure><img src="../.gitbook/assets/uploadingResortPhotos-7d42121311b31492fe6b45a4c30330e3.png" alt=""><figcaption></figcaption></figure>

In case of uploading more than one image, the title and the description field will be saved for each photo with the same values. After save, these fields can be edited from inside the list.

<figure><img src="../.gitbook/assets/editableFieldResortPhotos-e1c3c42024e4c0fa04085d5f64f25fdf.png" alt=""><figcaption></figcaption></figure>

To order the list of photos, press and keep click on the specific row and move cursor up/down to the position desired. Release and then press save to store the ordered list.
