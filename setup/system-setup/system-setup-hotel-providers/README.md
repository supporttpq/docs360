# System Setup – Hotel Providers

## **Overview**

The **Hotel Providers** section manages integrations with external hotel bed banks, including **Hotel Beds** and **Availpro/D-EDGE**. These integrations allow Tourpaq to import hotel availability, pricing, and images directly into the system.

## **Purpose**

* Automate hotel data import from external providers.
* Ensure up-to-date availability, pricing, and images for bookings.
* Enable centralized management of hotel credentials for all agencies.

## **Hotel Beds Integration**

| **Field**                | **Description**                                           |
| ------------------------ | --------------------------------------------------------- |
| **API Endpoint**         | URL endpoint for API communication.                       |
| **Cache Endpoint**       | Endpoint for cached hotel data.                           |
| **Image Endpoint**       | Endpoint for full-size hotel images.                      |
| **Small Image Endpoint** | Endpoint for small hotel images, used on the import page. |
| **API Key / API Secret** | Credentials provided by Hotel Beds for authentication.    |
| **Facilities Template**  | Template used by Tourpaq to map hotel facilities.         |

### **Setup Steps**

1. Obtain API credentials from Hotel Beds.
2. Navigate to **System Setup → Hotel Beds tab**.
3. Enter API Endpoint, Cache, Image, Small Image, API Key, API Secret, and Facilities Template.
4. Save the configuration.

***

## **Availpro / D-EDGE Integration**

| **Field**               | **Description**                                      |
| ----------------------- | ---------------------------------------------------- |
| **Username / Password** | Credentials provided by Availpro for authentication. |

### **Setup Steps**

1. Obtain login credentials from Availpro/D-EDGE.
2. Navigate to **System Setup → Availpro tab**.
3. Enter the **username** and **password** provided.
4. Save the configuration.

***

## **SkiStar Resort**

### &#x20;**Overview**

The **SkiStar Resort** tab allows administrators to configure mappings between **SkiStar Resort IDs** and **Transport Length IDs**. These mappings ensure that when SkiStar accommodation data is imported, the system can correctly determine the default transport duration associated with each resort.

This configuration is required for proper handling of allotment, availability, pricing, and booking logic for SkiStar accommodations.

### **Page Structure**

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The page displays a simple table with the following columns:

#### **1. Ski Resort ID**

Represents the unique identifier of the resort in the SkiStar system.\
Each row corresponds to one resort configuration.

#### **2. Transport Length ID**

Specifies the predefined travel length (e.g., 4 days, 7 days) linked to the resort.\
This determines the default stay duration applied to SkiStar bookings imported into Tourpaq.

#### **3. Actions**

A delete icon is available to remove an existing mapping.

### **Available Actions**

#### **Create New Mapping**

Click the **Create** button to add a new SkiStar Resort → Transport Length relationship.\
You will be prompted to select:

* **Ski Resort ID**
* **Transport Length ID**

Once saved, the new mapping appears in the table.

#### **Delete Mapping**

Use the trash icon to remove a mapping that is no longer required.

### **Purpose of This Configuration**

* Ensures SkiStar data is correctly linked to Tourpaq travel lengths.
* Eliminates manual selection of duration during import.
* Supports automation when syncing SkiStar allotment and availability.
* Required for accurate package creation and price calculation.

### **Usage Notes**

* Only administrators can configure hotel provider integrations.
* Correct credentials are required to successfully fetch hotel availability, pricing, and images.
* Integration ensures bookings and pricing remain synchronized with external providers.
