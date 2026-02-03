---
description: >-
  Enable webhooks per brand and configure API keys for sending hotel update
  events to an external URL.
---

# System Setup – Web Hook Configuration

The Web Hook tab in System Setup is used to enable/disable webhooks per brand and configure an API key per brand.

Go to **Setup → System Setup → Web Hook**.

### Web Hook Edit <a href="#web-hook-edit" id="web-hook-edit"></a>

To save a configuration for any brand, you must fill in **API key**.

<figure><img src="../../.gitbook/assets/webHookTab-f11ebd9f02befd9cf500432fe8b575ae.png" alt=""><figcaption></figcaption></figure>

After enabling the feature for a brand, updating hotel descriptions, photos, or facilities will send a webhook to the target URL configured in [System Setup – General Information Settings](system-setup-general-information-settings.md) → **Other Settings** → **Web Hook URL**.

<figure><img src="../../.gitbook/assets/webHookURL-3b85bd984339deda202b5169f2cd88ac.png" alt=""><figcaption></figcaption></figure>

You can find API details here: [Hotel API webhook](https://docsv2.tourpaq.com/docs/hotel-api/webhook).

### FAQ

<details>

<summary><strong>Is the webhook enabled per company or per brand?</strong></summary>

Webhook enablement and the API key are configured per brand in the Web Hook tab.

</details>

<details>

<summary><strong>Where do I set the target URL?</strong></summary>

Set it in **Setup → System Setup → General Information** → **Other Settings** → **Web Hook URL**.

</details>

<details>

<summary><strong>What events trigger a webhook?</strong></summary>

Hotel updates such as descriptions, photos, and facilities.

</details>

<details>

<summary><strong>Why can’t I save the configuration?</strong></summary>

The **API key** is required for saving per brand.

</details>

<details>

<summary><strong>How can I test that webhooks work?</strong></summary>

Enable the webhook for a test brand, set a test **Web Hook URL**, then update a hotel description/photo/facility and confirm the callback is received.

</details>
