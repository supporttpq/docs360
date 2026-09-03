---
cover: ../../.gitbook/assets/hb_logo_7.png
coverY: 0
layout:
  width: default
  cover:
    visible: false
    size: full
    mask: radial
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# Hotel Beds / D-Edge / SkiStar

### Overview

Hotel Providers configures integrations to external hotel systems.

This includes bed banks and channel managers used to import availability, prices, and images.

Go to **Setup → System Setup → Hotel Providers**.

{% hint style="warning" %}
Provider credentials are sensitive.

Limit access and rotate credentials if you suspect exposure.
{% endhint %}

### Purpose

* Automate hotel data import from external providers.
* Ensure up-to-date availability, pricing, and images for bookings.
* Enable centralized management of hotel credentials for all agencies.

### Providers

This page typically covers:

* **Hotel Beds** (Hotelbeds)
* **Availpro / D-EDGE**
* **SkiStar Resort** mappings (used by the SkiStar integration)

## Configuration

### Access

Navigate to:

```
Setup → System Setup → Hotel Providers
```

Only Administrator users can configure hotel provider integrations.

### Hotel Beds (Hotelbeds) integration

| **Field**                | **Description**                                           |
| ------------------------ | --------------------------------------------------------- |
| **API Endpoint**         | URL endpoint for API communication.                       |
| **Cache Endpoint**       | Endpoint for cached hotel data.                           |
| **Image Endpoint**       | Endpoint for full-size hotel images.                      |
| **Small Image Endpoint** | Endpoint for small hotel images, used on the import page. |
| **API Key / API Secret** | Credentials provided by Hotel Beds for authentication.    |
| **Facilities Template**  | Template used by Tourpaq to map hotel facilities.         |

After configuration, Tourpaq can begin importing hotel content and contract information.

#### Setup steps

1. Obtain API credentials from Hotel Beds.
2. Go to **Setup → System Setup → Hotel Providers** and open the **Hotel Beds** tab.
3. Enter API endpoint values, API key/secret, and the facilities template.
4. Save the configuration.

### Availpro / D-EDGE integration

| **Field**               | **Description**                                      |
| ----------------------- | ---------------------------------------------------- |
| **Username / Password** | Credentials provided by Availpro for authentication. |

Once credentials are entered and validated, Tourpaq can synchronize accommodation data from the provider.

#### Setup steps

1. Obtain login credentials from Availpro/D-EDGE.
2. Go to **Setup → System Setup → Hotel Providers** and open the **Availpro** tab.
3. Enter the **username** and **password** provided.
4. Save the configuration.

### SkiStar Resort mappings

#### Overview

The **SkiStar Resort** tab allows administrators to configure mappings between **SkiStar Resort IDs** and **Transport Length IDs**. These mappings ensure that when SkiStar accommodation data is imported, the system can correctly determine the default transport duration associated with each resort.

This configuration is required for proper handling of allotment, availability, pricing, and booking logic for SkiStar accommodations.

For the daily sync behavior and API logic, see [SkiStar Sync](skistar-sync.md).

#### Page structure

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The page displays a simple table with the following columns:

**Ski Resort ID**

Represents the unique identifier of the resort in the SkiStar system.\
Each row corresponds to one resort configuration.

**Transport Length ID**

Specifies the predefined travel length (e.g., 4 days, 7 days) linked to the resort.\
This determines the default stay duration applied to SkiStar bookings imported into Tourpaq.

**Actions**

A delete icon is available to remove an existing mapping.

#### Available actions

**Create a new mapping**

Click the **Create** button to add a new SkiStar Resort → Transport Length relationship.\
You will be prompted to select:

* **Ski Resort ID**
* **Transport Length ID**

Once saved, the new mapping appears in the table.

**Delete a mapping**

Use the trash icon to remove a mapping that is no longer required.

#### Why this matters

* Ensures SkiStar data is correctly linked to Tourpaq travel lengths.
* Eliminates manual selection of duration during import.
* Supports automation when syncing SkiStar allotment and availability.
* Required for accurate package creation and price calculation.

### Usage notes

* Only administrators can configure hotel provider integrations.
* Correct credentials are required to successfully fetch hotel availability, pricing, and images.
* Integration ensures bookings and pricing remain synchronized with external providers.

### Troubleshooting

* **No availability/prices imported:** Verify credentials first, then provider endpoints.
* **Images don’t import:** Verify Image/Small Image endpoints (Hotel Beds).
* **SkiStar import uses the wrong stay length:** Verify SkiStar Resort → Transport Length mappings.
* **A provider worked yesterday but fails today:** Rotate credentials and check provider service status.

## Hotel Import Process

### Step 1 – Configure Provider

Enter provider credentials in Hotel Providers setup.

### Step 2 – Search Available Hotels

Navigate to:

```
Hotel → Hotel Bed Bank
```

Search by:

* Country
* Destination
* Hotel name
* Available contracts

### Step 3 – Review Contract Information

Before importing, review:

* Room mappings
* Contract details
* Facilities
* Available room types

### Step 4 – Import Hotel

Select:

* Contract
* Room mappings
* Facilities
* Resort assignment
* Hotel photos

Save the hotel to import it into Tourpaq.

### Step 5 – Synchronization

After import, hotel information, images, prices, and availability become available within Tourpaq. Some data may require a few minutes before becoming visible.

***

## Example

### Importing a Hotel from Hotelbeds

#### Scenario

An administartor wants to add a new hotel in Mallorca.

#### Process

1. Open Hotel Bed Bank.
2. Search for Mallorca hotels.
3. Review available contracts.
4. Select room mappings.
5. Import hotel details and images.
6. Save the hotel.

#### Result

The hotel becomes available for:

* Booking creation
* Dynamic packages
* Availability searches
* Online sales

## Integration with Hotels Module

Imported hotels become standard Tourpaq hotel records and can be managed from:

```
Hotel → Hotels
```

Hotels can then be:

* Assigned to resorts
* Connected to suppliers
* Configured with room types
* Included in allotments
* Used in bookings
* Published online

This allows imported provider content to work seamlessly alongside manually created hotels.

***

## Administration

### Credential Management

Provider credentials are stored centrally in System Setup.

Benefits include:

* Single point of maintenance.
* Shared access across brands and agencies.
* Simplified integration management.

### Monitoring

Administrators should regularly verify:

* Connectivity status
* Import success
* Pricing synchronization
* Availability updates
* Contract validity
