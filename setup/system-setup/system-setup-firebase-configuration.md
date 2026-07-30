# System Setup – Firebase Configuration

### Overview

**Firebase Configuration** connects Tourpaq to Firebase services.

The connection supports notifications, analytics, and real-time data updates.

This page is part of [System Setup](./).

### Purpose

Use **Firebase Configuration** to store the Firebase credentials and parameters for a company.

The configuration supports Tourpaq features that use Firebase services.

### Requirements

Before configuring **Firebase Configuration**, complete these requirements:

* Ensure administrator access to **System Setup**.
* Contact **Tourpaq Support** for the company-specific Firebase configuration.
* Identify the Firebase-dependent features requiring validation.

{% hint style="warning" %}
Firebase credentials are sensitive.

Restrict access and rotate keys or tokens after suspected exposure.
{% endhint %}

### Navigation

In Tourpaq Office, open **Setup → System Setup → Firebase Configuration**.

### Interface overview

**Firebase Configuration** stores the Firebase credentials and configuration parameters supplied by **Tourpaq Support**.

The required values depend on the company and Firebase environment.

Do not replace values without a replacement configuration from **Tourpaq Support**.

### Configuration steps

Configure **Firebase Configuration** as follows:

1. Contact **Tourpaq Support** for the Firebase configuration.
2. Obtain the credentials and configuration parameters.
3. In **Firebase Configuration**, enter each supplied value.
4. Save the configuration.
5. Validate a Firebase-dependent feature.

### System behavior

Tourpaq uses the saved configuration to connect Firebase-dependent features to Firebase services.

The configuration supports push notifications, analytics, and real-time data updates.

Incorrect configuration prevents Firebase-dependent features from operating correctly.

Configuration changes can affect every brand and agency using the same setup.

### Validation examples

#### Real-time update

Trigger a configured real-time update in the relevant Tourpaq interface.

Confirm that the interface receives the expected updated data.

#### Push notification

Trigger a configured push-notification flow in the relevant application.

Confirm that the application receives the expected notification.

### Operational guidance

#### Usage notes

* Only administrators can configure **Firebase Configuration**.
* Validate each configured brand and environment after changes.
* Store credentials only in the approved configuration fields.

#### Troubleshooting

* **Real-time updates fail:** Confirm each supplied Firebase value is saved correctly.
* **Push notifications fail:** Confirm the relevant application uses the configured Firebase environment.
* **Configuration values are unavailable:** Contact **Tourpaq Support** for the company configuration.

### Related pages

* [System Setup](./) explains company-wide configuration.
* [SMS Configuration (Twilio)](../../integration/crm-and-marketing/system-setup-sms-configuration-twilio.md) covers SMS notification configuration.
