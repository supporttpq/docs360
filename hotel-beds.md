# Hotel beds

Please also see the Hotel bed bank faq / FAQ page

Hotel Bed Bank allows the user to import hotels from a bed bank provider. A bed bank is a third-party service that provides hotel information and a contract representation.

Hotel information:

* name
* description
* number of stars
* phone number
* address
* resort
* pictures
* available facilities

Contract representation:

* room types and their configuration (name, description, number of beds, min adults)
* room prices
* room availability

At the moment of this writing only **Hotel Beds** is implemented as a bed bank provider.

### SETUP <a href="#setup" id="setup"></a>

In order to start using this feature a company must setup hotel beds credentials in System setup (tab Hotel Beds):

<figure><img src=".gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

If the tab is missing, the feature must be activated by an administrator.

//Please allow up to 10 minutes for the service to run and download initial contract information.//

After setup you can go to Hotel Bed Bank menu item under Hotel menu group. Here you can search for hotels or search for offers in order to make an ideea of price range and availability of hotels in a specific area.

### SEARCH HOTELS <a href="#search-hotels" id="search-hotels"></a>

The user must fill the mandatory fields (country and destination) and press find. Rest of the fields are optional and can be used to filter the results.

The system will search for hotels in that area and will present the user a list of options having the following properties:

* hotel name
* hotel destination, zone and country.
* available room types for the hotel.
* contract codes that are available for that hotel.

The hotel can be imported only if it has at least one contract code assigned to it.

<figure><img src=".gitbook/assets/image (102).png" alt=""><figcaption></figcaption></figure>

### IMPORT HOTEL <a href="#import-hotel" id="import-hotel"></a>

On the import page the user must:

* select a contract
* select / check room mappings
* select / check facilities
* select a resort (Edit hotel)
* select photos that should be imported.

After everything has been selected the hotel can be saved in tourpaq.

//Images and allotments are not imported in realtime; all information will be available in about 5 minutes after the hotel has been saved.//

### SELECTING A CONTRACT <a href="#selecting-a-contract" id="selecting-a-contract"></a>

Clicking on **View contract details** should bring up a popup with all relevant contract information.

<figure><img src=".gitbook/assets/image (103).png" alt=""><figcaption></figcaption></figure>

* If the button does not appear than a message stating that there are no contracts defined should appear in place. In this case the hotel cannot be imported.
* There might be the case that on hotel search page the hotel seems to have one or more contracts but on the details page there is no contract available. This will only happen if the contracts are invalid (have no rooms defined) or the rooms defined in the contracts do not match the rooms of that particular hotel. This is yet another case that will prevent the hotel from beeing imported.

It is important to review a contract before importing it.

<figure><img src=".gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

### SELECT / CHECK ROOM MAPPINGS <a href="#select--check-room-mappings" id="select--check-room-mappings"></a>

The system has an automapping functionality in order to make future imports easier. It should remember any previous mappings and in some places will try to map rooms by their configurations.

The user should always assume that the system did not map the data correctly and check if the rooms are mapped correctly.

<figure><img src=".gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

### IMPORT / UPDATE HOTEL PHOTOS <a href="#import--update-hotel-photos" id="import--update-hotel-photos"></a>

You can also import hotel photos from the Bed Bank provider by simply selecting the desired photos and they will be imported along with the rest of the hotel information.

If you want to update the photos, please first delete the hotel photos in Tourpaq and then go to the Hotel import from bed bank page to import new photos.
