# Paxport

## **Overview**

The **Paxport** tab under **System Setup → Transport Providers** allows configuration of the integration between the platform and the **Paxport API**. This setup enables the system to communicate with Paxport’s services for flight bookings.

## **Purpose**

This configuration establishes the technical connection parameters required to authenticate and interact with the Paxport environment. It ensures the system can send requests and retrieve information (such as availability, fares, or booking confirmations) from the Paxport platform.

## **Fields**

<figure><img src="../../../.gitbook/assets/image (468).png" alt=""><figcaption></figcaption></figure>

| **Field**                       | **Description**                                                                                                              |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **Paxport API URL**             | The endpoint address of the Paxport API. This is where the system sends requests. Example: `https://api.paxport.net/`        |
| **Paxport Syndicator ID**       | The unique identifier provided by Paxport to identify your agency or syndicator account.                                     |
| **Paxport Target**              | Defines the operational environment — typically _test_ or _production_. Use _test_ for sandbox validation before going live. |
| **Paxport Version**             | Specifies the version of the Paxport API to be used.                                                                         |
| **Paxport Syndicator Password** | The password or API key associated with the **Paxport Syndicator ID**, used for authentication.                              |

## **How to use**

1. **Access the page**\
   Go to **Setup → System Setup → Transport Providers → Paxport**
2. **Enter the API details**
   * Fill in the **Paxport API URL** as provided by Paxport.
   * Add your **Syndicator ID** and **Password** for authentication.
3. **Select the environment**
   * Set **Paxport Target** to _test_ or _production_ depending on your usage.
   * Specify the **API Version** if required by Paxport’s technical team.
4. **Save configuration**\
   After completing all fields, click **Save** to apply the setup. The system will now be able to interact with Paxport services for flight searches, bookings, and ancillary data retrieval.
