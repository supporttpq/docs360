# System Setup – Hotel Providers

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

### Hotel Beds (Hotelbeds) integration

| **Field**                | **Description**                                           |
| ------------------------ | --------------------------------------------------------- |
| **API Endpoint**         | URL endpoint for API communication.                       |
| **Cache Endpoint**       | Endpoint for cached hotel data.                           |
| **Image Endpoint**       | Endpoint for full-size hotel images.                      |
| **Small Image Endpoint** | Endpoint for small hotel images, used on the import page. |
| **API Key / API Secret** | Credentials provided by Hotel Beds for authentication.    |
| **Facilities Template**  | Template used by Tourpaq to map hotel facilities.         |

#### Setup steps

1. Obtain API credentials from Hotel Beds.
2. Go to **Setup → System Setup → Hotel Providers** and open the **Hotel Beds** tab.
3. Enter API endpoint values, API key/secret, and the facilities template.
4. Save the configuration.

### Availpro / D-EDGE integration

| **Field**               | **Description**                                      |
| ----------------------- | ---------------------------------------------------- |
| **Username / Password** | Credentials provided by Availpro for authentication. |

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

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

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

### FAQ

<details>

<summary><strong>Do provider credentials apply to all brands and agencies?</strong></summary>

In most setups, System Setup credentials are company-wide.

If you need provider credentials per brand, confirm what’s supported in your environment.

</details>

<details>

<summary><strong>Where do the API endpoints come from for Hotel Beds?</strong></summary>

They are supplied by Hotel Beds (Hotelbeds).

Use the values provided for your account/environment.

</details>

<details>

<summary><strong>What is the “Facilities Template” used for?</strong></summary>

It maps provider facility codes into Tourpaq facility values.

If mapping is wrong, facility filters and displays can be inconsistent.

</details>

<details>

<summary><strong>Do I need SkiStar Resort mappings if we don’t use SkiStar?</strong></summary>

No. Those mappings only matter for SkiStar accommodation imports and sync.

</details>

<details>

<summary><strong>Should I delete old mappings and credentials?</strong></summary>

Avoid deleting unless you are sure they are not used.

If you need to disable a provider, prefer disabling the integration or removing access in the provider system.

</details>
