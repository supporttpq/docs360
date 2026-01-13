# Moved Booking

## Moved booking

### Overview

The **Moved booking** feature is used when a customer’s trip must be **rescheduled** (for example due to date changes, availability changes, or customer request).

Instead of editing the original booking into a completely new itinerary, Tourpaq lets you:

1. Create a **new booking** (the rescheduled booking)
2. Link the original booking to the new one and set the original booking’s status to **Moved**

This keeps history clear and makes it obvious which booking replaced which.

### Preconditions

Before you start:

* The feature must be enabled in **SuperAdmin**.
* You must have access/permission to edit bookings and change status.
* You should already know the **target itinerary** (new departure/hotel/transport) you are moving the customer to.

{% hint style="info" %}
In practice, moving a booking usually starts by creating a new booking and copying passengers from the original booking. See also [Copy Booking](copy-booking.md).
{% endhint %}

### Move a booking (recommended flow)

{% stepper %}
{% step %}
### 1. Create the new booking and copy passengers

1. Create the **new booking** that the customer will travel on.
2. Copy passengers from the original booking (so names and traveller details don’t have to be re-entered).

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (8).png" alt=""><figcaption><p>Create the new booking and copy passengers from the original booking.</p></figcaption></figure>
{% endstep %}

{% step %}
### 2. Mark the original booking as moved

1. Go back to the **original booking**.
2. Click **Mark as Moved**.
3. Enter the **new booking number** (the booking you created in Step 1).
4. Click **Mark as moved** to confirm.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Link the original booking to the new booking number.</p></figcaption></figure>
{% endstep %}

{% step %}
### 3. Confirm the action

Click **OK** in the confirmation dialog.

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Confirm the move action.</p></figcaption></figure>
{% endstep %}

{% step %}
### 4. Verify the result

After confirmation:

* The **original booking** status becomes **Moved**.
* The booking is now clearly marked as rescheduled.

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>The original booking is now marked as Moved.</p></figcaption></figure>
{% endstep %}
{% endstepper %}

### What changes when you move a booking

* **Original booking**
  * Status changes to **Moved**
  * Should no longer be treated as the active travel booking
* **New booking**
  * Becomes the booking that should be handled going forward (documents, payments, services, etc.)

{% hint style="warning" %}
Moving a booking links the two bookings, but it does not automatically transfer every downstream action (such as already-sent documents). Always review what has already been communicated to the customer.
{% endhint %}

### Troubleshooting

#### I can’t see the “Mark as Moved” button

* Confirm the feature is enabled in **SuperAdmin**.
* Check that your user role has permission to change booking status.

#### I entered the wrong new booking number

If you linked to the wrong booking number, correct it as soon as possible according to your internal procedure (often this requires admin/support assistance depending on permissions and audit rules).

#### The customer asks “which booking is valid?”

Use the status as the rule of thumb:

* **Moved** = old booking (no longer the active itinerary)
* The **new booking** = the booking that should be used for travel and further handling
