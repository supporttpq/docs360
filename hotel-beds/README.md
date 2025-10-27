# Hotel Beds

Please also see the [Hotel bed bank FAQ/FAQ](hotel-bed-banks-faq.md) page.

### **Overview**

The **Hotel Bed Bank** feature allows users to **import hotels from a bed bank provider**.\
A bed bank is a **third-party service** that supplies hotel information and contract details, allowing agencies to integrate hotel offerings directly into their booking system.

#### **Hotel Information Imported**

When importing hotels from a bed bank, the following data is available:

| **Field**                | **Description**                                                 |
| ------------------------ | --------------------------------------------------------------- |
| **Name**                 | Official hotel name provided by the bed bank.                   |
| **Description**          | Hotel description, including amenities and general information. |
| **Number of Stars**      | Hotel rating (e.g., 3-star, 4-star, 5-star).                    |
| **Phone Number**         | Contact number for the hotel.                                   |
| **Address**              | Full physical address.                                          |
| **Resort**               | Resort or destination area where the hotel is located.          |
| **Pictures**             | Images of the hotel, rooms, and facilities.                     |
| **Available Facilities** | Amenities available to guests (e.g., pool, spa, Wi-Fi, gym).    |

#### **Contract Representation**

The bed bank also provides information necessary for booking and pricing:

| **Field**                        | **Description**                                                                                     |
| -------------------------------- | --------------------------------------------------------------------------------------------------- |
| **Room Types and Configuration** | Details of each room type including name, description, number of beds, and minimum adults required. |
| **Room Prices**                  | Pricing information for each room type.                                                             |
| **Room Availability**            | Number of rooms available for each type on specific dates.                                          |

#### **Current Implementation**

* At the time of writing, **only Hotel Beds** is integrated as a bed bank provider.
* Future updates may include additional bed bank providers.

#### **Customer Outcome**

* **Streamlined Hotel Import:** Users can quickly add hotels from a trusted bed bank provider without manual data entry.
* **Comprehensive Hotel Data:** Complete hotel and contract information allows accurate booking and pricing.
* **Consistency:** Standardized data from the bed bank ensures reliable hotel information for agents and customers.

### Setup <a href="#setup" id="setup"></a>

In order to start using this feature, a company must set up Hotelbeds credentials in System Setup (tab Hotelbeds):

<figure><img src="../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

If the tab is missing, the feature must be activated by an administrator.

Please allow up to 10 minutes for the service to run and download initial contract information.&#x20;

After setup, you can go to the Hotel Bed Bank menu item under the Hotel menu group. Here you can search for hotels or search for offers in order to get an idea of the price range and availability of hotels in a specific area.

### Search hotels <a href="#search-hotels" id="search-hotels"></a>

The user must fill the mandatory fields (country and destination) and press Find. The rest of the fields are optional and can be used to filter the results.

The system will search for hotels in that area and will present the user a list of options having the following properties:

* hotel name
* hotel destination, zone, and country.
* available room types for the hotel.
* contract codes that are available for that hotel.

The hotel can be imported only if it has at least one contract code assigned to it.

<figure><img src="../.gitbook/assets/image (102).png" alt=""><figcaption></figcaption></figure>

### Import hotel <a href="#import-hotel" id="import-hotel"></a>

On the import page, the user must

* select a contract
* Select/check room mappings
* Select/check facilities
* select a resort (Edit hotel)
* Select photos that should be imported.

After everything has been selected, the hotel can be saved in Tourpaq.

Images and allotments are not imported in time; all information will be available in about 5 minutes after the hotel has been saved.

### Selecting a contract <a href="#selecting-a-contract" id="selecting-a-contract"></a>

Clicking on **View contract details** should bring up a popup with all relevant contract information.

<figure><img src="../.gitbook/assets/image (103).png" alt=""><figcaption></figcaption></figure>

* If the button does not appear, then a message stating that there are no contracts defined should appear in its place. In this case the hotel cannot be imported.
* There might be the case that on the hotel search page the hotel seems to have one or more contracts, but on the details page there is no contract available. This will only happen if the contracts are invalid (have no rooms defined) or the rooms defined in the contracts do not match the rooms of that particular hotel. This is yet another case that will prevent the hotel from being imported.

It is important to review a contract before importing it.

<figure><img src="../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

### Select / Check room mappings <a href="#select--check-room-mappings" id="select--check-room-mappings"></a>

The system has an automapping functionality in order to make future imports easier. It should remember any previous mappings and in some places will try to map rooms by their configurations.

The user should always assume that the system did not map the data correctly and check if the rooms are mapped correctly.

<figure><img src="../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

### Import / Update hotel photos <a href="#import--update-hotel-photos" id="import--update-hotel-photos"></a>

You can also import hotel photos from the Bed Bank provider by simply selecting the desired photos, and they will be imported along with the rest of the hotel information.

If you want to update the photos, please first delete the hotel photos in Tourpaq and then go to the Hotel Import from Bed Bank page to import new photos.
