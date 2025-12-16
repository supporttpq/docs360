# General Description

### Overview

An **A la Carte booking** is designed for situations where you want to start a booking with **minimal information** and add travel components later, based on what the customer needs.

In Tourpaq Office, this usually means:

* You can start the booking with **only a customer** (the customer is also treated as the first passenger).
* You can then add or adjust things like **insurance**, **discounts**, and **supplements**.
* Depending on your setup, the booking can later be completed with **hotel and/or transport** (e.g., Custom Hotel Days, one-way flights, mixed itineraries).

{% hint style="info" %}
Some discounts/supplements may be applied automatically by your rules and are **not editable** in the interface.
{% endhint %}

***

### Who is this page for?

* **Booking agents / sales users**: Use the **Creating a new A la Carte booking** section below.
* **Admins / setup users**: Use the **Office implementation (setup)** section below.

***

### Creating a new A la Carte booking (Office)

{% stepper %}
{% step %}
### 1. Open the A la Carte booking flow

Go to **Booking → New A La Carte Booking**.

You will typically start with a booking that only contains the **customer** (first passenger).
{% endstep %}

{% step %}
### 2. Select or create the customer

You can either:

* **Create / fetch by phone number**: Enter the customer’s phone number. Tourpaq will search the server and auto-fill matching customer data when available.
* **Choose an existing customer**: Click **Choose** and search by name.

Then review and update the customer details (if needed) and save.
{% endstep %}

{% step %}
### 3. Set insurance, discounts, and supplements

1. Review the customer’s **travel insurance**.
2. Add or adjust **discounts/supplements** that are allowed for manual editing in your setup.
3. Save your changes.
{% endstep %}

{% step %}
### 4. Save the booking

1. Click **Save** to create the booking.
2. After saving, the page reloads and the booking opens in **edit mode**.
3. The booking status typically changes from **ERROR** to **OK** once the minimum required information is filled in.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
If the booking stays in **ERROR**, it usually means required information is missing (for example, a required customer field or a mandatory booking component, depending on your configuration).
{% endhint %}

***

### Office implementation (setup)

To use **New A La Carte Booking**, your company must have the required A la Carte setup in place. In practice, Tourpaq uses special “A la Carte-ready” entities so you can create bookings with minimal information and still have pricing/allotments available when you add components.

#### What needs to be set up

**1) Base room types**

Create at least one base room type that is enabled for A la Carte.

* Go to **Hotel → Base room types**
* Create a room type and enable **For “A La Carte”**

Read more: [**Base room types**](../../../base-room-types.md)

**2) Hotels**

Create or configure hotels that are meant to be used in A la Carte flows.

In many setups, enabling **For A La Carte** on a hotel will auto-create the minimum required structure (e.g., allotments) so it can be used in the A la Carte system.

Read more: [**Hotel creation**](../../../hotel/hotel-creation/)

{% hint style="info" %}
If you are working with **Custom Hotel Days**, make sure the hotel/room types are enabled for price-per-day logic.
{% endhint %}

**3) Transports**

A la Carte transports are typically created/configured after the relevant A la Carte hotels exist.

When you create a transport that is enabled for A la Carte, the system can generate supporting data (e.g., allotments and price lists) depending on your configuration.

Read more: [**Transport creation**](../../../transport/transport/transport-creation/)

***

### Related pages

* [**A la Carte**](./) – Overview of booking types and where to go next.
* [**Price List Custom Hotel days Service**](../../../price-list-custom-hotel-days-service.md) – Setup reference for Custom Hotel Days.
