# Hotel Beds

See also: [Hotel Bed Banks - FAQ](hotel-bed-banks-faq.md).

### Overview

The **Hotel Bed Bank** feature lets you import hotels from a bed bank provider.

A bed bank is a third-party service. It provides hotel content and contract data.

### What gets imported

#### Hotel information

| Field                | Description                                            |
| -------------------- | ------------------------------------------------------ |
| Name                 | Official hotel name from the bed bank.                 |
| Description          | Hotel description, amenities, and general information. |
| Number of stars      | Hotel rating (for example, 3-star, 4-star, 5-star).    |
| Phone number         | Hotel contact number.                                  |
| Address              | Full physical address.                                 |
| Resort               | Resort or destination area.                            |
| Pictures             | Images of the hotel, rooms, and facilities.            |
| Available facilities | Amenities (for example, pool, spa, Wi‑Fi, gym).        |

#### Contract data

| Field                        | Description                                                                |
| ---------------------------- | -------------------------------------------------------------------------- |
| Room types and configuration | Room type name, description, bed count, and any minimum adult requirement. |
| Room prices                  | Pricing per room type.                                                     |
| Room availability            | Available rooms per date.                                                  |

### Current implementation

* At the time of writing, only **Hotelbeds** is integrated as a bed bank provider.
* Future updates may include additional bed bank providers.

### Customer outcome

* **Streamlined Hotel Import:** Users can quickly add hotels from a trusted bed bank provider without manual data entry.
* **Comprehensive Hotel Data:** Complete hotel and contract data supports accurate booking and pricing.
* **Consistency:** Standardized data from the bed bank ensures reliable hotel information for agents and customers.

### Limitations and timing

* The first sync can take up to 10 minutes after you save credentials.
* Photos and allotments are not available immediately. They usually appear within \~5 minutes after saving a hotel.

### Setup <a href="#setup" id="setup"></a>

To use this feature, set up your **Hotelbeds** credentials in **System Setup → Hotelbeds**:

<figure><img src="../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

If the tab is missing, an administrator must enable the feature.

Allow up to 10 minutes for the initial sync to complete.

After setup, go to **Hotel → Hotel Bed Bank**.

Search for hotels to import them.

Search for offers to check price ranges and availability in an area.

### Search hotels <a href="#search-hotels" id="search-hotels"></a>

Fill the required fields (country and destination). Then select **Find**.

All other fields are optional. Use them to narrow the results.

The system returns hotels in the selected area. The results include:

* Hotel name
* Destination, zone, and country
* Available room types
* Available contract codes

The hotel can be imported only if it has at least one contract code assigned to it.

<figure><img src="../.gitbook/assets/image (102).png" alt=""><figcaption></figcaption></figure>

### Import hotel <a href="#import-hotel" id="import-hotel"></a>

On the import page:

* Select a contract.
* Review room mappings.
* Review facilities.
* Select a resort (Edit hotel).
* Select the photos to import.

After everything has been selected, the hotel can be saved in Tourpaq.

Save the hotel in Tourpaq.

Photos and allotments are not available immediately. They are typically available within \~5 minutes after saving.

### Selecting a contract <a href="#selecting-a-contract" id="selecting-a-contract"></a>

Select **View contract details** to open a pop-up with the contract information.

<figure><img src="../.gitbook/assets/image (103).png" alt=""><figcaption></figcaption></figure>

* If the button is missing, a “no contracts defined” message is shown instead. The hotel cannot be imported.
* In some cases, a hotel appears to have contracts on the search page, but none are available on the details page. This happens when contracts are invalid (no rooms) or when contract rooms do not match the hotel’s rooms. The hotel cannot be imported.

It is important to review a contract before importing it.

<figure><img src="../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

### Select / Check room mappings <a href="#select--check-room-mappings" id="select--check-room-mappings"></a>

The system supports auto-mapping to make future imports easier.

It remembers previous mappings. It may also map rooms by configuration.

Always verify that rooms are mapped correctly before saving.

<figure><img src="../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

### Import / Update hotel photos <a href="#import--update-hotel-photos" id="import--update-hotel-photos"></a>

Select the photos you want. They will be imported with the hotel data.

To replace photos, delete the existing photos in Tourpaq first. Then re-import photos from **Hotel → Hotel Bed Bank**.

### FAQ

#### Can we make test bookings without payment to Hotelbeds?

No. Hotelbeds does not provide a test environment. Live test bookings use real contracts.

#### How do we know when a contract expires or changes?

There is no automatic notification today. Check contracts and price lists manually after changes.

#### Why do room costs still show the contract room type after renaming?

This is a known behavior. The Room Cost tab keeps the contract room type. A fix is planned for a future release.

#### How do I replace imported photos?

Delete the hotel photos in Tourpaq. Then re-import the selected photos from **Hotel → Hotel Bed Bank**.
