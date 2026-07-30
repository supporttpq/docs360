# System Setup – Radix Data

### Overview

**Radix Data** stores credentials for Radixx transport reporting in Tourpaq.

Tourpaq uses these credentials to retrieve transport data for reports and exports.

### Requirements

* Valid Radixx credentials are required.
* Radixx transport reporting must be configured for the company.

### Navigation

In Tourpaq Office, go to **Setup → System Setup → Radix Data**.

{% hint style="warning" %}
These are sensitive credentials.

Limit access and document changes internally.
{% endhint %}

### Purpose

Use Radix Data to:

* Authenticate Tourpaq against the Radixx platform.
* Retrieve transport data for reporting and exports.
* Keep Radixx credentials in one place.

### System behavior

Tourpaq authenticates against Radixx with the configured credentials.

Incorrect values can block report generation and exports. Update the fields after any credential change in Radixx.

### Configuration fields

Configure these fields:

All fields are required for Radixx reporting.

| **Field**                       | **Description**                                                   |
| ------------------------------- | ----------------------------------------------------------------- |
| **Username**                    | Radixx username used for system access.                           |
| **Password**                    | Password for the Radixx username.                                 |
| **TravelPortalName**            | Travel portal identifier in Radixx.                               |
| **TravelPortalIATANumber**      | IATA number linked to the travel portal.                          |
| **TravelPortalBookingAgent**    | Booking agent ID used when retrieving booking and passenger data. |
| **TravelPortalBookingAgentPWD** | Password for the booking agent ID.                                |

### Configuration steps

Configure Radix Data in this order:

1. Open **Radix Data**.
2. Enter the **Username** and **Password** credentials.
3. Enter the TravelPortal values supplied by Radixx.
4. Save the configuration.
5. Run a Radixx report.
6. Validate the result.

### Troubleshooting

If reporting fails, check these items:

* Verify usernames and passwords first.
* Confirm the TravelPortal values match Radixx.
* Re-run the report after saving changes.

### Related pages

* [System Setup](./)
