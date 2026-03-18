# Package Content

### Overview

The **Package Content** tab defines which extras are automatically included in a package product.

It allows you to bundle services (such as meals, activities, transfers, equipment rental, etc.) together with an accommodation or main product so they are:

* Automatically attached to the booking
* Clearly defined as part of the package
* Managed centrally
* Displayed correctly in Web Booking

This functionality ensures consistent package composition across brands and sales channels.

### Purpose

The purpose of the **Package Content** section is to:

* Define what is included in a package
* Control included extras at product level
* Ensure automatic inclusion during booking
* Avoid manual addition of standard services
* Maintain package consistency across brands

### **Package products**

When selecting a product that is flagged as a **package** for a passenger, all products that are inside the package are selected (after saving the passenger) with a price of `0`. Only the package itself has the price set.

For a product to be set as **package**, you need to check the option inside **Edit Product Page → Basic Setup → Other Settings → Package Type**.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

You can modify the products that are inside the package in **Edit Product Page → Package Content** tab.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Warning messages**

*   If you select the **package**, you cannot select the products inside the package as well. You will get a warning message like this:



    <figure><img src="https://tourpaq.gitbook.io/staging-tourpaq-docs/~gitbook/image?url=https%3A%2F%2Fdocs.tourpaq.com%2Fassets%2Fimages%2Fpackage_and_product_warning-ecd616e463d185d98ad5ac65be13b1a3.png%3Fwidth%3D1797&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=b7605443&#x26;sv=2" alt=""><figcaption></figcaption></figure>
*   All products inside the package must be **eligible** for the package to be selected. If they are not all eligible, you will get this warning message:



    <figure><img src="https://tourpaq.gitbook.io/staging-tourpaq-docs/~gitbook/image?url=https%3A%2F%2Fdocs.tourpaq.com%2Fassets%2Fimages%2Fpackage_and_product_warning_2-182f4c506926ede24ffbcb6c77f7a3c9.png%3Fwidth%3D1809&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=d66c7cf6&#x26;sv=2" alt=""><figcaption></figcaption></figure>

## How Package Content Works

When a product is booked:

1. The system checks the Package Content configuration.
2. All linked extras are automatically attached to the booking.
3. Pricing is calculated based on:
   * Included extras pricing logic
   * Passenger allocation rules
4. The extras appear in:
   * Booking overview
   * Confirmation
   * Operational reports

**Example: Winter Ski Package**

Product: Al Pension\
Package Content includes:

* Breakfast
* 6-day Ski Pass
* Final Cleaning Fee

Result in Booking:

When a customer books:

* All three services are automatically included.
* They cannot remove mandatory items.
* Price reflects total bundled cost.
* Supplier reports include these extras.

<br>
