# Add room cost rule with "Per Room Per Stay" type

### Overview

This page describes the **Hotel Room Cost Rule flow.** It explains each step a user must take to configure hotel costs, verify bookings, and ensure proper cost allocation and creditor integration.

The flow is used to define, apply, and validate **cost calculation rules** for hotel bookings — ensuring consistency across invoicing, profit margins, and multi-currency accounting.

### Purpose

Use this workflow to:

* Define how room costs are calculated for a hotel (per stay, per day, etc.)
* Confirm costs are applied correctly to bookings
* Validate totals and currency conversion
* Link the hotel to a creditor for correct supplier payment tracking

This prevents mismatched costs in Profit and invoicing.

### Preconditions

Before beginning this process:

* A hotel must already exist in the system.
* You must have permission to create and edit room cost rules.
* You need access to both the **Hotel** and **Booking** modules.
* Currency exchange rates must exist if the creditor uses another currency.

### Create and validate a **Per Room Per Stay** rule

{% hint style="info" %}
Per Room Per Stay is a **fixed cost per stay**. Tourpaq can still split the value across stay days internally for reporting and allocation.
{% endhint %}

{% stepper %}
{% step %}
### Open the hotel

1. Go to `Hotel → Hotels`.
2. Select the relevant hotel.
{% endstep %}

{% step %}
### Create the room cost rule

1. Open **Room Costs**.
2. Click **Create**.
3. Fill the rule fields:
   * **Stay Type**: `Per Room Per Stay`
   * **Stay/Arrival period**: the dates the rule should match
   * **Room type**: pick a room or use all rooms (if supported)
   * **Price/Cost** and **Currency**
   * Any occupancy filters your setup uses

When you select **Per Room Per Stay**, **Stay Days No** becomes available.
{% endstep %}

{% step %}
### Create a booking that matches the rule

1. Create a test booking using the same hotel, room type, and stay dates.
2. Confirm booking status is **OK**.
{% endstep %}

{% step %}
### Verify the cost on the booking

1. Open the booking.
2. Go to **Profit**.
3. Open **Hotel Cost**.

Verify:

* The **Room Cost** line exists.
* The value matches your rule logic.
* The cost can appear split across days, even for a per-stay rule.
{% endstep %}

{% step %}
### Verify invoice preview values

In the invoice preview (hotel cost details):

* The room cost should match the rule.
* Totals should align with the calculated room cost.
{% endstep %}

{% step %}
### Assign a creditor and re-check currency

1. Go back to the hotel details.
2. Select a **Creditor** (the payee).
3. Click **Save**.
4. Re-open the booking.
5. Re-check **Profit → Hotel Cost**.

If the creditor uses another currency, verify the cost is shown in the creditor currency and totals are converted correctly.
{% endstep %}
{% endstepper %}

### Related pages

* [Room cost](./)
* [Add room cost rule with "Per Room Per Stay" with a specific stay days value](add-room-cost-rule-with-per-room-per-stay-with-a-specific-stay-days-value.md)

### Summary of Key Concepts <a href="#summary-of-key-concepts" id="summary-of-key-concepts"></a>

**Room Cost Rule -** Defines how much a room costs per stay, per day, or per person.

**Stay Type -** Determines the cost calculation basis.

**Creditor -** The entity we pay for the hotel may use a different currency.

**Invoice Details -** Shows costs calculated and broken down for payment/billing.

**Currency Handling -** Costs may be stored in local currency but invoiced in creditor’s currency.

### Troubleshooting Tips

* If the rule does not apply, check stay dates, booking dates, and room type filters.
* If totals do not match, verify occupancy filters and overlapping date windows.
* If you changed the rule after creating the booking, re-open the booking after recalculation runs.
* If currency is not converted, confirm the hotel has a creditor and exchange rates exist.
* If booking status is not **OK**, fix availability or required data first.

### FAQ

#### When should I use **Per Room Per Stay**?

Use it when the supplier charges a fixed amount for the whole stay.\
Example: a cleaning fee or a flat package cost.

#### What is **Stay Days No** on a per-stay rule?

It limits when the rule applies.\
If you set it, the booking stay length must match that value.

#### Why is the per-stay cost shown “per day” in Hotel Cost?

Tourpaq can distribute the per-stay value across stay days internally.\
This supports allocation, reporting, and totals.

#### Why do I see different currencies before and after assigning a creditor?

Before you assign a creditor, costs can show in the rule currency.\
After you assign a creditor, costs can be shown in the creditor currency.

#### The rule matches, but I still see no hotel cost. Why?

Most misses come from filters. Check:

* stay period overlap
* room type selection
* booking date window (if used)
* required fields saved on the rule row
