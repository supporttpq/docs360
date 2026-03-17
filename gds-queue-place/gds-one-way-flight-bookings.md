---
description: >-
  Configure one-way GDS flights in Tourpaq Office. Enable Dynamic Packaging +
  OneWay, save search filters, then search and select flights from the booking
  GDS tab.
---

# GDS One way flight bookings

### **Overview**

Tourpaq Office supports **GDS Transport** configured as **one-way flights**.\
This functionality allows agencies to combine GDS one-way flights with other travel components such as **Charter**, **Hotel-only**, or **normal one-way flights** within the same booking.

### **Configuration**

1.  **Define GDS Transport**\
    To create a GDS one-way transport, start by defining a **GDS Transport** with **Dynamic Packaging** enabled.

    > _Note: “Dynamic Itineraries” must be selected first in order to reveal the “Dynamic Packaging” option._

<figure><img src="../.gitbook/assets/image (265).png" alt="GDS transport configuration showing Dynamic Itineraries and Dynamic Packaging options"><figcaption><p>Enable <strong>Dynamic Itineraries</strong>, then enable <strong>Dynamic Packaging</strong>.</p></figcaption></figure>

2. **Set Transport Legs**\
   Define the **legs** of the transport, specifying the **departure** and **arrival** airports, and select the appropriate **GDS provider**.\
   Ensure that the **OneWay** option is checked.

<figure><img src="../.gitbook/assets/image (15) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Transport legs setup with departure/arrival airports, GDS provider, and OneWay checkbox"><figcaption><p>Configure legs and enable <strong>OneWay</strong> for one-way GDS searching.</p></figcaption></figure>

3. **Configure Filters**

* Click **Configure** to open the GDS search configuration window.
* Set the filters to be used for **GDS flight searches** (e.g., departure time, airline, class, etc.).
*   Click **Save Filters** to confirm.

    > _Important: If filters are not saved, one-way GDS flight searches will not be possible._

<figure><img src="../.gitbook/assets/image (16) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="GDS search filter configuration window with Save Filters action"><figcaption><p>Configure flight search filters and click <strong>Save Filters</strong>.</p></figcaption></figure>

### **Searching for GDS One-Way Flights**

Once configuration is complete, GDS one-way flights can be searched directly from the **Booking page** using the **GDS tab**.

* When a search is performed, the system automatically generates the **interval definition** and **fixed quota** based on the search results.

<figure><img src="../.gitbook/assets/image (17) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Booking page GDS tab used to search for one-way GDS flights"><figcaption><p>Search one-way GDS flights from the booking’s <strong>GDS</strong> tab.</p></figcaption></figure>

* In the search window, the user can:
  * Select the **transport code** (only dynamic transports with dynamic packaging will appear).
  * Choose the **type of trip** (one-way-out, one-way-home, or both).
  * Specify the **departure** and **return dates**.

<figure><img src="../.gitbook/assets/image (18) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="GDS one-way search window selecting transport code, trip type, and dates"><figcaption><p>Select transport code, trip type (OW out/home), and travel dates.</p></figcaption></figure>

Based on the selected trip type, the system will return:

* **One-way-out flights**
* **One-way-home flights**
* **Both directions**, if applicable.

After selecting the flights, transport will be displayed on the booking at transport details.

<figure><img src="../.gitbook/assets/image (20) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Selected GDS one-way transport displayed in booking transport details"><figcaption><p>Selected one-way GDS flights appear in <strong>Transport Details</strong>.</p></figcaption></figure>

### **Creating a Booking**

After selecting the desired flights:

* The selected transport details are displayed in the **Transport Details** section of the booking.
* From this point, the user can proceed to **create a normal GDS booking**.

GDS One-Way Flights can be **combined** with other travel components on the same booking, such as:

* **Charter flights**
* **Hotel-only bookings**
* **Normal one-way flights**

This provides full flexibility for dynamic itinerary creation within a single booking.

#### **Expected Behavior**

* The system only displays GDS transports configured with **Dynamic Packaging** and **OneWay** enabled.
* Filters must be saved before performing searches.
* Interval and quota data are automatically generated when a flight search is performed.
* The booking behaves like any other GDS booking once the transport is selected.

### FAQ

<details>

<summary><strong>Why can’t I find any one-way GDS transports in the search window?</strong></summary>

Check these first:

* The transport has **Dynamic Packaging** enabled.
* The transport legs have **OneWay** checked.
* The transport uses a configured GDS provider and valid legs (departure/arrival).

</details>

<details>

<summary><strong>Why does the search return no flights?</strong></summary>

Most common causes:

* Filters are too strict (airline, departure time, class, etc.).
* Filters were configured but not saved via **Save Filters**.
* No availability exists for the selected dates/provider.

</details>

<details>

<summary><strong>What happens if I forget to save filters?</strong></summary>

One-way GDS searching will not work as expected.

Open **Configure**, adjust filters, then click **Save Filters**.

</details>

<details>

<summary><strong>Why are interval definition and fixed quota created automatically?</strong></summary>

For dynamic packaging searches, Tourpaq generates supporting transport data based on the returned flight options.

This enables normal booking behavior (availability, pricing, and reporting) after you select a flight.

</details>

<details>

<summary><strong>Can I combine one-way GDS flights with charter or hotel-only bookings?</strong></summary>

Yes.

GDS one-way flights can be combined with other components in the same booking, depending on your A la Carte setup and rules.

</details>
