# Add room cost rule with "Per Room Per Stay" with a specific stay days value

### Overview

This page shows how to create a **Per Room Per Stay** room cost rule that only applies to a **specific stay length**.

You will also test both outcomes:

* A booking where the stay length **matches** the rule.
* A booking where the stay length **does not match** the rule.

### Purpose

Use this workflow to:

* Ensure the rule applies **only** when the stay length matches **Stay Days No**.
* Verify that the cost line appears in **Profit → Hotel Cost** when it should.
* Verify that the cost line is **not** added when the stay length does not match.

This protects your margins and supplier costs from bad rule matches.

### Preconditions

Before you start:

* You have access to the **Hotel** and **Booking** modules.
* You have permission to create and edit room cost rules.
* You have a test setup where you can create bookings with **different stay lengths**.

{% hint style="info" %}
**Per Room Per Stay** is a fixed cost per stay.

Tourpaq can still split the value across stay days internally for allocation and reporting.
{% endhint %}

### Create and test a rule with **Stay Days No**

{% stepper %}
{% step %}
### Open the hotel

1. Go to **Hotel → Hotels**.
2. Select the hotel you want to test.
3. Open **Room Costs**.
{% endstep %}

{% step %}
### Create the room cost rule

1. Click **Create** (or **+**).
2. Fill the rule fields your setup requires, for example:
   * Cost value and currency
   * Validity period (start/end)
   * Room type
   * Transport interval (if used in your setup)
3. Set **Stay Type** to **Per Room Per Stay**.

When you select **Per Room Per Stay**, **Stay Days No** becomes available.
{% endstep %}

{% step %}
### Set the stay-length filter

1. In **Stay Days No**, enter a value (example: `5`).
2. Click the **Save** icon.

The rule now matches only bookings with this exact stay length.
{% endstep %}

{% step %}
### Test: booking where the stay length matches

1. Create a new booking that matches the **Stay Days No** value.
2. Confirm the booking status is **OK**.
3. Open **Profit → Hotel Cost**.
4. Verify there is a **Room Cost** line.

Note: the value may look divided by days in the cost view.
{% endstep %}

{% step %}
### Test: booking where the stay length does not match

1. Go back to the hotel’s **Room Costs**.
2. Edit the same rule.
3. Change **Stay Days No** to a different value.
4. Click the **Save** icon.
5. Create a new booking with a stay length that does **not** match the updated value.
6. Open **Profit → Hotel Cost**.
7. Verify there is **no Room Cost** line.
{% endstep %}
{% endstepper %}

### Key fields and behavior

* **Stay Type**
  * Controls the calculation basis.
  * **Per Room Per Stay** is one fixed cost for the whole stay.
* **Stay Days No**
  * Adds an **exact stay-length requirement**.
  * If it is set to `5`, only 5-day stays match.
* **Room Cost line (Profit → Hotel Cost)**
  * Appears only when the rule matches the booking.
  * May be distributed across stay days internally.

### Troubleshooting

If the cost does not show up:

* Check the rule’s **validity period**.
* Check room type and transport interval filters.
* Verify the booking stay length matches **Stay Days No** exactly.
* If you edited the rule after creating the booking, create a **new** test booking.

### FAQ

#### What does **Stay Days No** measure?

It is the stay length your setup uses for matching.

In most setups, it follows the booking’s arrival/departure interval.

If you are unsure, confirm by creating a booking and checking which stay length it reports.

#### Why does a per-stay cost look like a per-day value in Hotel Cost?

Tourpaq can distribute a per-stay value across days internally.

This supports allocation, reporting, and totals.

#### Does changing the rule update existing bookings?

Usually no.

Test changes on a **new booking** unless your process explicitly recalculates costs.

#### Can I support multiple stay lengths?

Yes.

Create one rule per stay length and set **Stay Days No** on each rule.

#### The booking is **OK**, but there is no Room Cost line. Why?

Most misses are caused by filters.

Re-check:

* validity period
* room type
* transport interval
* **Stay Days No** match

### Related pages

* [Add room cost rule with "Per Room Per Stay" type](add-room-cost-rule-with-per-room-per-stay-type.md)
* [Room cost](./)
