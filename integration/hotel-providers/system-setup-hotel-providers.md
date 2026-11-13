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
  anchors:
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
* **SkiStar Resort**: the stay lengths SkiStar Sync fetches for each SkiStar resort. The SkiStar connection itself has no tab: Tourpaq Support sets it up. See [SkiStar integration](skistar-sync.md).

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

### SkiStar Resort

#### Overview

The **SkiStar Resort** tab tells SkiStar Sync which stay lengths to fetch from SkiStar for each SkiStar resort. Each row is one resort and one stay length. See [SkiStar integration](skistar-sync.md).

For each row, the sync asks SkiStar about every Sunday arrival with that stay length, and updates allotment and cost on the room types coded for that stay, e.g. `-7D4` for 4 nights.

#### Page structure

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="The SkiStar Resort tab with two rows for Ski Resort ID 1: 4D and 7D, a delete icon per row and a Create button"><figcaption><p>Resort 1 synced for 4-night and 7-night stays.</p></figcaption></figure>

| Column                  | Description                                                                                                                                            |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Ski Resort ID**       | The resort's ID in SkiStar, e.g. `1` = Sälen, `4` = Hemsedal, `5` = Trysil. The same number as the **SkiStar Resort ID** on the hotels of that resort. |
| **Transport Length ID** | A stay length from [Transport Stay Days](../../setup/transport-stay-days.md), e.g. `4D`. Stay lengths longer than 7 days are not synced.               |

#### Add a stay length to a resort

1. Select **Create**. A new row appears at the bottom of the list.
2. In the new row, enter the **Ski Resort ID**.
3. In **Transport Length ID**, select the stay length.
4. Select the save icon at the start of the row. The **X** next to it discards the row.

Add one row per resort and stay length. To change a row, delete it and create a new one.

#### Remove a stay length from a resort

Select the trash icon on the row. From the next sync, SkiStar Sync no longer updates the rooms coded for that stay in that resort. Allotment and cost already in Tourpaq stay.

#### Example

| Ski Resort ID | Transport Length ID |
| ------------- | ------------------- |
| `1`           | `7D`                |
| `1`           | `5D`                |
| `4`           | `7D`                |
| `4`           | `5D`                |
| `4`           | `4D`                |

Hotels with SkiStar Resort ID `1` are synced for 7- and 5-night stays; hotels with `4` also for 4-night stays.

#### Why this matters

* Without a row for a resort, its hotels are not synced.
* Without a row for a stay length, the rooms coded for that stay get no allotment and no cost.
* Each stay length must also exist in Transport Stay Days, because SkiStar Sync stores the cost per transport length.

### Usage notes

* Only administrators can configure hotel provider integrations.
* Correct credentials are required to successfully fetch hotel availability, pricing, and images.
* Integration ensures bookings and pricing remain synchronized with external providers.

### Troubleshooting

* **No availability/prices imported:** Verify credentials first, then provider endpoints.
* **Images don’t import:** Verify Image/Small Image endpoints (Hotel Beds).
* **A SkiStar room gets no allotment or cost:** check that the hotel's SkiStar resort has a row for the room's stay length on the **SkiStar Resort** tab. See [SkiStar integration](skistar-sync.md#troubleshooting).
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
