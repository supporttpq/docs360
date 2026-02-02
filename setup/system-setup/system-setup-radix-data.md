# System Setup – Radix Data

### Overview

Radix Data stores the credentials used for **Radixx** transport reporting in Tourpaq.

Go to **Setup → System Setup → Radix Data**.

{% hint style="warning" %}
These are sensitive credentials.

Limit access and document changes internally.
{% endhint %}

### Purpose

Use Radix Data to:

* Authenticate Tourpaq against the Radixx platform.
* Retrieve transport data for reporting and exports.
* Keep Radixx credentials in one place.

### Configuration fields

| **Field**                       | **Description**                                                   |
| ------------------------------- | ----------------------------------------------------------------- |
| **Username**                    | Radixx username used for system access.                           |
| **Password**                    | Password for the Radixx username.                                 |
| **TravelPortalName**            | Travel portal identifier in Radixx.                               |
| **TravelPortalIATANumber**      | IATA number linked to the travel portal.                          |
| **TravelPortalBookingAgent**    | Booking agent ID used when retrieving booking and passenger data. |
| **TravelPortalBookingAgentPWD** | Password for the booking agent ID.                                |

### Usage notes

* These fields are required for Radixx reporting to work.
* Update values immediately after a credential change in Radixx.
* Wrong values can block report generation and exports.

### Quick checks

Use this list when reporting fails:

* Verify usernames and passwords first.
* Confirm the TravelPortal values match Radixx.
* Re-run the report after saving changes.

### FAQ

<details>

<summary><strong>Do I need Radix Data if we don’t use Radixx?</strong></summary>

No. It’s only needed for Radixx-based transport reporting.

</details>

<details>

<summary><strong>Where do I get these values?</strong></summary>

Your Radixx administrator provides them.

They are usually issued per portal and booking agent.

</details>

<details>

<summary><strong>Which password should I update if Radixx changes credentials?</strong></summary>

Update the password that matches what was changed in Radixx.

That can be **Password** or **TravelPortalBookingAgentPWD**.

</details>

<details>

<summary><strong>What happens if I enter the wrong values?</strong></summary>

Radixx authentication will fail.

Reports and exports can return errors or empty results.

</details>

<details>

<summary><strong>Who should have access to this screen?</strong></summary>

Limit access to admins who manage integrations.

Treat these values like API secrets.

</details>
