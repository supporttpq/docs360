# Web Customer Center

### Overview

The **Web Customer Center** section in Tourpaq controls the customer-facing content displayed during the web booking flow.

This section allows you to define informational texts and behavioral rules that appear to end customers when they book packages online. The content configured here is visible in the Web Customer Center  & Web Booking interface and directly affects how products, services, and extras are presented.

This area is content-driven and does not control pricing logic or availability. It controls how information is communicated and how extras are preselected during booking.

### Purpose

The purpose of the Web Customer Center configuration is to:

* Provide clear and structured information to customers during booking
* Reduce customer confusion by explaining transfers, insurance, tours, and pickup details
* Standardize communication across products
* Control how extras are automatically selected in web bookings
* Improve conversion by guiding customer decisions

Correct configuration ensures consistency between operational setup and customer expectations.

### Field-by-Field Explanation

Below is a description of each section visible in the Web Customer Center.

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### 1. Party Package

**Purpose**\
Used to describe what is included in a party package or special themed package.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**What to include**

* Description of inclusions
* Important restrictions
* Target audience
* Any operational limitations

**Customer impact**\
Displayed in the booking flow when a party package is selected. Helps customers understand what they are purchasing.

#### 2. Transfer

**Purpose**\
Explains how transfers work for the selected destination or product.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**What to include**

* Meeting point details
* Transfer type (shared or private)
* Timing information
* Special instructions for arrival
* Exceptions or additional costs

**Customer impact**\
Visible during booking and in customer documentation. Reduces transfer-related support cases.

Always verify operational accuracy with the transport setup.

#### 3. Insurance

**Purpose**\
Describes the standard travel insurance offered in the booking flow.

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**What to include**

* Coverage overview
* Claims process summary
* Legal references if required

#### 4. Cancellation Insurance

**Purpose**\
Explains the cancellation protection product.

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**What to include**

* Coverage scope
* Valid cancellation reasons
* Refund conditions
* Important exclusions

**Customer impact**\
Helps customers understand refund eligibility before purchase.

#### 5. Tours

**Purpose**\
Describes optional excursions or activities available at the destination.

**What to include**

* General information about excursions
* Booking process
* Whether prebooking is required
* Age or participation restrictions

**Customer impact**\
Encourages upselling and clarifies how excursions are handled.

#### 6. PickupPoint

**Purpose**\
Defines instructions regarding pickup locations for transfers or tours.

<figure><img src="../.gitbook/assets/image (5) (1) (3) (1).png" alt=""><figcaption></figcaption></figure>

**What to include**

* Default pickup location
* Communication process if pickup varies
* Special hotel-specific conditions

**Customer impact**\
Reduces confusion at arrival or excursion departure.

#### 7. Extras Selection on Web Booking

This section controls how extras are automatically selected during booking.

<figure><img src="../.gitbook/assets/image (6) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

Available options:

**Default**

System behavior follows standard configuration without automatic price prioritization.

**Select cheapest**

The system automatically preselects the lowest priced extra option.

Used when:

* You want price optimization
* Multiple similar extras exist

**Select the most expensive**

The system automatically preselects the highest priced extra option.

Used when:

* Premium upgrade strategy is desired
* Upsell optimization is a priority

## Add an Image to a Section in Web Customer Center

**Overview**\
In the Web Customer Center, each section (for example Party Package, Transfer, Insurance, Tours, etc.) can contain an image. This image is displayed to customers and helps visually represent the service or product offered in that section.

**Purpose**\
Adding an image improves the presentation of the section and helps customers quickly understand the type of service associated with it.

***

#### Steps to Add an Image

1. Open **Web Customer Center**.
2. Locate the section where you want to add an image (for example, _Party Package_, _Transfer_, _Insurance_).
3.  Click the **Edit icon (pencil)** on the right side of the section.&#x20;

    <figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
4.  In the edit window:&#x20;

    * Locate the **Image Upload** field.
    * Click **Upload** or **Choose File**.
    * Select the image from your computer.

    <figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
5. Save the changes.

After saving, the image will be associated with that section and will be displayed in the Web Customer Center interface.

***

#### Supported Image Formats

The system only accepts the following file formats:

* **.jpg**
* **.gif**
* **.png**
* **.bmp**

If a file with a different format is uploaded, the system will display the following warning message:

> **This file format is not supported. Please upload an image file with one of the following extensions: jpg, gif, png, bmp.**

<figure><img src="../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

In this case, the file will not be uploaded and the user must select a supported image format before saving.
