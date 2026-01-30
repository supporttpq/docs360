# System Setup

### Overview

**System Setup** is the global configuration for Tourpaq.

These settings affect the entire company, including bookings, payments, integrations, and reporting.

Go to **Setup → System Setup**.

{% hint style="warning" %}
Changes apply system-wide.

Test changes in a safe environment when possible.
{% endhint %}

Only users with **Administrator** rights should edit these settings.

Some rules and configurations cannot be deleted manually. Tourpaq removes them programmatically to protect data integrity.

### What you use it for

Use System Setup to:

* Establish **company-wide defaults** such as currency, payment rules, and booking visibility.
* Control **functional behavior** of dashboards, reminders, filters, and allotments.
* Configure **communication services**, including SMS and email.
* Manage **integration credentials** for third-party providers (transport, hotels, GDS, car rental, etc.).
* Define **reporting and export parameters** to support financial and operational workflows.

Correct setup keeps behavior consistent across brands and agencies. It also reduces errors in pricing, payments, and booking workflows.

### Main sections

Start here, then drill into the specific area you need:

* [System Setup – General Information Settings](system-setup-general-information-settings.md)
* [System Setup – Payment Rate Rules](system-setup-payment-rate-rules.md)
* [System Setup – Radix Data](system-setup-radix-data.md)
* [System Setup – Currency](system-setup-currency.md)
* [System Setup – Deposit Rules](system-setup-deposit-rules.md)
* [System Setup – SMS Configuration (Twilio)](system-setup-sms-configuration-twilio.md)
* [System Setup – Mail Platform](system-setup-mail-platform.md)
* [System Setup – Auto Europe (Car Rental Integration)](system-setup-auto-europe-car-rental-integration.md)
* [System Setup – Hotel Providers](system-setup-hotel-providers/)
* [System Setup – Hotel Import](system-setup-hotel-import.md)
* [System Setup - Transport Providers](system-setup-transport-providers.md)
* [System Setup – GDS Data](system-setup-gds-data.md)
* [System Setup – Inflight Service](system-setup-inflight-service.md)
* [System Setup – Firebase Configuration](system-setup-firebase-configuration.md)
* [System Setup – Travel Lengths](system-setup-travel-lengths.md)
* [System Setup – Two-Factor Authentication (2F Auth)](system-setup-two-factor-authentication-2f-auth.md)
* [System Setup – FTP Providers](system-setup-ftp-providers.md)
* [System Setup - Web Hook Configuration](web-hook-configuration.md)
* [System Setup – Flight Change Queue](system-setup-flight-change-queue.md)

### FAQ

<details>

<summary><strong>Who should edit System Setup?</strong></summary>

Admins only.

Many settings affect bookings, finance, and integrations immediately.

</details>

<details>

<summary><strong>Why can’t I delete a rule or configuration?</strong></summary>

Some configuration is protected to avoid breaking references in historical data.

Those items are removed by the system when it is safe to do so.

</details>

<details>

<summary><strong>What should I validate after changing a setting?</strong></summary>

At minimum:

* Create a test booking.
* Run the relevant export/report.
* Verify the downstream integration (email/SMS/provider) if impacted.

</details>

<details>

<summary><strong>Do System Setup changes affect all brands?</strong></summary>

Yes. System Setup is company-wide.

Brand-specific configuration is usually handled in brand/agency modules.

</details>
