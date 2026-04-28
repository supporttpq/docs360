---
description: >-
  How customer information (errata) is shown and acknowledged in Tourpaq
  WebBooking and Customer Center during checkout and when editing extras.
---

# Customer Information on WebBooking

Customer information (errata) can be shown in **Tourpaq WebBooking (WB)** and **Customer Center**. When **Acknowledge** is enabled on a rule, the guest must confirm each notice before continuing.

### New booking (Tourpaq WebBooking)

Customer information is typically shown at the **summary/confirmation** step in WebBooking. Each information line appears with a mandatory checkbox.

{% hint style="info" %}
The labels in the examples below may appear in Danish, depending on your setup:

* **Fortsæt** = Continue
* **Tillæg** = Extras
* **Opsummering** = Summary
* **Bestil Rejse** = Book trip
{% endhint %}

{% stepper %}
{% step %}
#### 1) Start a booking in WebBooking

Open the WebBooking flow and go to the traveller step (for example **Rejsedeltagere**).

**Expected result:** the booking flow is ready for customer and passenger input.
{% endstep %}

{% step %}
#### 2) Enter customer and passenger details

Fill in the required fields.

**Expected result:** the data is saved on the current step, and you can continue.
{% endstep %}

{% step %}
#### 3) Continue to Extras (Tillæg)

Click **Fortsæt** to continue. Select extras, if relevant.

**Expected result:** extras are selected (for testing, include an extra with customer information).
{% endstep %}

{% step %}
#### 4) Review Summary (Opsummering) and acknowledge notices

Click **Fortsæt** to open **Opsummering**.

In the confirmation area (for example **Godkend oplysningerne og bestil rejsen**), a **Passenger Information** section appears. It lists all customer information notices for the booking, for example from:

* destination
* resort
* hotel / room type
* transport
* extras

**Expected result:** each notice is shown with a checkbox. All checkboxes must be selected before **Bestil Rejse** is enabled.
{% endstep %}

{% step %}
#### 5) Complete the booking

Click **Bestil Rejse**.

**Expected result:** the booking is created and the confirmation page is shown (for example **ThankYouForBooking**).
{% endstep %}
{% endstepper %}

***

### Edit booking (Customer Center / booking confirmation)

This section outlines how to edit a booking from the Customer Center.\
**Important:** This applies to **extras only**. You cannot edit transport or hotel details via Customer Center.

{% stepper %}
{% step %}
#### 1) Go to Extras (Tillæg)

Open the booking in Customer Center and navigate to **Tillæg**.

**Expected result:** the extras page is shown.
{% endstep %}

{% step %}
#### 2) Change extras

Add or edit an extra that has customer information configured.

**Expected result:** the selected extra changes are staged for saving.
{% endstep %}

{% step %}
#### 3) Save and acknowledge the popup

Click **Gem** (Save).

A **Passenger Information** popup appears with the customer information notices for the selected extra(s).

**Expected result:** all checkboxes must be selected before the popup closes and the changes are saved. After confirmation, the flow returns to the first step.
{% endstep %}
{% endstepper %}

***

### Key notes (validation behavior)

* Customer information checkboxes are **mandatory** when acknowledgment is enabled.
* WebBooking typically blocks completion until all required notices are confirmed.
* Customer Center edits are **limited to extras**. Transport and hotel changes are not supported there.

### See also

* [Customer information (errata)](./)
* [Customer Information Booking Flow](customer-information-booking-flow.md)
