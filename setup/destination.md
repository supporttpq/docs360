# Destination

**Overview / Purpose**

The **Destinations** feature, located under **Setup → Destination**, allows users to create and manage destinations in Tourpaq. Destinations define geographical locations and can be linked to other system elements such as resorts and extras. This ensures bookings and resources are properly associated with the correct travel location.

<figure><img src="../.gitbook/assets/destinationmain-e8f3152d7db437457e91ef7405246a36.png" alt=""><figcaption></figcaption></figure>

### Destination Create <a href="#destination-create" id="destination-create"></a>

<figure><img src="../.gitbook/assets/destinationsave-16eb115620cee510abdf3601f4378f05.png" alt=""><figcaption></figcaption></figure>

### **How It Works**

When creating a destination, users enter core information such as **code, country, and name**, along with optional details like coordinates and agency-specific settings. Once created, destinations can be used in other parts of the system:

* Resorts can be tied to destinations to define their location.
* Extras can be linked to destinations to ensure services are available only in relevant areas.

### **Key Features / Functions**

#### **Destination Creation (Setup → Destination)**

* **Required Fields:**
  * **Code** – A unique identifier for the destination.
  * **Country** – The country where the destination is located.
  * **Default Name** – The standard name of the destination.
  * **List Name** – The display name shown in lists.
* **Geographic Coordinates:**
  * **Latitude**
  * **Longitude**
  * **Country** (used again for location precision)
* **Additional Fields:**
  * **URL Alias** – Optional alias used for links.
  * **Agency-Specific Details** – Custom settings per agency.
* **Customizable Fields:**
  * **Default Name**
  * **List Name**

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

### Destination usage <a href="#destination-usage" id="destination-usage"></a>

Location: **Setup/Resorts**

A resort can have a destination associated with it.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Extras setup/Extras** An extra resource can be associated with a destinaiton.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Notes / Best Practices**

* Always use a **unique code** when creating destinations to avoid conflicts.
* Latitude and longitude values help define the exact location—this is especially useful for mapping and geo-based filtering.
* Use **agency-specific details** when different agencies require unique naming or display settings.
* Keep **Default Name** consistent for system-wide recognition, but adjust **List Name** for better readability in customer-facing views.

### Passenger Information

#### **Overview**

The **Passenger Information** section, found under **Setup → Destination**, allows the user to define informational messages related to a specific destination.\
These entries control what information is associated with that destination and can be used to provide guests with destination-specific notes such as arrival guidelines, service information, or important updates.

Passenger Information is managed per destination and can include conditions based on **stay period** and **booking period**.

#### **Purpose**

The purpose of the **Passenger Information** page is to:

* Manage destination-level informational content that can later be used in various parts of the system or shared with guests.
* Define and control which information applies to passengers depending on their **travel dates** or **booking dates**.
* Set up acknowledgment requirements for specific messages that guests or guides need to confirm.

#### **Instructions**

**Accessing Passenger Information**

1. Go to **Setup → Destination**.
2. Select the desired **destination** (e.g., _CHQ_).
3. Open the **Passenger Information** tab.

The list will display all entries configured for the selected destination.

| **Column**                 | **Description**                                                                  |
| -------------------------- | -------------------------------------------------------------------------------- |
| **Stay From / Stay To**    | The travel period during which the information applies.                          |
| **Booking Date From / To** | Optional booking date limits that define when the message is relevant.           |
| **Information**            | The title or content reference of the passenger information.                     |
| **Acknowledge**            | Indicates if the message must be acknowledged by the guest (checked = required). |
| **Delete**                 | Removes the selected entry.                                                      |

**Creating Passenger Information**

1. Click **Create**.
2. Complete the following fields:
   * **Stay From / Stay To** – defines the period of stay when this message is valid.
   * **Booking Date From / To** – limits the message visibility to bookings made in a specific timeframe.
   * **Information** – enter or select the information to be displayed.
   * **Acknowledge** – enable if passengers must confirm they have read the information.
3. Click **Save** to store the configuration.

#### **Example**

In the provided example:

* The destination **CHQ** has one passenger information entry titled **Dest Errata Def**.
* It applies to stays from **28-10-2025** to **28-10-2025**.
* The entry is not marked as _Acknowledged_, meaning passengers are not required to confirm it.
