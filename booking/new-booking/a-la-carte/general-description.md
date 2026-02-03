# General Description

### Overview

{% hint style="warning" %}
If you do not see **Booking → New A La Carte Booking**, ask an admin.
{% endhint %}

* You need access to **Booking** in Tourpaq Office.
* Your company must have **A la Carte** enabled.
* Your setup controls which fields are **required**.

### Before you start

***

{% hint style="info" %}
Some discounts and supplements are rule-based.

Those values may be **locked** in the interface.
{% endhint %}

* Start with **only a customer**.
* The customer becomes **Passenger 1** automatically.
* Add **insurance**, **discounts**, and **supplements**.
* Add **hotel and/or transport** when you are ready.

In Tourpaq Office, this usually means:

You start with a **customer** and add trip components later.

An **A la Carte booking** lets you create a booking with **minimal details**.

***

### Who is this for?

* **Booking agents / sales users**: Use the **Creating a new A la Carte booking** section below.
* **Admins / setup users**: Use the **Office implementation (setup)** section below.

***

### Creating a new A la Carte booking (Office)

{% stepper %}
{% step %}
### 1. Open the A la Carte booking flow

Go to **Booking → New A La Carte Booking**.

You start with a booking that only contains a **customer**.

That customer is also **Passenger 1**.
{% endstep %}

{% step %}
### 2. Select or create the customer

You can either:

* **Search by phone**: Enter a phone number to look up a customer.
* **Choose existing**: Click **Choose** and search by name.

Review the customer fields and fill missing required values.

Then click **Save**.
{% endstep %}

{% step %}
### 3. Add insurance, discounts, and supplements

1. Review **travel insurance**.
2. Add allowed **discounts** and **supplements**.
3. Click **Save**.
{% endstep %}

{% step %}
### 4. Save the booking

1. Click **Save** to create the booking.
2. The booking reopens in **edit mode** after saving.
3. The status should move from **ERROR** to **OK**.
{% endstep %}

{% step %}
### 5. Add the trip components (next step)

After the booking exists, add the travel items you need.

What you can add depends on your setup.

Common A la Carte options:

* **Custom Hotel Days** (pick check-in and check-out dates)
* **Hotel-only**
* **Transport-only**
* **One-way flights** (single or multiple)
* **Circuit bookings** (multiple hotels and flights)

Use [**A la Carte**](./) to choose the right flow.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
If the booking stays in **ERROR**, required data is missing.

This is often a missing customer field or a mandatory component.
{% endhint %}

***

### Troubleshooting

#### The booking stays in ERROR

1. Reopen the customer and check for required fields.
2. Save again and verify the status.
3. If it still fails, add the missing required component.

Ask an admin which fields and components are mandatory.

#### I can’t find “New A la Carte Booking”

This is usually permissions or missing setup.

Ask an admin to enable the feature for your user or company.

***

### Office implementation (setup for admins)

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

Use [**A la Carte**](./) to pick the correct flow.
