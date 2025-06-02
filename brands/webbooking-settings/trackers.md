# Trackers

This section explains how to configure tracking codes and scripts for different parts of the **Web Booking Settings** under the **Trackers** tab.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Tracker Fields Overview

| Field                                  | Description                                                              | Recommended Usage                                                                              |
| -------------------------------------- | ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------- |
| **All Pages**                          | Script that will be inserted into all booking pages.                     | Insert general tracking scripts like Google Analytics, Meta Pixel, or Tag Manager.             |
| **All Pages Except Last Booking Step** | Scripts for all pages except the final booking step (confirmation page). | Use for marketing tags where you don't want conversion firing on confirmation.                 |
| **Body Bottom Dynamic**                | Script dynamically inserted just before `</body>` on all pages.          | Ideal for dynamically loaded tags like chat widgets or monitoring scripts.                     |
| **Body Bottom**                        | Static scripts placed at the bottom of the body on all pages.            | Use for consistent scripts that do not change often.                                           |
| **Body Top**                           | Scripts placed immediately after the opening `<body>` tag.               | Good for critical tracking that needs to load early, like tag managers or important analytics. |
| **First Booking Step Header**          | Script inserted into the header during the first booking step only.      | Helpful for measuring the start of the booking funnel.                                         |
| **Last Booking Step Header**           | Script inserted into the header during the final confirmation step.      | Use for conversion tracking (like Google Ads, Facebook Conversions API).                       |
| **Last Booking Step Body Top**         | Scripts placed at the top of the body during the last step.              | Alternative placement for lightweight tracking (e.g., event-based scripts).                    |
| **Last Booking Step Body Bottom**      | Scripts placed at the bottom of the body during the last step.           | Often used for "thank you" page-specific tracking, pixels, or customer surveys.                |

### How to Use

* **Paste or type** your full tracking script (e.g., JavaScript, HTML) into the desired field.
* Multiple scripts can be included in one field if separated properly (e.g., `<script>...</script>` tags).
* Ensure correct placement to avoid loading errors or missing event tracking.
* Always validate your page after inserting new scripts to make sure there are no console errors.

### Best Practices

* **Google Analytics / Tag Manager**: Place in **All Pages** or **Body Top**.
* **Conversion Pixels (e.g., Facebook, Google Ads)**: Place in **Last Booking Step Header** or **Last Booking Step Body Bottom**.
* **Chat widgets or dynamic plugins**: Place in **Body Bottom Dynamic**.
* **Performance Optimization**: Prefer asynchronous loading (`async` or `defer`) when possible to prevent slowing down page load times.
* **Testing**: Always test new scripts in a staging environment before pushing them to live bookings.

## Notes:

* Fields are **empty by default**—nothing will be injected unless you manually add content.
* Scripts here can be powerful but misplacement can cause critical issues; proceed with caution.
* Some fields can accept both `<script>` tags and inline scripts (depending on implementation).
