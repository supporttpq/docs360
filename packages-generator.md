# Packages Generator

### Overview

Packages are part of the **À la Carte** feature and are used to generate **preset custom trips or circuit offers**. They combine transports, hotels, and rooms into a ready-to-book package that can be offered to agencies and customers.

### Purpose

* To create multi-step trips that combine several transports and hotel stays.
* To simplify the selling process by offering pre-built travel packages.
* To allow agencies to market complex trips (e.g., multiple destinations, different hotels) as a single product.

### Preconditions

* Access to the **Price List** module.
* All transports used must have **one-way seats**.
* All selected hotels must already have a **Price List per Day** defined.

<figure><img src=".gitbook/assets/image (59) (1).png" alt=""><figcaption></figcaption></figure>

### Instructions

#### Step 1: Create a Package

1. Go to **Price List > Package Generator**.
2. Click **Create**.
3. Fill in the package details:
   * **Package Name**
   * **Agency**
   * **Booking Period** (start and end date)
   * **Travel Interval** (the period during which packages can be created)
   * **Discount** (optional)

#### Step 2: Add Transports and Hotels

1. **Add Transport** → Select a transport (must have one-way seats).
2. **Select Hotel** → Choose a hotel with an existing price list.
3. **Select Room** → Choose a room and set the number of nights.

#### Step 3: Add Next Travel Segments

1. Add another **Transport** for the next destination.
   * Example: Guests travel to Palma, but the transport arrival is set as Crete.
2. Add **Hotel** → If the hotel is already listed, remove duplicate lines.
3. Click **Ignore Filter by Arrival** to display hotels tied to both resorts.
4. Select hotel, room, and number of nights.

#### Step 4: Return Transport

* If no return transport exists (e.g., Crete → Billund), search again.
* Adjust the number of nights (e.g., change to 4).
* Select from available return transports (e.g., Crete → Aarhus).
* Mark this as **One-way Home**.

#### Step 5: Finalize

1. Click **Save**.
2. Click **Generate**.

<figure><img src=".gitbook/assets/image (61) (1).png" alt=""><figcaption></figcaption></figure>

### Result / Usage

* **View Content** → Displays all entities used in the package (transports, hotels, rooms).
* **Generated Packages** → Shows every departure date for transports and every hotel check-in date included.
* Packages can be booked via the **Select Offer** feature.
