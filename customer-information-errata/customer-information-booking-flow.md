---
description: >-
  Tourpaq Office booking flow for customer information (errata) acknowledgment.
  Learn when the Passenger Information popup appears and what blocks saving.
---

# Customer Information Booking Flow

### Purpose

This page describes expected behavior when **customer information (errata)** requires acknowledgment in the **Tourpaq Office booking flow**. It focuses on when the **Passenger Information** popup appears, and what blocks saving. It applies to messages configured on transport, hotels/rooms, resorts, destinations, and extras.

***

### New booking flow (Office)

#### Overview

When a user creates a new booking, they must acknowledge all mandatory customer information linked to the selected services. The booking cannot be completed until all required checkboxes are confirmed.

#### Steps and expected results

{% stepper %}
{% step %}
#### 1) Create a new booking

Click **New booking**.

**Expected result:** the Booking Edit page opens.
{% endstep %}

{% step %}
#### 2) Enter required data

Enter passenger counts and customer details.

**Expected result:** the data is saved, and you can continue selecting services.
{% endstep %}

{% step %}
#### 3) Select transport (if it has mandatory customer information)

Select a transport that has customer information configured with **Acknowledge** enabled.

**Expected result:** the transport is selected.
{% endstep %}

{% step %}
#### 4) Select hotel/room (if it has mandatory customer information)

Select a hotel and room type that has customer information configured with **Acknowledge** enabled.

**Expected result:** the hotel/room is selected and passengers are allocated (auto-allocation may apply).
{% endstep %}

{% step %}
#### 5) Take allotment and acknowledge messages

Click **Take allotment**.

**Expected result:** the **Passenger Information** popup appears. It lists customer information notices from items like:

* hotel / room type
* resort
* destination

All checkboxes must be selected to proceed.
{% endstep %}

{% step %}
#### 6) Add extras and acknowledge extra notices

Select extra services with mandatory customer information. Click **Save Passengers**.

**Expected result:** the Passenger Information popup appears again for the selected extra(s). All checkboxes must be selected to save.
{% endstep %}

{% step %}
#### 7) Save the booking

Click the final **Save**.

**Expected result:** the booking is saved with **OK** status.
{% endstep %}
{% endstepper %}

***

### Edit booking flow (Office)

#### Overview

Editing an existing booking can retrigger acknowledgments. This typically happens when hotels/rooms change, passengers are reallocated, or extras are added.

#### Steps and expected results

{% stepper %}
{% step %}
#### 1) Open an existing booking

Open the booking in edit mode.

**Expected result:** the Booking Edit page opens.
{% endstep %}

{% step %}
#### 2) Change hotel/room or reallocate passengers

Edit the hotel option and/or allocate passengers.

**Expected result:** you’re required to re-take allotment before saving.
{% endstep %}

{% step %}
#### 3) Take allotment and acknowledge updated notices

Click **Take allotment**.

**Expected result:** the **Passenger Information** popup appears with updated hotel/resort/destination notices. All checkboxes must be selected to proceed.
{% endstep %}

{% step %}
#### 4) Edit extras and acknowledge extra notices

Click **Edit Passengers**, select extras, then click **Save Passengers**.

**Expected result:** the Passenger Information popup appears for extra-related notices. All checkboxes must be selected to save.
{% endstep %}

{% step %}
#### 5) Save the booking

Click the final **Save**.

**Expected result:** the booking is saved with **OK** status.
{% endstep %}
{% endstepper %}

***

### Mandatory Acknowledgment Enforcement

* **All customer information requiring acknowledgment is marked as mandatory**.
* Users **cannot save or proceed** with the booking unless all checkboxes are checked.
*   If not acknowledged, a warning message appears:

    > "You must check all mandatory terms before you create the booking!"

***

### Notes

* The **"Passenger Information" pop-up** appears:
  * When allotment is taken.
  * When editing passengers or extras.
* All checkbox items in the pop-up are **mandatory terms** and must be confirmed before proceeding.

### See also

* [Customer information (errata)](./)
* [Customer Information on WebBooking](customer-information-on-webbooking.md)
