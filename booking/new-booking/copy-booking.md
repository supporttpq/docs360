---
description: >-
  Copy passengers from an existing booking into a new booking draft in Tourpaq
  Office. Follow the steps, checks, and FAQ to avoid mistakes.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# Copy Booking

### Overview

The **Copy Booking** feature in **Tourpaq Office** lets you create a **new booking** and **copy passengers** from an existing booking.

People often search for this as **duplicate booking** or **clone booking**. In Tourpaq, it focuses on copying the **passenger list**.

This is useful when you:

* recreate a similar booking for the same travellers
* reschedule a trip and want to avoid retyping passenger names
* create a follow-up booking with the same passenger list

It saves time and reduces manual errors.

### Before you start

Make sure you have:

* the **booking number** you want to copy passengers from
* created a **new booking draft** with the correct number of passengers, plus **transport** and **hotel** selected

{% hint style="info" %}
After copying, always review the passenger details to ensure names, titles, birthdates, and contact details are still correct.
{% endhint %}

### Copy passengers to a new booking

{% stepper %}
{% step %}
### 1. Start a new booking

1. Go to **Booking → New Booking**.
2. Insert the **number of passengers**.
3. Select the **transport**.
4. Select the **hotel**.

At this point, you are ready to take allotment.
{% endstep %}

{% step %}
### 2. Enter the booking number to copy from

Before you click **Take Allotment**:

1. Locate the field where you can enter the **booking number to copy passengers from**.
2. Enter the **original booking number**.

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Enter the original booking number before clicking <strong>Take Allotment</strong>.</p></figcaption></figure>
{% endstep %}

{% step %}
### 3. Take allotment and confirm

1. Click **Take Allotment**.
2. When prompted with the confirmation message (for example: “Are you sure you want to copy the passengers?”), click **OK**.

The passengers from the original booking are now copied into the new booking.
{% endstep %}

{% step %}
### 4. Save passengers and save the booking

1. Click **Save Passengers**.
2. Click **Save Booking** to complete the booking.
{% endstep %}
{% endstepper %}

### What gets copied (and what does not)

Typically, **Copy Booking** copies the passenger rows from the original booking into the new booking.

Always verify your new booking setup. Don’t assume other parts of the booking are carried over (for example: pricing, extras, documents, or payment state).

### What to check after copying

After passengers are copied, verify:

* passenger **names** and **titles** (spelling and ticket format)
* **birthdates/ages** (pricing rules can depend on these)
* room allocation (if relevant)
* who is marked as the **main customer/contact** (email/phone)

To edit passenger details, use [Edit Passenger](new-booking/edit-passenger/).

### FAQ

#### Can I copy passengers without creating a new booking first?

No. Start in **Booking → New Booking** and build the new booking draft first.

Then enter the original booking number **before** you click **Take Allotment**.

#### Does Copy Booking copy transport, hotel, and extras too?

You select **transport and hotel** in the new booking draft.

Copy Booking then copies the **passenger list** from the original booking. Always review the booking before saving and sending anything.

#### I don’t see the “copy booking number” field

This field typically appears in the new booking flow **before** taking allotment. If you don’t see it:

* confirm you have selected **transport and hotel** first
* check if your user role/company configuration has this feature enabled

#### The system says the booking number is invalid

* Ensure you entered the correct booking number (no extra spaces).
* Confirm that the original booking exists and that you have permission to view it.

#### Passengers copied, but something looks wrong

Open **Edit Passenger** and correct the details before sending documents or taking payment.

#### When should I use Copy Booking vs Moved booking?

Use **Copy Booking** to quickly reuse the passenger list.

Use **Moved booking** when you are rescheduling and want to link the old and new bookings. See [Moved Booking](moved-booking.md).
