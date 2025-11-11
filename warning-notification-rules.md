# Warning notification rules

### Overview

The **Warning Notification Rules** module enables administrators to configure automated warning emails or SMS messages for users based on a set of predefined conditions. These warnings help ensure that critical issues within the platform—such as email delivery failures, GDS booking issues, or service errors— are promptly communicated to the appropriate personnel.

Access: **E-mail Setup → Warning Notification Rules**

### Purpose

The purpose of the Warning Notification Rules module is to:

* Notify users about system issues, errors, or important changes automatically.
* Provide real-time alerts for operational issues, reducing response time.
* Ensure that warnings are targeted to the relevant user(s) based on configured rules.

### Tabs Overview

The module contains three main tabs:

1. **Warning Notification Rules** – Configure the conditions that trigger warnings.
2. **Warning Contacts** – Define which users or groups receive warnings.
3. **Warning Sent from E-mail** – Track and review previously sent warning notifications.

#### Warning Contacts <a href="#warning-contacts" id="warning-contacts"></a>

In here a user can be created that will receive the warning e-mails or SMS.

<figure><img src=".gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

#### Warning sent from e-mail <a href="#warning-sent-from-e-mail" id="warning-sent-from-e-mail"></a>

In here the sending e-mail address can be personalized. All e-mails will appear as sent from the address inserted.

<figure><img src=".gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

#### Warning Notification Rules <a href="#warning-notification-rules" id="warning-notification-rules"></a>

In here rules can be set for each user regarding what notification types he can receive.

<figure><img src=".gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>

### Types of Warnings

Below is a categorized list of common warnings and their purpose:

| Warning                                                                                  | Description                                                                                                                               |
| ---------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Informational**                                                                        | General information alerts.                                                                                                               |
| **HotelReporting Service – SMTP Error**                                                  | Alerts when an email fails to send from Hotel Communication.                                                                              |
| **HotelReporting Service – Other Errors**                                                | Alerts for other types of errors in Hotel Reporting.                                                                                      |
| **ExtraReporting Service – SMTP Error**                                                  | Alerts when an email fails to send from Extra Communication.                                                                              |
| **ExtraReporting Service – Other Errors**                                                | Alerts for other types of errors in Extra Reporting.                                                                                      |
| **TransportReporting Service – FTP / SMTP / Other Errors**                               | Alerts when emails or FTP operations fail in Transport Communication.                                                                     |
| **Mailer Helper – Error**                                                                | Alerts when the mail sending helper encounters an error.                                                                                  |
| **Services Watcher – Warning**                                                           | General service monitoring warnings.                                                                                                      |
| **Update GDS status from TKQ to TKOK Service**                                           | Notifies when a GDS booking status has changed from TKQ to TKOK.                                                                          |
| **Unable to configure GDS flight / Unable to check PNR / Unable to change Time Changes** | Alerts for issues with GDS flight configuration or Travelport reservations.                                                               |
| **ExtraSupplierReporting Service – SMTP / Other Errors**                                 | Alerts when emails from Extra Supplier Communication fail.                                                                                |
| **No Running GDS flights Service**                                                       | Alerts when the Flight Configuration service for GDS transports fails to run.                                                             |
| **Unable to submit WebBooking to Travelport**                                            | Alerts when webbooking GDS submissions fail.                                                                                              |
| **FewerGDSFlight**                                                                       | Warns when a Dynamic Transport has 10% fewer flights than the previous day.                                                               |
| **QueuemanagementGDS**                                                                   | Alerts about GDS bookings needing attention due to Travelport time changes.                                                               |
| **Success to change Time Changes / Success to submit WebBooking**                        | Confirms successful flight changes or webbooking submissions to Travelport.                                                               |
| **Failed to send email due to missing attachment**                                       | Warns when emails with tickets fail to send due to missing files.                                                                         |
| **Unable to Generate Price List Per Day**                                                | Alerts when price lists used for ALC settings fail to be generated.                                                                       |
| **Bookings in Error Status**                                                             | Sends email for bookings remaining in error status for over 1 hour.                                                                       |
| **Connected Hotel Error**                                                                | Alerts if there is no response from D-Edge API; repeated every 6 hours if unresolved, also displayed in Dashboard/Notifications/Warnings. |

### Instructions for Use

1. Navigate to **E-mail Setup → Warning Notification Rules**.
2. **Configure Warning Rules**: Define conditions that trigger notifications, including the type of warning and frequency.
3. **Set Warning Contacts**: Assign users or groups who should receive notifications.
4. **Monitor Sent Warnings**: Use the “Warning Sent from E-mail” tab to track sent warnings and verify successful delivery.
5. Adjust rules as needed to ensure critical issues are properly reported without causing notification overload.
