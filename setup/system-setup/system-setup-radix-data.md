# System Setup – Radix Data

### **Overview**

The **Radix Data** section contains the credentials and configuration fields required to enable **Radixx transport reporting** within Tourpaq. These values ensure seamless integration between Tourpaq and the Radixx system.

### **Purpose**

The purpose of Radix Data setup is to:

* Establish a secure connection between Tourpaq and the Radixx platform.
* Allow Tourpaq to retrieve, process, and report transport-related data.
* Enable administrators to configure credentials required for airline or transport reporting.

### **Configuration Fields**

| **Field**                       | **Description**                                       |
| ------------------------------- | ----------------------------------------------------- |
| **Username**                    | The username provided by Radixx for system access.    |
| **Password**                    | The corresponding password for Radixx authentication. |
| **TravelPortalName**            | The identifier for the travel portal.                 |
| **TravelPortalIATANumber**      | The IATA number assigned to the travel portal.        |
| **TravelPortalBookingAgent**    | The booking agent ID registered with Radixx.          |
| **TravelPortalBookingAgentPWD** | The booking agent password for authentication.        |

### **Usage Notes**

* These fields are **mandatory** for enabling Radixx reporting.
* Ensure that the credentials are kept **secure** and updated promptly if changes are made by Radixx.
* Incorrect or missing data will prevent Tourpaq from generating and processing Radixx transport reports.
