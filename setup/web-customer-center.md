---
description: >-
  Configure customer-facing information, images, and extra-selection behavior in
  Web Booking.
---

# Web Customer Center

## Web Customer Center

### Overview

**Web Customer Center** controls customer-facing texts, images, and extra-selection behavior in the web booking flow.

The configuration complements [WebBooking Settings](../brands/webbooking-settings/). It affects how products, services, and extras appear in Web Booking.

This area does not control pricing or availability. It controls information and preselected extras.

### Purpose

Use Web Customer Center to:

* Show consistent service information during booking.
* Explain transfers, insurance, tours, and pickup arrangements.
* Configure how Tourpaq preselects extras.

### Requirements

Before changing customer-facing content:

* Confirm the text with the responsible operational or commercial team.
* Confirm transfer, insurance, and tour details against the related setup.
* Prepare an image in a supported file format when adding an image.

### Navigation

In Tourpaq Office, open **Setup → Web Customer Center**.

### Interface overview

The page contains one content area for each customer-facing subject.

Select a section to edit its text or image. The **Extras Selection on Web Booking** section controls automatic extra selection.

### Field descriptions

Each section affects the matching part of the customer booking flow.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (2) (1) (1).png" alt="Web Customer Center sections in Tourpaq Office"><figcaption></figcaption></figure></div>

#### Party Package

Describes inclusions and conditions for a party package or themed package.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Party Package content section"><figcaption></figcaption></figure></div>

Include:

* Description of inclusions
* Important restrictions
* Target audience
* Any operational limitations

Tourpaq displays this content when a party package is selected.

#### Transfer

Explains transfer arrangements for the selected destination or product.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1).png" alt="Transfer content section"><figcaption></figcaption></figure></div>

Include:

* Meeting point details
* Transfer type (shared or private)
* Timing information
* Special instructions for arrival
* Exceptions or additional costs

Tourpaq shows this content during booking and in customer documentation.

Validate transfer information against [Transport](../transport/transport/) setup.

#### Insurance

Describes standard travel insurance in the booking flow.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1).png" alt="Insurance content section"><figcaption></figcaption></figure></div>

Include:

* Coverage overview
* Claims process summary
* Legal references if required

#### Cancellation Insurance

Explains the cancellation protection product.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (2) (1) (1) (1).png" alt="Cancellation Insurance content section"><figcaption></figcaption></figure></div>

Include:

* Coverage scope
* Valid cancellation reasons
* Refund conditions
* Important exclusions

Tourpaq shows this content before purchase.

#### Tours

Describes optional excursions or activities at the destination.

Include:

* General information about excursions
* Booking process
* Whether prebooking is required
* Age or participation restrictions

This content explains how excursion booking works.

#### PickupPoint

Defines pickup instructions for transfers or tours.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (5) (1) (3) (1).png" alt="PickupPoint content section"><figcaption></figcaption></figure></div>

Include:

* Default pickup location
* Communication process if pickup varies
* Special hotel-specific conditions

This content informs customers about arrival and excursion pickup arrangements.

#### Extras Selection on Web Booking

Controls how Tourpaq automatically selects extras during booking.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (6) (1) (2) (1).png" alt="Extras Selection on Web Booking options"><figcaption></figcaption></figure></div>

Use one of these options:

**Default**

Uses the standard configuration without automatic price prioritization.

**Select cheapest**

Tourpaq preselects the lowest-priced extra option.

Use when:

* You want price optimization
* Multiple similar extras exist

**Select the most expensive**

Tourpaq preselects the highest-priced extra option.

Use when:

* Premium upgrade strategy is desired
* Upsell optimization is a priority

### Add an image to a section

Each content section can include an image for the related service or product.

{% stepper %}
{% step %}
#### Select the section

Select the section that needs an image.
{% endstep %}

{% step %}
#### Edit the section

Click the **Edit icon (pencil)**.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Edit icon for a Web Customer Center section"><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
#### Locate Image Upload

Locate **Image Upload**.
{% endstep %}

{% step %}
#### Upload the file

Click **Upload** or **Choose File**.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Image Upload field in the section editor"><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
#### Select the file

Select the approved image file.
{% endstep %}

{% step %}
#### Save the section

Save the changes.
{% endstep %}
{% endstepper %}

Tourpaq associates the saved image with the selected section. The image appears in Web Customer Center.

#### Supported image formats

**Image Upload** accepts these file formats:

* **.jpg**
* **.gif**
* **.png**
* **.bmp**

For an unsupported format, Tourpaq displays this message:

> **This file format is not supported. Please upload an image file with one of the following extensions: jpg, gif, png, bmp.**

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (8) (1) (1) (1) (1).png" alt="Unsupported image format warning"><figcaption></figcaption></figure></div>

Tourpaq does not upload the file. Select a supported format before saving.

### System behavior

Text and images appear in the matching customer-facing section.

**Extras Selection on Web Booking** determines the preselected extra option. It does not change extra pricing.

### Related pages

* [WebBooking Settings](../brands/webbooking-settings/)
* [WebBooking images](../brands/webbooking-settings/images.md)
* [Travel Insurance](../travel-insurance/)
* [Cancellation Insurance](../cancellation-insurance/)
