# System Setup – Firebase Configuration

### Overview

The **Firebase Configuration** section allows Tourpaq to integrate with Firebase for notifications, analytics, and real-time data updates within the platform.

Go to **Setup → System Setup → Firebase Configuration**.

{% hint style="warning" %}
Firebase credentials are sensitive.

Limit access and rotate keys/tokens if you suspect exposure.
{% endhint %}

### Purpose

* Enable push notifications and real-time updates in the Tourpaq system.
* Centralize Firebase credentials for secure access.
* Support system features that rely on Firebase services, such as mobile notifications and analytics tracking.

### Configuration steps

1. Contact **Tourpaq Support** to obtain the correct Firebase setup for your company.
2. The support team will provide the necessary credentials and configuration parameters.
3. Insert the provided credentials into the **System Setup → Firebase Configuration** fields.
4. Save the configuration.

### What to validate after setup

Validate at least one Firebase-dependent flow:

* A real-time update in the relevant UI (if used in your setup).
* A push notification flow in the relevant app (if enabled).

If you have multiple brands/environments, validate each one.

### Usage notes

* Only administrators can configure Firebase settings.
* Incorrect configuration will prevent real-time updates and push notifications.
* All Firebase-dependent features rely on the credentials and setup provided by Tourpaq Support.

### FAQ

<details>

<summary><strong>Do I need Firebase Configuration if we don’t use mobile apps or chat?</strong></summary>

Not always.

If your Tourpaq features don’t rely on Firebase, it may not be required.

</details>

<details>

<summary><strong>Where do I get the Firebase credentials?</strong></summary>

Tourpaq Support provides the correct values for your company and environment.

</details>

<details>

<summary><strong>What happens if the configuration is wrong?</strong></summary>

Firebase-dependent features can stop working.

Common symptoms are missing real-time updates or failed push notifications.

</details>

<details>

<summary><strong>Should I change these values myself?</strong></summary>

Only if you know exactly what your environment expects.

When in doubt, coordinate changes with Tourpaq Support.

</details>
