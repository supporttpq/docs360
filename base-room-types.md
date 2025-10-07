# Base room types

### Overview

The **Base Room Types** feature is used to define and insert room types into the system. Each hotel has a variety of room types available for sale. These room types are chosen from the predefined **Base Room Types**, which must first be set up in the system by an administrator.

### Creating a New Room Type

1. Navigate to **Hotel → Base Room Types**.
2. Click the **Create** button.
3. Complete the required fields described below.

### Field Descriptions

<figure><img src=".gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

#### General Information

* **Room Code** – Unique identifier for the room in the system.
* **Plaintext** – Room name displayed in the system.
* **List Text** – Room name displayed on export files.
* **Internet** – Determines if the room is available via API (for website sales).
* **Status** – Defines if the room type is visible or hidden in the system.
* **Is Fictive** – Marks the room as a virtual/non-physical configuration, used for system logic or planning. Commonly applied for one-way hotels or one-way seats in transport.
* **For One Way** – Used only for one-way transport. (Only one room type can be defined per company.) Enables pricelist creation for one-way trips.
* **Ignore in Seats vs. Beds** – Excludes this room type from the **Seats vs. Beds** overview.
* **For “A La Carte”** – Used for A La Carte bookings.

#### Bed Configuration

* **No. Ordinary Beds** – Number of standard beds. These beds always pay full price and cannot receive extra bed discounts.
* **Min No. Beds** – Minimum number of beds, used to enforce the minimum occupancy for this room.
* **Extra Beds** – Number of additional beds for adults (eligible for extra bed discounts).
* **Extra Beds Child** – Number of additional beds for children (eligible for extra bed discounts).
* **Start Child Age** – Minimum age for children allowed to use extra child beds.
* **End Child Age** – Maximum age for children allowed to use extra child beds.

#### Cost Configuration

* **Cost Beds** – Number of beds considered in cost price calculations, used by the Hotel Cost Service.
* **Extra Beds Cost** – Number of extra beds considered in cost price calculations, used by the Hotel Cost Service.

### Hotel Allotment

* Displays a summary of all hotels and defined periods where allotments exist for this room type.

<figure><img src=".gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

#### Child Rooms

When adding a new room type for a specific hotel, users can customize the configuration:

<figure><img src=".gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

* Change the room name.
* Adjust the number and type of beds.

<figure><img src=".gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>
