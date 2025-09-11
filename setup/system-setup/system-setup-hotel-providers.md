# System Setup – Hotel Providers

### **Overview**

The **Hotel Providers** section manages integrations with external hotel bed banks, including **Hotel Beds** and **Availpro/D-EDGE**. These integrations allow Tourpaq to import hotel availability, pricing, and images directly into the system.

### **Purpose**

* Automate hotel data import from external providers.
* Ensure up-to-date availability, pricing, and images for bookings.
* Enable centralized management of hotel credentials for all agencies.

### **Hotel Beds Integration**

| **Field**                | **Description**                                           |
| ------------------------ | --------------------------------------------------------- |
| **API Endpoint**         | URL endpoint for API communication.                       |
| **Cache Endpoint**       | Endpoint for cached hotel data.                           |
| **Image Endpoint**       | Endpoint for full-size hotel images.                      |
| **Small Image Endpoint** | Endpoint for small hotel images, used on the import page. |
| **API Key / API Secret** | Credentials provided by Hotel Beds for authentication.    |
| **Facilities Template**  | Template used by Tourpaq to map hotel facilities.         |

#### **Setup Steps**

1. Obtain API credentials from Hotel Beds.
2. Navigate to **System Setup → Hotel Beds tab**.
3. Enter API Endpoint, Cache, Image, Small Image, API Key, API Secret, and Facilities Template.
4. Save the configuration.

***

### **Availpro / D-EDGE Integration**

| **Field**               | **Description**                                      |
| ----------------------- | ---------------------------------------------------- |
| **Username / Password** | Credentials provided by Availpro for authentication. |

#### **Setup Steps**

1. Obtain login credentials from Availpro/D-EDGE.
2. Navigate to **System Setup → Availpro tab**.
3. Enter the **username** and **password** provided.
4. Save the configuration.

***

### **Usage Notes**

* Only administrators can configure hotel provider integrations.
* Correct credentials are required to successfully fetch hotel availability, pricing, and images.
* Integration ensures bookings and pricing remain synchronized with external providers.
