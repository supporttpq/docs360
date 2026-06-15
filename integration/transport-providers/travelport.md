# TravelPort

## **Overview**

The **TravelPort** tab under **System Setup → Transport Providers** is used to configure credentials and parameters for integrating with the **TravelPort GDS (Global Distribution System)**. This setup enables communication between your platform and TravelPort for searching, booking, and ticketing transport services (such as flights).

## **Purpose**

This configuration ensures secure and accurate connection between the system and the TravelPort API. It defines:

* Authentication credentials and branch details
* Ticketing and queue management rules
* Fare types to be used in searches
* Email communication for confirmation and notifications

## **Fields**

<img src="https://tourpaq.gitbook.io/staging-tourpaq-docs/~gitbook/image?url=https%3A%2F%2F1539646852-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FZCqO8EQ5P5Mioq1zbQAc%252Fuploads%252FCRhjMzCaaj29FMDmkaqH%252Fimage.png%3Falt%3Dmedia%26token%3Db1476ab7-d451-4066-ad7a-ba9d27a00092&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=766bd02c&#x26;sv=2" alt="" height="492" width="950">

| **Field**                               | **Description**                                                                                      |
| --------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| **User**                                | The TravelPort Universal API username or key used to authenticate requests.                          |
| **Password**                            | The password linked to the TravelPort user. Required for all API communications.                     |
| **Branch**                              | Identifies the specific branch or agency code registered with TravelPort (e.g., _P107659_).          |
| **Days number for ticketing**           | The number of days for ticketing after the reservation is made. Example: _3_ days.                   |
| **Max GDS search results**              | Limits the number of results returned by the TravelPort GDS when searching for offers. Example: _3_. |
| **Queue Number**                        | Specifies the TravelPort queue where bookings or messages will be placed (e.g., _55_).               |
| **Pseudo City Code (PCC)**              | The TravelPort location code representing the main agency office (e.g., _TTL_).                      |
| **Own Pseudo City Code**                | Used when a secondary or internal PCC must be defined for specific operations (e.g., _6EE3_).        |
| **Fares Indicator**                     | Controls which fares are returned: Public, Private, or Public + Private.                             |
| **Confirmation Email**                  | Email address that receives confirmation messages from TravelPort after booking.                     |
| **Submit Customer Email to TravelPort** | If enabled, Tourpaq submits the customer email to TravelPort (instead of the company email).         |

## **How to use**

1. **Access the page** Go to **Setup → System Setup → Transport Providers → TravelPort**
2. **Enter authentication data** Enter _User_, _Password_, and _Branch_ provided by TravelPort.
3. **Configure operational parameters**
   * Define ticketing time limits and GDS result limits.
   * Specify queue and pseudo city codes based on your agency setup.
4. **Set fare and email preferences**
   * Choose **Fares Indicator** based on your fare agreements.
   * Set **Confirmation Email** for internal notifications.
   * Enable **Submit Customer Email to TravelPort** if needed.
5. **Save configuration** After completing all fields, click **Save** to apply the configuration. The connection will then be active for TravelPort-based searches and bookings.
