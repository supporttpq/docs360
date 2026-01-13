# Base room types

### Overview

The **Base Room Types** feature is used to define and insert room types into the system. Each hotel has a variety of room types available for sale. These room types are chosen from the predefined **Base Room Types**, which must first be set up in the system by an administrator.

{% hint style="info" %}
Think of a base room type as a “master” room definition. You can still adjust name and beds per hotel later.
{% endhint %}

### Where base room types are used

* Hotel setup, when you add room types to a hotel.
* Exports, where the room name can differ from the UI name.
* Availability dashboards like [Seats vs. Beds](seats-vs-beds.md) (unless excluded).

### Creating a New Room Type

1. Navigate to **Hotel → Base Room Types**.
2. Click the **Create** button.
3. Complete the required fields described below.

### Field Descriptions

<figure><img src=".gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

#### General Information

* **Room Code** – Unique system identifier. Treat this as stable once used.
* **Plaintext** – Room name shown in Tourpaq Office.
* **List Text** – Room name used in export files.
* **Internet** – Makes the room available via API. Used for website sales and integrations.
* **Status** – Shows or hides the room type in the UI.
* **Is Fictive** – Marks the room as virtual. Use for internal logic or planning. Common for one-way hotels and one-way transport seats.
* **For One Way** – Only for one-way transport. Only one room type can be defined per company. Enables price list creation for one-way trips.
* **Ignore in Seats vs. Beds** – Excludes the room from **Seats vs. Beds**.
* **For A La Carte** – Makes the room available for [A La Carte](booking/new-booking/a-la-carte/) bookings.

#### Bed Configuration

* **No. Ordinary Beds** – Standard beds in the room. These always pay full price. They cannot receive extra bed discounts.
* **Min No. Beds** – Minimum occupancy for the room.
* **Extra Beds** – Extra adult beds. These can get extra bed discounts.
* **Extra Beds Child** – Extra child beds. These can get extra bed discounts.
* **Start Child Age** – Minimum child age for child extra beds.
* **End Child Age** – Maximum child age for child extra beds.

#### Cost Configuration

* **Cost Beds** – Beds counted in cost price calculations. Used by the Hotel Cost Service.
* **Extra Beds Cost** – Extra beds counted in cost price calculations. Used by the Hotel Cost Service.

### Hotel Allotment

Shows all hotels and periods with allotments for this room type.

<figure><img src=".gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

#### Child Rooms

When you add a room type to a specific hotel, you can override:

<figure><img src=".gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

* The room name.
* The number and type of beds.

<figure><img src=".gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

### FAQ

#### 1. What is the difference between a base room type and a hotel room type?

**Q:** What’s the difference?\
**A:** A base room type is a shared template. A hotel room type is the hotel-specific version. The hotel version can override name and beds.

#### 2. Why can’t I see my room type in the booking flow?

**Q:** The room type exists, but it does not show up. Why?\
**A:** Check the room **Status** first. Then check if **Internet** must be enabled for your channel.

#### 3. When should I use “Is Fictive”?

**Q:** What is a fictive room type for?\
**A:** Use it for virtual configurations. Examples include one-way hotels or internal planning setups.

#### 4. What does “Ignore in Seats vs. Beds” do?

**Q:** Will it affect availability or sales?\
**A:** It only removes the room type from the **Seats vs. Beds** overview. It does not delete the room type.

#### 5. Can I rename the room without breaking exports?

**Q:** I want one name in the UI and another in exports. Can I do that?\
**A:** Yes. Use **Plaintext** for the UI name. Use **List Text** for the export name.

#### 6. Can I change the Room Code later?

**Q:** Is it safe to change?\
**A:** Avoid changes after the room type is in use. It is a unique identifier. Changing it can break references and integrations.
